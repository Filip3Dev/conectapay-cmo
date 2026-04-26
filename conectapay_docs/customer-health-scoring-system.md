# ConectaPay - Customer Health Scoring System and Early Warning Dashboard

**Version**: 1.0
**Created**: 2026-04-25
**Status**: Ready for Implementation
**Issue**: [CON-121](/conectapay/issues/CON-121)

---

## Executive Summary

This document defines ConectaPay's customer health scoring methodology and early warning dashboard design. The system enables proactive identification of at-risk customers and expansion opportunities, allowing the customer success team to prioritize actions and prevent churn before it happens.

**Key Objectives**:
- Predict churn 30+ days before it happens
- Identify expansion opportunities (upsell/cross-sell)
- Enable data-driven customer success prioritization
- Reduce churn rate by 20% in first 6 months

---

## 1. Health Score Methodology

### 1.1 Scoring Overview

**Scale**: 0-100 points
**Update Frequency**: Daily (automated)
**Data Sources**: Product usage, payment data, support interactions, engagement signals

| Health Level | Score Range | Status | Action Required |
|-------------|-------------|--------|-----------------|
| 🟢 Healthy | 80-100 | Green | Monitor, nurture for expansion |
| 🟡 At-Risk | 50-79 | Yellow | Proactive outreach required |
| 🔴 Critical | 0-49 | Red | Immediate intervention needed |
| ⚫ Unknown | N/A | Gray | New customer (<7 days), insufficient data |

### 1.2 Health Score Components

The health score is calculated from **6 weighted dimensions**:

```
Total Score = (Usage × 30%) + (Engagement × 20%) + (Payment × 15%) +
              (Support × 15%) + (Adoption × 10%) + (Growth × 10%)
```

#### Dimension 1: Product Usage (30% weight)

Measures how actively the customer uses ConectaPay's core features.

| Metric | Weight | Calculation | Max Points |
|--------|--------|-------------|------------|
| **WhatsApp Messages Sent** | 40% | Messages sent ÷ expected baseline (based on plan) | 40 |
| **Automation Rules Active** | 30% | Active rules ÷ total rules created | 30 |
| **Payment Volume (Pix)** | 20% | Monthly volume ÷ plan baseline | 20 |
| **Feature Usage Frequency** | 10% | Days with activity ÷ days in month | 10 |

**Expected Baselines by Plan**:
- **Starter** (R$ 97/mo): 500 messages/month, 2 automation rules
- **Growth** (R$ 197/mo): 2,000 messages/month, 5 automation rules
- **Scale** (R$ 397/mo): 10,000 messages/month, 15 automation rules

#### Dimension 2: Engagement (20% weight)

Measures customer interaction with the platform and team.

| Metric | Weight | Calculation | Max Points |
|--------|--------|-------------|------------|
| **Login Frequency** | 40% | Logins in last 30 days (0-30 scale) | 40 |
| **Response Rate** | 30% | Response to CS outreach ÷ total outreach | 30 |
| **Feature Exploration** | 20% | New features tried in last 90 days | 20 |
| **Content Engagement** | 10% | Email opens, link clicks, webinar attendance | 10 |

#### Dimension 3: Payment Health (15% weight)

Critical for SaaS revenue stability.

| Metric | Weight | Calculation | Max Points |
|--------|--------|-------------|------------|
| **Payment Status** | 50% | On-time = 50, Late 1-3 days = 30, Late 4+ days = 0 | 50 |
| **Payment Method** | 30% | Credit card = 30, Boleto = 20, Pix = 25 | 30 |
| **Outstanding Balance** | 20% | R$ 0 = 20, R$ 1-100 = 10, R$ 100+ = 0 | 20 |

#### Dimension 4: Support Signals (15% weight)

Support interactions can indicate both health and risk.

| Metric | Weight | Calculation | Max Points |
|--------|--------|-------------|------------|
| **Ticket Sentiment** | 40% | Positive = 40, Neutral = 20, Negative = 0 | 40 |
| **Ticket Volume** | 30% | 1-2 tickets = 30, 3-5 = 20, 6+ = 10, 0 = 15 | 30 |
| **Resolution Time** | 30% | <24h = 30, 24-48h = 20, 48h+ = 10 | 30 |

**Note**: High ticket volume with negative sentiment is a **critical churn signal**.

#### Dimension 5: Feature Adoption (10% weight)

Depth of platform adoption.

| Metric | Weight | Calculation | Max Points |
|--------|--------|-------------|------------|
| **Core Features Used** | 50% | (Features used ÷ total features) × 50 | 50 |
| **Advanced Features** | 30% | Using advanced features (API, webhooks) | 30 |
| **Integrations Active** | 20% | Active integrations (CRM, POS, etc.) | 20 |

**Core Features**: WhatsApp automation, Pix payments, message scheduling, contact management
**Advanced Features**: API access, webhooks, custom workflows, team collaboration

#### Dimension 6: Growth Signals (10% weight)

Indicators of account expansion potential.

| Metric | Weight | Calculation | Max Points |
|--------|--------|-------------|------------|
| **Team Size Trend** | 40% | Growing = 40, Stable = 20, Shrinking = 0 | 40 |
| **Volume Trend** | 30% | Growing = 30, Stable = 15, Shrinking = 0 | 30 |
| **Upgrade Inquiries** | 30% | Asked about upgrades = 30 | 30 |

---

## 2. Early Warning Dashboard Design

### 2.1 Dashboard Overview

**Purpose**: Real-time visibility into customer health portfolio
**Target Users**: Customer Success Managers, CSM Lead, CEO
**Refresh Rate**: Real-time (scores update daily, views refresh on load)

### 2.2 Dashboard Layout

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  CONECTAPAY - CUSTOMER HEALTH DASHBOARD                                    │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  📊 HEALTH SNAPSHOT                        🚨 ALERTS (3)                    │
│  ┌──────────────┐                        • CON-042: Health dropped 15pts    │
│  │ 🟢 127 (65%) │                        • CON-103: Payment 3 days late     │
│  │ 🟡  58 (30%) │                        • CON-087: 0 logins in 30 days     │
│  │ 🔴  12  (5%) │                                                         │
│  └──────────────┘                        [View All Alerts]                  │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  🔴 CRITICAL (12) - Requires Immediate Action                               │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Customer  │ Health │ Change│ Risk Factors         │ Last Contact    │   │
│  ├───────────┼────────┼───────┼──────────────────────┼─────────────────┤   │
│  │ Clínica   │  32    │  -15  │ 💳 Payment late      │ 45 days ago     │   │
│  │   São     │        │       │ 📉 Vol -80%          │                 │   │
│  │   Lucas   │        │       │ 🚫 0 logins (30d)    │                 │   │
│  ├───────────┼────────┼───────┼──────────────────────┼─────────────────┤   │
│  │ Imob.     │  41    │   -8  │ 💳 2 failed payments │ 12 days ago     │   │
│  │   Centro  │        │       │ 😠 Negative tickets  │                 │   │
│  │           │        │       │ 📉 Vol -45%          │                 │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│  [View All Critical] [Bulk Outreach]                                        │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  🟡 AT-RISK (58) - Schedule Outreach This Week                               │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Customer  │ Health │ Change│ Risk Factors         │ Action          │   │
│  ├───────────┼────────┼───────┼──────────────────────┼─────────────────┤   │
│  │ Clínica   │  72    │  -5   │ 📉 Vol -20%          │ [Call] [Email]  │   │
│  │   Vida    │        │       │ ⏱️ Low login freq    │                 │   │
│  ├───────────┼────────┼───────┼──────────────────────┼─────────────────┤   │
│  │ Imob.     │  68    │  -3   │ 🔧 1 automation rule │ [Call] [Email]  │   │
│  │   Sul     │        │       │ 📊 Stagnant usage    │                 │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│  [View All At-Risk] [Bulk Outreach]                                         │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  🟢 HEALTHY (127) - Expansion Opportunities                                  │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Customer  │ Health │ Change│ Growth Signals       │ Opportunity     │   │
│  ├───────────┼────────┼───────┼──────────────────────┼─────────────────┤   │
│  │ Clínica   │  94    │  +2   │ 📈 Vol +40%          │ [Upgrade]       │   │
│  │   Verde   │        │       │ 🆕 Asked about API   │ [Case Study]    │   │
│  ├───────────┼────────┼───────┼──────────────────────┼─────────────────┤   │
│  │ Imob.     │  91    │  +5   │ 👥 Team +2 users     │ [Upgrade]       │   │
│  │   Prime   │        │       │ ⚡ Hit plan limits   │ [Referral]      │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│  [View All Healthy] [Bulk Campaign]                                         │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  📈 TRENDS & INSIGHTS                                                       │
│  ┌───────────────────┐ ┌───────────────────┐ ┌───────────────────┐         │
│  │ Health Score      │ │ Churn Risk        │ │ Expansion Opp     │         │
│  │ Distribution      │ │ Forecast          │ │ Pipeline          │         │
│  │                   │ │                   │ │                   │         │
│  │ 🟢 65%            │ │ ⚠️ 8 customers     │ │ 💰 18 customers   │         │
│  │ 🟡 30%            │ │    at high risk    │ │    ready to       │         │
│  │ 🔴  5%            │ │    (30% churn      │ │    upgrade        │         │
│  │                   │ │    probability)    │ │                   │         │
│  └───────────────────┘ └───────────────────┘ └───────────────────┘         │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 2.3 Customer Detail View

Clicking any customer opens the **Health Detail Panel**:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  Clínica São Lucas - Health Score Detail                                    │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  Overall Health: 32/100 🔴 CRITICAL     (Last 30 days: 47 → 32)             │
│                                                                             │
│  📊 SCORE BREAKDOWN                                                         │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Dimension         │ Score │ Weight │ Contribution │ Status           │   │
│  ├───────────────────┼───────┼────────┼──────────────┼─────────────────┤   │
│  │ Usage             │  18/100│  30%   │    5.4       │ 🔴 Poor         │   │
│  │ Engagement        │  25/100│  20%   │    5.0       │ 🔴 Poor         │   │
│  │ Payment           │   0/100│  15%   │    0.0       │ 🔴 Critical     │   │
│  │ Support           │  45/100│  15%   │    6.8       │ 🟡 Fair         │   │
│  │ Adoption          │  30/100│  10%   │    3.0       │ 🔴 Poor         │   │
│  │ Growth            │  10/100│  10%   │    1.0       │ 🔴 Poor         │   │
│  ├───────────────────┼───────┼────────┼──────────────┼─────────────────┤   │
│  │ TOTAL             │  32/100│  100%  │   21.2       │ 🔴 Critical     │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
│  ⚠️ RISK FACTORS (5)                                                         │
│  • 💳 Payment is 12 days late (R$ 197 outstanding)                          │
│  • 📉 Message volume down 80% in last 30 days                               │
│  • 🚫 Zero logins in last 30 days                                           │
│  • 🔧 Only 1 of 5 automation rules active                                   │
│  • 😠 2 negative support tickets in last 90 days                            │
│                                                                             │
│  📈 30-DAY TREND                                                             │
│  100│                                                                       │
│ │   ╭──╮                                                                  │
│ 80│  ╭╯  ╰─╮                                                               │
│ │  ╭╯      ╰─╮                                                            │
│ 60│ ╭╯         ╰───╮                                                       │
│ │ ╭╯              ╰──╮                                                    │
│ 40│╭╯                  ╰──╮                                                │
│ │╭╯                      ╰─╮                                              │
│ 20│╭─────────────────────────╰───╮                                         │
│ 0├─────────────────────────────────╮                                       │
│   Mar 28 Apr 04 Apr 11 Apr 18 Apr 25                                         │
│                                                                             │
│  🎯 RECOMMENDED ACTIONS                                                     │
│  Priority 1 (Immediate):                                                   │
│  • [ ] Call customer about payment (use script #PAYMENT-RECOVERY)           │
│  • [ ] Schedule account review meeting                                     │
│  • [ ] Offer payment plan if needed                                        │
│                                                                             │
│  Priority 2 (This Week):                                                   │
│  • [ ] Conduct feature gap analysis                                        │
│  • [ ] Identify pain points from negative tickets                           │
│  • [ ] Create re-engagement campaign                                       │
│                                                                             │
│  Priority 3 (Next Week):                                                   │
│  • [ ] Assign dedicated CSM for 30-day recovery                            │
│  • [ ] Set weekly check-in cadence                                         │
│                                                                             │
│  📞 CONTACT HISTORY                                                         │
│  2026-04-10: Call - Discussed automation setup (Positive)                  │
│  2026-03-15: Email - Monthly check-in (No response)                        │
│  2026-02-28: Call - Onboarding completion (Positive)                       │
│                                                                             │
│  [Start Call] [Send Email] [Create Task] [Escalate]                        │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## 3. Automated Alert System

### 3.1 Alert Triggers

Alerts are generated automatically when health scores cross defined thresholds.

| Alert Level | Trigger Condition | Notifications |
|-------------|-------------------|---------------|
| 🔴 **Critical** | Health drops below 50 OR any dimension < 20 | Email + Slack + SMS |
| 🟡 **Warning** | Health drops 10+ points in 7 days | Email + Slack |
| 🟡 **At-Risk** | Health between 50-79 for 14+ days | Email + Slack |
| 🟢 **Opportunity** | Health above 90 AND growth signal | Slack only |
| ⚫ **New Customer** | Customer < 7 days old | No alerts (monitoring) |

### 3.2 Alert Notifications

**Email Alerts** (sent to assigned CSM + CSM Lead):
```
Subject: 🔴 ALERT: Clínica São Lucas - Health Score Critical (32/100)

Customer: Clínica São Lucas (CON-042)
Health Score: 32/100 🔴 CRITICAL
Change: -15 points in last 7 days

Top Risk Factors:
• 💳 Payment is 12 days late (R$ 197 outstanding)
• 📉 Message volume down 80% in last 30 days
• 🚫 Zero logins in last 30 days

Recommended Action:
Immediate phone call required. Use payment recovery script #PAYMENT-RECOVERY.

View in Dashboard: [link]
```

**Slack Alerts** (posted to #customer-health channel):
```
🚨 CUSTOMER HEALTH ALERT

🔴 Clínica São Lucas (CON-042) - Health: 32/100 (-15pts)

Risk Factors:
• 💳 Payment 12 days late
• 📉 Volume -80%
• 🚫 0 logins (30d)

Owner: @maria
Action: Call within 2 hours
Dashboard: [link]
```

**SMS Alerts** (for critical accounts only):
```
ConectaPay: 🔴 ALERT: Clínica São Lucas health critical (32/100).
Immediate action required. Check dashboard for details.
```

### 3.3 Alert Escalation

If no action is taken within defined timeframes:

| Alert Level | Escalation Time | Escalation Action |
|-------------|-----------------|-------------------|
| 🔴 Critical | 4 hours | Notify CSM Lead |
| 🔴 Critical | 24 hours | Notify CEO |
| 🟡 Warning | 48 hours | Notify CSM Lead |
| 🟡 At-Risk | 7 days | Notify CSM Lead |

---

## 4. Intervention Playbooks

### 4.1 Critical Health (0-49) - Immediate Intervention

**Objective**: Stop churn, recover account
**Timeline**: Act within 24 hours
**Owner**: Assigned CSM + CSM Lead

**Playbook Steps**:
1. **Payment Recovery** (if payment issue)
   - Call within 4 hours using script #PAYMENT-RECOVERY
   - Offer payment plan if needed (3-month max)
   - Understand root cause (financial vs. value)

2. **Account Review** (mandatory)
   - Schedule 30-min call within 48 hours
   - Review usage, pain points, value gaps
   - Document in CRM

3. **Recovery Plan** (co-create with customer)
   - Identify 1-2 quick wins
   - Set 30-day success metrics
   - Weekly check-in schedule

4. **Escalation** (if no response)
   - Day 3: Escalate to CSM Lead
   - Day 7: CEO outreach for enterprise accounts
   - Day 14: Final outreach before churn classification

**Success Metrics**:
- Health score increases 15+ points in 30 days
- Payment current
- 2+ logins per week

### 4.2 At-Risk Health (50-79) - Proactive Outreach

**Objective**: Prevent decline, restore health
**Timeline**: Act within 7 days
**Owner**: Assigned CSM

**Playbook Steps**:
1. **Risk Factor Analysis**
   - Identify primary risk factor(s)
   - Check for recent support tickets
   - Review usage trends

2. **Outreach** (choose based on risk factor)
   - **Low engagement**: Personalized email + value reminder
   - **Feature gaps**: Feature training session offer
   - **Payment concerns**: Proactive payment options email
   - **Support issues**: Follow-up call on ticket resolution

3. **Engagement Campaign**
   - Weekly value-focused touchpoints
   - Relevant content sharing (case studies, tips)
   - Feature webinar invitations

4. **30-Day Review**
   - Reassess health score
   - If improved → maintain quarterly touchpoint
   - If declined → escalate to critical playbook

**Success Metrics**:
- Health score stabilizes or increases
- Customer responds to outreach
- Feature adoption increases

### 4.3 Healthy Health (80-100) - Expansion & Advocacy

**Objective**: Drive growth, build advocacy
**Timeline**: Quarterly outreach + trigger-based
**Owner**: Assigned CSM

**Playbook Steps**:
1. **Growth Signal Monitoring**
   - Hitting plan limits → upgrade conversation
   - Team growth → additional seats offer
   - Feature inquiries → advanced feature demo
   - Positive feedback → case study request

2. **Expansion Outreach**
   - Timing: When health > 90 + growth signal present
   - Offer: Personalized upgrade proposal
   - Incentive: 20% discount for annual commitment

3. **Advocacy Building**
   - Identify happy customers (health > 90, positive tickets)
   - Request: Google review, case study, referral
   - Reward: R$ 150 referral credit per new customer

4. **Community Engagement**
   - Invite to customer advisory board (top 10%)
   - Feature beta testing opportunities
   - Exclusive webinars and events

**Success Metrics**:
- 20% of healthy customers upgrade annually
- 30% provide referrals or reviews
- 10% become case studies

### 4.4 New Customer (<7 days) - Onboarding Focus

**Objective**: Drive to first value fast
**Timeline**: First 14 days
**Owner**: Customer Success + Onboarding Specialist

**Playbook Steps**:
1. **Day 1**: Welcome email + onboarding scheduler
2. **Day 3**: Check-in on onboarding progress
3. **Day 7**: First value milestone celebration
4. **Day 14**: Health score first calculation (target: >70)

**Success Metrics**:
- Complete onboarding in 7 days
- Send first WhatsApp automation by day 14
- Health score > 70 by day 14

---

## 5. Data Collection & Integration

### 5.1 Required Data Sources

| Data Source | Metrics | Integration Method | Priority |
|-------------|---------|-------------------|----------|
| **Product DB** | Messages sent, automation rules, logins | Daily ETL | P0 |
| **Payment Gateway** | Payment status, failed transactions, volume | Webhook + API | P0 |
| **Support System** | Tickets, sentiment, response time | API integration | P0 |
| **CRM** | Customer demographics, plan, team size | API sync | P1 |
| **Email Platform** | Open rates, click rates | Webhook | P2 |
| **Analytics** | Feature usage, page views | SDK + API | P2 |

### 5.2 Minimum Viable Product (MVP) Data

For initial launch (Week 1-4), implement with:

**Essential Metrics** (can calculate 70% of health score):
- Messages sent (last 30 days)
- Login count (last 30 days)
- Payment status (current)
- Support ticket count (last 90 days)

**Nice-to-Have Metrics** (add in Month 2):
- Automation rules active
- Payment volume
- Feature adoption
- Team size changes

---

## 6. Implementation Roadmap

### Phase 1: Foundation (Week 1-2)
- [ ] Define data schema and collection requirements
- [ ] Set up database tables for health scores
- [ ] Build health score calculation engine
- [ ] Create basic dashboard UI (list view with health scores)

### Phase 2: Alerting (Week 3-4)
- [ ] Implement alert trigger system
- [ ] Set up email notifications
- [ ] Configure Slack alerts
- [ ] Create alert escalation rules

### Phase 3: Dashboard (Week 5-6)
- [ ] Build customer detail view
- [ ] Add health score trend charts
- [ ] Implement risk factor visualization
- [ ] Create recommended actions module

### Phase 4: Integration (Week 7-8)
- [ ] Integrate with product database
- [ ] Connect payment gateway webhooks
- [ ] Link support ticket system
- [ ] Set up automated data pipelines

### Phase 5: Testing (Week 9-10)
- [ ] Test with pilot customers (20 accounts)
- [ ] Validate score accuracy with manual review
- [ ] Train CSM team on dashboard and playbooks
- [ ] Collect feedback and iterate

### Phase 6: Launch (Week 11-12)
- [ ] Full rollout to all customers
- [ ] Monitor alert accuracy
- [ ] Measure impact on churn rate
- [ ] Optimize scoring weights quarterly

---

## 7. Success Metrics & KPIs

### 7.1 System Performance Metrics

| Metric | Target | Measurement |
|--------|--------|-------------|
| Health score accuracy | >80% | Correlation with actual churn |
| Alert precision | >70% | % of alerts that need action |
| False positive rate | <30% | % of alerts that don't need action |
| Dashboard usage | Daily | Active CSM users per day |

### 7.2 Business Impact Metrics

| Metric | Baseline | 6-Month Target | 12-Month Target |
|--------|----------|----------------|-----------------|
| Churn rate | 5% | 4% (-20%) | 3% (-40%) |
| Expansion revenue | 0% | 5% MRR | 10% MRR |
| Customer NPS | 40 | 50 | 60 |
| CSAT score | 4.2 | 4.5 | 4.7 |

### 7.3 Team Efficiency Metrics

| Metric | Before | After | Improvement |
|--------|--------|-------|-------------|
| Time to identify at-risk | 7-14 days | <1 day | 90% faster |
| Proactive outreach rate | 20% | 80% | 4x increase |
| Customer coverage per CSM | 50 | 100 | 2x increase |

---

## 8. Maintenance & Optimization

### 8.1 Quarterly Reviews

Every quarter, review and adjust:
- **Score weights**: Based on churn correlation analysis
- **Thresholds**: Based on false positive/negative rates
- **Alert triggers**: Based on CSM feedback
- **New metrics**: Add emerging signals

### 8.2 A/B Testing Framework

Test improvements to:
- Scoring methodology (e.g., new metrics, different weights)
- Alert thresholds (e.g., critical at 45 vs 50)
- Outreach timing (e.g., same day vs next day)
- Playbook effectiveness (e.g., call vs email first)

### 8.3 Continuous Learning

- **Churn post-mortems**: For every churned customer, analyze health score history
- **False positive analysis**: Review alerts that didn't need action, adjust triggers
- **Customer feedback**: Ask customers about health score accuracy
- **Competitive benchmarking**: Review industry best practices annually

---

## 9. Privacy & Security

### 9.1 Data Access

- **Dashboard access**: CSM team, CSM Lead, CEO only
- **Customer data**: Encrypted at rest and in transit
- **Audit logs**: All health score changes tracked
- **Retention**: Health score history kept for 2 years

### 9.2 Customer Communication

**Recommendation**: Do NOT share health scores with customers in early stages. Once validated:
- Share only if customer asks
- Frame as "engagement score" not "health score"
- Focus on positive factors first

---

## 10. Appendix

### 10.1 Health Score Calculation Example

**Customer**: Clínica São Lucas
**Plan**: Growth (R$ 197/mo)
**Billing Period**: Last 30 days

| Dimension | Raw Data | Calculation | Score | Weighted |
|-----------|----------|-------------|-------|----------|
| Usage | 500 messages sent | 500 ÷ 2000 × 40 = 10 | 18/100 | 5.4 |
| Engagement | 3 logins in 30d | 3 ÷ 30 × 40 = 4 | 25/100 | 5.0 |
| Payment | 12 days late | 0 points | 0/100 | 0.0 |
| Support | 2 negative tickets | 0 points | 45/100 | 6.8 |
| Adoption | 1 of 5 features | 20% × 50 = 10 | 30/100 | 3.0 |
| Growth | Volume -80% | 0 points | 10/100 | 1.0 |
| **TOTAL** | | | **32/100** | **21.2** |

### 10.2 Risk Factor Quick Reference

| Risk Factor | Severity | Weight | Action Timeline |
|-------------|----------|--------|-----------------|
| Payment >7 days late | 🔴 Critical | -20 | Immediate (4h) |
| Volume >50% decline | 🔴 Critical | -15 | Same day |
| Zero logins (30d) | 🔴 Critical | -15 | Same day |
| Negative tickets (2+) | 🟡 Warning | -10 | Within 7 days |
| Low feature adoption | 🟡 Warning | -5 | Within 14 days |
| Single automation rule | 🟡 Warning | -5 | Within 14 days |

---

## Document Control

**Next Review Date**: 2026-07-25 (Quarterly)
**Owner**: CMO Agent (55827422-a849-41d3-9286-0b5b8b002079)
**Related Documents**:
- [Customer Success Playbook](/conectapay/docs/customer-success-playbook.md)
- [Customer Retention Strategy](/conectapay/docs/customer-retention-strategy.md)
- [Sales Process Design](/conectapay/docs/sales-process-design.md)

**Change Log**:
| Date | Version | Changes | Author |
|------|---------|---------|--------|
| 2026-04-25 | 1.0 | Initial document creation | CMO Agent |
