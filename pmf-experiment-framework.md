# Product-Market Fit Experiment Framework
## ConectaPay - Systematic Validation Across 4 Segments

**Version**: 1.0
**Date**: April 25, 2026
**Author**: CMO Agent
**Related**: [CON-74](/PAP/issues/CON-74)

---

## Executive Summary

This framework provides a systematic approach to validating Product-Market Fit (PMF) for ConectaPay across 4 priority segments. It builds on existing ICP discovery work ([CON-43](/PAP/issues/CON-43)) and smoke test infrastructure ([CON-63](/PAP/issues/CON-63)) to create data-backed Go/No-Go decisions for each segment.

**Key Hypothesis**: ConectaPay can recover 20-30% of abandoned sales through WhatsApp automation + Pix payments for Brazilian SMBs.

**Segments to Validate**:
1. **Clínicas Médicas** (No-show recovery)
2. **Imobiliárias** (Lead conversion)
3. **Academias** (Churn reduction/reactivation)
4. **Óticas** (Abandoned cart recovery)

---

## Part 1: Core PMF Hypothesis by Segment

### Segment 1: Clínicas Médicas (Medical Clinics)

**Hypothesis Statement**:
> "Medical clinics lose 15-25% of monthly revenue to patient no-shows. ConectaPay can recover 60% of missed appointments through automated WhatsApp confirmations + Pix pre-payment, saving clinics R$ 3,000-15,000/month."

**Problem Validation Questions**:
- What is your current no-show rate? (Target: >15%)
- How much revenue do you lose monthly to no-shows? (Target: >R$ 3,000)
- How do you currently confirm appointments? (Target: Manual phone/WhatsApp)
- Would you pay R$ 397/month to reduce no-shows by 60%? (Target: YES)

**Value Proposition**:
- Reduce no-shows from 20% → 8%
- Recover R$ 3,000-15,000/month in lost revenue
- Automate 100% of confirmation workflows
- Zero upfront cost (pay after results)

**Success Metrics**:
| Metric | Threshold | Excellent |
|--------|-----------|-----------|
| Problem recognition | 70% say no-shows are costly | 85%+ |
| Willingness to pay | R$ 297-497/month | R$ 497+ |
| Feature must-have | Automated confirmations | + Pix payment |
| Time to close | <14 days | <7 days |
| NPS after 30 days | >40 | >60 |

---

### Segment 2: Imobiliárias (Real Estate Agencies)

**Hypothesis Statement**:
> "Real estate agencies convert only 3-5% of leads into sales because 80% of leads are never followed up beyond first contact. ConectaPay automates follow-up sequences across WhatsApp, increasing conversion to 8-12% and generating R$ 15,000-50,000/month in additional commission."

**Problem Validation Questions**:
- What is your current lead-to-sale conversion rate? (Target: <8%)
- How many leads do you generate monthly? (Target: >100)
- How do you follow up with cold leads? (Target: Manual/sporadic)
- Would you pay R$ 597/month to double conversion rates? (Target: YES)

**Value Proposition**:
- Increase lead conversion from 4% → 10%
- Generate R$ 15,000-50,000/month in extra commission
- Automate WhatsApp follow-up sequences
- Tag and qualify leads automatically

**Success Metrics**:
| Metric | Threshold | Excellent |
|--------|-----------|-----------|
| Problem recognition | 70% say follow-up is broken | 85%+ |
| Willingness to pay | R$ 497-797/month | R$ 797+ |
| Feature must-have | WhatsApp sequences | + Lead tagging |
| Time to close | <14 days | <7 days |
| NPS after 30 days | >40 | >60 |

---

### Segment 3: Academias (Fitness Studios/Gyms)

**Hypothesis Statement**:
> "Gyms lose 8-12% of members monthly to churn, with 40% of cancellations preventable through early intervention. ConectaPay detects at-risk members via attendance tracking and sends automated WhatsApp re-engagement campaigns, reducing churn by 30% and saving R$ 2,000-8,000/month."

**Problem Validation Questions**:
- What is your monthly churn rate? (Target: >8%)
- How do you identify at-risk members? (Target: Manual/reactive)
- How do you re-engage inactive members? (Target: Phone/email)
- Would you pay R$ 397/month to reduce churn by 30%? (Target: YES)

**Value Proposition**:
- Reduce churn from 10% → 7%
- Save R$ 2,000-8,000/month in lost revenue
- Automatically detect at-risk members
- Send WhatsApp re-engagement campaigns

**Success Metrics**:
| Metric | Threshold | Excellent |
|--------|-----------|-----------|
| Problem recognition | 70% say churn is costly | 85%+ |
| Willingness to pay | R$ 297-497/month | R$ 497+ |
| Feature must-have | At-risk detection | + WhatsApp campaigns |
| Time to close | <14 days | <7 days |
| NPS after 30 days | >40 | >60 |

---

### Segment 4: Óticas (Optical Stores)

**Hypothesis Statement**:
> "Optical stores have 60-70% cart abandonment on glasses/contacts because customers defer decisions. ConectaPay recovers 25% of abandoned carts via WhatsApp reminders + Pix discount codes, generating R$ 4,000-12,000/month in recovered revenue."

**Problem Validation Questions**:
- What is your cart abandonment rate? (Target: >50%)
- How do you follow up on incomplete sales? (Target: Manual/rarely)
- Would you pay R$ 397/month to recover 25% of abandoned carts? (Target: YES)

**Value Proposition**:
- Recover 25% of abandoned carts
- Generate R$ 4,000-12,000/month
- Automate WhatsApp reminders
- Offer time-limited Pix discounts

**Success Metrics**:
| Metric | Threshold | Excellent |
|--------|-----------|-----------|
| Problem recognition | 70% say abandonment is costly | 85%+ |
| Willingness to pay | R$ 297-497/month | R$ 497+ |
| Feature must-have | Cart reminders | + Discount codes |
| Time to close | <14 days | <7 days |
| NPS after 30 days | >40 | >60 |

---

## Part 2: Experiment Designs (5 Frameworks)

### Experiment 1: Landing Page Smoke Test (All Segments)

**Objective**: Validate problem awareness and lead capture at scale

**Design**:
- Create 4 segment-specific landing pages (Webflow/Framer)
- Drive traffic via Meta Ads (R$ 3,000 total budget)
- Capture waitlist signups + booking calls

**Variables**:
- Headlines (3 variations per segment)
- Value props (feature vs. benefit focus)
- CTA buttons ("Join Waitlist" vs. "Book Demo")

**Metrics**:
| Metric | Target | PESSIMISTIC | REALISTIC | OPTIMISTIC |
|--------|--------|------------|-----------|------------|
| CTR | >2% | 1% | 2.5% | 4% |
| Landing page conversion | >15% | 8% | 18% | 30% |
| Cost per lead (CPL) | <R$ 50 | R$ 80 | R$ 40 | R$ 25 |
| Demo booking rate | >30% | 15% | 35% | 50% |

**Duration**: 2 weeks per segment

**Go/No-Go Criteria**:
- **GO**: CPL < R$ 50 AND demo booking > 25%
- **PIVOT**: CPL R$ 50-100 OR demo booking 15-25%
- **STOP**: CPL > R$ 100 OR demo booking < 15%

**Related**: [smoke-test-landing-page-copy.md](workspace:/smoke-test-landing-page-copy.md)

---

### Experiment 2: Pre-Sale Validation (Closest Friends)

**Objective**: Validate willingness-to-pay with real money

**Design**:
- Offer 50% lifetime discount to first 10 customers per segment
- Require 12-month pre-payment commitment
- Deliver MVP manually (no-code automation)
- Validate payment + usage over 90 days

**Variables**:
- Price anchoring (R$ 297 vs R$ 497 vs R$ 697)
- Payment terms (monthly vs annual)
- Onboarding friction (self-service vs assisted)

**Metrics**:
| Metric | Target | PESSIMISTIC | REALISTIC | OPTIMISTIC |
|--------|--------|------------|-----------|------------|
| Pre-sale conversion | >20% | 10% | 25% | 40% |
| Avg. deal size | >R$ 3,000 | R$ 2,000 | R$ 4,000 | R$ 6,000 |
| Time to first payment | <7 days | 14 days | 5 days | 2 days |
| Active usage (90d) | >70% | 50% | 80% | 95% |

**Duration**: 4 weeks outreach + 90 days usage

**Go/No-Go Criteria**:
- **GO**: >20% convert AND pay upfront
- **PIVOT**: 10-20% convert OR need payment plan
- **STOP**: <10% convert OR >50% refund

---

### Experiment 3: Concierge MVP (Wizard of Oz)

**Objective**: Validate value delivery before building automation

**Design**:
- 5 customers per segment get "full automation"
- Behind the scenes: human team sends manual WhatsApp messages
- Measure outcomes (no-show reduction, lead conversion, etc.)
- Interview customers after 30 days

**Variables**:
- Message frequency (daily vs every 2 days vs weekly)
- Message tone (professional vs friendly vs urgent)
- Personalization level (generic vs customized)

**Metrics**:
| Metric | Target | PESSIMISTIC | REALISTIC | OPTIMISTIC |
|--------|--------|------------|-----------|------------|
| Outcome improvement | >30% | 15% | 40% | 60% |
| Customer satisfaction (CSAT) | >4.0/5 | 3.5 | 4.3 | 4.8 |
| Referral requests | >40% | 20% | 50% | 80% |
| Time to set up | <2 hours | 4 hours | 1 hour | 30 min |

**Duration**: 6 weeks (1 week setup + 30 days usage + 1 week analysis)

**Go/No-Go Criteria**:
- **GO**: >30% outcome improvement AND CSAT >4.0
- **PIVOT**: 15-30% improvement OR CSAT 3.5-4.0
- **STOP**: <15% improvement OR CSAT <3.5

---

### Experiment 4: Fake Door Test (Feature Validation)

**Objective**: Test specific feature demand without building

**Design**:
- Add "Upgrade" buttons to existing workflows
- Show feature pricing and benefits
- Track click-through as demand signal
- Capture emails for interested users

**Variables**:
- Feature positioning (before vs after pain point)
- Price display (show vs hide pricing)
- Social proof (testimonials vs none)

**Metrics**:
| Metric | Target | PESSIMISTIC | REALISTIC | OPTIMISTIC |
|--------|--------|------------|-----------|------------|
| Fake door CTR | >5% | 2% | 7% | 15% |
| Email capture rate | >40% | 20% | 50% | 70% |
| Follow-up engagement | >30% | 15% | 35% | 55% |
| Feature preference ranking | Clear winner | Mixed | 2 clear winners | 1 dominant |

**Duration**: 3 weeks

**Go/No-Go Criteria**:
- **GO**: >5% CTR AND clear feature preference
- **PIVOT**: 3-5% CTR OR mixed preferences
- **STOP**: <3% CTR OR no clear winner

---

### Experiment 5: A/B Pricing Test (Revenue Validation)

**Objective**: Find optimal price point for each segment

**Design**:
- Test 3 price tiers simultaneously
- Randomize visitors across pricing pages
- Track conversion at each tier
- Calculate revenue per visitor

**Variables**:
- Price points (R$ 297 / R$ 497 / R$ 697)
- Billing frequency (monthly vs annual)
- Discount framing (50% off vs R$ 297/mo vs R$ 3,564/year)

**Metrics**:
| Metric | Target | PESSIMISTIC | REALISTIC | OPTIMISTIC |
|--------|--------|------------|-----------|------------|
| Conversion rate (low price) | >8% | 4% | 10% | 15% |
| Conversion rate (mid price) | >5% | 2% | 6% | 10% |
| Conversion rate (high price) | >3% | 1% | 4% | 8% |
| Revenue per visitor | >R$ 20 | R$ 10 | R$ 28 | R$ 45 |

**Duration**: 2 weeks

**Go/No-Go Criteria**:
- **GO**: Clear winner with >5% conversion
- **PIVOT**: All prices 2-5% conversion
- **STOP**: All prices <2% conversion

---

## Part 3: Segment Selection Framework

### PMF Scoring Matrix (0-100 points)

Score each segment on 5 dimensions (20 points each):

#### 1. Problem Severity (0-20)
- **0-5**: Nice-to-have problem, low urgency
- **6-10**: Moderate pain, some urgency
- **11-15**: Significant pain, high urgency
- **16-20**: Critical pain, urgent solution needed

#### 2. Willingness-to-Pay (0-20)
- **0-5**: R$ 0-200/month maximum
- **6-10**: R$ 200-400/month
- **11-15**: R$ 400-600/month
- **16-20**: R$ 600+/month

#### 3. Market Size (0-20)
- **0-5**: <1,000 potential customers in Brazil
- **6-10**: 1,000-5,000 potential customers
- **11-15**: 5,000-20,000 potential customers
- **16-20**: 20,000+ potential customers

#### 4. Acquisition Efficiency (0-20)
- **0-5**: CPL > R$ 100, unclear channels
- **6-10**: CPL R$ 50-100, 1-2 channels work
- **11-15**: CPL R$ 25-50, 2-3 channels work
- **16-20**: CPL < R$ 25, 3+ channels scale

#### 5. Retention Potential (0-20)
- **0-5**: High churn expected (>10% monthly)
- **6-10**: Moderate churn (5-10% monthly)
- **11-15**: Low churn (2-5% monthly)
- **16-20**: Very low churn (<2% monthly), high LTV

### Scoring Interpretation

| Total Score | PMF Signal | Decision |
|-------------|------------|----------|
| 80-100 | STRONG PMF | Scale immediately |
| 60-79 | Moderate PMF | Optimize then scale |
| 40-59 | Weak PMF | Pivot or deprioritize |
| 0-39 | No PMF | Kill segment |

---

## Part 4: Go/No-Go Decision Framework

### Segment-Level Decision Tree

```
START: Landing page smoke test
│
├─ CPL < R$ 50 AND Conversion > 15%?
│  ├─ YES → Proceed to pre-sale validation
│  │        │
│  │        ├─ >20% pre-sale conversion?
│  │        │  ├─ YES → Proceed to concierge MVP
│  │        │  │        │
│  │        │  │        ├─ >30% outcome improvement?
│  │        │  │  │       ├─ YES → **GO: Build MVP for segment**
│  │        │  │  │       └─ NO → Pivot value prop or price
│  │        │  │
│  │        │  └─ NO → Pivot pricing or offer
│  │
│  └─ NO → Pivot messaging or kill segment
│
└─ CPL > R$ 100 OR Conversion < 8%?
   └─ YES → **NO-GO: Kill segment immediately**
```

### Company-Level Portfolio Decision

After all segments complete experiments:

**Scenario A: 1 segment hits STRONG PMF (80+ score)**
- Decision: **FOCUS 100%** on that segment
- Allocate all resources to scale
- Defer other segments to Phase 2

**Scenario B: 2 segments hit MODERATE PMF (60-79 score)**
- Decision: **PARALLEL TRACK** both segments
- 60% resources to leader, 40% to runner-up
- Re-evaluate after 90 days

**Scenario C: 3+ segments hit WEAK PMF (40-59 score)**
- Decision: **CONSOLIDATE** into horizontal play
- Build generic "WhatsApp automation" product
- Let market pull decide use cases

**Scenario D: All segments score <40**
- Decision: **PIVOT ENTIRELY**
- Problem may be wrong, solution may be wrong, or both
- Return to customer discovery

---

## Part 5: Experiment Timeline & Resources

### Phase 1: Smoke Tests (Weeks 1-4)

| Week | Activity | Owner | Deliverable |
|------|----------|-------|-------------|
| 1 | Build landing pages (4 segments) | Growth Marketing | 4 live pages |
| 2 | Launch Meta Ads campaigns | Growth Marketing | Campaigns live |
| 3 | Monitor + iterate ads | Growth Marketing | Weekly reports |
| 4 | Analyze results + decision | CMO + CEO | Go/No-Go per segment |

**Budget**: R$ 3,000 (R$ 750/segment)
**Outcome**: 0-4 segments advance to Phase 2

---

### Phase 2: Pre-Sale Validation (Weeks 5-8)

| Week | Activity | Owner | Deliverable |
|------|----------|-------|-------------|
| 5 | Create pre-sale offer + outreach list | CMO | 50 prospects/segment |
| 6 | Execute outreach (phone + WhatsApp) | CEO | 10 pre-sales/segment |
| 7 | Onboarding + manual setup | CEO | 5 active customers/segment |
| 8 | Checkpoint review + decision | CMO + CEO | Go/No-Go per segment |

**Budget**: R$ 0 (bootstrap)
**Outcome**: 0-4 segments advance to Phase 3

---

### Phase 3: Concierge MVP (Weeks 9-14)

| Week | Activity | Owner | Deliverable |
|------|----------|-------|-------------|
| 9-10 | Manual WhatsApp operations | Operations | 5 customers/segment |
| 11 | Mid-point check-in interviews | CMO | Customer feedback |
| 12-13 | Continue operations + iterate | Operations | 30-day outcomes |
| 14 | Final analysis + segment scoring | CMO | PMF score per segment |

**Budget**: R$ 2,000 (WhatsApp Business API)
**Outcome**: Final segment selection + build decision

---

### Phase 4: MVP Build (Weeks 15-24)

| Week | Activity | Owner | Deliverable |
|------|----------|-------|-------------|
| 15-18 | Build automation core | CTO | Working MVP |
| 19-20 | Beta test with 5 customers | CSM | Feedback incorporated |
| 21-22 | Launch to 50 customers | Growth | Revenue generated |
| 23-24 | Review + scale decision | CEO + Board | Go/No-Go for scale |

**Budget**: R$ 20,000-50,000 (development)
**Outcome**: Self-sustaining product OR pivot

---

## Part 6: Risk Assessment & Mitigation

### Risk 1: Low Ad Response Rate (Meta Ads)

**Probability**: Medium (40%)
**Impact**: High (blocks all experiments)

**Mitigation**:
- Run 2 channels in parallel (Meta + LinkedIn)
- Build organic outreach as backup
- Partner with industry associations for access

**Trigger**: CPL > R$ 80 after 1 week
**Response**: Immediately pivot to LinkedIn/organic

---

### Risk 2: Customers Won't Pre-Pay

**Probability**: High (60%)
**Impact**: Medium (slows validation)

**Mitigation**:
- Offer money-back guarantee
- Provide payment plan option
- Reduce commitment to 3 months

**Trigger**: <10% pre-sale conversion
**Response**: Switch to monthly billing or free trial

---

### Risk 3: Manual Operations Don't Scale

**Probability**: Low (20%)
**Impact**: Medium (operational bottleneck)

**Mitigation**:
- Limit concierge to 5 customers/segment
- Use no-code tools (Zapier, Make)
- Document SOPs for future automation

**Trigger**: >2 hours/day per customer
**Response**: Pause new signups until automation

---

### Risk 4: All Segments Fail PMF

**Probability**: Low (15%)
**Impact**: Critical (business viability)

**Mitigation**:
- Test 2 backup segments (restaurants, salons)
- Keep customer discovery running continuously
- Build horizontal platform from Day 1

**Trigger**: All segments score <40
**Response**: Return to discovery, reassess entire thesis

---

## Part 7: Success Metrics Summary

### Leading Indicators (Weeks 1-8)

| Metric | Target per Segment |
|--------|-------------------|
| Landing page visitors | >500/week |
| Lead capture rate | >15% |
| Cost per lead | <R$ 50 |
| Demo booking rate | >30% |
| Pre-sale conversion | >20% |

### Lagging Indicators (Weeks 9-24)

| Metric | Target per Segment |
|--------|-------------------|
| Active customers (90 days) | >5 |
| Monthly revenue generated | >R$ 2,000 |
| Net Promoter Score | >40 |
| Customer retention (90d) | >70% |
| Referral rate | >30% |

### Portfolio-Level Targets

| Metric | Target (All Segments) |
|--------|----------------------|
| Segments passing smoke test | ≥2 |
| Segments passing pre-sale | ≥1 |
| Segments passing concierge MVP | ≥1 |
| Final PMF score (winner) | >70 |
| Time to first revenue | <8 weeks |

---

## Part 8: Quick Reference - Experiment Selection Guide

| Question | Use This Experiment |
|----------|---------------------|
| Do people recognize this problem? | Landing Page Smoke Test |
| Will they pay for a solution? | Pre-Sale Validation |
| Can we actually deliver value? | Concierge MVP (Wizard of Oz) |
| Which features matter most? | Fake Door Test |
| What's the optimal price point? | A/B Pricing Test |

---

## Part 9: Next Steps (Immediate Actions)

1. **Week 1**: Build 4 landing pages (Growth Marketing)
2. **Week 1**: Configure Meta Ads + analytics (Growth Marketing)
3. **Week 2**: Launch smoke tests (all segments)
4. **Week 2**: Create pre-sale outreach list (CMO)
5. **Week 4**: Smoke test decision checkpoint (CEO + CMO)

**Decision Point**: April 25 + 4 weeks = May 23, 2026

---

## Appendix A: Related Documents

- [Smoke Test Execution Guide](workspace:/smoke-test-execution-guide.md)
- [Daily Monitoring Framework](workspace:/daily-smoke-test-monitoring-framework.md)
- [ICP Interview Guides](workspace:/icp-interview-guide-clinics.md)
- [Messaging Framework](workspace:/messaging-framework.md)
- [Ad Copy Variations](workspace:/smoke-test-ad-copy.md)

---

## Appendix B: Template Files

- [PMF Score Calculator](workspace:/pmf-score-calculator.csv) - *To be created*
- [Segment Comparison Matrix](workspace:/segment-comparison-matrix.csv) - *To be created*
- [Experiment Tracking Sheet](workspace:/experiment-tracking-sheet.csv) - *To be created*

---

**End of Framework**
