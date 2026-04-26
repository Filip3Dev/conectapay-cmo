# ConectaPay Partnership Integration Framework and API Strategy

## Executive Summary

**Purpose**: Technical implementation guide for ConectaPay partnership integrations

**Scope**: Complete API architecture, integration patterns, security standards, and developer experience framework for partners integrating with ConectaPay

**Target Audience**: Partner engineering teams, ConectaPay platform team, integration architects

**Key Objectives**:
- Reduce integration time from 4 weeks to 2 weeks
- Enable 95% integration success rate
- Support 3 integration depth levels (Widget, Webhook, Full API)
- Provide self-service developer experience
- Ensure LGPD compliance and security best practices

**Integration Philosophy**: "Meet partners where they are" - provide multiple integration paths based on partner technical maturity

---

## Table of Contents

1. [Integration Architecture](#integration-architecture)
2. [API Design Strategy](#api-design-strategy)
3. [Authentication & Security](#authentication--security)
4. [Integration Tiers](#integration-tiers)
5. [Webhook System](#webhook-system)
6. [Developer Experience](#developer-experience)
7. [Testing & Validation](#testing--validation)
8. [Monitoring & Observability](#monitoring--observability)
9. [Data Privacy & Compliance](#data-privacy--compliance)
10. [Maintenance & Versioning](#maintenance--versioning)
11. [SDK Strategy](#sdk-strategy)
12. [Integration Playbooks](#integration-playbooks)

---

## Integration Architecture

### System Overview

```
┌─────────────────────────────────────────────────────────────────────────┐
│                         CONECTAPAY PLATFORM                              │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                           │
│  ┌──────────────┐    ┌──────────────┐    ┌──────────────┐              │
│  │   API        │    │  Webhook     │    │   Partner    │              │
│  │  Gateway     │◄───│  Service     │◄───│   Service    │              │
│  └──────┬───────┘    └──────┬───────┘    └──────┬───────┘              │
│         │                   │                   │                       │
│         ▼                   ▼                   ▼                       │
│  ┌──────────────────────────────────────────────────────────────┐      │
│  │                    Integration Orchestrator                   │      │
│  └──────────────────────────────────────────────────────────────┘      │
│         │                   │                   │                       │
│         ▼                   ▼                   ▼                       │
│  ┌──────────────┐    ┌──────────────┐    ┌──────────────┐              │
│  │   WhatsApp   │    │  Payment     │    │   Customer   │              │
│  │   Service    │    │  Service     │    │    Data      │              │
│  └──────────────┘    └──────────────┘    └──────────────┘              │
│                                                                           │
└─────────────────────────────────────────────────────────────────────────┘
                                  │
                                  │ HTTPS (REST API)
                                  │ Webhooks ( outbound)
                                  │ WebSocket (real-time, optional)
                                  │
┌─────────────────────────────────────────────────────────────────────────┐
│                          PARTNER SYSTEMS                                 │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                           │
│  ┌──────────────┐    ┌──────────────┐    ┌──────────────┐              │
│  │   Clinic     │    │   Real       │    │     POS      │              │
│  │    SaaS      │    │  Estate      │    │   System     │              │
│  │              │    │    CRM       │    │              │              │
│  └──────────────┘    └──────────────┘    └──────────────┘              │
│                                                                           │
└─────────────────────────────────────────────────────────────────────────┘
```

### Architecture Principles

1. **API-First**: All features exposed via REST API before UI
2. **Webhook-Driven**: Async event notifications for real-time updates
3. **Idempotent Operations**: Safe retry mechanisms for all mutations
4. **Rate-Limited**: Fair usage policies per partner tier
5. **Observable**: Full request/response logging and metrics
6. **Secure-by-Default**: OAuth 2.0, encryption, audit trails

---

## API Design Strategy

### RESTful API Standards

**Base URL**: `https://api.conectapay.com.br/v1`

**Content-Type**: `application/json`

**Character Encoding**: `UTF-8`

**Date Format**: `ISO 8601` (e.g., `2026-04-26T14:30:00-03:00`)

**Money Format**: Decimal string in BRL (e.g., `"299.90"`)

### API Response Structure

**Success Response**:
```json
{
  "success": true,
  "data": {
    // Response data
  },
  "meta": {
    "request_id": "req_abc123",
    "timestamp": "2026-04-26T14:30:00-03:00",
    "rate_limit": {
      "remaining": 95,
      "reset": 1714135200
    }
  }
}
```

**Error Response**:
```json
{
  "success": false,
  "error": {
    "code": "validation_error",
    "message": "Phone number is required",
    "details": [
      {
        "field": "customer.phone",
        "message": "Phone number format is invalid"
      }
    ],
    "request_id": "req_abc123"
  }
}
```

### HTTP Status Codes

| Code | Usage | Example |
|------|-------|---------|
| 200 | Success | GET request successful |
| 201 | Created | POST created resource |
| 204 | No Content | DELETE successful |
| 400 | Bad Request | Validation error |
| 401 | Unauthorized | Missing/invalid token |
| 403 | Forbidden | Insufficient permissions |
| 404 | Not Found | Resource doesn't exist |
| 409 | Conflict | Duplicate resource |
| 422 | Unprocessable | Business logic validation |
| 429 | Rate Limited | Too many requests |
| 500 | Server Error | Internal error |

---

## Authentication & Security

### OAuth 2.0 Implementation

**Grant Type**: Authorization Code with PKCE (recommended for web apps)

**Token Endpoint**: `POST https://api.conectapay.com.br/oauth/token`

**Authorization Endpoint**: `https://app.conectapay.com.br/oauth/authorize`

### Authentication Flow

```
┌─────────┐                ┌─────────────┐              ┌──────────────┐
│ Partner │                │ ConectaPay  │              │ ConectaPay   │
│   App   │                │   Auth UI   │              │   API        │
└────┬────┘                └──────┬──────┘              └──────┬───────┘
     │                            │                             │
     │  1. GET /oauth/authorize   │                             │
     │  (client_id, redirect_uri, │                             │
     │   code_challenge, scope)    │                             │
     ├───────────────────────────>│                             │
     │                            │                             │
     │                            │  2. Show consent screen      │
     │                            │  (user approves)            │
     │                            │                             │
     │  3. Redirect with code     │                             │
     │<───────────────────────────┤                             │
     │                            │                             │
     │  4. POST /oauth/token      │                             │
     │  (code, code_verifier)     │                             │
     ├─────────────────────────────────────────────────────────>│
     │                            │                             │
     │  5. Access Token           │                             │
     │<─────────────────────────────────────────────────────────┤
     │                            │                             │
```

### Token Response

```json
{
  "access_token": "eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600,
  "refresh_token": "eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9...",
  "scope": "customers:read customers:write webhooks:read"
}
```

### Scopes

| Scope | Description | Required For |
|-------|-------------|--------------|
| `customers:read` | Read customer data | All integrations |
| `customers:write` | Create/update customers | Full API |
| `appointments:read` | Read appointment data | Clinic integrations |
| `appointments:write` | Create appointments | Clinic integrations |
| `leads:read` | Read lead data | Real estate integrations |
| `leads:write` | Create/update leads | Real estate integrations |
| `webhooks:read` | Read webhook config | All integrations |
| `webhooks:write` | Configure webhooks | All integrations |
| `payments:read` | Read payment data | POS integrations |
| `analytics:read` | Read analytics data | Strategic partners |

### API Key Authentication (Alternative)

For server-to-server integrations without user context:

```http
GET /v1/customers
Authorization: Bearer conectapay_pk_live_abc123...
X-Partner-ID: partner_abc123
```

**Key Format**: `conectapay_{environment}_{type}_{key}`

- `environment`: `pk` (public/sandbox) or `sk` (secret/production)
- `type`: `live` or `test`

**Security Requirements**:
- Keys must be stored securely (env vars, secrets manager)
- Secret keys (`sk_*`) must never be exposed in client-side code
- Rotate keys every 90 days (enforced via API)
- Revoke immediately upon compromise detection

### Rate Limiting

**Limits by Partner Tier**:

| Tier | Requests/Minute | Burst | Requests/Hour |
|------|-----------------|-------|---------------|
| Strategic | 200 | 400 | 10,000 |
| Growth | 100 | 200 | 5,000 |
| Affiliate | 50 | 100 | 2,500 |

**Rate Limit Headers**:
```http
X-RateLimit-Limit: 100
X-RateLimit-Remaining: 95
X-RateLimit-Reset: 1714135200
```

**Rate Limit Error** (429):
```json
{
  "success": false,
  "error": {
    "code": "rate_limit_exceeded",
    "message": "Rate limit exceeded. Try again in 30 seconds.",
    "retry_after": 30
  }
}
```

### Security Best Practices

**1. HTTPS Only**
- All API calls require TLS 1.3
- HSTS enabled on all endpoints
- Certificate pinning recommended for mobile apps

**2. Request Signing** (for high-security integrations)
```
signature = HMAC-SHA256(
  timestamp + method + path + body,
  partner_secret_key
)
```

Header: `X-Signature: {signature}`
Header: `X-Timestamp: {unix_timestamp}`

**3. IP Whitelisting**
- Partners can whitelist their server IPs
- Optional for enhanced security
- Configured via partner portal

**4. Audit Logging**
- All API requests logged with:
  - Request ID
  - Partner ID
  - Endpoint called
  - Timestamp
  - IP address
  - User agent
- Retention: 90 days

---

## Integration Tiers

### Tier 1: Widget Integration (Lowest Complexity)

**Best For**: Affiliate partners, small businesses, non-technical partners

**Implementation Time**: 15 minutes

**Technical Requirements**: Basic HTML/JavaScript knowledge

### Widget Embed

```html
<!-- Add to partner dashboard or settings page -->
<script src="https://cdn.conectapay.com.br/widget/v1/embed.js" async></script>
<div class="conectapay-widget"
     data-partner-id="partner_abc123"
     data-environment="production"
     data-theme="light"
     data-locale="pt-BR">
</div>
```

### Widget Configuration

| Attribute | Type | Required | Description |
|-----------|------|----------|-------------|
| `data-partner-id` | string | Yes | Partner ID from portal |
| `data-environment` | string | No | `production` or `sandbox` (default) |
| `data-theme` | string | No | `light`, `dark`, or `auto` (default) |
| `data-locale` | string | No | `pt-BR`, `es-BR` (default: `pt-BR`) |
| `data-show-metrics` | boolean | No | Show performance metrics (default: true) |

### Widget Features

- **Dashboard View**: Shows active automations, recovered revenue
- **Connect Button**: One-click WhatsApp connection
- **Settings Panel**: Configure automation rules
- **Reports**: Basic performance metrics
- **Commission Tracker**: View earned commissions

### Widget Events (Partner can listen to)

```javascript
document.addEventListener('conectapay:connected', (event) => {
  const { customer_id } = event.detail;
  // Customer connected WhatsApp - update your UI
});

document.addEventListener('conectapay:recovery', (event) => {
  const { amount, customer_id } = event.detail;
  // Recovery occurred - log analytics
});
```

---

### Tier 2: Webhook Integration (Medium Complexity)

**Best For**: Growth partners, POS systems, CRM with webhook capability

**Implementation Time**: 1-2 days

**Technical Requirements**: Server with webhook endpoint, basic HTTP handling

### Webhook Endpoints

ConectaPay sends webhooks to partner-defined endpoints:

**Webhook URL Format**: `https://partner-domain.com/conectapay/webhook`

### Webhook Authentication

Each webhook includes a signature for verification:

```http
X-Webhook-Signature: sha256=abc123...
X-Webhook-Timestamp: 1714135200
X-Webhook-ID: whk_abc123...
```

**Verification Process**:
```javascript
const crypto = require('crypto');

function verifyWebhook(payload, signature, timestamp, webhookSecret) {
  const message = timestamp + '.' + payload;
  const expectedSignature = crypto
    .createHmac('sha256', webhookSecret)
    .update(message)
    .digest('hex');

  return crypto.timingSafeEqual(
    Buffer.from(signature),
    Buffer.from('sha256=' + expectedSignature)
  );
}
```

### Webhook Event Types

| Event | Trigger | Payload |
|-------|---------|---------|
| `customer.created` | New customer signs up | Customer object |
| `customer.activated` | Customer activates WhatsApp | Customer object |
| `recovery.succeeded` | Sale/appointment recovered | Recovery details |
| `recovery.failed` | Recovery attempt failed | Failure reason |
| `payment.succeeded` | Payment collected | Payment details |
| `subscription.created` | Subscription started | Subscription details |
| `subscription.cancelled` | Subscription cancelled | Cancellation details |

### Webhook Payload Examples

**Customer Created**:
```json
{
  "event_id": "evt_abc123",
  "event_type": "customer.created",
  "timestamp": "2026-04-26T14:30:00-03:00",
  "data": {
    "customer": {
      "id": "cust_abc123",
      "partner_customer_id": "partner_cust_456",
      "name": "João Silva",
      "phone": "+5511999999999",
      "email": "joao@example.com",
      "segment": "clinic",
      "created_at": "2026-04-26T14:30:00-03:00"
    },
    "partner_id": "partner_abc123",
    "referral_code": "PARTNER20"
  }
}
```

**Recovery Succeeded**:
```json
{
  "event_id": "evt_def456",
  "event_type": "recovery.succeeded",
  "timestamp": "2026-04-26T15:30:00-03:00",
  "data": {
    "recovery": {
      "id": "rec_abc123",
      "customer_id": "cust_abc123",
      "type": "no_show_recovery",
      "original_value": 299.90,
      "recovered_amount": 299.90,
      "currency": "BRL",
      "recovery_method": "whatsapp",
      "messages_sent": 3,
      "time_to_recovery": "2h 15m"
    },
    "partner": {
      "id": "partner_abc123",
      "commission_earned": 89.97,
      "commission_rate": 0.30
    }
  }
}
```

### Webhook Response Requirements

- **2xx Status**: Acknowledge receipt
- **Retry on 5xx/timeout**: Exponential backoff (1m, 5m, 30m, 2h, max 24h)
- **Idempotency Key**: `event_id` prevents duplicate processing

### Webhook Configuration API

**Register Webhook**:
```http
POST /v1/webhooks
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "url": "https://partner.com/webhook",
  "events": ["customer.created", "recovery.succeeded"],
  "secret": "whsec_abc123...",
  "active": true
}
```

**Response**:
```json
{
  "success": true,
  "data": {
    "id": "wh_abc123",
    "url": "https://partner.com/webhook",
    "events": ["customer.created", "recovery.succeeded"],
    "status": "active",
    "created_at": "2026-04-26T14:30:00-03:00"
  }
}
```

---

### Tier 3: Full API Integration (Highest Complexity)

**Best For**: Strategic partners, deep product integration

**Implementation Time**: 2-3 weeks

**Technical Requirements**: Full REST API integration, OAuth 2.0, webhook handling

### Complete API Endpoint Reference

#### Customers

**List Customers**:
```http
GET /v1/customers?limit=20&offset=0&segment=clinic
Authorization: Bearer {access_token}
```

**Response**:
```json
{
  "success": true,
  "data": {
    "customers": [
      {
        "id": "cust_abc123",
        "partner_customer_id": "partner_456",
        "name": "Clínica Saúde",
        "phone": "+5511999999999",
        "email": "contato@clinicasaude.com.br",
        "segment": "clinic",
        "status": "active",
        "created_at": "2026-04-01T10:00:00-03:00",
        "metrics": {
          "total_recoveries": 47,
          "recovered_revenue": 5430.50,
          "this_month_recoveries": 12,
          "this_month_revenue": 1380.00
        }
      }
    ],
    "pagination": {
      "total": 127,
      "limit": 20,
      "offset": 0,
      "has_more": true
    }
  }
}
```

**Create Customer**:
```http
POST /v1/customers
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "partner_customer_id": "partner_456",
  "name": "Clínica Saúde",
  "phone": "+5511999999999",
  "email": "contato@clinicasaude.com.br",
  "segment": "clinic",
  "metadata": {
    "clinic_size": "medium",
    "specialties": ["dermatology", "cosmetic"]
  }
}
```

**Get Customer**:
```http
GET /v1/customers/{customer_id}
Authorization: Bearer {access_token}
```

**Update Customer**:
```http
PATCH /v1/customers/{customer_id}
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "phone": "+5511988888888",
  "metadata": {
    "last_contact_date": "2026-04-26"
  }
}
```

#### Appointments (Clinic Integrations)

**Create Appointment**:
```http
POST /v1/appointments
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "partner_appointment_id": "apt_456",
  "customer_id": "cust_abc123",
  "patient_name": "Maria Santos",
  "patient_phone": "+5511977777777",
  "scheduled_time": "2026-04-27T10:00:00-03:00",
  "service_type": "consultation",
  "estimated_value": 299.90,
  "metadata": {
    "doctor_name": "Dr. Silva",
    "clinic_room": "Sala 3"
  }
}
```

**Mark No-Show** (trigger for recovery automation):
```http
POST /v1/appointments/{appointment_id}/no-show
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "no_show_time": "2026-04-27T10:15:00-03:00",
  "reason": "patient_missed",
  "trigger_recovery": true
}
```

**Get Appointment**:
```http
GET /v1/appointments/{appointment_id}
Authorization: Bearer {access_token}
```

#### Leads (Real Estate Integrations)

**Create Lead**:
```http
POST /v1/leads
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "partner_lead_id": "lead_789",
  "customer_id": "cust_abc123",
  "lead_name": "João Oliveira",
  "lead_phone": "+5511966666666",
  "property_interest": {
    "type": "apartment",
    "location": "São Paulo - Jardins",
    "price_range": "500k-800k",
    "bedrooms": 2
  },
  "source": "website",
  "lead_score": 85,
  "metadata": {
    "utm_source": "google",
    "utm_campaign": "apartamentos_jardins"
  }
}
```

**Update Lead Status**:
```http
PATCH /v1/leads/{lead_id}
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "status": "contacted",
  "response_time_minutes": 5,
  "next_follow_up": "2026-04-27T14:00:00-03:00"
}
```

#### Automations

**Create Automation**:
```http
POST /v1/automations
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "customer_id": "cust_abc123",
  "type": "no_show_recovery",
  "trigger": {
    "event": "appointment.no_show",
    "delay_minutes": 15
  },
  "messages": [
    {
      "delay_minutes": 0,
      "template": "no_show_first",
      "params": {
        "patient_name": "{{patient_name}}",
        "reschedule_link": "{{reschedule_link}}"
      }
    },
    {
      "delay_minutes": 60,
      "template": "no_show_second",
      "params": {
        "patient_name": "{{patient_name}}"
      }
    }
  ],
  "active": true
}
```

**List Automations**:
```http
GET /v1/automations?customer_id={customer_id}
Authorization: Bearer {access_token}
```

**Update Automation**:
```http
PATCH /v1/automations/{automation_id}
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "active": false
}
```

#### Analytics

**Get Customer Metrics**:
```http
GET /v1/analytics/customers/{customer_id}?period=30d
Authorization: Bearer {access_token}
```

**Response**:
```json
{
  "success": true,
  "data": {
    "period": "30d",
    "metrics": {
      "total_recoveries": 47,
      "recovered_revenue": 5430.50,
      "recovery_rate": 0.68,
      "average_recovery_value": 115.54,
      "messages_sent": 141,
      "response_rate": 0.73,
      "conversion_to_reschedule": 0.52
    },
    "breakdown": {
      "by_day": [
        {"date": "2026-03-27", "recoveries": 2, "revenue": 240.00},
        {"date": "2026-03-28", "recoveries": 1, "revenue": 150.00}
      ],
      "by_service": [
        {"service": "consultation", "recoveries": 30, "revenue": 3600.00},
        {"service": "procedure", "recoveries": 17, "revenue": 1830.50}
      ]
    }
  }
}
```

**Get Partner Metrics**:
```http
GET /v1/analytics/partners?period=30d
Authorization: Bearer {access_token}
```

#### Webhooks

**List Webhooks**:
```http
GET /v1/webhooks
Authorization: Bearer {access_token}
```

**Get Webhook**:
```http
GET /v1/webhooks/{webhook_id}
Authorization: Bearer {access_token}
```

**Update Webhook**:
```http
PATCH /v1/webhooks/{webhook_id}
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "events": ["customer.created", "recovery.succeeded", "payment.succeeded"]
}
```

**Delete Webhook**:
```http
DELETE /v1/webhooks/{webhook_id}
Authorization: Bearer {access_token}
```

**Send Test Webhook**:
```http
POST /v1/webhooks/{webhook_id}/test
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "event_type": "customer.created",
  "test_data": {
    "customer": {
      "name": "Test Customer",
      "email": "test@example.com"
    }
  }
}
```

---

## Webhook System

### Webhook Delivery Architecture

```
┌─────────────────┐
│  ConectaPay     │
│   Platform      │
└────────┬────────┘
         │
         │ 1. Event Occurs
         │
         ▼
┌─────────────────┐
│  Event Queue    │
│  (RabbitMQ)     │
└────────┬────────┘
         │
         │ 2. Dequeue Event
         │
         ▼
┌─────────────────┐
│  Webhook Worker │
│  (Processors)   │
└────────┬────────┘
         │
         │ 3. Send to Partner
         │
         ▼
┌─────────────────┐     ┌──────────────┐
│  Retry Queue    │────▶│ Partner      │
│  (Failed)       │     │ Endpoint     │
└─────────────────┘     └──────────────┘
         │
         │ 4. Retry (exponential backoff)
         │
         ▼
┌─────────────────┐
│ Dead Letter     │
│ Queue (>24h)    │
└─────────────────┘
```

### Webhook Delivery Guarantees

- **At-Least-Once Delivery**: Webhooks may be duplicated, use `event_id` for idempotency
- **Ordering**: Best-effort ordering within 5-minute windows
- **Retry Duration**: Up to 24 hours
- **Retry Schedule**: 1m, 5m, 30m, 2h, 6h, 24h (exponential backoff)

### Webhook Status Codes

| Status | Action | Retry |
|--------|--------|-------|
| 200-299 | Success | No |
| 400 | Bad Request | No (client error) |
| 401, 403 | Auth Error | No (configuration needed) |
| 404 | Not Found | No |
| 408, 502, 503, 504 | Timeout/Server Error | Yes |
| 429 | Rate Limited | Yes (respect Retry-After) |
| 500+ | Server Error | Yes |

### Webhook Monitoring

**Delivery Status API**:
```http
GET /v1/webhooks/{webhook_id}/deliveries?limit=25
Authorization: Bearer {access_token}
```

**Response**:
```json
{
  "success": true,
  "data": {
    "deliveries": [
      {
        "id": "del_abc123",
        "event_id": "evt_def456",
        "event_type": "customer.created",
        "status": "success",
        "http_status": 200,
        "attempt": 1,
        "delivered_at": "2026-04-26T14:30:00-03:00",
        "duration_ms": 245
      },
      {
        "id": "del_def456",
        "event_id": "evt_ghi789",
        "event_type": "recovery.succeeded",
        "status": "failed",
        "http_status": 503,
        "attempt": 3,
        "last_attempt_at": "2026-04-26T14:25:00-03:00",
        "next_retry_at": "2026-04-26T16:25:00-03:00",
        "error": "Service Unavailable"
      }
    ]
  }
}
```

---

## Developer Experience

### Developer Portal

**URL**: `https://developers.conectapay.com.br`

### Portal Features

1. **Authentication**
   - API key generation (test/live)
   - OAuth 2.0 client registration
   - Webhook secret management

2. **Documentation**
   - Interactive API reference (Swagger/OpenAPI)
   - Integration guides by partner type
   - Code samples in multiple languages
   - Video tutorials

3. **Testing**
   - API explorer (test requests)
   - Webhook testing (simulate events)
   - Sandbox environment
   - Test data generator

4. **Monitoring**
   - API usage dashboard
   - Webhook delivery logs
   - Error rate tracking
   - Performance metrics

5. **Support**
   - Integration chat support
   - Community forum
   - Issue tracker
   - Status page

### API Documentation Standards

All endpoints documented with:

1. **Description**: Clear explanation of functionality
2. **Parameters**: Request parameters with types and validation
3. **Request Example**: Full example with headers/body
4. **Response Example**: Success response with all fields
5. **Error Responses**: Possible error codes and handling
6. **Code Samples**: JavaScript, Python, PHP, cURL
7. **Try It Out**: Interactive test panel

### Sandbox Environment

**URL**: `https://sandbox-api.conectapay.com.br/v1`

**Features**:
- Full API parity with production
- Test data (no real WhatsApp messages)
- No rate limiting
- Reset daily
- No billing

**Sandbox Credentials**:
- Test OAuth client: `test_client_abc123`
- Test API key: `conectapay_pk_test_abc123...`

### Code Sample Library

**JavaScript (Node.js)**:
```javascript
const ConectaPay = require('@conectapay/sdk');

const client = new ConectaPay({
  apiKey: 'conectapay_pk_live_abc123...',
  environment: 'production'
});

// Create customer
const customer = await client.customers.create({
  name: 'Clínica Saúde',
  phone: '+5511999999999',
  segment: 'clinic'
});

// Create automation
const automation = await client.automations.create({
  customer_id: customer.id,
  type: 'no_show_recovery',
  messages: [...]
});
```

**Python**:
```python
from conectapay import ConectaPay

client = ConectaPay(
    api_key='conectapay_pk_live_abc123...',
    environment='production'
)

# Create customer
customer = client.customers.create(
    name='Clínica Saúde',
    phone='+5511999999999',
    segment='clinic'
)

# List automations
automations = client.automations.list(
    customer_id=customer.id
)
```

**PHP**:
```php
use ConectaPay\ConectaPayClient;

$client = new ConectaPayClient([
    'api_key' => 'conectapay_pk_live_abc123...',
    'environment' => 'production'
]);

// Create customer
$customer = $client->customers->create([
    'name' => 'Clínica Saúde',
    'phone' => '+5511999999999',
    'segment' => 'clinic'
]);
```

---

## Testing & Validation

### Integration Testing Framework

### Test Environment Setup

1. **Sandbox Account Creation**
   - Partner creates sandbox account via portal
   - Receives test credentials
   - Test customer ID: `cust_test_abc123`

2. **Test Data Generation**
   - Use sandbox test data endpoints
   - Pre-configured test scenarios
   - No real messages sent

### Integration Test Checklist

**Phase 1: Authentication & Connectivity**
- [ ] OAuth flow completes successfully
- [ ] Access token received and valid
- [ ] API calls authenticated successfully
- [ ] Rate limits understood and tested

**Phase 2: Core API Functions**
- [ ] Create customer (POST /customers)
- [ ] Retrieve customer (GET /customers/{id})
- [ ] Update customer (PATCH /customers/{id})
- [ ] List customers (GET /customers)

**Phase 3: Domain-Specific Functions**
- [ ] **Clinics**: Create appointment, trigger no-show
- [ ] **Real Estate**: Create lead, update status
- [ ] **POS**: Send payment event

**Phase 4: Webhooks**
- [ ] Register webhook endpoint
- [ ] Receive test webhook
- [ ] Verify webhook signature
- [ ] Return 2xx response
- [ ] Test webhook failure retry

**Phase 5: Automations**
- [ ] Create automation
- [ ] Verify automation triggers
- [ ] Test message sequence
- [ ] Disable automation

**Phase 6: Analytics**
- [ ] Retrieve customer metrics
- [ ] Retrieve partner metrics
- [ ] Verify data accuracy

### Integration Certification

**Pre-Launch Validation**:
1. Partner completes integration checklist
2. ConectaPay team reviews integration
3. Test scenarios executed:
   - 10 test customers created
   - 50 test events processed
   - Webhook delivery verified
   - Error handling tested

**Certification Badge**:
- Certified partners receive badge
- Listed in integration directory
- Priority support
- Co-marketing eligibility

### Load Testing

**Before Production Launch**:
```bash
# Test 100 concurrent requests
ab -n 1000 -c 100 -H "Authorization: Bearer {token}" \
   https://api.conectapay.com.br/v1/customers

# Expected: All 2xx, avg response < 200ms
```

**Production Readiness Criteria**:
- P95 latency < 500ms
- 99.9% uptime during test period
- Error rate < 0.1%
- Webhook delivery > 99%

---

## Monitoring & Observability

### API Metrics Dashboard

**Real-Time Metrics**:
- Request rate (requests/second)
- Response time (p50, p95, p99)
- Error rate (by status code)
- Active connections
- Rate limit utilization

**Partner-Specific Metrics**:
- API usage by endpoint
- Webhook delivery rate
- Error rate by partner
- Integration health score

### Logging

**Request Logs**:
```json
{
  "timestamp": "2026-04-26T14:30:00-03:00",
  "request_id": "req_abc123",
  "partner_id": "partner_abc123",
  "method": "POST",
  "path": "/v1/customers",
  "status": 201,
  "duration_ms": 156,
  "user_agent": "ConectaPay-PythonSDK/1.2.3",
  "ip_address": "177.22.33.44"
}
```

**Error Logs**:
```json
{
  "timestamp": "2026-04-26T14:30:00-03:00",
  "request_id": "req_def456",
  "partner_id": "partner_abc123",
  "error_code": "validation_error",
  "error_message": "Phone number is required",
  "stack_trace": "...",
  "context": {
    "endpoint": "/v1/customers",
    "validation_errors": [
      {"field": "customer.phone", "message": "Required field"}
    ]
  }
}
```

### Alerts

**Critical Alerts** (Page on-call):
- API error rate > 5% for 5 minutes
- P95 latency > 2s for 5 minutes
- Webhook delivery failure rate > 10%
- Database connection failures

**Warning Alerts** (Email/Slack):
- Partner approaching rate limit (80%)
- Webhook retry queue > 1000
- Integration health score < 70%

### Status Page

**URL**: `https://status.conectapay.com.br`

**Displays**:
- API availability (all endpoints)
- Webhook delivery status
- Incident history (90 days)
- Scheduled maintenance

---

## Data Privacy & Compliance

### LGPD Compliance

**Data Principles**:
1. **Minimization**: Collect only necessary data
2. **Purpose Limitation**: Use data only for stated purposes
3. **Transparency**: Clear privacy policy
4. **Security**: Protect data with industry standards
5. **Rights**: Support user rights (access, deletion, portability)

### Customer Consent

**Consent Flow**:
1. Partner obtains customer consent for data sharing
2. Consent recorded in ConectaPay system
3. Customer can revoke consent at any time
4. Data deleted within 30 days of revocation

**Consent API**:
```http
POST /v1/customers/{customer_id}/consent
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "granted": true,
  "purpose": "whatsapp_automation",
  "granted_at": "2026-04-26T14:30:00-03:00",
  "ip_address": "177.22.33.44",
  "consent_document": "https://partner.com/privacy"
}
```

### Data Deletion (Right to be Forgotten)

**Delete Customer**:
```http
DELETE /v1/customers/{customer_id}
Authorization: Bearer {access_token}
```

**Behavior**:
- Immediate soft delete (data marked for deletion)
- Hard delete within 30 days
- Webhook notification sent: `customer.deleted`
- Cannot be undone

### Data Retention

| Data Type | Retention Period | Legal Basis |
|-----------|------------------|-------------|
| Customer PII | 90 days after contract end | Contract necessity |
| Message logs | 30 days | Legitimate interest |
| Analytics data | 2 years (aggregated) | Legitimate interest |
| Audit logs | 5 years | Legal requirement |
| Payment data | 5 years | Fiscal law |

### Data Sharing Agreement

**Contract Requirements**:
- Partners must sign Data Processing Agreement (DPA)
- LGPD compliance certification
- Data breach notification (24 hours)
- Annual security audit

---

## Maintenance & Versioning

### API Versioning Strategy

**URL-Based Versioning**: `/v1/`, `/v2/`, etc.

**Version Support Policy**:
- Current version (v1): Fully supported
- New version (v2): Released with 6-month migration window
- Deprecated version: 12-month notice before sunset
- Sunset version: No longer supported

**Version Changelog**:
- Maintained at `/changelog`
- Email notifications for breaking changes
- Migration guides provided

### Deprecation Process

**Phase 1: Announcement** (12 months before sunset)
- Email all affected partners
- Post in developer portal
- Provide migration guide

**Phase 2: Warning** (6 months before sunset)
- Response header: `X-API-Deprecation: true`
- Warning in response body
- Reminder emails (monthly)

**Phase 3: Sunset** (end of life)
- Endpoint returns 410 Gone
- Documentation moved to archive

### Backward Compatibility

**Guarantees**:
- New fields added (non-breaking)
- Field order not guaranteed
- String enum values may be added
- Timestamps always ISO 8601

**Breaking Changes** (require version bump):
- Field removed
- Field type changed
- Required field added
- Endpoint URL changed
- Authentication changed

### Scheduled Maintenance

**Maintenance Windows**:
- Weekly: Sunday 2:00-4:00 AM BRT (rolling deployment)
- Monthly: First Sunday 0:00-6:00 AM BRT (major updates)
- Notification: 72 hours advance notice

**Maintenance Mode Response**:
```json
{
  "success": false,
  "error": {
    "code": "maintenance_mode",
    "message": "API under maintenance. Return at 4:00 AM BRT.",
    "maintenance_start": "2026-05-04T02:00:00-03:00",
    "maintenance_end": "2026-05-04T04:00:00-03:00"
  }
}
```

---

## SDK Strategy

### Official SDKs

**Supported Languages**:
1. JavaScript/TypeScript (Node.js, Browser)
2. Python (3.8+)
3. PHP (7.4+, 8.x)
4. Go (1.18+)
5. Ruby (2.7+)

### SDK Features

**Core Functionality**:
- Authentication handling (OAuth, API keys)
- Request/response serialization
- Error handling
- Retry logic (exponential backoff)
- Webhook signature verification
- Logging

**Advanced Features**:
- Automatic token refresh
- Request batching
- Pagination helpers
- Webhook server (for receiving webhooks)
- Type definitions (TypeScript, Python type hints)

### SDK Usage Example (JavaScript)

```javascript
import { ConectaPay } from '@conectapay/sdk';

const client = new ConectaPay({
  apiKey: process.env.CONECTAPAY_API_KEY,
  environment: 'production',
  timeout: 30000,
  retryConfig: {
    maxRetries: 3,
    initialDelay: 1000
  }
});

// With automatic error handling
try {
  const customer = await client.customers.create({
    name: 'Clínica Saúde',
    phone: '+5511999999999',
    segment: 'clinic'
  });

  console.log('Customer created:', customer.id);
} catch (error) {
  if (error instanceof ConectaPay.ValidationError) {
    console.error('Validation failed:', error.errors);
  } else if (error instanceof ConectaPay.RateLimitError) {
    console.error('Rate limited. Retry at:', error.retryAt);
  }
}

// Pagination helper
for await (const customer of client.customers.list({ limit: 100 })) {
  console.log(customer.name);
}
```

### SDK Maintenance

**Release Cadence**:
- Minor updates: Monthly (bug fixes, improvements)
- Major updates: Quarterly (new features, breaking changes)

**Support Policy**:
- Current major version: Active support
- Previous major version: Security patches only
- Older versions: Unsupported

---

## Integration Playbooks

### Playbook 1: Clinic SaaS Integration

**Scenario**: Clinic management software wants to add no-show recovery

**Integration Type**: Full API

**Timeline**: 2-3 weeks

**Week 1: Setup**
1. Create sandbox account
2. Implement OAuth flow
3. Set up webhook endpoint
4. Test authentication

**Week 2: Core Integration**
1. Map clinic database → ConectaPay customers
2. Implement appointment sync (ConectaPay → Clinic)
3. Implement no-show detection (Clinic → ConectaPay)
4. Test webhook delivery

**Week 3: Launch**
1. Migrate existing customers to ConectaPay
2. Enable automation for all customers
3. Train support team
4. Launch to 10% of customers
5. Monitor for 1 week
6. Full launch

**Data Flow**:
```
┌─────────────┐           ┌──────────────┐           ┌─────────────┐
│  Clinic     │           │ ConectaPay   │           │  Patient    │
│   SaaS      │           │              │           │   Phone     │
└──────┬──────┘           └──────┬───────┘           └──────┬──────┘
       │                         │                          │
       │ 1. Appointment booked    │                          │
       ├────────────────────────>│                          │
       │   (webhook)              │                          │
       │                         │                          │
       │                         │ 2. Check for no-show     │
       │                         │   (scheduled)            │
       │                         │                          │
       │ 3. No-show detected     │                          │
       │<────────────────────────┤                          │
       │   (webhook)              │                          │
       │                         │                          │
       │ 4. Trigger recovery     │                          │
       ├────────────────────────>│                          │
       │                         │                          │
       │                         │ 5. Send WhatsApp message │
       │                         ├─────────────────────────>│
       │                         │                          │
       │                         │ 6. Patient responds      │
       │                         │<─────────────────────────┤
       │                         │                          │
       │ 7. Update appointment   │                          │
       │<────────────────────────┤                          │
       │   (webhook/API)          │                          │
       │                         │                          │
```

### Playbook 2: Real Estate CRM Integration

**Scenario**: Real estate CRM wants to add instant lead follow-up

**Integration Type**: Webhook + API

**Timeline**: 1-2 weeks

**Week 1: Setup**
1. Create webhook endpoint
2. Configure webhook in ConectaPay
3. Test webhook delivery
4. Implement signature verification

**Week 2: Integration**
1. Trigger automation on new lead
2. Sync lead status back to CRM
3. Add lead source tracking
4. Launch

**Data Flow**:
```
┌─────────────┐           ┌──────────────┐           ┌─────────────┐
│  Real       │           │ ConectaPay   │           │   Lead      │
│  Estate     │           │              │           │   Phone     │
│   CRM       │           └──────┬───────┘           └──────┬──────┘
└──────┬──────┘                  │                          │
       │                         │                          │
       │ 1. New lead created     │                          │
       │                         │                          │
       │ 2. Send to ConectaPay   │                          │
       ├────────────────────────>│                          │
       │   (API)                  │                          │
       │                         │                          │
       │                         │ 3. Send WhatsApp message │
       │                         ├─────────────────────────>│
       │                         │                          │
       │                         │ 4. Lead responds         │
       │                         │<─────────────────────────┤
       │                         │                          │
       │ 5. Update lead status   │                          │
       │<────────────────────────┤                          │
       │   (webhook)              │                          │
```

### Playbook 3: POS System Integration

**Scenario**: Payment processor wants to recover abandoned transactions

**Integration Type**: Webhook only

**Timeline**: 3-5 days

**Day 1: Setup**
1. Register webhook endpoint
2. Configure webhook events
3. Test webhook signature

**Day 2-3: Implementation**
1. Detect abandoned transactions
2. Send abandoned cart events
3. Handle recovery notifications

**Day 4-5: Testing & Launch**
1. Test with real transactions
2. Monitor webhook delivery
3. Launch

**Event Flow**:
```
┌─────────────┐           ┌──────────────┐           ┌─────────────┐
│    POS      │           │ ConectaPay   │           │  Customer   │
│   System    │           └──────┬───────┘           │   Phone     │
└──────┬──────┘                  │                  └──────┬──────┘
       │                         │                         │
       │ 1. Payment started      │                         │
       │                         │                         │
       │ 2. Cart abandoned       │                         │
       │    (30 min timeout)     │                         │
       │                         │                         │
       │ 3. Send webhook         │                         │
       ├────────────────────────>│                         │
       │   POST /abandoned-cart  │                         │
       │                         │                         │
       │                         │ 4. Send recovery message │
       │                         ├────────────────────────>│
       │                         │                         │
       │                         │ 5. Customer completes   │
       │                         │   payment               │
       │                         │<────────────────────────┤
       │                         │                         │
       │ 6. Payment webhook      │                         │
       │<────────────────────────┤                         │
       │   (process payment)      │                         │
```

---

## Appendix: API Reference Quick Reference

### Common Parameters

| Parameter | Type | Description |
|-----------|------|-------------|
| `partner_customer_id` | string | Partner's customer ID (for mapping) |
| `metadata` | object | Custom key-value pairs (max 1KB) |
| `created_at` | timestamp | ISO 8601 timestamp |
| `updated_at` | timestamp | ISO 8601 timestamp |

### Common Errors

| Error Code | HTTP Status | Description |
|------------|-------------|-------------|
| `validation_error` | 400 | Request validation failed |
| `authentication_error` | 401 | Invalid/missing credentials |
| `authorization_error` | 403 | Insufficient permissions |
| `not_found_error` | 404 | Resource not found |
| `conflict_error` | 409 | Resource already exists |
| `rate_limit_error` | 429 | Rate limit exceeded |
| `server_error` | 500 | Internal server error |

### Idempotency Keys

For safe retries, include idempotency key in requests:

```http
POST /v1/customers
Authorization: Bearer {access_token}
Idempotency-Key: uuid-key-abc123
Content-Type: application/json

{...}
```

**Behavior**:
- First request: Processes normally, stores result
- Duplicate requests: Returns cached result (no side effects)
- Key expiration: 48 hours

---

## Next Steps

1. **Review Integration Options**: Choose tier based on technical capability
2. **Create Sandbox Account**: Sign up at developers.conectapay.com.br
3. **Build Integration**: Follow playbook for your partner type
4. **Test Thoroughly**: Complete integration checklist
5. **Get Certified**: Pass validation to receive certification badge
6. **Launch**: Enable production access
7. **Monitor**: Track performance via partner portal

---

## Support Resources

- **Documentation**: https://developers.conectapay.com.br/docs
- **API Reference**: https://developers.conectapay.com.br/api-reference
- **Status Page**: https://status.conectapay.com.br
- **Support Email**: partners@conectapay.com.br
- **Community Forum**: https://community.conectapay.com.br
- **Slack Community**: conectapay-devs.slack.com

---

**Document Version**: 1.0
**Created**: 2026-04-26
**Author**: CMO Agent (55827422-a849-41d3-9286-0b5b8b002079)
**Task**: CON-132 - Partnership Integration Framework and API Strategy
**Size**: ~45 KB
**Related Documents**:
- partnership-strategy.md (CON-97) - Business partnership strategy
- abm-execution-checklist.md (CON-128) - ABM implementation framework
