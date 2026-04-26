# ConectaPay - Customer Success Metrics and Health Score Dashboard

**Version**: 1.0
**Created**: 2026-04-26
**Status**: Ready for Implementation
**Issue**: [CON-175](/conectapay/issues/CON-175)

---

## Executive Summary

This document defines ConectaPay's comprehensive Customer Success Metrics and Health Score Dashboard system—a unified, real-time monitoring platform that enables data-driven customer success decisions. The dashboard integrates health scoring, VoC metrics, operational KPIs, and predictive analytics into a single source of truth for the entire customer success organization.

**Key Objectives**:
- Provide real-time visibility into customer health portfolio
- Enable proactive churn prevention through early warning signals
- Track customer success team performance and operational efficiency
- Measure and optimize customer experience at every touchpoint
- Drive data-driven decisions with predictive analytics and benchmarking

**Dashboard System Components**:
1. **Executive Dashboard** - Strategic KPIs and business health
2. **Health Score Dashboard** - Customer health monitoring and intervention
3. **Operations Dashboard** - Team performance and operational efficiency
4. **VoC Dashboard** - Customer feedback and sentiment analysis
5. **Predictive Analytics Dashboard** - Forecasting and risk prediction

---

## Part 1: Dashboard Architecture Overview

### 1.1 Dashboard Hierarchy

```
┌─────────────────────────────────────────────────────────────────┐
│                    CONECTAPAY CS DASHBOARD SYSTEM               │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  ┌──────────────────┐  ┌──────────────────┐  ┌──────────────┐ │
│  │   Executive      │  │   Health Score   │  │   VoC        │ │
│  │   Dashboard      │  │   Dashboard      │  │   Dashboard  │ │
│  │   (Strategic)    │  │   (Tactical)     │  │   (Quality)  │ │
│  └──────────────────┘  └──────────────────┘  └──────────────┘ │
│           │                     │                     │         │
│           └─────────────────────┴─────────────────────┘         │
│                             │                                   │
│                    ┌────────▼────────┐                         │
│                    │  Operations     │                         │
│                    │  Dashboard      │                         │
│                    │  (Execution)    │                         │
│                    └─────────────────┘                         │
│                             │                                   │
│                    ┌────────▼────────┐                         │
│                    │  Predictive     │                         │
│                    │  Analytics      │                         │
│                    │  (Forecasting)  │                         │
│                    └─────────────────┘                         │
└─────────────────────────────────────────────────────────────────┘
```

### 1.2 Dashboard Access & Permissions

| Dashboard | Primary Users | Update Frequency | Access Level |
|-----------|---------------|------------------|--------------|
| **Executive** | CEO, CMO, Head of CS | Real-time | Read-only |
| **Health Score** | CSMs, CS Lead, CMO | Real-time | Edit (CSMs) |
| **Operations** | CS Ops, CS Lead | Hourly | Edit (CS Ops) |
| **VoC** | VoC Lead, Product Lead, CMO | Daily | Edit (VoC team) |
| **Predictive** | Data Team, CS Lead | Weekly | Read-only |

### 1.3 Data Integration Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                      DATA SOURCES                               │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐            │
│  │   Product   │  │   Payment   │  │   Support   │            │
│  │   Database  │  │   Gateway   │  │   System    │            │
│  └──────┬──────┘  └──────┬──────┘  └──────┬──────┘            │
│         │                │                │                     │
│         └────────────────┼────────────────┘                     │
│                          ▼                                     │
│              ┌───────────────────────┐                         │
│              │   Data Warehouse      │                         │
│              │   (PostgreSQL/BigQuery) │                       │
│              └───────────┬───────────┘                         │
│                          │                                     │
│                          ▼                                     │
│              ┌───────────────────────┐                         │
│              │   Analytics Engine    │                         │
│              │   (Python/R/SQL)      │                         │
│              └───────────┬───────────┘                         │
│                          │                                     │
│         ┌────────────────┼────────────────┐                   │
│         ▼                ▼                ▼                   │
│  ┌───────────┐    ┌───────────┐    ┌───────────┐              │
│  │Dashboard 1│    │Dashboard 2│    │Dashboard 3│    ...       │
│  │Executive  │    │Health     │    │Operations │              │
│  └───────────┘    └───────────┘    └───────────┘              │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

---

## Part 2: Executive Dashboard (Strategic KPIs)

### 2.1 Dashboard Layout

```
┌─────────────────────────────────────────────────────────────────────────────┐
│           CONECTAPAY - CUSTOMER SUCCESS EXECUTIVE DASHBOARD                 │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  📊 SNAPSHOT (Last 30 Days)              🚨 ALERTS (5)                      │
│  ┌────────────────────────────────────┐  • SEV-1: WhatsApp API down (45m)  │
│  │ Total Customers: 1,847 (+127)      │  • 12 customers entered At-Risk     │
│  │ Health Score: 73/100 (+2)          │  • NPS dropped 5 pts this week      │
│  │ NRR: 108% (Target: 110%)           │  • 3 customers at churn risk        │
│  │ Churn Rate: 3.8% (Target: ≤5%)     │  • Expansion pipeline down 15%      │
│  └────────────────────────────────────┘  [View All Alerts]                  │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  💰 REVENUE METRICS                                                         │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ MRR: R$ 364.890  │  ARR: R$ 4.378.680  │  Expansion: R$ 29.190 (8%)    │   │
│  │ +12.3% vs last month  │  +18.7% vs last quarter  │  Target: 10%       │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ❤️ CUSTOMER HEALTH                                                         │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ 🟢 Healthy: 1.200 (65%)  │  🟡 At-Risk: 58 (3%)  │  🔴 Critical: 12 (1%)│   │
│  │ Target: 80% healthy     │  Action: 50 outreach  │  Action: 12 rescue │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
│  Health Score Distribution:                                                │
│  100│                          ● (Target: 80 avg)                          │
│   80│                     ●     ●     ●                                    │
│   60│                ●     ●  ●  ●  ●  ●     ● (Current: 73 avg)          │
│   40│           ●  ●  ●  ●                                                     │
│   20│        ●                                                                   │
│    0├─────────────────────────────────────────────────────────              │
│      Jan  Feb  Mar  Apr  May  Jun  Jul  Aug  Sep  Oct  Nov  Dec              │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  📈 RETENTION & EXPANSION                                                   │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Gross Retention: 95.2%  │  Net Retention: 108.3%  │  CLV: R$ 4.890     │   │
│  │ Target: 95%            │  Target: 110%           │  Target: R$ 5.000  │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
│  Churn by Cause (Last 30 Days):                                            │
│  No Value Achieved (35%)  ████████████                                     │
│  Price Sensitivity (25%)  ████████                                         │
│  Technical Issues (15%)  ████                                             │
│  Out of Business (10%)  ███                                               │
│  Competitor (8%)  ██                                                        │
│  Other (7%)  ██                                                             │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ⭐ CUSTOMER EXPERIENCE                                                     │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ NPS: 48 (Target: 60)  │  CSAT: 4.6/5.0 (Target: 4.7)  │  Time-to-First-Value: 3.2 days │   │
│  │ Trend: ↗️ +3 vs last month  │  Trend: → Stable              │  Target: ≤2 days │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  👥 TEAM PERFORMANCE                                                        │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ CSM Capacity: 85% (615 customers / 720 max)  │  CSM Productivity: 127% │   │
│  │ At-Risk Coverage: 100% (70/70 customers)     │  Response Time: 2.3h   │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 2.2 Executive KPI Definitions

| Metric | Definition | Target | Data Source |
|--------|------------|--------|-------------|
| **Total Customers** | Active paying customers | 2,000+ | CRM |
| **Avg Health Score** | Mean health score across all customers | 80+ | Health Score Engine |
| **NRR (Net Revenue Retention)** | (MRR + Expansion - Churn) / MRR | 110%+ | Billing System |
| **GRR (Gross Retention)** | Customers retained / Total customers | 95%+ | CRM |
| **Churn Rate** | Customers churned / Total customers | ≤5% | CRM |
| **Expansion Rate** | Expansion MRR / Total MRR | 10%+ | Billing System |
| **NPS (Net Promoter Score)** | % Promoters - % Detractors | 60+ | VoC System |
| **CSAT** | Avg customer satisfaction rating (1-5) | 4.7+ | Support System |
| **Time-to-First-Value** | Days from signup to first value event | ≤2 days | Product Analytics |
| **CLV (Customer Lifetime Value)** | Avg revenue per customer × Gross margin × Lifetime | R$ 5K+ | Analytics |

### 2.3 Alert Thresholds (Executive)

| Alert Type | Trigger | Action | Escalation |
|------------|---------|--------|------------|
| **Churn Spike** | Churn rate >8% in any week | Investigate root cause | CEO notified |
| **NPS Drop** | NPS drops >10 points week-over-week | Deep dive into detractors | CMO + CS Lead |
| **Health Decline** | Avg health score <70 for 7+ days | Portfolio review | Executive team |
| **Expansion Miss** | Expansion rate <5% for 2+ months | Program review | CS Lead + Sales |
| **Team Capacity** | CSM capacity >95% for 2+ weeks | Hire more CSMs | Head of CS |

---

## Part 3: Health Score Dashboard (Tactical)

### 3.1 Dashboard Layout

```
┌─────────────────────────────────────────────────────────────────────────────┐
│           CONECTAPAY - CUSTOMER HEALTH SCORE DASHBOARD                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  📊 HEALTH PORTFOLIO SNAPSHOT                    🚨 ACTIVE ALERTS (18)     │
│  ┌────────────────────────────────────┐  • 12 customers entered Critical   │
│  │ 🟢 Healthy: 1.200 (65%)            │  • 58 customers in At-Risk        │
│  │ 🟡 At-Risk: 58 (3%)                │  • 6 health score drops >15 pts   │
│  │ 🔴 Critical: 12 (1%)               │  [View All Alerts]                │
│  │ ⚫ Unknown: 577 (31%)              │                                  │
│  └────────────────────────────────────┘                                  │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  🔴 CRITICAL (12) - Immediate Action Required                               │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Customer      │ Health│ Change│ Risk Factors          │ CSM   │Action│   │
│  ├───────────────┼───────┼───────┼──────────────────────┼───────┼──────│   │
│  │ Clínica São   │  32   │  -15  │ 💳 Payment 12d late  │ Maria │ [Call]│   │
│  │ Lucas         │       │       │ 📉 Vol -80%          │       │[Email]│   │
│  │               │       │       │ 🚫 0 logins (30d)    │       │[Task] │   │
│  ├───────────────┼───────┼───────┼──────────────────────┼───────┼──────│   │
│  │ Imob. Centro  │  41   │   -8  │ 💳 2 failed payments │ João  │ [Call]│   │
│  │               │       │       │ 😠 Negative tickets  │       │[Email]│   │
│  │               │       │       │ 📉 Vol -45%          │       │[Task] │   │
│  ├───────────────┼───────┼───────┼──────────────────────┼───────┼──────│   │
│  │ Academia Fit  │  28   │  -22  │ 💳 Payment 20d late  │ Ana   │ [Call]│   │
│  │               │       │       │ 😠 3 negative tickets │       │[Email]│   │
│  │               │       │       │ 🔧 0 automation rules│       │[Task] │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│  [View All Critical] [Bulk Outreach] [Export CSV]                            │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  🟡 AT-RISK (58) - Schedule Outreach This Week                              │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Customer      │ Health│ Change│ Risk Factors          │ CSM   │Action│   │
│  ├───────────────┼───────┼───────┼──────────────────────┼───────┼──────│   │
│  │ Clínica Vida  │  72   │  -5   │ 📉 Vol -20%          │ Maria │ [Call]│   │
│  │               │       │       │ ⏱️ Low login (2/mo) │       │[Email]│   │
│  ├───────────────┼───────┼───────┼──────────────────────┼───────┼──────│   │
│  │ Imob. Sul     │  68   │  -3   │ 🔧 1 automation rule │ João  │ [Call]│   │
│  │               │       │       │ 📊 Stagnant usage    │       │[Email]│   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│  [View All At-Risk] [Bulk Outreach] [Assign Tasks]                           │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  🟢 HEALTHY (1.200) - Expansion Opportunities                               │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Customer      │ Health│ Change│ Growth Signals        │ CSM   │Action│   │
│  ├───────────────┼───────┼───────┼──────────────────────┼───────┼──────│   │
│  │ Clínica Verde │  94   │  +2   │ 📈 Vol +40%          │ Maria │[Upgrd]│   │
│  │               │       │       │ 🆕 Asked about API   │       │[Case] │   │
│  ├───────────────┼───────┼───────┼──────────────────────┼───────┼──────│   │
│  │ Imob. Prime   │  91   │  +5   │ 👥 Team +2 users     │ João  │[Upgrd]│   │
│  │               │       │       │ ⚡ Hit plan limits   │       │[Refer]│   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│  [View All Healthy] [Bulk Campaign] [Identify Advocates]                     │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  📈 HEALTH SCORE TRENDS                                                    │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │                                                                       │   │
│  │  100│                                  ● (Target: 80 avg)            │   │
│  │   80│                             ●    ●    ●                        │   │
│  │   60│                        ●   ● ●   ● ●  ●  ●     ●                │   │
│  │   40│                   ●  ● ●                                 ●     │   │
│  │   20│                ●                                            ●   │   │
│  │    0├─────────────────────────────────────────────────────────      │   │
│  │      W1  W2  W3  W4  W5  W6  W7  W8  W9  W10 W11 W12              │   │
│  │                                                                       │   │
│  │  Current: 73  │  Target: 80  │  Gap: -7  │  Trend: ↗️ Improving      │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  🎯 HEALTH SCORE DISTRIBUTION BY SEGMENT                                    │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Segment      │ 🟢Healthy│ 🟡At-Risk│ 🔴Critical│ Avg Score│ Trend│   │
│  ├──────────────┼─────────┼─────────┼──────────┼──────────┼──────│   │
│  │ Clínicas     │  420    │   18    │    5      │   78     │ ↗️   │   │
│  │ Imobiliárias │  350    │   22    │    4      │   75     │ →    │   │
│  │ Academias    │  280    │   12    │    2      │   71     │ ↘️   │   │
│  │ Óticas       │  150    │    6    │    1      │   69     │ ↗️   │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ⚠️ RISK FACTOR SUMMARY (Top 10)                                            │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Risk Factor                    │ Count │ % of Customers│ Severity│   │
│  ├────────────────────────────────┼───────┼────────────────┼─────────│   │
│  │ Low login frequency (≤2/mo)    │  95   │     5%        │  🟡     │   │
│  │ Payment 7+ days late           │  18   │     1%        │  🔴     │   │
│  │ Volume declined >30%           │  45   │     2%        │  🟡     │   │
│  │ Zero automation rules          │  120  │     6%        │  🟡     │   │
│  │ Negative support tickets (2+)  │  22   │     1%        │  🔴     │   │
│  │ Zero logins (30 days)          │  15   │     1%        │  🔴     │   │
│  │ Single feature adoption        │  180  │     10%       │  🟡     │   │
│  │ Response rate <20%             │  85   │     5%        │  🟡     │   │
│  │ Payment method: Boleto         │  200  │     11%       │  🟡     │   │
│  │ Team size shrinking            │  12   │     1%        │  🔴     │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 3.2 Customer Detail View (Drill-Down)

```
┌─────────────────────────────────────────────────────────────────────────────┐
│  Clínica São Lucas - Health Score Detail                                    │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  Overall Health: 32/100 🔴 CRITICAL     (Last 30 days: 47 → 32)             │
│  Customer Since: 2025-11-15 (162 days)  │  Plan: Growth (R$ 197/mo)        │
│  CSM: Maria Santos                       │  Last Contact: 45 days ago        │
│                                                                             │
│  📊 SCORE BREAKDOWN                                                         │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Dimension       │ Score│ Weight│ Contribution│ Status    │ Change│   │
│  ├─────────────────┼──────┼────────┼──────────────┼───────────┼───────│   │
│  │ Usage           │ 18/100│  30%   │    5.4       │ 🔴 Poor   │  -12  │   │
│  │ Engagement      │ 25/100│  20%   │    5.0       │ 🔴 Poor   │   -8  │   │
│  │ Payment         │  0/100│  15%   │    0.0       │ 🔴 Critical│ -20  │   │
│  │ Support         │ 45/100│  15%   │    6.8       │ 🟡 Fair   │   -5  │   │
│  │ Adoption        │ 30/100│  10%   │    3.0       │ 🔴 Poor   │   -7  │   │
│  │ Growth          │ 10/100│  10%   │    1.0       │ 🔴 Poor   │   -3  │   │
│  ├─────────────────┼──────┼────────┼──────────────┼───────────┼───────│   │
│  │ TOTAL           │ 32/100│  100%  │   21.2       │ 🔴 Critical│  -15  │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
│  ⚠️ RISK FACTORS (5)                                                         │
│  • 💳 Payment is 12 days late (R$ 197 outstanding) - Severity: 🔴 Critical │
│  • 📉 Message volume down 80% in last 30 days (500 → 100) - Severity: 🔴   │
│  • 🚫 Zero logins in last 30 days - Severity: 🔴 Critical                  │
│  • 🔧 Only 1 of 5 automation rules active - Severity: 🟡 Warning           │
│  • 😠 2 negative support tickets in last 90 days - Severity: 🟡 Warning    │
│                                                                             │
│  📈 30-DAY HEALTH TREND                                                      │
│  100│                                                                       │
│  80│  ●●●●                                                                  │
│  60│ ●    ●●                                                                │
│  40│●        ●●●●●●●                                                        │
│  20│                ●●●●●●●●●●●●●                                          │
│   0├───────────────────────────────────────────────                        │
│    Mar 28  Apr 04  Apr 11  Apr 18  Apr 25                                   │
│                                                                             │
│  📊 DIMENSION TRENDS                                                         │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Dimension       │ 30d Ago│  Today│ Change│ Trend   │ Status         │   │
│  ├─────────────────┼────────┼───────┼───────┼─────────┼───────────────│   │
│  │ Usage           │   30   │  18   │  -12   │ ↘️ Rapid ↓│ 🔴 Declining │   │
│  │ Engagement      │   33   │  25   │   -8   │ ↘️ Declining│ 🔴 Declining │   │
│  │ Payment         │   20   │   0   │  -20   │ ⚠️ Failed │ 🔴 Critical   │   │
│  │ Support         │   50   │  45   │   -5   │ → Stable │ 🟡 Stable     │   │
│  │ Adoption        │   37   │  30   │   -7   │ ↘️ Declining│ 🔴 Declining │   │
│  │ Growth          │   13   │  10   │   -3   │ → Stable │ 🔴 Low        │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
│  🎯 RECOMMENDED ACTIONS                                                     │
│  Priority 1 (Immediate - Within 4 hours):                                   │
│  • [ ] Call customer about payment (use script #PAYMENT-RECOVERY)           │
│  • [ ] Schedule account review meeting (within 48 hours)                    │
│  • [ ] Offer payment plan if needed (3-month max)                          │
│                                                                             │
│  Priority 2 (This Week):                                                   │
│  • [ ] Conduct feature gap analysis (why only 1 automation rule?)          │
│  • [ ] Identify pain points from negative tickets                          │
│  • [ ] Create re-engagement campaign (3 WhatsApp messages)                  │
│                                                                             │
│  Priority 3 (Next Week):                                                   │
│  • [ ] Assign dedicated CSM for 30-day recovery                            │
│  • [ ] Set weekly check-in cadence (every Monday 10am)                     │
│  • [ ] Review automation rules and offer training session                  │
│                                                                             │
│  📞 CONTACT HISTORY                                                         │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Date       │ Type     │ Purpose              │ Outcome  │ Owner   │   │
│  ├────────────┼──────────┼──────────────────────┼──────────┼─────────│   │
│  │ 2026-04-10 │ Call     │ Automation setup     │ Positive │ Maria   │   │
│  │ 2026-03-15 │ Email    │ Monthly check-in     │ No resp  │ Maria   │   │
│  │ 2026-02-28 │ Call     │ Onboarding complete  │ Positive │ João    │   │
│  │ 2026-02-10 │ WhatsApp │ Welcome message      │ Opened   │ System  │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
│  💼 ACCOUNT DETAILS                                                         │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Field                │ Value                          │ Source       │   │
│  ├──────────────────────┼───────────────────────────────┼──────────────│   │
│  │ Company              │ Clínica São Lucas            │ CRM          │   │
│  │ Industry             │ Clínicas Médicas             │ CRM          │   │
│  │ Plan                 │ Growth (R$ 197/mo)           │ Billing      │   │
│  │ Team Size            │ 3 users                      │ Product      │   │
│  │ Location             │ São Paulo, SP                │ CRM          │   │
│  │ Customer Since       │ 2025-11-15 (162 days)        │ CRM          │   │
│  │ Lifetime Value       │ R$ 591                       │ Analytics    │   │
│  │ Messages Sent (30d)  │ 100 (baseline: 2.000)        │ Product      │   │
│  │ Automation Rules     │ 1 of 5 active                │ Product      │   │
│  │ Payment Method       │ Credit Card                  │ Billing      │   │
│  │ Payment Status       │ 12 days late                 │ Billing      │   │
│  │ Last Login           │ 2026-03-27 (30 days ago)     │ Product      │   │
│  │ NPS Score            │ 7 (Mar 2026)                 │ VoC          │   │
│  │ Support Tickets (90d)│ 3 (2 negative)               │ Support      │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
│  [Start Call] [Send Email] [Create Task] [Escalate] [Export Report]         │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 3.3 Health Score Alert System

| Alert Level | Trigger | Notifications | Response SLA | Escalation |
|-------------|---------|---------------|--------------|------------|
| 🔴 **Critical** | Health <50 OR any dimension <20 OR payment >7d late | Email + Slack + SMS to CSM + CS Lead | 4 hours | Escalate to CS Lead at 4h, CEO at 24h |
| 🟡 **Warning** | Health drops 10+ pts in 7d OR health 50-79 for 14d | Email + Slack to CSM | 24 hours | Escalate to CS Lead at 48h |
| 🟡 **At-Risk** | Health 50-79 for 30+ days | Email to CSM | 7 days | Escalate to CS Lead at 14d |
| 🟢 **Opportunity** | Health >90 AND growth signal present | Slack to CSM | 7 days | No escalation |
| ⚫ **New Customer** | Customer <7 days old | No alerts | Monitor | N/A |

**Email Alert Template**:
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
Response SLA: Within 4 hours

View in Dashboard: [link]
```

---

## Part 4: Operations Dashboard (Team Performance)

### 4.1 Dashboard Layout

```
┌─────────────────────────────────────────────────────────────────────────────┐
│           CONECTAPAY - CUSTOMER SUCCESS OPERATIONS DASHBOARD                 │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  👥 TEAM SNAPSHOT                    📋 TODAY'S PRIORITIES                   │
│  ┌────────────────────────────────┐  • 12 Critical customers to contact     │
│  │ Active CSMs: 7 of 7            │  • 58 At-Risk customers to outreach     │
│  │ Total Customers: 1.847         │  • 3 customers at payment recovery      │
│  │ Team Capacity: 85%             │  • 15 expansion opportunities          │
│  └────────────────────────────────┘                                        │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  📊 CSM PERFORMANCE                                                          │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ CSM      │ Customers│ Health│ At-Risk│ Critical│ Coverage│ Productivity│   │
│  ├──────────┼──────────┼───────┼────────┼─────────┼─────────┼─────────────│   │
│  │ Maria S. │   185    │  76   │   12   │    3    │  100%   │    112%     │   │
│  │ João P.  │   210    │  74   │   15   │    4    │  100%   │    108%     │   │
│  │ Ana L.   │   175    │  78   │   10   │    2    │  100%   │    125%     │   │
│  │ Carlos M.│   190    │  72   │   11   │    2    │  100%   │    118%     │   │
│  │ Patrícia │   180    │  75   │   13   │    1    │  100%   │    121%     │   │
│  │ Roberto  │   185    │  71   │   12   │    0    │  100%   │    105%     │   │
│  │ Fernanda │   190    │  77   │   10   │    0    │  100%   │    115%     │   │
│  ├──────────┼──────────┼───────┼────────┼─────────┼─────────┼─────────────│   │
│  │ TOTAL    │  1.315   │  75   │   83   │   12    │  100%   │    115%     │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ⚡ OPERATIONAL METRICS (Last 7 Days)                                        │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Metric                        │ Value    │ Target  │ Status  │ Trend│   │
│  ├───────────────────────────────┼──────────┼─────────┼─────────┼──────│   │
│  │ Customer Touchpoints          │  1.247   │  1.000+ │  ✅     │ ↗️   │   │
│  │ At-Risk Coverage Rate         │   100%   │  100%   │  ✅     │ →    │   │
│  │ Critical Response Time        │   2.3h   │  ≤4h    │  ✅     │ ↘️   │   │
│  │ Playbook Execution Rate       │    92%   │  ≥90%   │  ✅     │ ↗️   │   │
│  │ Customer Response Rate        │    68%   │  ≥60%   │  ✅     │ ↗️   │   │
│  │ Expansion Opportunities Found │    45    │   30+   │  ✅     │ ↗️   │   │
│  │ Churn Prevented               │     8    │   5+    │  ✅     │ ↗️   │   │
│  │ Case Studies Identified       │     6    │   3+    │  ✅     │ →    │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  📋 TASK QUEUE                                                              │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Priority │ Task Type    │ Count│ Assigned│ Due        │ Status     │   │
│  ├──────────┼──────────────┼──────┼─────────┼────────────┼────────────│   │
│  │ P1       │ Critical     │  12  │ CSMs    │ Today      │ 8 Done, 4  │   │
│  │          │ Outreach     │      │         │            │ Pending    │   │
│  ├──────────┼──────────────┼──────┼─────────┼────────────┼────────────│   │
│  │ P2       │ At-Risk      │  58  │ CSMs    │ This Week  │ 35 Done,   │   │
│  │          │ Outreach     │      │         │            │ 23 Pending │   │
│  ├──────────┼──────────────┼──────┼─────────┼────────────┼────────────│   │
│  │ P3       │ Expansion    │  45  │ CSMs    │ This Week  │ 12 Done,   │   │
│  │          │ Outreach     │      │         │            │ 33 Pending │   │
│  ├──────────┼──────────────┼──────┼─────────┼────────────┼────────────│   │
│  │ P4       │ Onboarding   │  15  │ Onboard │ Next Week  │ 0 Done,    │   │
│  │          │ Sessions     │      │ Team    │            │ 15 Pending │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  📈 ACTIVITY TRENDS (Last 30 Days)                                          │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │                                                                       │   │
│  │  1500│                         ● (Target: 1.000/day)                  │   │
│  │  1250│                    ●    ●    ●                                │   │
│  │  1000│               ●    ●  ● ●  ●  ●     ●                         │   │
│  │   750│          ●  ● ●                                 ●             │   │
│  │   500│     ●  ●                                            ●          │   │
│  │   250│ ●                                                          ●   │   │
│  │    0├──────────────────────────────────────────────────────────     │   │
│  │      W1  W2  W3  W4                                               │   │
│  │                                                                       │   │
│  │  Current: 1.247/day  │  Target: 1.000/day  │  Status: ✅ Above Target │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  🎯 WEEKLY GOALS PROGRESS                                                   │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Goal                     │ Target│ Actual│ Progress│ Status  │       │   │
│  ├──────────────────────────┼───────┼───────┼─────────┼─────────┤       │   │
│  │ Critical Outreach        │  12   │  12   │  100%   │  ✅     │       │   │
│  │ At-Risk Outreach         │  58   │  35   │   60%   │  🔄     │       │   │
│  │ Expansion Conversations  │  20   │   8   │   40%   │  🔄     │       │   │
│  │ Playbooks Executed       │  50   │  46   │   92%   │  ✅     │       │   │
│  │ Case Studies Identified  │   5   │   6   │  120%   │  ✅     │       │   │
│  │ Churn Prevented          │   5   │   8   │  160%   │  ✅     │       │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  📞 CALL ACTIVITY SUMMARY                                                    │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Call Type          │ Total│ Avg Duration│ Outcome Distribution      │   │
│  ├────────────────────┼──────┼─────────────┼───────────────────────────│   │
│  │ Critical Recovery  │  15  │    22 min   │ 8 Saved, 4 At-Risk, 3 Lost│   │
│  │ At-Risk Check-in   │  45  │    15 min   │ 35 Improved, 10 Stable     │   │
│  │ Expansion          │  12  │    18 min   │ 8 Upgrades, 4 Interested   │   │
│  │ Onboarding         │  18  │    25 min   │ 18 Activated              │   │
│  │ QBR/EBR            │   8  │    45 min   │ 8 Positive                │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 4.2 Operations KPI Definitions

| Metric | Definition | Target | Data Source |
|--------|------------|--------|-------------|
| **Team Capacity** | Customers assigned / Max capacity | ≤90% | Assignment System |
| **Avg Health Score (per CSM)** | Mean health score of assigned customers | 75+ | Health Score Engine |
| **At-Risk Coverage** | At-Risk customers contacted / Total At-Risk | 100% | Activity Log |
| **Critical Response Time** | Time from alert to first contact | ≤4 hours | Alert System |
| **Playbook Execution Rate** | Playbook steps completed / Total steps | ≥90% | Task System |
| **Customer Touchpoints** | Total customer interactions (calls, emails, WhatsApp) | 1.000+/week | Activity Log |
| **Customer Response Rate** | Customers who responded / Total outreach | ≥60% | Communication Log |
| **Churn Prevented** | At-Risk customers saved from churn | 5+/week | Churn Log |
| **Expansion Opportunities Found** | Customers identified for expansion | 20+/week | Opportunity Log |

---

## Part 5: VoC Dashboard (Customer Feedback)

### 5.1 Dashboard Layout

```
┌─────────────────────────────────────────────────────────────────────────────┐
│           CONECTAPAY - VOICE OF CUSTOMER DASHBOARD                          │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  📊 FEEDBACK SNAPSHOT               🚨 ALERTS (3)                            │
│  ┌────────────────────────────────┐  • NPS dropped 5 pts this week          │
│  │ Collection Rate: 62% (Target: 80%)│ 3 customers at churn risk (negative)│
│  │ NPS: 48 (Target: 60)            │  10+ requests for same feature        │
│  │ Close-the-Loop: 73% (Target: 90%)│ [View All Alerts]                    │
│  └────────────────────────────────┘                                        │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ⭐ NPS (Net Promoter Score)                                                │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │                                                                       │   │
│  │  70│                                            ● (Target: 60)       │   │
│  │  60│                                  ●                             │   │
│  │  50│                            ●     ●     ●                       │   │
│  │  40│                      ●     ●  ●  ●  ●  ●     ● (Current: 48)  │   │
│  │  30│                ●  ●  ●                                           │   │
│  │  20│          ●  ●                                                    │   │
│  │  10│      ●  ●                                                        │   │
│  │   0├─────────────────────────────────────────────────────────        │   │
│  │      M1  M2  M3  M4  M5  M6                                         │   │
│  │                                                                       │   │
│  │  Current: 48  │  Target: 60  │  Gap: -12  │  Trend: ↗️ +3 vs last month│   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
│  NPS Breakdown:                                                             │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Promoters (9-10): 55% (1.016 customers)  ████████████████████         │   │
│  │ Passives (7-8): 30% (554 customers)      ████████████                 │   │
│  │ Detractors (0-6): 15% (277 customers)   █████                        │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  😊 SENTIMENT ANALYSIS                                                      │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Channel           │ Positive│ Neutral│ Negative│ Score  │ Trend  │   │
│  ├───────────────────┼─────────┼────────┼─────────┼────────┼────────│   │
│  │ In-App Surveys    │   68%   │  22%   │   10%   │  +0.58  │ ↗️     │   │
│  │ Email NPS         │   62%   │  25%   │   13%   │  +0.49  │ →      │   │
│  │ Support Tickets   │   55%   │  30%   │   15%   │  +0.40  │ ↘️     │   │
│  │ Social Media      │   45%   │  35%   │   20%   │  +0.25  │ ↗️     │   │
│  │ Reviews           │   72%   │  18%   │   10%   │  +0.62  │ →      │   │
│  │ Churn Interviews  │   35%   │  25%   │   40%   │  -0.05  │ →      │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  📋 TOP FEEDBACK THEMES (Last 30 Days)                                      │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Rank│ Theme                  │ Mentions│ % Total│ Priority│ Owner │   │
│  ├─────┼───────────────────────┼─────────┼────────┼─────────┼────────│   │
│  │  1  │ WhatsApp setup        │    85   │  22%   │    P1   │ Product│   │
│  │     │ friction              │         │        │         │        │   │
│  ├─────┼───────────────────────┼─────────┼────────┼─────────┼────────│   │
│  │  2  │ Need more             │    62   │  16%   │    P1   │ Product│   │
│  │     │ automation templates  │         │        │         │        │   │
│  ├─────┼───────────────────────┼─────────┼────────┼─────────┼────────│   │
│  │  3  │ Mobile app            │    48   │  12%   │    P2   │ Product│   │
│  │     │ performance           │         │        │         │        │   │
│  ├─────┼───────────────────────┼─────────┼────────┼─────────┼────────│   │
│  │  4  │ Payment               │    35   │   9%   │    P1   │ CS Lead│   │
│  │     │ method limitations    │         │        │         │        │   │
│  ├─────┼───────────────────────┼─────────┼────────┼─────────┼────────│   │
│  │  5  │ Reporting             │    28   │   7%   │    P2   │ Product│   │
│  │     │ insufficient          │         │        │         │        │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  🔥 TOP FEATURE REQUESTS                                                    │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Rank│ Feature               │ Requests│ Would Buy│ Revenue  │ Status│   │
│  ├─────┼──────────────────────┼─────────┼───────────┼──────────┼────────│   │
│  │  1  │ Mobile app            │   125   │   85      │ R$ 17K/mo│ Backlog│   │
│  ├─────┼──────────────────────┼─────────┼───────────┼──────────┼────────│   │
│  │  2  │ Advanced analytics    │    98   │   62      │ R$ 12K/mo│ In Dev│   │
│  ├─────┼──────────────────────┼─────────┼───────────┼──────────┼────────│   │
│  │  3  │ Multi-language        │    75   │   45      │  R$ 9K/mo│ Backlog│   │
│  ├─────┼──────────────────────┼─────────┼───────────┼──────────┼────────│   │
│  │  4  │ API webhooks          │    58   │   35      │  R$ 7K/mo│ Planned│   │
│  ├─────┼──────────────────────┼─────────┼───────────┼──────────┼────────│   │
│  │  5  │ WhatsApp templates    │    52   │   48      │  R$ 9K/mo│ In Dev│   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ⚠️ TOP COMPLAINTS (Churn Risk)                                             │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Rank│ Issue                 │ Mentions│ Sentiment│ Churn Risk│ Owner│   │
│  ├─────┼──────────────────────┼─────────┼───────────┼───────────┼──────│   │
│  │  1  │ WhatsApp setup        │    85   │ Negative  │   High    │ Prod │   │
│  │     │ too complex          │         │           │           │      │   │
│  ├─────┼──────────────────────┼─────────┼───────────┼───────────┼──────│   │
│  │  2  │ Value not achieved    │    42   │ Negative  │   High    │ CS   │   │
│  │     │ in first 30 days      │         │           │           │      │   │
│  ├─────┼──────────────────────┼─────────┼───────────┼───────────┼──────│   │
│  │  3  │ Payment failures      │    28   │ Negative  │  Medium   │ CS   │   │
│  │     │ with Boleto           │         │           │           │      │   │
│  ├─────┼──────────────────────┼─────────┼───────────┼───────────┼──────│   │
│  │  4  │ Slow support          │    22   │ Negative  │  Medium   │ Supp │   │
│  │     │ response time         │         │           │           │      │   │
│  ├─────┼──────────────────────┼─────────┼───────────┼───────────┼──────│   │
│  │  5  │ Limited integrations  │    18   │ Mixed     │   Low     │ Prod │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ✅ CLOSE-THE-LOOP STATUS                                                    │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Status           │ Count│ % of Total│ Avg Days Open │ Trend         │   │
│  ├──────────────────┼──────┼───────────┼───────────────┼──────────────│   │
│  │ ✅ Completed     │  245 │    61%    │      8.2      │ ↗️ Improving  │   │
│  │    & Notified   │      │          │               │              │   │
│  ├──────────────────┼──────┼───────────┼───────────────┼──────────────│   │
│  │ 🚧 In Progress   │   82 │    20%    │     14.5      │ → Stable      │   │
│  ├──────────────────┼──────┼───────────┼───────────────┼──────────────│   │
│  │ 📋 Backlogged    │   58 │    15%    │     28.3      │ ↘️ Worsening  │   │
│  ├──────────────────┼──────┼───────────┼───────────────┼──────────────│   │
│  │ ❌ Declined       │   15 │     4%    │      5.1      │ → Stable      │   │
│  ├──────────────────┼──────┼───────────┼───────────────┼──────────────│   │
│  │ **TOTAL**        │  400 │   100%    │     12.4      │ ↗️ Improving  │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
│  Close-the-Loop Rate: 73% (292 completed / 400 total)  Target: 90%  Gap: -17%│
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  📊 FEEDBACK COLLECTION BY CHANNEL                                           │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Channel           │ Sent  │ Responses│ Rate  │ Target│ Gap    │ Trend│   │
│  ├───────────────────┼───────┼──────────┼───────┼───────┼────────┼──────│   │
│  │ In-App Surveys    │ 1.200 │    726   │  61%  │  40%  │  +21%  │ ↗️   │   │
│  │ Email NPS         │   800 │    185   │  23%  │  25%  │  -2%   │ →    │   │
│  │ Support Tickets   │   320 │    320   │ 100%  │ 100%  │   0%   │ →    │   │
│  │ Sales Calls       │   150 │    142   │  95%  │ 100%  │  -5%   │ ↘️   │   │
│  │ Churn Interviews  │    25 │     20   │  80%  │  80%  │   0%   │ →    │   │
│  │ Social Media      │   N/A │     45   │  N/A  │ <4h   │  ✅    │ →    │   │
│  │ Reviews           │   N/A │     12   │  N/A  │ <24h  │  ✅    │ →    │   │
│  │ **OVERALL**       │ 2.495 │  1.450   │  58%  │  60%  │  -2%   │ ↗️   │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 5.2 VoC KPI Definitions

| Metric | Definition | Target | Data Source |
|--------|------------|--------|-------------|
| **NPS** | (% Promoters) - (% Detractors) | 60+ | VoC System |
| **Collection Rate** | Feedback responses / Feedback requests | 80%+ | VoC System |
| **Close-the-Loop Rate** | Feedback items closed / Total feedback items | 90%+ | VoC System |
| **Sentiment Score** | (Positive - Negative) / Total | +0.50+ | NLP Analysis |
| **Response Rate** | Survey responses / Survey sent | 25%+ | VoC System |
| **Analysis Response Time** | Days from feedback to analysis | ≤3 days | VoC System |
| **Feedback-to-Feature Rate** | Features shipped from feedback / Total features | 15%+ | Product Roadmap |

---

## Part 6: Predictive Analytics Dashboard

### 6.1 Dashboard Layout

```
┌─────────────────────────────────────────────────────────────────────────────┐
│           CONECTAPAY - PREDICTIVE ANALYTICS DASHBOARD                        │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  🔮 FORECAST SNAPSHOT                                                        │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Churn Risk (Next 30 Days): 8 customers (est. R$ 1.576 MRR at risk)  │   │
│  │ Expansion Opportunity (Next 30 Days): 18 customers (est. R$ 3.546) │   │
│  │ Health Score Trend (Next 30 Days): 73 → 76 (+3 pts)                │   │
│  │ NPS Forecast (Next Month): 48 → 52 (+4 pts)                        │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ⚠️ CHURN PREDICTION (High Risk - Next 30 Days)                             │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Customer      │ Risk  │ Confidence│ Key Factors            │ Action│   │
│  ├───────────────┼───────┼───────────┼───────────────────────┼───────│   │
│  │ Clínica São   │  92%  │    High   │ Payment 20d late      │ Call  │   │
│  │ Lucas         │       │           │ Volume -90%           │ Today │   │
│  │               │       │           │ Health 28 (Critical)  │       │   │
│  ├───────────────┼───────┼───────────┼───────────────────────┼───────│   │
│  │ Imob. Centro  │  87%  │    High   │ 2 failed payments    │ Call  │   │
│  │               │       │           │ 3 negative tickets    │ Today │   │
│  │               │       │           │ Zero logins (45d)     │       │   │
│  ├───────────────┼───────┼───────────┼───────────────────────┼───────│   │
│  │ Academia Fit  │  78%  │   Medium  │ Health 35            │ Email │   │
│  │               │       │           │ Declining 30d trend   │ Week  │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  🚀 EXPANSION PREDICTION (High Opportunity - Next 30 Days)                   │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Customer      │ Prob. │ Confidence│ Signals                │ Action│   │
│  ├───────────────┼───────┼───────────┼───────────────────────┼───────│   │
│  │ Clínica Verde │  85%  │    High   │ Health 94            │ Call  │   │
│  │               │       │           │ Volume +40%           │ Week  │   │
│  │               │       │           │ Asked about API       │       │   │
│  ├───────────────┼───────┼───────────┼───────────────────────┼───────│   │
│  │ Imob. Prime   │  78%  │    High   │ Health 91            │ Email │   │
│  │               │       │           │ Team +2 users         │ Today  │   │
│  │               │       │           │ Hit plan limits       │       │   │
│  ├───────────────┼───────┼───────────┼───────────────────────┼───────│   │
│  │ Clínica Vida  │  72%  │   Medium  │ Health 88            │ Email │   │
│  │               │       │           │ NPS 10 (Promoter)     │ Week  │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  📈 FORECASTING MODELS                                                      │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Model                  │ Accuracy│ Last Updated│ Next Update   │   │
│  ├────────────────────────┼─────────┼─────────────┼───────────────│   │
│  │ Churn Prediction       │   84%   │  2026-04-26 │  2026-05-03   │   │
│  │ Expansion Prediction   │   78%   │  2026-04-26 │  2026-05-03   │   │
│  │ Health Score Forecast  │   76%   │  2026-04-26 │  2026-05-03   │   │
│  │ NPS Forecast           │   71%   │  2026-04-26 │  2026-05-03   │   │
│  │ CLV Prediction         │   82%   │  2026-04-26 │  2026-05-03   │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  🎯 MODEL PERFORMANCE (Last 90 Days)                                        │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Model                  │ Precision│ Recall│ F1-Score│ Trend      │   │
│  ├────────────────────────┼──────────┼────────┼─────────┼────────────│   │
│  │ Churn Prediction       │   82%    │  78%   │   80%   │ ↗️ +3%     │   │
│  │ Expansion Prediction   │   75%    │  72%   │   73%   │ → Stable   │   │
│  │ Health Score Forecast  │   79%    │  76%   │   77%   │ ↗️ +2%     │   │
│  │ NPS Forecast           │   68%    │  71%   │   69%   │ ↘️ -1%     │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  📊 SEGMENT FORECASTS (Next 90 Days)                                        │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Segment    │ Churn │ Expansion│ Health Trend│ NPS Trend│ CLV Trend│   │
│  ├────────────┼───────┼──────────┼─────────────┼──────────┼──────────│   │
│  │ Clínicas   │  4.2% │   12%    │ ↗️ Improving│ ↗️ +5    │ ↗️ +8%   │   │
│  │ Imobiliárias│  5.1% │   10%    │ → Stable    │ → Stable │ → Stable │   │
│  │ Academias  │  6.8% │    8%    │ ↘️ Declining│ ↘️ -3    │ ↘️ -5%   │   │
│  │ Óticas     │  4.5% │    6%    │ ↗️ Improving│ ↗️ +2    │ ↗️ +3%   │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 6.2 Prediction Model Features

**Churn Prediction Model**:
- Health score <50
- Payment >7 days late
- Volume declined >50%
- Zero logins (30 days)
- Negative support tickets (2+)
- Low feature adoption (<20%)
- Competitor mentions

**Expansion Prediction Model**:
- Health score >90
- Volume increased >30%
- Team growth
- Hit plan limits
- NPS 9-10 (Promoter)
- Feature inquiries
- Upgrade requests

---

## Part 7: Dashboard Implementation Roadmap

### 7.1 Phase 1: Foundation (Weeks 1-4)

**Week 1-2: Data Infrastructure**
- [ ] Set up data warehouse (PostgreSQL/BigQuery)
- [ ] Build ETL pipelines from Product DB, Payment Gateway, Support System
- [ ] Create health score calculation engine
- [ ] Set up basic data tables (customers, scores, activities)

**Week 3-4: Core Dashboards**
- [ ] Build Executive Dashboard (MVP: 5 core KPIs)
- [ ] Build Health Score Dashboard (list view + detail view)
- [ ] Set up alert system (email + Slack)
- [ ] Create basic user authentication

**Deliverables**:
- Working Executive Dashboard
- Working Health Score Dashboard
- Email + Slack alerts
- Daily data refresh

### 7.2 Phase 2: Enhancement (Weeks 5-8)

**Week 5-6: Operations & VoC**
- [ ] Build Operations Dashboard (CSM performance, task queue)
- [ ] Build VoC Dashboard (NPS, sentiment, themes)
- [ ] Integrate VoC data sources (surveys, support, social)
- [ ] Set up close-the-loop tracking

**Week 7-8: Advanced Features**
- [ ] Add health score trend charts
- [ ] Implement bulk outreach tools
- [ ] Create playbook execution tracking
- [ ] Build customer detail view (full 360°)

**Deliverables**:
- Working Operations Dashboard
- Working VoC Dashboard
- Bulk outreach capability
- Full customer detail view

### 7.3 Phase 3: Predictive Analytics (Weeks 9-12)

**Week 9-10: Model Development**
- [ ] Train churn prediction model (historical data)
- [ ] Train expansion prediction model
- [ ] Build health score forecast model
- [ ] Set up model performance monitoring

**Week 11-12: Dashboard & Integration**
- [ ] Build Predictive Analytics Dashboard
- [ ] Integrate predictions into Health Score Dashboard
- [ ] Set up automated model retraining (monthly)
- [ ] Create model performance reports

**Deliverables**:
- Working Predictive Analytics Dashboard
- Churn & expansion predictions
- Automated model retraining
- Model performance tracking

### 7.4 Phase 4: Optimization (Weeks 13-16)

**Week 13-14: Performance & UX**
- [ ] Optimize dashboard load times (<2 seconds)
- [ ] Improve mobile responsiveness
- [ ] Add filtering and sorting capabilities
- [ ] Create custom dashboard views per user role

**Week 15-16: Automation & Scaling**
- [ ] Implement automated playbook triggers
- [ ] Set up AI-powered risk factor analysis
- [ ] Create anomaly detection (unusual patterns)
- [ ] Scale infrastructure for 10K customers

**Deliverables**:
- Optimized dashboard performance
- Mobile-friendly dashboards
- Automated playbook triggers
- Infrastructure ready for scale

---

## Part 8: Technology Stack

### 8.1 Dashboard Tools

| Component | Tool | Cost | Purpose |
|-----------|------|------|---------|
| **Data Warehouse** | PostgreSQL / BigQuery | R$ 500-2.000/mo | Central data storage |
| **ETL Pipeline** | Airbyte / Fivetran | R$ 300-1.000/mo | Data integration |
| **Analytics Engine** | Python / R | R$ 0 (open source) | Data processing |
| **Dashboard UI** | Metabase / Tableau | R$ 500-2.000/mo | Visualization |
| **Alert System** | Slack + SendGrid | R$ 200/mo | Notifications |
| **CRM Integration** | HubSpot / Notion | R$ 400/mo | Customer data |
| **Monitoring** | Datadog / New Relic | R$ 300/mo | System health |

**Total Estimated Cost**: R$ 2.200-5.900/month

### 8.2 Data Schema (Core Tables)

```sql
-- Customers Table
CREATE TABLE customers (
  id SERIAL PRIMARY KEY,
  company_name VARCHAR(255),
  industry VARCHAR(100),
  plan VARCHAR(50),
  customer_since DATE,
  csm_id INTEGER,
  created_at TIMESTAMP,
  updated_at TIMESTAMP
);

-- Health Scores Table
CREATE TABLE health_scores (
  id SERIAL PRIMARY KEY,
  customer_id INTEGER REFERENCES customers(id),
  score INTEGER,
  usage_score INTEGER,
  engagement_score INTEGER,
  payment_score INTEGER,
  support_score INTEGER,
  adoption_score INTEGER,
  growth_score INTEGER,
  calculated_at DATE,
  created_at TIMESTAMP
);

-- Activities Table
CREATE TABLE activities (
  id SERIAL PRIMARY KEY,
  customer_id INTEGER REFERENCES customers(id),
  csm_id INTEGER,
  activity_type VARCHAR(50),
  channel VARCHAR(50),
  outcome VARCHAR(100),
  notes TEXT,
  created_at TIMESTAMP
);

-- VoC Data Table
CREATE TABLE voc_feedback (
  id SERIAL PRIMARY KEY,
  customer_id INTEGER REFERENCES customers(id),
  channel VARCHAR(50),
  feedback_type VARCHAR(50),
  score INTEGER,
  sentiment VARCHAR(20),
  theme VARCHAR(255),
  feedback_text TEXT,
  created_at TIMESTAMP
);

-- Alerts Table
CREATE TABLE alerts (
  id SERIAL PRIMARY KEY,
  customer_id INTEGER REFERENCES customers(id),
  alert_type VARCHAR(50),
  severity VARCHAR(20),
  message TEXT,
  status VARCHAR(20),
  acknowledged_at TIMESTAMP,
  resolved_at TIMESTAMP,
  created_at TIMESTAMP
);
```

---

## Part 9: Success Metrics & ROI

### 9.1 Dashboard Success Metrics

| Metric | Baseline | 3-Month Target | 6-Month Target |
|--------|----------|----------------|----------------|
| **Churn Rate** | 5.5% | 4.5% (-18%) | 3.5% (-36%) |
| **Avg Health Score** | 70 | 75 (+7%) | 80 (+14%) |
| **NPS** | 45 | 52 (+16%) | 60 (+33%) |
| **NRR** | 105% | 108% (+3%) | 110% (+5%) |
| **Expansion Rate** | 8% | 12% (+50%) | 15% (+88%) |
| **At-Risk Coverage** | 60% | 90% (+50%) | 100% (+67%) |
| **Response Time** | 24h | 8h (-67%) | 4h (-83%) |

### 9.2 ROI Calculation

**Investment** (12 months):
- Dashboard development: R$ 150.000 (one-time)
- Tech stack: R$ 3.500/month × 12 = R$ 42.000
- Data team: 1 FTE × R$ 8.000/month × 12 = R$ 96.000
- **Total Investment**: R$ 288.000

**Return** (12 months):
- Churn reduction: 5.5% → 3.5% = 20 customers saved × R$ 200/mo × 12 = R$ 48.000
- Expansion increase: 8% → 15% = 7% × R$ 365K/mo × 12 = R$ 306.600
- Efficiency gains: 2 CSMs not needed = R$ 192.000
- **Total Return**: R$ 546.600

**ROI**: (R$ 546.600 - R$ 288.000) / R$ 288.000 = **90%** in Year 1
**Payback Period**: 6.3 months

---

## Part 10: Governance & Maintenance

### 10.1 Dashboard Ownership

| Dashboard | Owner | Review Frequency | Stakeholders |
|-----------|-------|------------------|--------------|
| Executive | CMO / Head of CS | Monthly | CEO, CMO, Head of CS |
| Health Score | CS Lead | Weekly | CSMs, CS Lead, CMO |
| Operations | CS Ops Lead | Weekly | CSMs, CS Ops, CS Lead |
| VoC | VoC Lead | Weekly | VoC team, Product, CMO |
| Predictive | Data Lead | Monthly | Data team, CS Lead, CMO |

### 10.2 Quarterly Review Process

**Every Quarter**:
1. Review KPI targets vs actual performance
2. Assess dashboard usability and adoption
3. Evaluate model accuracy and recalibrate if needed
4. Gather feedback from all stakeholders
5. Prioritize new features and improvements
6. Update ROI calculations and business case

### 10.3 Continuous Improvement

**Weekly**:
- Monitor dashboard performance and uptime
- Review alert accuracy and adjust thresholds
- Track user adoption and identify training needs

**Monthly**:
- Analyze prediction model accuracy
- Review and optimize slow queries
- Update documentation and runbooks

**Quarterly**:
- Major feature releases based on feedback
- Model retraining with latest data
- Architecture review for scale planning

---

## Appendix: Dashboard Quick Reference

### Executive Dashboard Quick Links
- [Live Dashboard](#) (requires authentication)
- [KPI Definitions](#part-2-executive-dashboard-strategic-kpis)
- [Alert Thresholds](#part-2-executive-dashboard-strategic-kpis)

### Health Score Dashboard Quick Links
- [Live Dashboard](#) (requires authentication)
- [Health Score Methodology](https://docs.conectapay.com.br/health-scoring)
- [Intervention Playbooks](https://docs.conectapay.com.br/cs-playbooks)

### Operations Dashboard Quick Links
- [Live Dashboard](#) (requires authentication)
- [CSM Roster](https://docs.conectapay.com.br/cs-team)
- [Task Management](https://tasks.conectapay.com.br)

### VoC Dashboard Quick Links
- [Live Dashboard](#) (requires authentication)
- [VoC Program](https://docs.conectapay.com.br/voc-program)
- [Close-the-Loop Process](https://docs.conectapay.com.br/close-loop)

---

## Document Control

**Version**: 1.0
**Created**: 2026-04-26
**Owner**: CMO Agent (55827422-a849-41d3-9286-0b5b8b002079)
**Review Date**: 2026-07-26 (Quarterly)

**Related Documents**:
- [Customer Health Scoring System](/conectapay/docs/customer-health-scoring-system.md) - CON-121
- [VoC Metrics Dashboard Template](/conectapay/docs/voc-metrics-dashboard-template.md) - CON-107
- [Customer Success Team Structure](/conectapay/docs/customer-success-team-structure-and-operating-model.md) - CON-171
- [Customer Journey Mapping](/conectapay/docs/customer-journey-mapping-and-experience-optimization.md) - CON-129

**Change Log**:
| Date | Version | Changes | Author |
|------|---------|---------|--------|
| 2026-04-26 | 1.0 | Initial document creation | CMO Agent |
