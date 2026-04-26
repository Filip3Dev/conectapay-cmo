# ConectaPay Customer Success Performance Tracking System

**Version**: 1.0
**Created**: 2026-04-26
**Status**: Ready for Implementation
**Issue**: [CON-184](/conectapay/issues/CON-184)

---

## Executive Summary

This document defines ConectaPay's comprehensive Customer Success Performance Tracking System—a data-driven framework that transforms metrics into actionable insights, continuous improvement, and predictable business outcomes. Unlike dashboards that show "what's happening," this system defines "what to track," "when to act," and "how to improve."

**Key Objectives**:
- Establish leading indicators that predict churn and expansion 30-90 days in advance
- Define lagging indicators that measure business outcomes and team performance
- Create standardized reporting cadences and formats for all stakeholders
- Implement performance improvement processes that close the loop between insight and action
- Enable data-driven decision-making across the entire customer success organization

**Complementary Documents**:
- **[Customer Success Metrics and Health Score Dashboard](/conectapay/docs/customer-success-metrics-and-health-score-dashboard.md)** ([CON-175](/conectapay/issues/CON-175)) - Visual dashboards and real-time monitoring
- **[Customer Success Playbook for At-Risk Accounts](/conectapay/docs/customer-success-at-risk-accounts-playbook.md)** - Intervention protocols
- **[Customer Success Playbook](/conectapay/docs/customer-success-playbook.md)** - Operating procedures

---

## Part 1: Metrics Framework Overview

### 1.1 The Metrics Hierarchy

```
┌─────────────────────────────────────────────────────────────────────────┐
│                 CUSTOMER SUCCESS METRICS FRAMEWORK                     │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                         │
│  ┌─────────────────────────────────────────────────────────────────┐   │
│  │              NORTH STAR METRIC (1)                               │   │
│  │        Net Revenue Retention (NRR) - 110% target                │   │
│  └─────────────────────────────────────────────────────────────────┘   │
│                              ↓                                         │
│  ┌─────────────────────────────────────────────────────────────────┐   │
│  │           OUTCOME METRICS (Lagging - 6)                         │   │
│  │    Churn Rate │ NRR │ GRR │ CLV │ Expansion │ NPS/CSAT          │   │
│  └─────────────────────────────────────────────────────────────────┘   │
│                              ↓                                         │
│  ┌─────────────────────────────────────────────────────────────────┐   │
│  │          OUTPUT METRICS (Lagging - 8)                           │   │
│  │  Time-to-Value │ Feature Adoption │ Support Tickets │ Cases     │   │
│  └─────────────────────────────────────────────────────────────────┘   │
│                              ↓                                         │
│  ┌─────────────────────────────────────────────────────────────────┐   │
│  │          INPUT METRICS (Leading - 12)                          │   │
│  │  Health Score │ Login Freq │ Msg Volume │ Payment Status        │   │
│  └─────────────────────────────────────────────────────────────────┘   │
│                              ↓                                         │
│  ┌─────────────────────────────────────────────────────────────────┐   │
│  │          OPERATIONAL METRICS (Team - 10)                       │   │
│  │  Touchpoints │ Response Time │ Coverage │ Playbook Execution    │   │
│  └─────────────────────────────────────────────────────────────────┘   │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

### 1.2 Leading vs. Lagging Indicators

| Type | Definition | Time Horizon | Purpose | Example |
|------|------------|--------------|---------|---------|
| **Leading** | Predictive indicators that signal future outcomes | 30-90 days ahead | Early intervention, prevention | Health score drops, login decline |
| **Lagging** | Outcome indicators that measure past performance | After the fact | Performance assessment, goal tracking | Churn rate, NRR, NPS |

**Golden Rule**: For every lagging metric, identify at least 3 leading metrics that predict it.

---

## Part 2: Leading Indicators (Predictive Metrics)

### 2.1 Adoption Leading Indicators

| Metric | Definition | Target | Frequency | Predicts |
|--------|------------|--------|-----------|----------|
| **Day 7 Activation Rate** | % of new customers who complete onboarding by Day 7 | ≥80% | Daily | 90-day retention |
| **Feature Adoption Velocity** | Avg days to adopt 3rd core feature | ≤21 days | Weekly | Expansion eligibility |
| **Daily Active Users (DAU)** | % of customers logging in daily | ≥40% | Daily | Long-term engagement |
| **Automation Rule Creation** | % of customers with 2+ automation rules | ≥60% | Weekly | 90-day retention |
| **First Value Time** | Hours from signup to first recovered sale | ≤48h | Daily | Churn risk |

**Early Warning Thresholds**:
- Day 7 Activation <60%: 40% churn risk in 90 days
- Feature Adoption Velocity >30 days: 50% churn risk
- DAU <20% for 14+ days: Enter at-risk watchlist

### 2.2 Engagement Leading Indicators

| Metric | Definition | Target | Frequency | Predicts |
|--------|------------|--------|-----------|----------|
| **Login Frequency Trend** | 7-day rolling avg of logins per customer | ≥4/week | Daily | 30-day churn risk |
| **Message Volume Trend** | 7-day rolling avg of automated messages | ≥100/week | Daily | Feature adoption |
| **Dashboard View Frequency** | Avg dashboard views per customer | ≥3/week | Weekly | Expansion readiness |
| **Support Ticket Sentiment** | NLP sentiment score of support tickets | ≥+0.4 | Daily | NPS, churn risk |
| **Response Rate to CSM** | % of CSM outreach that gets response | ≥70% | Weekly | Relationship health |

**Early Warning Thresholds**:
- Login Frequency ↓50% for 7 days: 35% churn risk
- Message Volume ↓40% for 14 days: 45% churn risk
- Support Ticket Sentiment <0 for 5+ tickets: 60% churn risk

### 2.3 Health Leading Indicators

| Metric | Definition | Target | Frequency | Predicts |
|--------|------------|--------|-----------|----------|
| **Health Score Trend** | 7-day change in health score | Stable or ↑ | Daily | 30-day churn risk |
| **Health Score Distribution** | % of customers in "Healthy" (80+) zone | ≥80% | Weekly | Portfolio health |
| **Risk Factor Accumulation** | Avg number of risk factors per customer | ≤1 | Weekly | Churn probability |
| **Payment Health** | % of customers with no payment issues | ≥95% | Daily | Revenue retention |
| **At-Risk Escalation Rate** | % of at-risk moving to critical | ≤10% | Weekly | Churn volume |

**Early Warning Thresholds**:
- Health Score ↓10 points in 7 days: Immediate outreach required
- Health Score Distribution <70% healthy: Portfolio review needed
- At-Risk Escalation Rate >20%: Systemic issue investigation

### 2.4 Expansion Leading Indicators

| Metric | Definition | Target | Frequency | Predicts |
|--------|------------|--------|-----------|----------|
| **Plan Limit Utilization** | % of customers at 80%+ of plan limits | ≥15% | Weekly | Expansion pipeline |
| **Team Size Growth** | % of customers adding users in 30 days | ≥5% | Monthly | Upsell opportunity |
| **Feature Inquiry Rate** | Support tickets asking about premium features | ≥10% | Monthly | Cross-sell pipeline |
| **NPS Promoter Rate** | % of customers with NPS 9-10 | ≥60% | Quarterly | Referral pipeline |
| **ROI Achievement Velocity** | Days to reach 3x ROI | ≤90 days | Monthly | Case study eligibility |

**Early Warning Thresholds**:
- Plan Limit Utilization >25%: Expansion campaign trigger
- NPS Promoter Rate <50%: Advocacy program review needed
- ROI Achievement Velocity >120 days: Value delivery review needed

---

## Part 3: Lagging Indicators (Outcome Metrics)

### 3.1 Outcome Metrics (Business Results)

| Metric | Definition | Target | Frequency | Owner |
|--------|------------|--------|-----------|-------|
| **Net Revenue Retention (NRR)** | (MRR + Expansion - Churn) / MRR | ≥110% | Monthly | Head of CS |
| **Gross Revenue Retention (GRR)** | MRR retained / MRR at start | ≥95% | Monthly | Head of CS |
| **Churn Rate** | Customers churned / Total customers | ≤5% | Monthly | Head of CS |
| **Customer Lifetime Value (CLV)** | Avg revenue per customer × Gross margin × Lifetime | ≥R$ 5K | Quarterly | CMO |
| **Expansion Revenue Rate** | Expansion MRR / Total MRR | ≥10% | Monthly | Head of CS |
| **Net Promoter Score (NPS)** | % Promoters - % Detractors | ≥60 | Quarterly | VoC Lead |

### 3.2 Output Metrics (Customer Results)

| Metric | Definition | Target | Frequency | Owner |
|--------|------------|--------|-----------|-------|
| **Time-to-First-Value** | Days from signup to first recovered sale | ≤2 days | Weekly | CS Ops |
| **Feature Adoption Rate** | % of customers using each core feature | ≥70% | Monthly | CS Ops |
| **Support Tickets per Customer** | Avg monthly tickets per customer | ≤2 | Monthly | Support Lead |
| **Customer Satisfaction (CSAT)** | Avg CSAT score (1-5) | ≥4.7 | Monthly | Support Lead |
| **Case Studies Produced** | Number of published case studies | ≥4/month | Marketing | CMO |
| **Referral Count** | New customers from referrals | ≥15% of growth | Monthly | CMO |

---

## Part 4: Reporting Framework

### 4.1 Reporting Cadences

```
┌─────────────────────────────────────────────────────────────────────────┐
│                    REPORTING CADENCE MATRIX                             │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                         │
│  DAILY         │  WEEKLY         │  MONTHLY    │  QUARTERLY            │
│  ─────────     │  ─────────      │  ─────────  │  ──────────           │
│  • Health      │  • Portfolio    │  • NRR      │  • Strategic Review    │
│    Score       │    Health       │  • Churn    │  • Benchmark Analysis  │
│    Alerts      │  • At-Risk      │  • Expansion│  • Goal Setting        │
│  • Critical    │    Coverage     │  • NPS      │  • Resource Planning   │
│    Accounts    │  • CSM          │  • CLV      │  • Compensation Review │
│  • Payment     │    Performance  │  • Case     │  • Forecast Updates    │
│    Issues      │  • Operational  │    Studies  │                       │
│                │    Metrics      │  • Team     │                       │
│                │                 │    Capacity │                       │
│                                                                         │
│  Audience:     │  Audience:      │  Audience:  │  Audience:            │
│  CSMs, CS Lead │  CS Lead, CMO   │  Exec Team  │  Board, Exec Team     │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

### 4.2 Daily Report Format

**Report Name**: CS Daily Pulse
**Distribution**: Email + Slack (8:00 AM)
**Audience**: CSMs, CS Lead, CMO
**Format**: 1-page summary

```markdown
# CS Daily Pulse - 2026-04-26

## 🔴 Critical Alerts (3)
- Clínica São Lucas: Health 32 → 28, Payment 20d late
- Imob. Centro: Health 41 → 35, Zero logins 45d
- Academia Fit: Health 28 → 22, 3 negative tickets

## 📊 Health Portfolio Snapshot
- Healthy: 1.200 (65%) │ At-Risk: 58 (3%) │ Critical: 12 (1%)
- Avg Health Score: 73 (Target: 80)
- Health Trend: ↗️ +2 vs last week

## ✅ Yesterday's Actions
- Critical outreach: 12/12 completed (100%)
- At-risk outreach: 35/58 completed (60%)
- Playbooks executed: 46/50 (92%)

## 📋 Today's Priorities
- 12 Critical customers: Call within 4h
- 23 At-risk customers: Outreach this week
- 8 Expansion conversations: Schedule calls

## 👥 Team Status
- All CSMs active
- Team capacity: 85% (615 customers / 720 max)
- No blockers reported

---
Generated at 08:00 | Data refresh: 07:55 | Next update: Tomorrow 08:00
```

### 4.3 Weekly Report Format

**Report Name**: CS Weekly Performance Report
**Distribution**: Email (Monday 9:00 AM)
**Audience**: CS Lead, CMO, CEO
**Format**: 3-page slide deck

**Slide 1: Executive Summary**
```
CS Weekly Performance - Week 17 (Apr 19-25, 2026)

┌─────────────────────────────────────────────────────────┐
│ TOP 3 WINS                                              │
├─────────────────────────────────────────────────────────┤
│ ✓ Churn reduced to 3.2% (target: ≤5%)                  │
│ ✓ 8 customers saved from critical (R$ 1.576 MRR)       │
│ ✓ 6 expansion deals closed (R$ 1.180 ARR)              │
└─────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────┐
│ TOP 3 RISKS                                             │
├─────────────────────────────────────────────────────────┤
│ ⚠ Academias segment health declining (71 → 68)         │
│ ⚠ Day 7 activation rate dropped to 72% (target: 80%)  │
│ ⚠ 3 customers at payment recovery (R$ 591 MRR at risk)│
└─────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────┐
│ KEY METRICS vs TARGET                                   │
├─────────────────────────────────────────────────────────┤
│ NRR: 108.3% (Target: 110%) │ Gap: -1.7% │ Status: 🟡   │
│ Churn: 3.2% (Target: ≤5%) │ Gap: -1.8% │ Status: ✅   │
│ Health: 73 (Target: 80) │ Gap: -7 │ Status: 🟡        │
│ Expansion: 8% (Target: 10%) │ Gap: -2% │ Status: 🟡   │
└─────────────────────────────────────────────────────────┘
```

**Slide 2: Customer Health Deep Dive**
```
Health Portfolio Movement

┌─────────────────────────────────────────────────────────┐
│ SEGMENT HEALTH TRENDS                                   │
├─────────────────────────────────────────────────────────┤
│ Clínicas:     78 → 79 (+1)  ↗️ Improving               │
│ Imobiliárias: 75 → 75 (0)   → Stable                   │
│ Academias:    71 → 68 (-3) ↘️ Declining (ACTION)       │
│ Óticas:       69 → 71 (+2)  ↗️ Improving               │
└─────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────┐
│ HEALTH MIGRATION (This Week)                            │
├─────────────────────────────────────────────────────────┤
│ Critical → At-Risk:   3 (25% recovery rate)            │
│ At-Risk → Healthy:    18 (31% recovery rate)           │
│ Healthy → At-Risk:    22 (1.8% degradation rate)       │
│ Healthy → Critical:   2 (0.2% degradation rate)        │
└─────────────────────────────────────────────────────────┘

TOP RISK FACTORS (By Count)
1. Low login frequency (≤2/mo): 95 customers
2. Zero automation rules: 120 customers
3. Payment 7+ days late: 18 customers
```

**Slide 3: Team Performance & Next Week**
```
CSM Performance (Week 17)

┌─────────────────────────────────────────────────────────┐
│ CSM      │Health│At-Risk│Critical│Coverage│Productivity│
│ Maria S. │  76  │  12   │   3    │  100%  │    112%    │
│ João P.  │  74  │  15   │   4    │  100%  │    108%    │
│ Ana L.   │  78  │  10   │   2    │  100%  │    125%    │
└─────────────────────────────────────────────────────────┘

NEXT WEEK'S PRIORITIES
• Academias segment health investigation
• Day 7 activation process review
• 3 payment recovery accounts
• 6 expansion deals in pipeline
• 2 case studies to produce

WEEKLY GOALS
• Critical outreach: 100% coverage
• At-risk outreach: 100% coverage
• Expansion conversations: 8 minimum
• Case studies identified: 3 minimum
```

### 4.4 Monthly Report Format

**Report Name**: CS Monthly Business Review (MBR)
**Distribution**: Email + Presentation (5th business day)
**Audience**: Exec Team, CEO, Board
**Format**: 10-slide presentation + 3-page written summary

**Slide Structure**:
1. Executive Summary (1 slide)
2. Revenue Metrics (NRR, GRR, Churn, Expansion) (1 slide)
3. Customer Health Portfolio (1 slide)
4. Customer Experience (NPS, CSAT, VoC) (1 slide)
5. Team Performance & Capacity (1 slide)
6. Operational Excellence (1 slide)
7. Segment Deep Dive (1 slide)
8. Predictive Analytics & Forecast (1 slide)
9. Strategic Initiatives Progress (1 slide)
10. Next Month's Plan (1 slide)

**Written Summary Sections**:
- Key Achievements
- Missed Targets & Root Causes
- Customer Wins & Case Studies
- At-Risk Accounts & Mitigation
- Team Highlights
- Strategic Recommendations

### 4.5 Quarterly Report Format

**Report Name**: CS Quarterly Business Review (QBR)
**Distribution**: Board Meeting Presentation
**Audience**: Board, Exec Team
**Format**: 20-slide presentation + full written report

**Key Sections**:
1. Q1 Executive Summary
2. Q1 Performance vs Goals (all metrics)
3. Customer Health Portfolio Analysis
4. Segment Performance Deep Dive
5. Competitive Benchmarking
6. Customer Success Team Performance
7. Financial Impact & ROI
8. Predictive Model Performance
9. Strategic Initiative Reviews
10. Q2 Goals & Initiatives
11. Resource Requirements
12. Risk Assessment & Mitigation

---

## Part 5: Performance Improvement Processes

### 5.1 The Performance Improvement Loop

```
┌─────────────────────────────────────────────────────────────────────────┐
│                  PERFORMANCE IMPROVEMENT LOOP                          │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                         │
│  1. MEASURE                                                           │
│  ├─ Collect metrics from all sources                                   │
│  ├─ Calculate leading and lagging indicators                           │
│  └─ Identify gaps vs targets                                           │
│                              ↓                                         │
│  2. ANALYZE                                                           │
│  ├─ Root cause analysis (5 Whys, Fishbone)                             │
│  ├─ Segment and cohort breakdowns                                      │
│  └─ Correlation analysis (leading → lagging)                           │
│                              ↓                                         │
│  3. PLAN                                                              │
│  ├─ Define improvement targets                                         │
│  ├─ Select intervention playbooks                                      │
│  └─ Assign owners and timelines                                        │
│                              ↓                                         │
│  4. EXECUTE                                                           │
│  ├─ Launch interventions                                               │
│  ├─ Monitor leading indicators daily                                   │
│  └─ Document outcomes and learnings                                    │
│                              ↓                                         │
│  5. EVALUATE                                                          │
│  ├─ Measure impact on lagging indicators                               │
│  ├─ Calculate ROI and cost-benefit                                     │
│  └─ Scale successful interventions or pivot                            │
│                              ↓                                         │
│                    Back to Step 1 (Continuous)                         │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

### 5.2 Metric-to-Action Mapping

| When Leading Metric... | Then Take This Action | Owner | Timeline |
|------------------------|----------------------|-------|----------|
| **Health Score drops 10+ points in 7 days** | Immediate outreach call + account review | CSM | 4 hours |
| **Day 7 Activation <60%** | Review onboarding process + implement improvements | CS Ops | 1 week |
| **Login Frequency ↓50% for 7 days** | Re-engagement campaign (3 WhatsApp messages) | CSM | 48 hours |
| **Payment 7+ days late** | Payment recovery outreach (call + email) | CSM | 24 hours |
| **Support Ticket Sentiment <0 for 5+ tickets** | Executive sponsorship + feature gap analysis | CS Lead | 1 week |
| **Plan Limit Utilization >25%** | Expansion outreach call | CSM | 1 week |
| **NPS drops 10+ points QoQ** | VoC deep dive + systemic issue investigation | VoC Lead | 2 weeks |
| **At-Risk Escalation Rate >20%** | Portfolio-wide health review + systemic fix | CS Lead | 1 week |

### 5.3 Performance Improvement Playbooks

#### **Playbook 1: Day 7 Activation Recovery**
**Trigger**: Day 7 Activation Rate <60%

**Steps**:
1. **Identify blocked customers** (Day 7+ not activated)
2. **Categorize by blocker type**:
   - Technical: WhatsApp integration failed
   - Resource: No time to complete setup
   - Value: Unclear about next steps
3. **Assign specialized outreach**:
   - Technical: Technical specialist call within 24h
   - Resource: CSM "done-for-you" setup offer
   - Value: ROI demo call with case studies
4. **Monitor leading indicators**:
   - Daily activation count
   - Integration completion rate
5. **Success criteria**: 80% activation by Day 14

#### **Playbook 2: Segment Health Decline Recovery**
**Trigger**: Segment health score ↓5+ points in 30 days

**Steps**:
1. **Segment deep dive analysis**:
   - Health score distribution
   - Top risk factors in segment
   - Common themes from support tickets
2. **Root cause investigation**:
   - Survey at-risk customers in segment
   - Analyze feature adoption patterns
   - Review competitive landscape
3. **Intervention design**:
   - Segment-specific communication
   - Feature training webinars
   - Value realization workshops
4. **Execute and monitor**:
   - Weekly health score tracking
   - Daily engagement metrics
5. **Success criteria**: Health score returns to baseline within 60 days

#### **Playbook 3: Churn Spike Response**
**Trigger**: Churn rate >8% in any week

**Steps**:
1. **Immediate triage (within 4 hours)**:
   - Identify all churned customers
   - Categorize by churn reason
   - Calculate revenue at risk
2. **Root cause analysis (within 24 hours)**:
   - Interview churned customers (willing)
   - Review health score trends pre-churn
   - Analyze support ticket history
3. **Systemic fix design (within 48 hours)**:
   - Define issue (product, process, pricing, competition)
   - Design intervention for remaining at-risk customers
   - Escalate to product/sales/leadership as needed
4. **Execute prevention campaign (within 1 week)**:
   - Outreach all similar-risk customers
   - Apply retention offers if appropriate
   - Monitor for additional churn
5. **Post-mortem (within 2 weeks)**:
   - Document root cause and resolution
   - Update playbooks and processes
   - Share learnings across organization

#### **Playbook 4: Expansion Pipeline Acceleration**
**Trigger**: Expansion pipeline below target (30% below goal)

**Steps**:
1. **Pipeline health check**:
   - Identify all customers at plan limits
   - Score expansion readiness (0-100)
   - Prioritize top 20% for outreach
2. **Readiness gap analysis**:
   - Why hasn't expansion happened yet?
   - Technical blockers? Budget? ROI not proven?
3. **Targeted interventions**:
   - Technical: Feature demo + implementation plan
   - Budget: ROI analysis + finance approval support
   - ROI: Case study sharing + value realization workshop
4. **Incentive offers (if appropriate)**:
   - Annual pre-pay discount
   - Limited-time promotion
   - Value-add services (training, migration)
5. **Monitor and iterate**:
   - Weekly pipeline review
   - Conversion funnel analysis
   - Offer effectiveness tracking

### 5.4 Root Cause Analysis Framework

#### **The 5 Whys Technique**

**Example**: Churn Rate Spike to 8.2%

| Why | Question | Answer | Next Step |
|-----|----------|--------|-----------|
| 1 | Why did churn increase? | 12 customers cancelled last week | → Why did they cancel? |
| 2 | Why did they cancel? | 8 cited "value not achieved" | → Why wasn't value achieved? |
| 3 | Why wasn't value achieved? | Zero automation rules created | → Why no rules created? |
| 4 | Why no rules created? | Setup too complex, abandoned at Day 5 | → Why is setup complex? |
| 5 | Why is setup complex? | No templates, requires technical knowledge | → Fix: Add templates + guided setup |

**Root Cause**: Lack of automation templates and guided setup
**Solution**: Launch template library + guided onboarding (Q3)

#### **Fishbone Diagram (Cause Categories)**

```
                    CHURN RATE SPIKE
                          │
        ┌─────────────────┼─────────────────┐
        │                 │                 │
    PEOPLE           PROCESS          PRODUCT   ENVIRONMENT
        │                 │                 │          │
    ┌───┴───┐         ┌───┴───┐         ┌───┴───┐  ┌───┴───┐
    │CSM    │         │Onboard│         │Bug    │  │Compet-│
    │Training│         │ing    │         │       │  │itor   │
    └───────┘         └───────┘         └───────┘  └───────┘
```

**Analysis Process**:
1. Brainstorm causes in each category
2. Vote on top 3 most likely causes
3. Validate with data (not assumptions)
4. Design interventions for top causes

---

## Part 6: Metrics Governance

### 6.1 Metrics Council

**Purpose**: Ensure metrics remain relevant, accurate, and actionable

**Membership**:
- Head of Customer Success (Chair)
- CMO
- VP Product
- Data Lead
- CS Operations Lead

**Meeting Cadence**: Monthly (1st Tuesday)

**Meeting Agenda**:
1. Review metric performance vs targets (15 min)
2. Assess metric relevance and accuracy (15 min)
3. Discuss emerging metrics to add/remove (20 min)
3. Review dashboard usability and feedback (10 min)
4. Approve metric changes and communicate (10 min)

**Decision Authority**:
- Add new metrics: Majority vote
- Remove metrics: Majority vote
- Change targets: Chair approval
- Dashboard changes: Data Lead approval

### 6.2 Metric Lifecycle Management

| Stage | Criteria | Actions | Decision Gate |
|-------|----------|---------|---------------|
| **Proposed** | New metric proposed by team member | Define metric, data source, target | Metrics Council review |
| **Pilot** | Approved by Metrics Council | Track for 30 days, assess reliability | Council decision: adopt/reject |
| **Active** | Adopted metric | Track, report, use in decisions | Quarterly relevance review |
| **Deprecated** | No longer relevant or reliable | Stop reporting, archive data | Council approval |

### 6.3 Data Quality Standards

**Accuracy**: Metric calculations must be 99%+ accurate
- Weekly data quality audits
- Discrepancy >1% triggers investigation
- Root cause analysis for all data errors

**Timeliness**: Data must be available within agreed SLAs
- Real-time metrics: <5 minutes latency
- Daily metrics: Available by 8:00 AM
- Weekly metrics: Available by Monday 9:00 AM
- Monthly metrics: Available by 5th business day

**Completeness**: No missing data points
- Zero tolerance for missing data in critical metrics
- Automated alerts for data quality issues
- Manual data entry audit trail

### 6.4 Metric Access & Security

| Access Level | Who | What They Can See | What They Can Edit |
|--------------|-----|-------------------|-------------------|
| **Executive** | CEO, CMO, Head of CS | All dashboards, raw data | Metric targets, report distribution |
| **Manager** | CS Lead, VoC Lead | Team dashboards, portfolio health | Team assignments, playbook triggers |
| **Individual Contributor** | CSMs | Assigned customers only | Customer notes, activities |
| **View-Only** | Board, External Advisors | Executive dashboard only | None (read-only) |
| **Restricted** | No access to customer PII | Aggregated data only | N/A |

---

## Part 7: Implementation Roadmap

### 7.1 Phase 1: Foundation (Weeks 1-4)

**Week 1-2: Metric Definition & Data Source Setup**
- [ ] Finalize leading/lagging indicator list
- [ ] Map all metrics to data sources
- [ ] Build ETL pipelines for metric calculation
- [ ] Create metric calculation engine

**Week 3-4: Reporting Infrastructure**
- [ ] Set up daily/weekly/monthly report templates
- [ ] Configure automated report distribution
- [ ] Build Slack/email integration for alerts
- [ ] Train team on new reporting system

**Deliverables**:
- Complete metrics catalog
- Working ETL pipelines
- Daily, weekly, monthly reports running
- Team trained on system

### 7.2 Phase 2: Process Integration (Weeks 5-8)

**Week 5-6: Performance Improvement Processes**
- [ ] Document metric-to-action mapping
- [ ] Create performance improvement playbooks
- [ ] Build root cause analysis templates
- [ ] Train CSMs on intervention processes

**Week 7-8: Governance & Optimization**
- [ ] Establish Metrics Council
- [ ] Set up data quality monitoring
- [ ] Create metric lifecycle process
- [ ] Implement access controls

**Deliverables**:
- 4 performance improvement playbooks live
- Metrics Council established
- Data quality SLAs met
- Full team trained

### 7.3 Phase 3: Advanced Analytics (Weeks 9-12)

**Week 9-10: Predictive Modeling**
- [ ] Train churn prediction model
- [ ] Train expansion prediction model
- [ ] Validate model accuracy (80%+ target)
- [ ] Set up model retraining pipeline

**Week 11-12: Reporting Enhancement**
- [ ] Add predictive metrics to reports
- [ ] Create custom report builder
- [ ] Build mobile-friendly report view
- [ ] Implement drill-down capabilities

**Deliverables**:
- Working churn/expansion predictions
- Enhanced reports with predictive insights
- Mobile-accessible reports
- Custom report builder

### 7.4 Phase 4: Continuous Improvement (Ongoing)

**Weekly**:
- Monitor data quality
- Review report usage and feedback
- Track metric performance vs targets

**Monthly**:
- Metrics Council meeting
- Report optimization based on feedback
- Performance improvement playbook updates

**Quarterly**:
- Strategic metric review (add/remove)
- Benchmark analysis vs competitors
- System scalability assessment
- ROI calculation and optimization

---

## Part 8: Success Metrics & ROI

### 8.1 System Success Metrics

| Metric | Baseline | 3-Month Target | 6-Month Target | 12-Month Target |
|--------|----------|----------------|----------------|-----------------|
| **Churn Rate** | 5.5% | 4.5% (-18%) | 3.5% (-36%) | 3.0% (-45%) |
| **NRR** | 105% | 108% (+3%) | 110% (+5%) | 115% (+10%) |
| **Avg Health Score** | 70 | 75 (+7%) | 80 (+14%) | 85 (+21%) |
| **NPS** | 45 | 52 (+16%) | 60 (+33%) | 65 (+44%) |
| **Expansion Rate** | 8% | 12% (+50%) | 15% (+88%) | 18% (+125%) |
| **At-Risk Recovery Rate** | 40% | 55% (+38%) | 65% (+63%) | 70% (+75%) |
| **Time-to-First-Value** | 4.2 days | 3.0 days (-29%) | 2.0 days (-52%) | 1.5 days (-64%) |
| **Day 7 Activation** | 65% | 75% (+15%) | 80% (+23%) | 85% (+31%) |

### 8.2 ROI Calculation

**Investment** (12 months):
- System development: R$ 75.000 (one-time)
- Tech stack (reporting tools, data infrastructure): R$ 2.000/month × 12 = R$ 24.000
- CS Ops time (maintenance): 20% FTE × R$ 6.000/month × 12 = R$ 14.400
- Training & change management: R$ 15.000 (one-time)
- **Total Investment**: R$ 128.400

**Return** (12 months):
- Churn reduction: 5.5% → 3.0% = 25 customers saved × R$ 200/mo × 12 = **R$ 60.000**
- Expansion increase: 8% → 18% = 10% × R$ 365K/mo × 12 = **R$ 438.000**
- Efficiency gains (1 CSM not needed): R$ 96.000
- At-risk recovery improvement: 40% → 70% = 15 customers saved × R$ 200/mo × 12 = **R$ 36.000**
- **Total Return**: R$ 630.000

**ROI**: (R$ 630.000 - R$ 128.400) / R$ 128.400 = **391%** in Year 1
**Payback Period**: 2.4 months

---

## Part 9: Quick Reference Guides

### 9.1 Leading Indicators Quick Reference

| What to Watch | Warning Threshold | Action | Timeline |
|---------------|-------------------|--------|----------|
| Health Score | ↓10 points in 7 days | Immediate outreach | 4 hours |
| Login Frequency | ↓50% for 7 days | Re-engagement campaign | 48 hours |
| Message Volume | ↓40% for 14 days | Account review call | 1 week |
| Payment Status | 7+ days late | Payment recovery outreach | 24 hours |
| Day 7 Activation | <60% weekly rate | Onboarding process review | 1 week |
| Support Sentiment | <0 for 5+ tickets | Executive sponsorship | 1 week |
| Plan Utilization | >25% at limits | Expansion outreach | 1 week |
| At-Risk Escalation | >20% to critical | Portfolio review | 1 week |

### 9.2 Lagging Indicators Quick Reference

| Metric | Target | Report Frequency | Owner | Escalation |
|--------|--------|------------------|-------|------------|
| NRR | ≥110% | Monthly | Head of CS | <105% → CMO |
| Churn Rate | ≤5% | Monthly | Head of CS | >6% → CEO |
| Health Score | ≥80 avg | Weekly | CS Lead | <75 → Exec team |
| NPS | ≥60 | Quarterly | VoC Lead | <50 → CMO |
| Expansion Rate | ≥10% | Monthly | Head of CS | <8% → CS Lead |
| Day 7 Activation | ≥80% | Weekly | CS Ops | <70% → Head of CS |

### 9.3 Reporting Quick Reference

| Report | Frequency | Distribution | Purpose | Action Items |
|--------|-----------|--------------|---------|--------------|
| Daily Pulse | Daily (8am) | CSMs, CS Lead, CMO | Critical alerts, daily priorities | Address critical accounts |
| Weekly Performance | Weekly (Mon 9am) | CS Lead, CMO, CEO | Week review, metrics vs targets | Approve weekly plan |
| Monthly Business Review | Monthly (5th day) | Exec Team, Board | Monthly performance, trends | Approve strategic initiatives |
| Quarterly Business Review | Quarterly | Board | Strategic review, forecasting | Approve quarterly goals |
| Segment Deep Dive | Monthly | Segment owners | Segment-specific health | Segment interventions |

---

## Appendix: Metric Definitions Catalog

### A.1 Adoption Metrics

| Metric | Formula | Data Source | Frequency |
|--------|---------|-------------|-----------|
| **Day 7 Activation Rate** | (Customers activated by Day 7) / (Total new customers) | Product DB | Daily |
| **Feature Adoption Velocity** | Avg days to adopt 3rd core feature | Product Analytics | Weekly |
| **Daily Active Users (DAU)** | (Unique logins today) / (Total customers) | Product DB | Daily |
| **Automation Rule Creation** | (Customers with 2+ rules) / (Total customers) | Product DB | Weekly |
| **First Value Time** | Hours from signup to first recovered sale | Product DB | Daily |

### A.2 Engagement Metrics

| Metric | Formula | Data Source | Frequency |
|--------|---------|-------------|-----------|
| **Login Frequency** | 7-day rolling avg of logins per customer | Product DB | Daily |
| **Message Volume Trend** | 7-day rolling avg of automated messages | Product DB | Daily |
| **Dashboard View Frequency** | Avg dashboard views per customer per week | Product DB | Weekly |
| **Support Ticket Sentiment** | NLP sentiment score (-1 to +1) | Support System | Daily |
| **Response Rate to CSM** | (CSM outreach with response) / (Total CSM outreach) | CRM | Weekly |

### A.3 Health Metrics

| Metric | Formula | Data Source | Frequency |
|--------|---------|-------------|-----------|
| **Health Score Trend** | 7-day change in avg health score | Health Engine | Daily |
| **Health Score Distribution** | (% customers with score 80+) | Health Engine | Weekly |
| **Risk Factor Accumulation** | Avg risk factors per customer | Health Engine | Weekly |
| **Payment Health** | (% customers with no payment issues) | Billing System | Daily |
| **At-Risk Escalation Rate** | (% At-Risk moving to Critical) | Health Engine | Weekly |

### A.4 Expansion Metrics

| Metric | Formula | Data Source | Frequency |
|--------|---------|-------------|-----------|
| **Plan Limit Utilization** | (% customers at 80%+ of plan limits) | Product DB | Weekly |
| **Team Size Growth** | (% customers adding users in 30 days) | Product DB | Monthly |
| **Feature Inquiry Rate** | (Premium feature tickets) / (Total tickets) | Support System | Monthly |
| **NPS Promoter Rate** | (% customers with NPS 9-10) | VoC System | Quarterly |
| **ROI Achievement Velocity** | Avg days to reach 3x ROI | Analytics | Monthly |

---

## Document Control

**Version**: 1.0
**Created**: 2026-04-26
**Owner**: CMO Agent (55827422-a849-41d3-9286-0b5b8b002079)
**Review Date**: 2026-07-26 (Quarterly)

**Related Documents**:
- [Customer Success Metrics and Health Score Dashboard](/conectapay/docs/customer-success-metrics-and-health-score-dashboard.md) - CON-175
- [Customer Success Playbook for At-Risk Accounts](/conectapay/docs/customer-success-at-risk-accounts-playbook.md) - CON-181
- [Customer Success Playbook](/conectapay/docs/customer-success-playbook.md)
- [Customer Journey Mapping](/conectapay/docs/customer-journey-mapping-and-experience-optimization.md) - CON-129

**Change Log**:
| Date | Version | Changes | Author |
|------|---------|---------|--------|
| 2026-04-26 | 1.0 | Initial document creation | CMO Agent |
