# Customer Success Playbook for At-Risk Accounts

**Version:** 1.0
**Created:** April 26, 2026
**Owner:** CMO - ConectaPay
**Purpose:** Comprehensive playbook for identifying, managing, and recovering at-risk and churning customer accounts

---

## Executive Summary

This playbook provides ConectaPay Customer Success teams with a complete framework for managing at-risk accounts throughout the customer lifecycle. It enables early risk identification, staged intervention protocols, and systematic win-back strategies to minimize churn and maximize customer lifetime value.

**Key Objectives:**
- Reduce churn rate by 40% through early identification
- Recover 60% of at-risk accounts before cancellation
- Win back 25% of churned customers within 90 days
- Establish standardized intervention protocols across all segments

**Target Audience:** Customer Success Managers, Account Managers, Retention Specialists

---

## Table of Contents

1. [At-Risk Account Definition](#1-at-risk-account-definition)
2. [Risk Identification Framework](#2-risk-identification-framework)
3. [Risk Scoring System](#3-risk-scoring-system)
4. [Intervention Playbooks](#4-intervention-playbooks)
5. [Retention Escalation Procedures](#5-retention-escalation-procedures)
6. [Win-Back Strategies](#6-win-back-strategies)
7. [Retention Offers Framework](#7-retention-offers-framework)
8. [Segment-Specific Tactics](#8-segment-specific-tactics)
9. [Success Metrics and KPIs](#9-success-metrics-and-kpis)
10. [Tools and Templates](#10-tools-and-templates)

---

## 1. At-Risk Account Definition

### 1.1 What is an At-Risk Account?

An **at-risk account** is a customer showing behavioral indicators that suggest a high probability of churn (cancellation, non-renewal, downgrade) within the next 30-90 days.

### 1.2 At-Risk Account Categories

| Category | Definition | Time Horizon | Urgency |
|----------|------------|--------------|---------|
| **Critical Risk** | Account has initiated cancellation or shown extreme disengagement | 0-7 days | Immediate |
| **High Risk** | Multiple strong risk signals present, rapid decline in usage | 7-30 days | High |
| **Medium Risk** | Some risk signals present, early stage of disengagement | 30-60 days | Medium |
| **Low Risk** | Single or minor risk signals, still engaged | 60-90 days | Monitor |

### 1.3 Churn Stage Definitions

| Stage | Description | Recovery Probability |
|-------|-------------|---------------------|
| **Pre-Churn** | Risk signals present, no cancellation initiated | 70-80% |
| **Soft Churn** | Cancellation discussed or requested, still negotiable | 40-60% |
| **Hard Churn** | Cancellation confirmed, account closed | 10-25% (win-back) |
| **Post-Churn** | Account closed 30+ days ago | 5-15% (win-back) |

---

## 2. Risk Identification Framework

### 2.1 Early Warning Signals (The 7 Signals)

#### Behavioral Signals

1. **Usage Decline**
   - 50%+ drop in WhatsApp automation triggers (7-day avg)
   - 40%+ drop in Pix payment volume (30-day avg)
   - Zero automation runs for 14+ days

2. **Engagement Drop**
   - No login for 14+ days (previously active weekly)
   - Dashboard views down 60%+
   - Support ticket frequency drops to zero (previously active)

3. **Feature Abandonment**
   - Core features unused for 30+ days
   - Advanced features never activated after onboarding
   - Integration/API usage stops

4. **Payment Issues**
   - Failed payment attempts
   - Late payments (7+ days past due)
   - Downgrade payment method requests

#### Relationship Signals

5. **Communication Withdrawal**
   - No response to 3+ outreach attempts
   - One-word responses to check-ins
   - Declining scheduled meetings

6. **Sentiment Shift**
   - Negative NPS score (0-3)
   - Increase in complaint frequency
   - Negative keywords in communication: "complicated", "expensive", "not working"

#### External Signals

7. **Business Changes**
   - Key stakeholder leaves (champion exit)
   - Company restructuring/downsizing
   - Competitor adoption signals

### 2.2 Automated Risk Detection Triggers

| Trigger | Threshold | Action |
|---------|-----------|--------|
| Usage Alert | 50% drop in 7-day average | Auto-tag "at-risk", notify CSM |
| Login Alert | 14 days no login | Auto-email re-engagement sequence |
| Payment Alert | Failed payment | Immediate CSM outreach |
| Champion Alert | Key contact removed | High-priority relationship check |
| Competitor Alert | Competitor domain detected | Competitive win-back playbook |

### 2.3 Manual Risk Discovery Methods

**Quarterly Business Reviews (QBRs):**
- Discuss customer goals and ConectaPay alignment
- Identify unmet needs or friction points
- Gauge sentiment and renewal intent

**Health Score Monitoring:**
- Review health score trends weekly
- Flag accounts with declining scores (3+ point drop)
- Cross-reference with NPS data

**Customer Feedback Loop:**
- Support ticket sentiment analysis
- Feature request patterns (unmet needs)
- Cancellation survey data

---

## 3. Risk Scoring System

### 3.1 At-Risk Score Calculation (0-100)

**Formula:** Weighted sum of risk indicators

```
At-Risk Score = (Usage Score × 0.30) + (Engagement Score × 0.25) + (Relationship Score × 0.20) + (Payment Score × 0.15) + (Sentiment Score × 0.10)
```

### 3.2 Score Components

#### Usage Score (0-100)
| Metric | Score |
|--------|-------|
| Usage increased 20%+ | 0 |
| Usage stable (±20%) | 10 |
| Usage declined 20-40% | 40 |
| Usage declined 40-60% | 70 |
| Usage declined 60%+ or zero | 100 |

#### Engagement Score (0-100)
| Metric | Score |
|--------|-------|
| Daily login | 0 |
| Weekly login | 10 |
| Bi-weekly login | 40 |
| Monthly login | 70 |
| 30+ days no login | 100 |

#### Relationship Score (0-100)
| Metric | Score |
|--------|-------|
| Champion engaged, responsive | 0 |
| Champion responsive but less engaged | 30 |
| Champion unresponsive, secondary contact responsive | 60 |
| All contacts unresponsive | 100 |

#### Payment Score (0-100)
| Metric | Score |
|---------------|
| Always on time | 0 |
| Occasional late (1-3 days) | 20 |
| Frequently late (4-7 days) | 50 |
| Failed payment or 7+ days late | 100 |

#### Sentiment Score (0-100)
| Metric | Score |
|--------|-------|
| NPS 9-10 (Promoter) | 0 |
| NPS 7-8 (Passive) | 20 |
| NPS 5-6 | 50 |
| NPS 0-4 (Detractor) | 100 |
| No NPS data but recent positive feedback | 10 |
| No NPS data but recent negative feedback | 70 |

### 3.3 Risk Level Classification

| Total Score | Risk Level | Response Time | Owner |
|-------------|------------|---------------|-------|
| 0-20 | Low Risk | Monitor weekly | CSM (routine) |
| 21-40 | Medium Risk | Bi-weekly outreach | CSM + Account Manager |
| 41-60 | High Risk | Weekly outreach | CSM + Customer Success Lead |
| 61-80 | Critical Risk | Daily outreach | CSM + CS Lead + VP Customer Success |
| 81-100 | Emergency | Immediate intervention | VP Customer Success + CEO (if enterprise) |

### 3.4 Dynamic Scoring

**Recalculate risk scores weekly** for all active accounts. Flag accounts with:
- 15+ point increase (rapid deterioration)
- 3 consecutive weeks of upward trend (sustained decline)

---

## 4. Intervention Playbooks

### 4.1 Intervention Staging Model

**Stage 1: Early Intervention (Score 21-40)**
- Goal: Re-engage before disengagement deepens
- Timeline: First contact within 48 hours of flag
- Owner: Assigned CSM

**Stage 2: Active Intervention (Score 41-60)**
- Goal: Identify root cause and deliver corrective action plan
- Timeline: Daily to bi-weekly contact depending on urgency
- Owner: CSM + Customer Success Lead

**Stage 3: Critical Intervention (Score 61-80)**
- Goal: Prevent cancellation through aggressive retention tactics
- Timeline: Daily contact, executive involvement
- Owner: VP Customer Success + CSM

**Stage 4: Emergency Intervention (Score 81-100)**
- Goal: Save account at all costs or manage graceful exit
- Timeline: Immediate, multiple touchpoints daily
- Owner: VP Customer Success + CEO (for strategic accounts)

### 4.2 Stage 1: Early Intervention Playbook

**Trigger:** Risk score 21-40 or single major risk signal

**Objective:** Re-engage customer and identify emerging issues

**Action Plan:**

1. **Day 0-2: Discovery Call**
   - Schedule 30-minute check-in call
   - Agenda: "How are things going? Any changes since we last spoke?"
   - Goal: Uncover changes in business, priorities, or challenges

2. **Day 3-7: Value Reinforcement**
   - Share personalized impact report
   - Highlight recent achievements (automation saved X hours, recovered R$ Y in abandoned sales)
   - Send 2-3 relevant tips/resources

3. **Day 8-14: Feature Re-education**
   - Offer training on underutilized features
   - Share customer success story from similar business
   - Propose optimization ideas for their use case

4. **Day 15-30: Relationship Deepening**
   - Invite to exclusive customer webinar
   - Request feedback on new feature (make them feel heard)
   - Offer to optimize their automation workflows

**Success Criteria:**
- Risk score decreases by 10+ points within 30 days
- Customer responds to outreach within 7 days
- Usage stabilizes or increases

**If Unsuccessful:**
- Escalate to Stage 2 intervention
- Re-assign CSM if relationship issue identified

### 4.3 Stage 2: Active Intervention Playbook

**Trigger:** Risk score 41-60 or Stage 1 unsuccessful

**Objective:** Diagnose root cause and deliver targeted solution

**Action Plan:**

1. **Day 0: Rapid Risk Assessment**
   - CSM + Customer Success Lead review account history
   - Identify all red flags (usage, sentiment, payments, relationship)
   - Prepare hypothesis: "Why is this account at-risk?"

2. **Day 1-2: Root Cause Discovery Call**
   - 45-minute call with decision-maker
   - Direct approach: "We've noticed [X signal], help us understand what's changed"
   - Listen 80% of the call, take detailed notes

3. **Day 3-5: Solution Proposal**
   - Draft customized solution addressing identified pain points
   - Include: quick wins (immediate actions) + long-term fixes (30-60 days)
   - Present to customer with clear timeline

4. **Day 6-14: Quick Win Execution**
   - Deliver at least one immediate improvement
   - Examples: optimize automation flow, fix integration bug, provide custom training
   - Proactive communication: "Here's what we did, here's the result"

5. **Day 15-30: Monitor and Adjust**
   - Weekly check-ins
   - Track leading indicators: usage, sentiment, responsiveness
   - Adjust approach based on feedback

**Success Criteria:**
- Risk score decreases by 20+ points within 30 days
- Customer commits to continued relationship
- Usage increases by 20%+

**If Unsuccessful:**
- Escalate to Stage 3 critical intervention
- Offer retention incentive (discount, extended trial, free features)

### 4.4 Stage 3: Critical Intervention Playbook

**Trigger:** Risk score 61-80, cancellation requested, or Stage 2 unsuccessful

**Objective:** Prevent cancellation through executive involvement and retention offers

**Action Plan:**

1. **Day 0: Emergency War Room**
   - VP Customer Success + CSM + Account Manager review
   - Assemble all available data: usage history, support tickets, NPS, payments, communications
   - Determine: "Is this account saveable? At what cost?"

2. **Day 0-1: Executive Outreach**
   - VP Customer Success sends personal email/WhatsApp to decision-maker
   - Message: "I noticed [X], can we hop on a call to understand how we can fix this?"
   - Signal importance: executive-to-executive communication

3. **Day 1-3: Retention Discovery Call**
   - VP Customer Success leads the call, CSM supports
   - Acknowledge issues directly: "We see we haven't delivered [X], here's our plan to fix it"
   - Ask: "What would make you stay?"

4. **Day 3-7: Retention Offer Package**
   - Prepare customized retention offer (see Section 7)
   - Include: immediate value (discount/credit) + future value (roadmap commitment)
   - Present with 7-day acceptance window

5. **Day 8-14: Close the Retention**
   - Secure commitment to 90-day recovery plan
   - Document agreement and set clear expectations
   - Assign dedicated success manager (if not already)

6. **Day 15-90: Recovery Execution**
   - Weekly executive check-ins for first month
   - Bi-weekly thereafter
   - Monthly business review to demonstrate progress

**Success Criteria:**
- Cancellation withdrawn
- Customer commits to 90-day recovery plan
- Risk score decreases by 30+ points within 60 days

**If Unsuccessful:**
- Transition to win-back strategy (Section 6)
- Conduct exit interview to gather insights
- Mark account for re-engagement in 90 days

### 4.5 Stage 4: Emergency Intervention Playbook

**Trigger:** Risk score 81-100, immediate cancellation, or strategic account at risk

**Objective:** Save account at all costs or manage graceful exit

**Action Plan:**

1. **Hour 0-4: Crisis Response**
   - VP Customer Success + CEO notification (for strategic accounts)
   - All-hands review: mobilize any available resource
   - Determine "save threshold" - maximum retention offer authorized

2. **Hour 4-24: Direct Executive Outreach**
   - CEO or VP Customer Success calls decision-maker directly
   - No intermediaries, direct leader-to-leader communication
   - Message: "Your success is our priority. What do you need to stay?"

3. **Day 1-3: Custom Retention Agreement**
   - Build bespoke offer based on customer's stated needs
   - Include: pricing/terms flexibility + feature prioritization + service level commitments
   - Fast-track legal/approval (bypass normal processes if needed)

4. **Day 4-7: Decision and On-Retrention**
   - Secure commitment with signed addendum
   - Immediate onboarding/re-orientation call
   - Assign executive sponsor for 90-day recovery period

5. **Day 8-90: Executive Sponsorship**
   - Executive sponsor meets with customer weekly for first month
   - Monthly executive business reviews thereafter
   - Direct escalation path to CEO/VP for any issues

**Success Criteria:**
- Account saved from immediate cancellation
- Customer signs 6-12 month extended commitment
- NPS increases to 7+ within 90 days

**If Unsuccessful:**
- Execute graceful exit process
- Preserve relationship for future win-back
- Document lessons learned for prevention

---

## 5. Retention Escalation Procedures

### 5.1 Escalation Triggers

Escalate to next level when:
- Risk score increases by 15+ points in 7 days
- Customer requests cancellation or downgrade
- CSM unable to reach decision-maker after 5 attempts
- Customer threatens to post negative review or refer to competitor
- Payment issues unresolved for 14+ days

### 5.2 Escalation Matrix

| From | To | Trigger | Timeline | Approval |
|------|----|---------|----------|----------|
| CSM | Customer Success Lead | Risk score 41-60, Stage 2 needed | Within 24 hours | Automatic |
| CSM | VP Customer Success | Risk score 61-80, cancellation request | Within 4 hours | Automatic |
| Customer Success Lead | VP Customer Success | Stage 2 unsuccessful, retention offer needed | Within 48 hours | VP approval |
| VP Customer Success | CEO | Strategic account (R$ 50k+ ARR) at risk | Within 24 hours | CEO discretion |
| Any | Emergency Crisis Team | Multiple accounts at-risk simultaneously (systemic issue) | Immediate | CEO + VP Customer Success |

### 5.3 Escalation Communication Protocol

**Internal Escalation Template:**
```
SUBJECT: ESCALATION: [Customer Name] - Risk Score [X]

ACCOUNT: [Customer Name] (CON-XXX)
CURRENT RISK SCORE: [X] (increased from [Y])
RISK LEVEL: [High/Critical]
TRIGGER: [Brief description of escalation trigger]

ATTEMPTS MADE:
- [Date]: [Action taken, result]
- [Date]: [Action taken, result]

ROOT CAUSE (known or suspected):
- [Hypothesis]

REQUESTED ACTION:
- [What you need from the escalatee]

NEXT STEPS IF NO ACTION:
- [What happens if escalation doesn't resolve issue]

ASSIGNED TO: [Name]
FOLLOW-UP BY: [Date]
```

### 5.4 Escalation Response SLAs

| Escalation Level | Response Time | Resolution Target |
|------------------|---------------|-------------------|
| CSM → CS Lead | 4 hours | 48 hours |
| CSM → VP CS | 2 hours | 24 hours |
| Any → CEO | 1 hour | 8 hours |
| Crisis Team | Immediate | 4 hours |

### 5.5 De-escalation Procedure

When risk score decreases by 20+ points or customer confirms satisfaction:

1. **Document resolution:** What worked, what didn't
2. **Update account status:** Change risk level in CRM
3. **Notify escalation chain:** "Resolved - no further action needed"
4. **Schedule follow-up:** Set calendar reminder for 30-day check-in
5. **Conduct retrospective:** What could we have done earlier?

---

## 6. Win-Back Strategies

### 6.1 Win-Back Segmentation

| Segment | Definition | Win-Back Approach | Expected Success Rate |
|---------|------------|-------------------|---------------------|
| **Soft Churn** | Cancellation requested but not finalized | Negotiate retention, address concerns | 40-60% |
| **Hard Churn (0-30 days)** | Account closed within 30 days | Aggressive win-back, incentives | 25-40% |
| **Hard Churn (31-90 days)** | Account closed 31-90 days ago | Targeted re-engagement, new features | 15-25% |
| **Post-Churn (91-180 days)** | Account closed 91-180 days ago | Check-in, market updates | 5-15% |
| **Post-Churn (180+ days)** | Account closed 6+ months ago | Quarterly newsletter only | 1-5% |

### 6.2 Win-Back Strategy: Soft Churn (Pre-Cancellation)

**Trigger:** Customer initiates cancellation but not yet processed

**Approach:** Last-chance retention before account closes

**Playbook:**

1. **Immediate Response (Within 2 hours)**
   - Acknowledge cancellation request
   - Express regret: "We're sorry to see you go"
   - Ask: "Before we process, can you share the main reason?"
   - Goal: Uncover true objection (price, features, service, competitor)

2. **Root Cause Discovery (Within 24 hours)**
   - Schedule 15-minute call with decision-maker
   - Listen without defensiveness
   - Ask: "What would need to change for you to stay?"

3. **Counter-Offer (Within 48 hours)**
   - Present customized solution addressing stated reason
   - Examples:
     - Price issue → Offer 10-20% discount for 6 months
     - Feature gap → Commit to roadmap timeline, offer beta access
     - Service issue → Assign dedicated success manager
   - Include: "If we do [X], will you stay?"

4. **Decision Deadline (7 days)**
   - Set clear deadline: "This offer is valid for 7 days"
   - Follow up on day 3 and day 6
   - If no response, process cancellation

5. **Graceful Exit (If declined)**
   - Honor cancellation promptly
   - Offer: "If things change, come back within 90 days for [welcome-back offer]"
   - Request exit interview

**Success Rate:** 40-60%

### 6.3 Win-Back Strategy: Hard Churn 0-30 Days

**Trigger:** Account closed 0-30 days ago

**Approach:** Immediate win-back with incentives

**Playbook:**

1. **Day 0-7: No Contact Period**
   - Let customer experience life without ConectaPay
   - They need to feel the pain of lost automation

2. **Day 8-14: First Win-Back Outreach**
   - Channel: Email + WhatsApp
   - Message: "It's been [X] days, how are things going without our automation?"
   - Include: 2-3 specific metrics they're losing (e.g., "You recovered R$ 4,500 in abandoned sales in March - that's now at risk")
   - Offer: 20% discount for 6 months if they reactivate within 14 days

3. **Day 15-21: Follow-Up Outreach**
   - Channel: Phone call (if number available)
   - Script: "I haven't heard back - I wanted to personally check in. Is there anything we can do to bring you back?"
   - Goal: Get them on a call to discuss concerns

4. **Day 22-30: Final Chance Offer**
   - Channel: Certified email
   - Offer: "We've upgraded our platform since you left. Come back and get [new feature] + 15% off for 3 months"
   - Deadline: "This offer expires in 7 days"

**Success Rate:** 25-40%

### 6.4 Win-Back Strategy: Hard Churn 31-90 Days

**Trigger:** Account closed 31-90 days ago

**Approach:** Feature-based win-back

**Playbook:**

1. **Monthly Touchpoints (Day 31, 60, 90)**
   - Share product updates and new features
   - Include customer case studies: "See how [similar business] is succeeding with ConectaPay"
   - Position as: "We've made improvements based on feedback from customers like you"

2. **Personalized Re-Engagement (Day 45-60)**
   - Research: What's changed in their business?
   - Look for: Growth, new hires, new locations (signals they might need automation again)
   - Outreach: "I saw you opened a new location - congratulations! ConectaPay can help you manage..."
   - Offer: "Come back with no setup fee (R$ 500 value)"

3. **Quarterly Business Review Invitation (Day 75-90)**
   - Invite to exclusive customer webinar
   - Topic: "What's new at ConectaPay and how it helps [industry]"
   - Offer: "Rejoin and get first month free"

**Success Rate:** 15-25%

### 6.5 Win-Back Strategy: Post-Churn 91-180 Days

**Trigger:** Account closed 91-180 days ago

**Approach:** Light touch, value-focused

**Playbook:**

1. **Quarterly Newsletter**
   - Add to "Alumni Newsletter" list
   - Content: Product updates, customer success stories, industry insights
   - Goal: Keep ConectaPay top-of-mind for future consideration

2. **Trigger-Based Outreach**
   - Monitor for business events: new locations, funding, leadership changes
   - Reach out with: "Congratulations on [milestone]! As you scale, ConectaPay can help..."
   - Offer: "Welcome back discount: 10% off for 3 months"

3. **Competitive Win-Back**
   - Monitor if they adopt competitor (social media, job postings)
   - If competitor identified, research competitor weaknesses
   - Outreach: "I saw you're using [competitor]. Here's what ConectaPay does better: [X, Y, Z]"
   - Offer: Switch back with 2 months free + dedicated onboarding

**Success Rate:** 5-15%

### 6.6 Win-Back Message Templates

#### Template 1: Empathetic Check-In (0-30 days)

**Subject:** How are things going without ConectaPay?

Hi [Name],

It's been [X] days since your account closed. I wanted to personally check in - how are things going?

I remember you were using our automation to recover [specific metric they achieved]. Without it, you might be leaving R$ [X] on the table every month.

We'd love to have you back. If you reactivate within the next 14 days, I can offer you **20% off for 6 months**.

Is there a specific issue that caused you to leave? I'd love to understand and fix it.

Best,
[Your Name]

---

#### Template 2: Feature Update (31-90 days)

**Subject:** We've built [feature] based on customer feedback

Hi [Name],

Since you've been gone, we've been hard at work improving ConectaPay based on feedback from customers like you.

**New features you missed:**
- [Feature 1] - [brief description, benefit]
- [Feature 2] - [brief description, benefit]
- [Feature 3] - [brief description, benefit]

These updates specifically address [pain point they might have had].

If you're ready to give ConectaPay another try, we'll waive the setup fee (R$ 500 value) and provide personalized training to get you up to speed on the new features.

Interested? Let's schedule a 15-minute call.

Best,
[Your Name]

---

#### Template 3: Competitive Win-Back (91-180 days)

**Subject:** ConectaPay vs [Competitor]: Why customers switch back

Hi [Name],

I noticed you've been using [Competitor]. While they're a solid option, many customers who try them come back to ConectaPay for three reasons:

1. **WhatsApp-native experience:** We're built specifically for Brazilian businesses using WhatsApp
2. **Pix integration:** Instant payments with 0% fees (most competitors charge 2-3%)
3. **Local support:** Portuguese-speaking team that understands Brazilian business

If you're not 100% satisfied with [Competitor], we'll make switching easy:
- 2 months free when you come back
- Dedicated migration specialist to transfer your data
- Training on features [Competitor] doesn't have

Is it worth a 15-minute conversation to compare?

Best,
[Your Name]

---

## 7. Retention Offers Framework

### 7.1 Retention Offer Hierarchy

Use offers in order of cost to ConectaPay (start with lowest cost):

| Tier | Offer Type | Cost to ConectaPay | Use When | Success Rate |
|------|------------|-------------------|----------|--------------|
| **Tier 1** | Service improvements (training, optimization) | Time only | Early stage risk | 60-70% |
| **Tier 2** | Feature unlocks (give access to higher plan features) | Minimal revenue impact | Feature gap identified | 50-60% |
| **Tier 3** | Extended payment terms (net 30 instead of net 15) | Cash flow timing | Cash flow issue | 40-50% |
| **Tier 4** | One-time credit (10-20% of one month) | Low revenue impact | First retention attempt | 35-45% |
| **Tier 5** | Discounted pricing (10-20% for 3-6 months) | Medium revenue impact | Tier 1-4 unsuccessful | 40-50% |
| **Tier 6** | Discounted pricing (25-40% for 6-12 months) | High revenue impact | Critical accounts only | 50-60% |
| **Tier 7** | Custom pricing/contract | Case-by-case | Strategic accounts | 60-80% |

### 7.2 Tier-Specific Authorization Matrix

| Offer Tier | Authorized By | Approval Required |
|------------|---------------|-------------------|
| Tier 1 | CSM | None |
| Tier 2 | Customer Success Lead | CSM recommendation |
| Tier 3 | Customer Success Lead | Finance review |
| Tier 4 | Customer Success Lead | None (up to R$ 500 credit) |
| Tier 5 | VP Customer Success | Finance approval |
| Tier 6 | VP Customer Success | CEO approval |
| Tier 7 | CEO | Board approval for strategic accounts |

### 7.3 Offer Validity Periods

| Offer Type | Validity Period | Rationale |
|------------|-----------------|-----------|
| All retention offers | 7-14 days | Create urgency, prevent indefinite discounting |
| Win-back offers (0-30 days churn) | 14 days | High urgency, customer still feels pain |
| Win-back offers (31-90 days churn) | 30 days | Medium urgency, needs more consideration |
| Custom contracts | 30 days | Legal review time needed |

### 7.4 Retention Offer Scripts

#### Script 1: Service Improvement (Tier 1)

"I hear you - [specific pain point]. Here's what I can do immediately:

1. I'll personally audit your automation setup and optimize it
2. I'll schedule a 1-hour training session for your team on [feature]
3. I'll create a custom [report/dashboard] to address [concern]

No cost to you - this is on me. Can we try this for 30 days and see if it solves the problem?"

#### Script 2: Feature Unlock (Tier 2)

"I understand you need [feature from higher plan]. I can't lower the price, but here's what I can do:

I'll give you access to [feature] at your current plan level for the next 3 months. If it delivers value, we can discuss moving to the higher plan. If not, you can downgrade without penalty.

Fair?"

#### Script 3: One-Time Credit (Tier 4)

"I hear your frustration with [specific issue]. While I can't change our pricing model, I want to make this right.

I'm applying a one-time credit of R$ [X] to your next invoice. This covers [Y] months of service.

This is my best offer - I can't do ongoing discounts, but I hope this shows we're committed to your success."

#### Script 4: Discounted Pricing (Tier 5)

"I want to keep you as a customer. Here's my best offer:

- [X]% discount for [Y] months
- After [Y] months, pricing returns to normal
- You're locked in at your current plan features

This offer is valid for 7 days. I can't do better than this - is there anything else holding you back?"

#### Script 5: Custom Pricing (Tier 7) - Executive Level

"You're a valued customer, and we want to make this work. Here's what I can propose:

- Custom pricing at R$ [X]/month (vs. current R$ [Y])
- 12-month commitment
- [Custom terms: payment schedule, cancellation clause, etc.]

This pricing is based on your [specific situation: volume, long-term potential, etc.].

I'll need to get this approved by our board. If you agree in principle, I can present this for approval and have a final contract to you within 48 hours."

---

## 8. Segment-Specific Tactics

### 8.1 Clínicas Médicas (Medical Clinics)

**Key Pain Points:**
- No-show appointments (revenue loss)
- Patient communication overhead
- Payment collection friction

**Risk Signals:**
- Drop in automated appointment reminders (50%+)
- Decrease in Pix payment collection rate
- Negative feedback about patient no-show reduction

**Retention Tactics:**

1. **ROI Demonstration**
   - Calculate: "You've saved R$ X in no-shows this month with ConectaPay"
   - Compare: Without automation, no-shows would cost R$ Y
   - Visual: Send monthly "No-Show Recovery Report"

2. **Feature-Specific Training**
   - Offer training on appointment reminder templates
   - Optimize reminder timing (24h vs 48h before)
   - A/B test message content to improve show-up rate

3. **Champion Identification**
   - Identify clinic manager or receptionist who uses the tool most
   - Make them the internal advocate
   - Provide "Champion Kit" with presentation to clinic owner

**Win-Back Offer:**
- "We've improved our no-show recovery feature - clinics using it see 30% fewer no-shows"
- Free setup of new automated reminder flows
- Case study: "How Clínica Saúde recovered R$ 8,000/month in no-show revenue"

### 8.2 Imobiliárias (Real Estate Agencies)

**Key Pain Points:**
- Lead response time (losing leads to competitors)
- Follow-up consistency (agents forgetting to follow up)
- Lead-to-visit conversion rate

**Risk Signals:**
- Increase in average lead response time (from <5 min to >30 min)
- Drop in automated follow-up sequences
- Agent adoption rate drops below 50%

**Retention Tactics:**

1. **Competitive Benchmarking**
   - "Top-performing agencies respond to leads in 3 minutes. Your average is 12 minutes - we can help you get to 5 minutes"
   - Show: "You're losing X leads per month to faster agencies"

2. **Agent Adoption Support**
   - Offer agent training webinars
   - Create "Quick Start Guide for Real Estate Agents"
   - Gamification: "Agent Leaderboard - who responds fastest?"

3. **Integration Optimization**
   - Integrate with their CRM (if not already)
   - Set up automatic lead sync
   - Reduce manual data entry

**Win-Back Offer:**
- "We've integrated with [major real estate CRM] - seamless lead management"
- Free migration of existing lead database
- Case study: "Imobiliária X increased lead conversion by 40% with ConectaPay"

### 8.3 Academias (Fitness Centers)

**Key Pain Points:**
- Member retention (churn)
- Payment collection (failed payments)
- Class booking automation

**Risk Signals:**
- Drop in automated payment collection success rate
- Decrease in class reminder automation
- Cancellation attributed to "automation not working"

**Retention Tactics:**

1. **Churn Reduction Focus**
   - Show: "Members who receive automated WhatsApp renewals stay 2.3x longer"
   - Implement: Automated win-back for members who don't renew
   - Report: Monthly "Member Recovery Report"

2. **Payment Success Optimization**
   - Set up automatic retry for failed payments (Pix and card)
   - Send payment reminders 48h before due date
   - Offer alternative payment methods

3. **Class Attendance Optimization**
   - Automate class reminders (2h before)
   - Automate waitlist notifications
   - Track attendance patterns for capacity planning

**Win-Back Offer:**
- "We've launched automated member win-back - academies see 15% higher retention"
- Free setup of payment retry automation
- Case study: "Academia Fit reduced failed payments by 60%"

### 8.4 Óticas (Optical Shops)

**Key Pain Points:**
- Appointment booking (eye exams)
- Frame readiness notifications
- Promotion distribution

**Risk Signals:**
- Drop in appointment booking automation
- Decrease in promotional message sends
- Negative feedback about delivery notifications

**Retention Tactics:**

1. **Appointment Efficiency**
   - Automate appointment confirmations and reminders
   - Reduce no-shows for eye exams (high-value appointments)
   - Send prep instructions (e.g., "Don't wear contacts to exam")

2. **Frame Pickup Optimization**
   - Automate "Your frames are ready!" notifications
   - Reduce pickup time from 14 days to 7 days average
   - Increase customer satisfaction

3. **Promotional Campaigns**
   - Targeted promotions based on purchase history
   - "Time for new lenses?" automation (12-month cycle)
   - Seasonal promotions (sunglasses summer, etc.)

**Win-Back Offer:**
- "We've added optical-specific templates for appointments and pickups"
- Free import of customer database for targeted campaigns
- Case study: "Ótica Vision increased repeat purchases by 35%"

---

## 9. Success Metrics and KPIs

### 9.1 At-Risk Account Management KPIs

| Metric | Definition | Target | Measurement Frequency |
|--------|------------|--------|----------------------|
| **Churn Rate** | Cancellations / Total customers | <5% monthly | Monthly |
| **At-Risk Recovery Rate** | At-risk accounts recovered / Total at-risk accounts | >60% | Monthly |
| **Early Identification Rate** | At-risk accounts identified before cancellation request | >80% | Monthly |
| **Average Risk Score** | Mean risk score across all customers | <25 | Weekly |
| **Risk Score Trend** | Week-over-week change in average risk score | Stable or decreasing | Weekly |
| **Time to Intervention** | Time from risk flag to first outreach | <48 hours | Weekly |
| **Intervention Success Rate** | Interventions resulting in risk score decrease | >70% | Monthly |
| **Win-Back Success Rate** | Churned customers reactivated / Win-back attempts | >25% | Quarterly |
| **Retention Offer Acceptance Rate** | Retention offers accepted / Offers made | >50% | Monthly |
| **NPS of At-Risk Accounts** | NPS score from customers in at-risk segment | >30 | Quarterly |

### 9.2 Process KPIs

| Metric | Definition | Target | Measurement Frequency |
|--------|------------|--------|----------------------|
| **Escalation Response Time** | Time from escalation request to response | <4 hours | Weekly |
| **Risk Score Update Frequency** | How often risk scores are recalculated | Weekly | Ongoing |
| **At-Risk Review Frequency** | How often CSMs review at-risk accounts | Weekly | Ongoing |
| **Intervention Documentation Rate** | Interventions with documented action plan | 100% | Monthly |
| **Post-Churn Interview Rate** | Exit interviews conducted / Total churn | >80% | Monthly |

### 9.3 Business Impact Metrics

| Metric | Definition | Target | Measurement Frequency |
|--------|------------|--------|----------------------|
| **Churn Revenue Saved** | ARR saved from at-risk account recoveries | R$ 50k+/month | Monthly |
| **Win-Back Revenue Recovered** | ARR recovered from win-back campaigns | R$ 20k+/quarter | Quarterly |
| **Retention Offer Cost** | Total cost of retention offers / ARR saved | <15% | Monthly |
| **Customer Lifetime Value (CLV)** | Average revenue per customer over lifetime | Increasing | Quarterly |
| **Net Revenue Retention (NRR)** | Revenue retained including expansion | >100% | Quarterly |

### 9.4 Dashboard and Reporting

**Weekly At-Risk Dashboard (for CSMs):**
- Top 20 at-risk accounts with risk scores
- Accounts requiring immediate intervention (score >60)
- Win-back opportunities this week
- Intervention success rate

**Monthly Executive Dashboard (for VP Customer Success):**
- Churn rate vs. target
- At-risk recovery rate
- Revenue saved from interventions
- Top 5 churn reasons (root cause analysis)
- Win-back campaign results

**Quarterly Business Review (for CEO/Board):**
- Churn trend (3-month and 12-month)
- At-risk account distribution (by segment, risk level)
- Retention offer ROI analysis
- Win-back program ROI
- Recommendations for process improvements

---

## 10. Tools and Templates

### 10.1 At-Risk Account Tracker Template

**Google Sheets / Airtable Structure:**

| Column | Description | Values |
|--------|-------------|--------|
| Account ID | Unique identifier | CON-XXX |
| Account Name | Customer name | [Name] |
| Segment | Business segment | Clínica / Imobiliária / Academia / Ótica |
| Current Risk Score | 0-100 | [Number] |
| Risk Level | Category | Low / Medium / High / Critical |
| Risk Trend | Direction | ↗ Increasing / ↘ Decreasing / → Stable |
| Primary Risk Signals | Top 3 reasons | [Signals] |
| Intervention Stage | Current stage | Stage 1 / 2 / 3 / 4 |
| Assigned CSM | Owner | [Name] |
| Last Contact Date | Most recent outreach | [Date] |
| Intervention Status | State | Not started / In progress / Successful / Unsuccessful |
| Retention Offer | Offer type (if any) | [Offer details] |
| Next Action Date | Scheduled follow-up | [Date] |
| Days in At-Risk | Duration at-risk | [Number] |
| Recovery Probability | Likelihood of retention | % |
| Notes | Detailed notes | [Text] |

### 10.2 Intervention Plan Template

**Account:** [Name]
**Risk Score:** [X] (High Risk)
**Date Flagged:** [Date]
**Assigned CSM:** [Name]

**Root Cause Analysis:**
- Primary Issue: [e.g., Price sensitivity]
- Secondary Issues: [e.g., Feature gap, service response time]
- Customer Quote: ["Direct quote from customer"]

**Intervention Plan:**
1. **Action:** [e.g., Schedule call with decision-maker]
   - Owner: [Name]
   - Due: [Date]
   - Status: [ ]

2. **Action:** [e.g., Prepare ROI report]
   - Owner: [Name]
   - Due: [Date]
   - Status: [ ]

3. **Action:** [e.g., Present retention offer]
   - Owner: [Name]
   - Due: [Date]
   - Status: [ ]

**Success Criteria:**
- [ ] Risk score decreases to <40 within 30 days
- [ ] Customer commits to 6-month renewal
- [ ] Usage increases by 20%+

**Follow-Up Schedule:**
- [ ] Day 7: Check-in call
- [ ] Day 14: Progress review
- [ ] Day 30: Final assessment

### 10.3 Win-Back Campaign Tracker Template

| Column | Description | Values |
|--------|-------------|--------|
| Account ID | Unique identifier | CON-XXX |
| Account Name | Customer name | [Name] |
| Churn Date | When account closed | [Date] |
| Days Since Churn | Days since closed | [Number] |
| Win-Back Segment | 0-30 / 31-90 / 91-180 days | [Segment] |
| Win-Back Attempt | Number of outreach attempts | [Number] |
| Last Contact Date | Most recent outreach | [Date] |
| Offer Made | Retention offer (if any) | [Offer details] |
| Response | Customer response | Positive / Negative / No response |
| Status | Current state | Contacting / Negotiating / Reactivated / Lost |
| Reactivation Date | If reactivated | [Date] |
| Notes | Detailed notes | [Text] |

### 10.4 Email Templates

#### Template 1: At-Risk Check-In (Stage 1)

**Subject:** Checking in - how's everything going?

Hi [Name],

I hope things are going well at [Company Name]!

I noticed that we haven't seen you using ConectaPay as much as usual over the past couple of weeks. Is everything okay?

Sometimes business priorities shift, or maybe there's a technical issue we can help with. Either way, I'm here to help.

Can we schedule a quick 15-minute call this week to catch up?

Best,
[Your Name]

---

#### Template 2: Risk Acknowledgment (Stage 2)

**Subject:** I've noticed some changes - let's talk

Hi [Name],

I'm writing because I've noticed some concerning signals with your account:

- [Signal 1: e.g., 60% drop in usage]
- [Signal 2: e.g., No logins for 3 weeks]
- [Signal 3: e.g., Recent support ticket about [issue]]

I want to make sure we're delivering the value you expected from ConectaPay. If something isn't working, I want to fix it.

Can we hop on a call this week to discuss? I have some ideas on how we can improve things for you.

Best,
[Your Name]

---

#### Template 3: Retention Offer (Stage 3)

**Subject:** I don't want to lose you as a customer

Hi [Name],

I heard that you're considering cancelling your account. Honestly, I don't want to see you go.

Based on our conversation, I understand that [primary reason for leaving]. Here's what I can do:

[Retention offer details - specific to their situation]

This offer is valid for 7 days. I really hope you'll accept it.

If there's anything else I can do to keep you as a customer, please let me know. Your success is important to me and to ConectaPay.

Best,
[Your Name]

---

#### Template 4: Cancellation Confirmation (Graceful Exit)

**Subject:** Your account has been cancelled

Hi [Name],

I've processed your cancellation request as of [date].

I'm sorry to see you go, but I respect your decision. Here's what happens next:

- Your account will remain active until [end of billing period]
- You can export your data by [date] from [link]
- After [date], your account will be closed

If things change in the future, we'd love to have you back. Customers who return within 90 days get [welcome-back offer].

Thank you for being a ConectaPay customer. I wish you and [Company Name] all the best.

Best,
[Your Name]

---

### 10.5 Call Scripts

#### Script 1: Discovery Call (Stage 1)

**Opening:**
"Hi [Name], thanks for taking the time to chat. I've noticed [change in behavior], and I wanted to check in - is everything okay with ConectaPay?"

**Listening Questions:**
- "How have things been going since we last spoke?"
- "What's working well for you?"
- "What's not working well?"
- "Have your priorities or business needs changed recently?"
- "Is there anything we could do better?"

**Closing:**
"Thanks for sharing that with me. Based on what you've said, I have a few ideas on how we can improve your experience. Can I put together a plan and send it over by [day]? Then we can review it together on a call next week."

---

#### Script 2: Root Cause Call (Stage 2)

**Opening:**
"Thanks for making time, [Name]. I'll be direct - we've identified some risk signals on your account, and I want to understand what's really going on so we can fix it."

**Diagnosis Questions:**
- "You mentioned [issue]. Can you tell me more about that?"
- "How is this impacting your business daily?"
- "What have you tried so far to solve it?"
- "What would an ideal solution look like for you?"
- "If we can't solve this, what's your Plan B?"

**Solution Proposal:**
"Based on what you've shared, here's what I propose:
- [Solution 1 - quick win]
- [Solution 2 - longer term]
- [Solution 3 - if applicable]

If we do these things, will it address your concerns?"

**Closing:**
"Let's implement [Solution 1] this week. I'll follow up with you on [day] to make sure it's working. Does that sound good?"

---

#### Script 3: Retention Negotiation (Stage 3)

**Opening:**
"[Name], I heard that you're planning to cancel. Before we process that, I want to understand - is there anything I can do to change your mind?"

**Understanding the Real Reason:**
- "What's the primary reason for leaving?"
- "Is it [price], or is there something else?"
- "If we could solve [issue], would you stay?"

**Making the Offer:**
"I hear you. Based on what you've said, here's what I can offer:
- [Offer details]

This is my best offer. I can't do better than this, but I really want to make this work."

**Closing the Deal:**
"If I send over the paperwork today, can you review it by [day]? I'd hate to lose you over this."

---

#### Script 4: Win-Back Call (Post-Churn)

**Opening:**
"Hi [Name], I know it's been a while since you used ConectaPay. I'm calling to check in - how have things been going without us?"

**Discovery:**
- "What are you using for [automation/payments/etc.] now?"
- "How is that working out?"
- "Do you miss anything from ConectaPay?"
- "What would make you consider coming back?"

**The Pitch:**
"Since you left, we've added [new features]. Customers are seeing [results]. If you come back, I can offer you [incentive]."

**Closing:**
"Can I send you some information about what's new? No pressure - just want you to know what you're missing."

---

### 10.6 Escalation Form Template

**Internal Use Only**

**Date:** [Date]
**Time:** [Time]
**Escalated By:** [Name, Role]
**Account:** [Name, CON-XXX]

**Escalation Reason:**
[ ] Cancellation requested
[ ] Risk score increased by 15+ points
[ ] Unable to reach decision-maker (5+ attempts)
[ ] Customer threat (negative review, competitor)
[ ] Payment issue unresolved (14+ days)
[ ] Other: [specify]

**Account Details:**
- **Current Risk Score:** [X]
- **Risk Level:** [Low/Medium/High/Critical]
- **ARR:** [R$ X]
- **Segment:** [Clínica/Imobiliária/Academia/Ótica]
- **Assigned CSM:** [Name]
- **Days in At-Risk:** [X]

**Attempts Made:**
1. [Date]: [Action] - [Result]
2. [Date]: [Action] - [Result]
3. [Date]: [Action] - [Result]

**Root Cause (Known or Suspected):**
[Hypothesis]

**Requested Action:**
[What you need from the escalatee]

**Urgency:**
[ ] Immediate (respond within 4 hours)
[ ] Today (respond within 8 hours)
[ ] This week (respond within 48 hours)

**Follow-Up Required By:** [Date/Time]

**Escalation Sent To:** [Name, Role]
**Notification Method:** [Email/Slack/Phone/In-person]

---

## Appendix A: Implementation Checklist

### Phase 1: Foundation (Week 1-2)

- [ ] Set up at-risk account tracking spreadsheet/database
- [ ] Configure automated risk detection triggers (usage, login, payment)
- [ ] Train CSMs on risk scoring system
- [ ] Create intervention playbook quick reference guide
- [ ] Set up weekly at-risk account review meetings

### Phase 2: Tools & Templates (Week 3-4)

- [ ] Build email templates in CRM/email tool
- [ ] Create call script cheat sheets for CSMs
- [ ] Set up escalation notification system (Slack/Email)
- [ ] Configure at-risk dashboard in analytics tool
- [ ] Test win-back email sequences

### Phase 3: Training & Rollout (Week 5-6)

- [ ] Conduct CSM training on all intervention stages
- [ ] Role-play retention negotiation scenarios
- [ ] Train Customer Success Lead on escalation procedures
- [ ] Train VP Customer Success on critical interventions
- [ ] Roll out to all customer accounts

### Phase 4: Optimization (Week 7-8)

- [ ] Review first month of at-risk account data
- [ ] Calculate success rates by stage and segment
- [ ] Identify bottlenecks in intervention process
- [ ] Adjust risk scoring thresholds if needed
- [ ] Document lessons learned and best practices

---

## Appendix B: Glossary

- **ARR (Annual Recurring Revenue):** Annualized revenue from subscriptions
- **Churn:** Customer cancellation or non-renewal
- **CSM (Customer Success Manager):** Account manager responsible for customer health
- **Health Score:** Overall customer satisfaction and engagement score
- **NPS (Net Promoter Score):** Customer loyalty metric (0-10 scale)
- **ROI (Return on Investment):** Financial return relative to investment
- **Soft Churn:** Customer discussing cancellation but not finalized
- **Hard Churn:** Cancellation confirmed, account closed
- **Win-Back:** Reactivating a churned customer
- **Retention Offer:** Incentive to prevent cancellation
- **Escalation:** Bringing in higher-level resources to address issue

---

## Appendix C: Related Documents

- Customer Retention Strategy Framework (#39)
- Customer Success Metrics and Health Score Dashboard System
- Customer Lifecycle Marketing and Nurture Programs (#53)
- Customer Journey Mapping and Experience Optimization (#48)
- Customer Onboarding Optimization and Time-to-Value (#174)

---

**Document Control**

- **Version:** 1.0
- **Author:** CMO Agent
- **Date Created:** April 26, 2026
- **Last Updated:** April 26, 2026
- **Next Review:** July 26, 2026
- **Approval Status:** Pending implementation
- **Distribution:** Customer Success Team, Account Managers, VP Customer Success

---

**End of Document**
