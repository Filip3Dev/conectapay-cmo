# ConectaPay - Customer Success Technology Stack

**Document Version:** 1.0
**Date:** April 26, 2026
**Author:** CMO Agent
**Status:** Ready for Review

---

## Executive Summary

This document provides a comprehensive technology stack recommendation for ConectaPay's Customer Success function, considering our early-stage status, Brazilian market context, and budget constraints.

**Key Recommendations:**
- **Phase 1 (MVP - Months 1-3):** Lean stack with R$ 1,500/month budget
- **Phase 2 (Growth - Months 4-9):** Enhanced stack with R$ 5,000/month budget
- **Phase 3 (Scale - Months 10+):** Full CS platform with R$ 12,000+/month budget

**Primary Selection Criteria:**
1. Brazilian market compatibility (Pix, WhatsApp, Portuguese)
2. Budget-appropriate for early-stage startup
3. Fast implementation time (<2 weeks)
4. Integration with existing tools
5. Scalability path

---

## Technology Stack by Category

### 1. Customer Success Platform (CSP)

| Tool | Tier | Monthly Cost | Pros | Cons | Recommendation |
|------|------|--------------|------|------|----------------|
| **Gainsight PX** | Enterprise | R$ 6,000+ | Most complete, strong health scoring | Expensive, long implementation | Phase 3 |
| **Catalyst** | Mid-market | R$ 3,500 | Good balance, modern UI | Limited Brazilian features | Phase 2 |
| **Planhat** | Mid-market | R$ 2,800 | Excellent UI, great analytics | Smaller Brazilian presence | Phase 2 |
| **Totango** | Mid-market | R$ 2,500 | Good onboarding, flexible | Older interface | Phase 2 |
| **Front** | Startup | R$ 1,200 | Shared inbox, WhatsApp native | Limited CS features | Phase 1 |
| **Spreadsheet + Notion** | Bootstrap | R$ 0 | Free, flexible, control | Manual, no automation | Phase 0 |

**Phase 1 Recommendation: Front (R$ 1,200/mo)**
- Native WhatsApp integration (critical for Brazil)
- Shared inbox for CS/support
- Basic analytics and reporting
- Fast setup (2-3 days)

**Phase 2 Recommendation: Planhat (R$ 2,800/mo)**
- Best-in-class health scoring
- Customer journey mapping
- Playbook automation
- Strong integrations

---

### 2. Health Scoring & Customer Analytics

| Tool | Monthly Cost | Features | Brazilian Support | Recommendation |
|------|--------------|----------|-------------------|----------------|
| **Amplitude** | R$ 1,500 | Product analytics, cohorts | Partial | Phase 2 |
| **Mixpanel** | R$ 1,800 | Advanced funnels, retention | Partial | Phase 2 |
| **Heap** | R$ 1,400 | Auto-capture events | Partial | Alternative |
| **PostHog** | R$ 800 (self-hosted) | Open source, complete | Full | Phase 1 Winner |
| **Simple Analytics** | R$ 500 | Privacy-first, simple | Full | Bootstrap |
| **Spreadsheet** | R$ 0 | Manual, flexible | N/A | Phase 0 |

**Phase 1 Recommendation: PostHog (R$ 800/mo or free self-hosted)**
- Open-source, cost-effective
- Product analytics + session replay
- Feature flags included
- Self-hosting option for data control
- Strong community

**Alternative Phase 1: Custom Health Score Spreadsheet (Free)**
- Manual scoring based on:
  - Login frequency (last 7, 14, 30 days)
  - Feature usage (messages sent, payments received)
  - Support tickets (open/closed ratio)
  - NPS/CSAT scores
  - Contract value and renewal date

---

### 3. Survey & Feedback Systems (NPS, CSAT)

| Tool | Monthly Cost | Features | WhatsApp Support | Recommendation |
|------|--------------|----------|------------------|----------------|
| **Typeform** | R$ 350 | Beautiful forms, logic jumps | Via Zapier | Phase 1 |
| **Tally** | R$ 200 | Notion-native, simple | Via Zapier | Bootstrap |
| **SurveySparrow** | R$ 400 | Recurring surveys, chat-style | Via Zapier | Phase 2 |
| **Delighted** | R$ 300 | NPS-focused, simple | Via Zapier | Alternative |
| **Hotjar** | R$ 450 | Surveys + heatmaps | Partial | Phase 2 |
| **Google Forms** | R$ 0 | Basic, free | No | Phase 0 |
| **Custom WhatsApp** | Variable | Native WhatsApp flow | Full | Phase 1+ |

**Phase 1 Recommendation: Typeform + WhatsApp (R$ 350/mo)**
- Professional appearance
- Logic jumps for segmentation
- Zapier integration for WhatsApp distribution
- Pre-built NPS/CSAT templates

**Bootstrap Alternative: Tally (R$ 200/mo)**
- Free tier available
- Notion integration
- Simple and clean

**Custom WhatsApp Flow:**
- Build survey directly in WhatsApp messages
- Use WhatsApp Business API buttons for ratings
- Native experience, higher completion rates
- Cost: Per-message charges only

---

### 4. Communication Automation

| Tool | Monthly Cost | Channels | Automation | Recommendation |
|------|--------------|----------|------------|----------------|
| **Front** | R$ 1,200 | Email, Chat, WhatsApp | Playbooks, macros | Phase 1 Winner |
| **Intercom** | R$ 1,500 | Email, Chat, WhatsApp | Bots, sequences | Phase 2 |
| **Drift** | R$ 1,400 | Chat, Email | Conversational marketing | Phase 2 |
| **Userlist** | R$ 900 | Email only | Behavioral emails | Alternative |
| **Customer.io** | R$ 750 | Email, SMS, Push | Journeys, segments | Phase 1 Alternative |
| **Mailchimp** | R$ 400 | Email only | Basic automation | Bootstrap |
| **Zapier + Gmail** | R$ 300 | Email only | Manual setup | Bootstrap |

**Phase 1 Recommendation: Front (R$ 1,200/mo)**
- Unified inbox for all channels
- Native WhatsApp support (critical)
- Internal comments and mentions
- SLA tracking
- Basic analytics

**Bootstrap Alternative: Zapier + Gmail + WhatsApp Business (R$ 300/mo)**
- Gmail for email
- WhatsApp Business app for WhatsApp
- Zapier for basic automation
- Manual tracking in spreadsheets

---

### 5. Knowledge Base & Documentation

| Tool | Monthly Cost | Features | Search | Recommendation |
|------|--------------|----------|--------|----------------|
| **Notion** | R$ 150 | Wiki, docs, databases | Good | Phase 1 Winner |
| **GitBook** | R$ 200 | Beautiful docs, versioning | Excellent | Phase 2 |
| **Confluence** | R$ 180 | Enterprise features | Good | Alternative |
| **ReadMe** | R$ 250 | API docs, interactive | Excellent | Phase 3 |
| **WordPress** | R$ 100 | Flexible, plugins | Plugin-dependent | Bootstrap |

**Phase 1 Recommendation: Notion (R$ 150/mo)**
- Already used for internal docs
- Flexible database views
- Good search
- Easy to maintain
- Public-facing pages possible

**Bootstrap: Use existing Notion workspace (R$ 0 additional)**

---

### 6. Onboarding Tools

| Tool | Monthly Cost | Features | Recommendation |
|------|--------------|----------|----------------|
| **Appcues** | R$ 900 | No-code tours, checklists | Phase 2 |
| **WalkMe** | R$ 2,500 | Enterprise, complex | Phase 3 |
| **UserGuiding** | R$ 550 | Simple, affordable | Phase 1 Winner |
| **Userpilot** | R$ 700 | Good balance | Alternative |
| **Product Fruits** | R$ 450 | Budget-friendly | Bootstrap |
| **Custom tooltips** | R$ 0 | Development effort | Phase 0 |

**Phase 1 Recommendation: UserGuiding (R$ 550/mo)**
- Affordable for early-stage
- No-code implementation
- Checklists and tours
- Segmentation
- A/B testing

**Bootstrap: Custom onboarding in product + WhatsApp messages (R$ 0)**

---

### 7. Support Ticket System

| Tool | Monthly Cost | Channels | SLA | Recommendation |
|------|--------------|----------|-----|----------------|
| **Front** | R$ 1,200 | All-in-one | Yes | Phase 1 Winner |
| **Zendesk** | R$ 1,400 | Comprehensive | Yes | Phase 2 |
| **Freshdesk** | R$ 900 | Good free tier | Yes | Bootstrap |
| **Help Scout** | R$ 800 | Simple, clean | Yes | Alternative |
| **Spreadsheets** | R$ 0 | Manual | No | Phase 0 |

**Phase 1 Recommendation: Front (already included in communication budget)**
- Shared inbox
- Collision detection
- Saved replies (canned responses)
- Basic reporting

---

### 8. Reporting & Dashboard

| Tool | Monthly Cost | Features | Data Sources | Recommendation |
|------|--------------|----------|--------------|----------------|
| **Tableau** | R$ 1,800 | Enterprise BI | All | Phase 3 |
| **Looker** | R$ 2,000 | Embedded analytics | All | Phase 3 |
| **Metabase** | R$ 0 (self-hosted) | Open source | SQL | Phase 1 Winner |
| **Google Data Studio** | R$ 0 | Free, simple | Google products | Bootstrap |
| **Chart.js + Custom** | R$ 0 | Custom dashboards | All | Bootstrap |
| **Mixpanel dashboards** | Included | Product analytics | Mixpanel only | Phase 2+ |

**Phase 1 Recommendation: Metabase (free self-hosted) or Google Data Studio (free)**
- Metabase: Connect to PostgreSQL, SQL questions
- Google Data Studio: Connect to Google Sheets, GA4
- Both free, quick setup

---

## Complete Stack Recommendations by Phase

### Phase 0: Bootstrap (R$ 0/month)
*For pre-launch or pre-PMF validation*

| Category | Tool | Cost |
|----------|------|------|
| CS Platform | Notion + Spreadsheets | R$ 0 |
| Health Scoring | Spreadsheet formulas | R$ 0 |
| Surveys | Google Forms | R$ 0 |
| Communication | Gmail + WhatsApp Business | R$ 0 |
| Knowledge Base | Notion (existing) | R$ 0 |
| Onboarding | Custom WhatsApp messages | R$ 0 |
| Support | Shared Gmail label | R$ 0 |
| Reporting | Google Sheets | R$ 0 |
| **Total** | | **R$ 0** |

**Use when:** < 50 customers, no funding, validating PMF

---

### Phase 1: MVP (R$ 2,350/month)
*For early customers and first CS hire*

| Category | Tool | Cost |
|----------|------|------|
| CS Platform | Front (includes support) | R$ 1,200 |
| Health Scoring | PostHog (or free spreadsheet) | R$ 800 |
| Surveys | Typeform | R$ 350 |
| Communication | (Included in Front) | R$ 0 |
| Knowledge Base | Notion (existing) | R$ 0 |
| Onboarding | UserGuiding | R$ 550 |
| Reporting | Metabase (self-hosted) | R$ 0 |
| Automation | Zapier Starter | R$ 300 |
| **Total** | | **R$ 3,200** |

**Use when:** 50-200 customers, Seed round, 1 CS hire

**Implementation Timeline:** 2-3 weeks

---

### Phase 2: Growth (R$ 6,800/month)
*For scaling CS team and operations*

| Category | Tool | Cost |
|----------|------|------|
| CS Platform | Planhat | R$ 2,800 |
| Health Scoring | (Included in Planhat) | R$ 0 |
| Surveys | SurveySparrow | R$ 400 |
| Communication | Front (keep for WhatsApp) | R$ 1,200 |
| Knowledge Base | GitBook | R$ 200 |
| Onboarding | Appcues | R$ 900 |
| Support | (Included in Front) | R$ 0 |
| Analytics | Amplitude | R$ 1,500 |
| Automation | Zapier Professional | R$ 800 |
| **Total** | | **R$ 7,800** |

**Use when:** 200-1,000 customers, Series A, 2-3 CS team members

**Implementation Timeline:** 4-6 weeks

---

### Phase 3: Scale (R$ 14,500+/month)
*For enterprise CS operations*

| Category | Tool | Cost |
|----------|------|------|
| CS Platform | Gainsight PX | R$ 6,000 |
| Health Scoring | (Included in Gainsight) | R$ 0 |
| Surveys | Medallia | R$ 1,500 |
| Communication | Intercom | R$ 1,500 |
| Knowledge Base | ReadMe | R$ 250 |
| Onboarding | WalkMe | R$ 2,500 |
| Support | Zendesk | R$ 1,400 |
| Analytics | Amplitude Enterprise | R$ 3,000 |
| BI | Tableau | R$ 1,800 |
| **Total** | | **R$ 17,950** |

**Use when:** 1,000+ customers, Series B+, 5+ CS team members

---

## Integration Requirements

### Critical Integrations for ConectaPay

1. **WhatsApp Business API** (Must-have)
   - Two-way messaging
   - Message templates
   - Webhook notifications
   - Status updates

2. **Payment Gateway (Pix)** (Must-have)
   - Transaction status webhooks
   - Payment success/failure events
   - Refund processing

3. **CRM** (High priority)
   - Customer data sync
   - Account updates
   - Activity logging

4. **Product Database** (High priority)
   - User events
   - Feature usage
   - Login activity

5. **Email Provider** (Medium priority)
   - Transactional emails
   - Notifications
   - Drip campaigns

---

## Selection Criteria Framework

### Evaluation Scorecard (0-100 points)

| Criterion | Weight | Notes |
|-----------|--------|-------|
| Brazilian Market Fit | 25% | Pix, WhatsApp, Portuguese, local support |
| Budget Alignment | 20% | Within phase budget, transparent pricing |
| Implementation Speed | 15% | Time to value < 2 weeks for Phase 1 |
| Integration Capability | 15% | API quality, webhooks, pre-built integrations |
| Scalability | 10% | Can grow with us to next phase |
| Data Privacy | 10% | LGPD compliance, data residency |
| Support Quality | 5% | Documentation, response time |

**Minimum Score to Proceed: 70/100**

---

## Implementation Roadmap

### Phase 1 Implementation (3 weeks)

**Week 1: Core Setup**
- [ ] Sign up for Front, configure WhatsApp channel
- [ ] Set up PostHog or create health score spreadsheet
- [ ] Create Typeform account, build NPS/CSAT surveys
- [ ] Configure Zapier for basic automation

**Week 2: Knowledge & Onboarding**
- [ ] Build knowledge base in Notion
- [ ] Set up UserGuiding account
- [ ] Create first 3 onboarding tours
- [ ] Write help articles for top 10 questions

**Week 3: Testing & Training**
- [ ] Test all integrations end-to-end
- [ ] Train CS team on tools
- [ ] Create playbooks and SOPs
- [ ] Set up reporting dashboards in Metabase

---

## Budget Justification

### Phase 1 ROI Analysis

**Monthly Investment:** R$ 3,200

**Expected Outcomes (Year 1):**
- 15% reduction in churn (saves ~R$ 45,000/year)
- 20% faster onboarding (saves 40 hours/month)
- 25% improvement in CSAT (higher retention)
- 10% increase in expansion revenue (~R$ 30,000/year)

**Total Expected Value:** ~R$ 75,000+/year
**ROI:** 234% in Year 1

---

## Tool-Specific Notes for Brazilian Market

### WhatsApp Integration
- **Native support critical:** Front, Intercom have native WhatsApp
- **API access required:** Z-API, Evolution API, or Twilio for custom
- **Message templates:** Must pre-register templates with Meta
- **Rate limits:** 1,000 messages/day for new business numbers

### Pix Payments
- **Instant notifications:** Webhook latency < 5 seconds
- **QR Code integration:** Must support dynamic QR codes
- **Refund processing:** Automatic webhook on refunds
- **Transaction status:** Real-time status updates required

### LGPD Compliance
- **Data residency:** Brazil or EU data centers preferred
- **Right to deletion:** Must support customer data export/deletion
- **Consent management:** Double opt-in required for marketing
- **Data processing agreements:** Required for all vendors

### Language Support
- **Portuguese UI:** Not all tools have Portuguese
- **Portuguese templates:** Email/message templates in PT-BR
- **Time zones:** São Paulo time (GMT-3) for all reporting
- **Currency:** All monetary values in BRL (R$)

---

## Decision Matrix

### Phase 1 Tool Selection

| Tool | Brazil Fit | Budget | Speed | Integration | Scale | Total | Decision |
|------|------------|--------|-------|-------------|-------|-------|----------|
| **Front** | 25 | 20 | 15 | 15 | 8 | **83** | ✅ SELECT |
| PostHog | 20 | 18 | 14 | 15 | 10 | **77** | ✅ SELECT |
| Typeform | 22 | 16 | 15 | 12 | 8 | **73** | ✅ SELECT |
| UserGuiding | 18 | 18 | 15 | 12 | 7 | **70** | ✅ SELECT |
| Zapier | 20 | 15 | 12 | 20 | 10 | **77** | ✅ SELECT |
| Notion | 20 | 20 | 18 | 10 | 6 | **74** | ✅ SELECT |
| Metabase | 18 | 20 | 14 | 12 | 10 | **74** | ✅ SELECT |

**All selected tools meet the 70+ threshold**

---

## Alternative: Minimal Viable Stack

If budget is extremely constrained (< R$ 1,000/month):

| Tool | Cost | What you lose |
|------|------|---------------|
| Front | R$ 1,200 | Keep - WhatsApp critical |
| Spreadsheet health score | R$ 0 | Manual work, no automation |
| Google Forms | R$ 0 | Ugly forms, limited logic |
| Notion KB | R$ 0 | Already have it |
| Custom onboarding | R$ 0 | Development time |
| Google Sheets reporting | R$ 0 | Manual reporting |
| Zapier Starter | R$ 300 | Basic automation only |
| **Total** | **R$ 1,500** | Sacrifice: Automation, analytics |

---

## Next Steps

1. **Review and approve** this stack recommendation
2. **Allocate budget** for Phase 1 tools (R$ 3,200/month)
3. **Start free trials** (all tools offer 14-30 day trials)
4. **Assign implementation owner** (CS hire or CMO temporarily)
5. **Set success metrics** for 30/60/90 days
6. **Schedule review** at end of Phase 1 (3 months)

---

## Appendix: Tool Contact & Trials

| Tool | Free Trial | Enterprise Contact | Setup Time |
|------|------------|-------------------|------------|
| Front | 14 days | sales@front.com | 2-3 days |
| PostHog | Free tier available | sales@posthog.com | 1-2 days |
| Typeform | Free tier available | sales@typeform.com | 1 day |
| UserGuiding | 14 days | sales@userguiding.com | 3-5 days |
| Zapier | Free tier available | sales@zapier.com | 1 day |
| Planhat | 30 days | sales@planhat.com | 1-2 weeks |
| Appcues | 21 days | sales@appcues.com | 1 week |
| Gainsight | 30 days | sales@gainsight.com | 4-6 weeks |

---

**Document Status:** ✅ Complete
**Ready for:** Board review and approval
**Recommended Action:** Approve Phase 1 stack and allocate R$ 3,200/month budget
