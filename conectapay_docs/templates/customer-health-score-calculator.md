# Customer Health Score Calculator

**Purpose**: Monitor customer health and identify at-risk customers before they churn
**Score Range**: 0-100 (Green: 80-100, Yellow: 60-79, Red: 0-59)
**Frequency**: Calculate weekly starting Day 14 after signup

---

## Health Score Dimensions (100 Total Points)

### 1. Product Usage (0-30 points)

**What it measures**: How actively the customer uses ConectaPay

| Metric | Points | Calculation |
|--------|--------|-------------|
| **Active Campaigns** | 0-15 | Active campaigns ÷ 3 expected × 15 |
| **Messages Sent** | 0-10 | Messages sent ÷ 100 expected × 10 |
| **Pix Transactions** | 0-5 | Transactions ÷ 10 expected × 5 |

**Scoring Examples**:
- 3+ active campaigns → 15 points
- 100+ messages sent → 10 points
- 10+ Pix transactions → 5 points
- **Maximum**: 30 points

**Data Source**: ConectaPay app dashboard

**Red Flags**:
- 0 active campaigns → 0 points (Critical)
- 0 messages sent → 0 points (Not using product)
- 0 Pix transactions → 0 points (No revenue captured)

---

### 2. Engagement (0-25 points)

**What it measures**: How recently and frequently the customer interacts with ConectaPay

| Metric | Points | Criteria |
|--------|--------|----------|
| **Last Login** | 0-15 | <7 days (15), 7-14 days (10), 14-30 days (5), >30 days (0) |
| **Login Frequency** | 0-10 | Daily (10), Weekly (7), Monthly (3), Rarely (0) |

**Scoring Examples**:
- Logged in today → 15 points
- Logs in daily → 10 points
- **Maximum**: 25 points

**Data Source**: App analytics / Login logs

**Red Flags**:
- Last login >30 days ago → 0 points (Churn risk)
- Logs in <1x per month → 0 points (Not engaged)

---

### 3. Payment Success (0-20 points)

**What it measures**: How successfully ConectaPay processes Pix payments for their customers

| Metric | Points | Calculation |
|--------|--------|-------------|
| **Pix Success Rate** | 0-20 | Successful Pix ÷ Total Pix × 20 |

**Scoring Examples**:
- 100% success rate → 20 points
- 95% success rate → 19 points
- 80% success rate → 16 points
- <50% success rate → <10 points (Critical issue)

**Maximum**: 20 points

**Data Source**: Payment processor logs

**Red Flags**:
- <80% success rate → Under 16 points (Technical issue)
- 0% success rate → 0 points (Not working at all)

---

### 4. Support Requests (0-15 points)

**What it measures**: How many support tickets the customer has submitted

| Ticket Volume (30 days) | Points | Rationale |
|------------------------|--------|-----------|
| 0-2 tickets | 15 | Healthy - using product without issues |
| 3-5 tickets | 10 | Normal - learning curve |
| 6-10 tickets | 5 | Struggling - needs help |
| 11+ tickets | 0 | Frustrated - high churn risk |

**Maximum**: 15 points

**Data Source**: Support ticket system (HubSpot/Freshdesk/Zendesk)

**Red Flags**:
- 11+ tickets in 30 days → 0 points (Very unhappy)
- Same issue reported 3+ times → Technical debt

---

### 5. NPS Score (0-10 points)

**What it measures**: Customer sentiment and likelihood to recommend

| NPS Response | Points | Category |
|--------------|--------|----------|
| 9-10 (Promoter) | 10 | Love the product |
| 7-8 (Passive) | 5 | Satisfied but not excited |
| 0-6 (Detractor) | 0 | Unhappy - churn risk |
| No response | 5 | Neutral assumption |

**Maximum**: 10 points

**Data Source**: NPS survey (sent monthly starting Month 1)

**Red Flags**:
- NPS 0-6 → 0 points (At risk of churning)
- No response to 3+ surveys → Engagement issue

---

## Total Health Score Calculation

```
Product Usage (30) +
Engagement (25) +
Payment Success (20) +
Support Requests (15) +
NPS Score (10)
=
TOTAL HEALTH SCORE (0-100)
```

---

## Health Categories & Actions

### 🟢 Green (80-100 points): Healthy
**Characteristics**:
- Actively using all features
- Logs in regularly
- High payment success
- Few support requests
- Promoter NPS score

**Actions**:
- Ask for referral (Month 1)
- Request case study (Month 3)
- Offer upgrade to higher plan (Month 6)
- Invite to beta features (Ongoing)

**Message Example**:
```
Oi [Name]! 🎉

Tudo ótimo por aqui! Vi que você está usando muito o ConectaPay
e recuperando várias vendas.

Teria 5 minutos para me contar sua experiência? Queremos usar
sua história como case de sucesso!

Abraço,
[Equipe ConectaPay]
```

---

### 🟡 Yellow (60-79 points): At Risk
**Characteristics**:
- Using some features but not all
- Inconsistent engagement
- Payment success <90%
- Moderate support requests
- Passive NPS score

**Actions**:
- Proactive outreach within 48 hours
- Identify specific pain points
- Offer training/resources
- Schedule success call
- Monitor closely (weekly health checks)

**Message Example**:
```
Oi [Name]! 👋

Notei que você não está usando alguns recursos do ConectaPay.
Tem algo que está te impedindo de usar mais?

Posso te ajudar a configurar [feature X] para recuperar
mais vendas. Quer agendar uma call rápida?

Abraço,
[Equipe ConectaPay]
```

**Diagnostic Questions**:
1. Which features are confusing?
2. What's your biggest challenge right now?
3. What would make ConectaPay more valuable?
4. Are you seeing ROI? If not, why?

---

### 🔴 Red (0-59 points): Critical
**Characteristics**:
- Barely using product
- Haven't logged in >30 days
- Payment success <50%
- Many support requests
- Detractor NPS score

**Actions**:
- Immediate intervention (within 24 hours)
- Understand why they're unhappy
- Fix technical issues ASAP
- Offer concession if needed (discount, free month)
- If unsaveable - graceful exit request

**Message Example**:
```
Oi [Name]! 🚨

Notei que você não está tendo uma boa experiência com o
ConectaPay e eu quero mudar isso.

O que aconteceu? Tem algum problema técnico? Posso te ligar
agora para resolver isso?

Abraço,
[Founder/CS Lead]
```

**Save Playbook**:
1. Acknowledge the issue
2. Fix technical problems immediately
3. Offer training/onboarding redo
4. Provide 1 month free if needed
5. If still unhappy - request exit interview

---

## Health Score Tracking Template

### Google Sheets Structure

| Customer ID | Customer Name | Industry | Signup Date | Health Score | Product Usage | Engagement | Payment Success | Support Requests | NPS | Category | Last Updated |
|-------------|---------------|----------|-------------|--------------|---------------|------------|-----------------|------------------|-----|----------|--------------|
| C-001 | Clínica São José | Clínica | 2026-05-01 | 85 | 28/30 | 23/25 | 18/20 | 15/15 | 10/10 | Green | 2026-05-15 |
| C-002 | Imobiliária Costa | Imobiliária | 2026-05-01 | 62 | 15/30 | 18/25 | 16/20 | 10/15 | 5/10 | Yellow | 2026-05-15 |
| C-003 | Academia Fit | Academia | 2026-05-01 | 45 | 8/30 | 5/25 | 10/20 | 5/15 | 0/10 | Red | 2026-05-15 |

### Formulas

- **Health Score**: `=Product_Usage + Engagement + Payment_Success + Support_Requests + NPS`
- **Category**: `=IF(Health_Score>=80,"Green",IF(Health_Score>=60,"Yellow","Red"))`
- **Days Since Signup**: `=TODAY()-Signup_Date`
- **Should Score**: `=IF(Days_Since_Signup>=14,TRUE,FALSE)`

### Conditional Formatting

- **Green (80-100)**: Green background, white text
- **Yellow (60-79)**: Yellow background, black text
- **Red (0-59)**: Red background, white text

---

## Weekly Health Review Process

### Every Friday 4:00 PM (15 minutes)

**Review Agenda**:

1. **Red Customers First** (10 min)
   - List all red scores
   - Discuss each customer
   - Assign intervention actions
   - Set follow-up date

2. **Yellow Customers** (3 min)
   - Identify declining scores
   - Plan proactive outreach
   - Schedule success calls

3. **Green Customers** (2 min)
   - Identify referral opportunities
   - Select case study candidates
   - Plan upgrade offers

**Output**: Action items for next week

---

## Health Score Automation (Future)

### When Ready to Automate

**Tool**: HubSpot Workflows or Custom Script

**Trigger**: Every Friday at 4:00 PM

**Actions**:
1. Pull all customer data from ConectaPay API
2. Calculate health scores automatically
3. Update health score field in HubSpot
4. Send Slack alert for red scores
5. Create tasks for yellow scores

**Alert Format**:
```
🔴 Health Score Alert: [Customer Name]

Score: [XX/100] (Red)
Top Issue: [Low engagement / Payment issues / etc.]
Action Required: [Immediate outreach needed]

View: [Link to customer record]
```

---

## Pre-Launch Mode (Current State)

**Since we have 0 customers, health scoring is not active yet**

### What to Do Now:
1. ✅ Health score calculator documented (this doc)
2. ✅ Health score dimensions defined
3. ✅ Scoring formulas created
4. ⏳ Wait for first customer to go live
5. ⏳ Calculate first health score on Day 14

### When First Customer Signs Up:
1. Day 0-13: Monitor usage, don't calculate score
2. Day 14: Calculate first health score manually
3. Day 14: Send NPS survey (if using)
4. Day 15: Document score in tracking sheet
5. Week 2-4: Calculate weekly, identify trends

### When 10+ Customers:
1. Set up automated health scoring (script/API)
2. Create health score dashboard
3. Schedule weekly health reviews
4. Build intervention playbooks

---

## Health Score Targets (Month 3)

| Metric | Target | Rationale |
|--------|--------|-----------|
| **Average Health Score** | 80+ | Healthy customer base |
| **Green Customers** | 70%+ | Most customers thriving |
| **Yellow Customers** | 20% | Some need help |
| **Red Customers** | <10% | Minimize churn risk |
| **Health Score Improvement** | +5 points/month | Customers getting healthier |

---

## Troubleshooting Health Scores

### Issue: All Customers Are Red
**Possible Causes**:
- Product is broken (check payment success)
- Onboarding is too hard (check engagement)
- Wrong ICP (check if using wrong segments)

**Actions**:
1. Fix product issues first
2. Improve onboarding
3. Revisit ICP definition

### Issue: Health Scores Not Correlating with Churn
**Possible Causes**:
- Wrong dimensions (missing key metrics)
- Wrong weights (over/under-valued)
- Data quality issues (bad data)

**Actions**:
1. Analyze churned customers' scores
2. Identify which dimensions predicted churn
3. Adjust weights and dimensions
4. Re-test with new customers

### Issue: Scores Jumping Around (Unstable)
**Possible Causes**:
- Calculating too frequently (daily vs weekly)
- Seasonal usage patterns
- One-time events (campaign spikes)

**Actions**:
1. Calculate weekly (not daily)
2. Use rolling averages (4-week trend)
3. Smooth out one-time spikes

---

**Calculator Version**: 1.0
**Last Updated**: April 27, 2026
**Owner**: CMO Agent (transitions to CS Hire)
**Review Frequency**: Monthly (adjust dimensions/weights as needed)
