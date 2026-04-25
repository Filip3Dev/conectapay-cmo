# ConectaPay - Customer Feedback Loop and Voice of Customer Program
## Complete VoC System for Continuous Customer Learning

**Version**: 1.0
**Date**: April 25, 2026
**Author**: CMO Agent (55827422-a849-41d3-9286-0b5b8b002079)
**Task**: CON-107 - Customer Feedback Loop and Voice of Customer Program

---

## Executive Summary

This document defines ConectaPay's complete Voice of Customer (VoC) program—a systematic approach to collecting, analyzing, and acting on customer feedback to drive product decisions, improve customer experience, and reduce churn.

**Primary Objective**: Build a closed-loop feedback system where every customer insight is captured, analyzed, routed to the right team, acted upon, and communicated back to the customer.

**Target Metrics**:
| Metric | Month 3 | Month 6 | Month 12 |
|--------|---------|---------|----------|
| **Feedback Collection Rate** | 40% | 60% | 80% |
| **Analysis Response Time** | 7 days | 5 days | 3 days |
| **Action Closure Rate** | 60% | 75% | 90% |
| **Customer Notification Rate** | 50% | 70% | 90% |
| **NPS** | 40 | 50 | 60 |
| **Feedback-to-Feature Rate** | 5% | 10% | 15% |

**Key Insight**: Companies with mature VoC programs see 2.5x higher customer retention and 3x higher employee engagement. Feedback is not a cost center—it's a strategic asset.

---

# Part 1: VoC Program Philosophy

## The Feedback Flywheel

```
┌─────────────────────────────────────────────────────────────┐
│                    VOICE OF CUSTOMER FLYWHEEL                │
│                                                             │
│  COLLECT → ANALYZE → ROUTE → ACT → CLOSE LOOP → COLLECT     │
│    ↑                                                ↓        │
│    └──────────────── BETTER PRODUCT ←────────────────┘        │
│                                                             │
│  More Feedback → Better Insights → Better Product →         │
│  Happier Customers → More Feedback → ...                    │
└─────────────────────────────────────────────────────────────┘
```

**Core Principles**:

1. **Every Interaction is Feedback**
   - Support tickets, sales calls, churn reasons, feature requests
   - Social media mentions, review sites, in-app behavior
   - All data points are VoC data

2. **Close the Loop or Don't Collect**
   - Collecting feedback without acting creates customer resentment
   - If you can't/won't act, don't ask
   - Every customer who gives feedback deserves a response

3. **VoC is Everyone's Job**
   - Product: Feature prioritization, roadmap validation
   - Marketing: Messaging refinement, content creation
   - Customer Success: Health management, churn prevention
   - Sales: Objection handling, competitive intelligence
   - Engineering: Bug prioritization, UX improvements

4. **Quantify Everything**
   - Not just "customers want X"
   - "23% of customers mentioned X, representing R$ 45K ARR"
   - ROI of acting vs. not acting

---

# Part 2: Feedback Collection Architecture

## The 10 Feedback Collection Channels

### Channel 1: In-App Microsurveys (Passive)

**Trigger**: After key actions

| Trigger | Survey Type | Timing | Response Target |
|---------|-------------|--------|-----------------|
| Signup completed | CSAT (1 question) | Instant | 80%+ |
| First automation created | CES (1 question) | Instant | 70%+ |
| First recovery achieved | Delight (1 question) | Instant | 60%+ |
| Support ticket closed | CSAT (3 questions) | 1 hour | 50%+ |
| Feature used 5x times | PSS (Feature-specific) | Instant | 40%+ |
| Churn initiated | Exit survey (5 questions) | Instant | 30%+ |

**Survey Types**:
- **CSAT** (Customer Satisfaction): "How satisfied are you with [X]?" (1-5 stars)
- **CES** (Customer Effort Score): "How easy was it to [X]?" (1-7 scale)
- **PSS** (Product-Specific Score): "How useful is [feature]?" (1-10 scale)
- **NPS** (Net Promoter Score): "How likely to recommend?" (0-10 scale)

**In-App Survey Template**:
```
┌─────────────────────────────────────┐
│  🎉 Parabéns! Sua primeira venda     │
│     foi recuperada com sucesso!     │
│                                     │
│  Em uma escala de 1 a 5, quão       │
│  satisfeito você está com este      │
│  resultado?                         │
│                                     │
│  ⭐⭐⭐⭐⭐                          │
│                                     │
│  [ENVIAR]    [Talvez depois]        │
└─────────────────────────────────────┘
```

**Success Metric**: 40%+ average response rate across all in-app surveys

---

### Channel 2: Email Surveys (Active)

**Cadence**: Strategic touchpoints, not spam

| Timing | Survey Type | Audience | Response Target |
|--------|-------------|----------|-----------------|
| Day 7 post-signup | Onboarding NPS | All new customers | 40%+ |
| Day 30 post-signup | Product NPS | All customers | 35%+ |
| Day 90 post-signup | Relationship NPS | All customers | 30%+ |
| Quarterly (Q1, Q2, Q3, Q4) | Comprehensive NPS | All customers | 25%+ |
| Post-churn (30 days) | Win-back survey | Churned customers | 15%+ |

**Email Survey Template (Day 30 NPS)**:
```
Subject: Uma pergunta rápida sobre sua experiência

Olá [Nome],

Você está usando o ConectaPay há 30 dias. Queremos saber:
Como está sendo sua experiência?

Em uma escala de 0 a 10, qual a probabilidade de você
recomendar o ConectaPay para um colega?

[0 1 2 3 4 5 6 7 8 9 10]

Por que você deu essa nota? (opcional)
[Open text field - 500 char limit]

O que precisaríamos fazer para melhorar sua experiência?
[Open text field - 500 char limit]

[ENVIAR FEEDBACK]

Obrigado por sua opinião. Ela nos ajuda a melhorar.
Equipe ConectaPay
```

**Success Metric**: 30%+ average email open rate, 25%+ response rate

---

### Channel 3: Customer Interviews (Deep Dive)

**Frequency**: Ongoing, not campaign-based

| Interview Type | Cadence | Duration | Participants | Frequency |
|----------------|---------|----------|--------------|------------|
| Onboarding interview | Day 14-30 | 30 min | 5/month | Weekly |
| Quarterly check-in | Every 90 days | 45 min | 10/month | Weekly |
| Churn interview | Upon churn | 30 min | All churned | Real-time |
| Feature validation | Pre-build | 30 min | 10/feature | Ad-hoc |
| Strategic advisory | Quarterly | 60 min | CAB (12) | Quarterly |

**Interview Template** (Day 30 Onboarding):
```
Part 1: Warm-up (5 min)
- "Como você conheceu o ConectaPay?"
- "Qual era seu maior problema antes de nós?"

Part 2: Experience (15 min)
- "Conte sobre sua experiência de setup (0-10)"
- "O que foi mais fácil? Mais difícil?"
- "Qual recurso você mais usa? Por quê?"
- "O que você NÃO usa? Por quê?"

Part 3: Value (5 min)
- "Você já recuperou vendas? Quantas? Qual valor?"
- "O ConectaPay vale o investimento? Por quê?"

Part 4: Future (5 min)
- "Se você fosse o CEO do ConectaPay por um dia, o que mudaria?"
- "Qual recurso sonhado você gostaria que tivéssemos?"

Closing: "Podemos entrar em contato quando implementarmos suas sugestões?"
```

**Success Metric**: 10 interviews/month minimum, 95% transcription rate

---

### Channel 4: Support Ticket Analysis (Passive)

**Data Source**: All customer interactions with support

**Analysis Dimensions**:

| Dimension | What to Track | Frequency | Report To |
|-----------|---------------|-----------|-----------|
| **Topic Classification** | Bug, feature request, billing, UX, how-to | Daily | Product, Engineering |
| **Sentiment Analysis** | Positive, neutral, negative (AI-scored) | Daily | CS Leadership |
| **Recurring Issues** | Top 10 issues mentioned | Weekly | All Teams |
| **Feature Requests** | Aggregated by feature + count | Weekly | Product |
| **Churn Signals** | Keywords: "cancelar", "caro", "não funciona" | Real-time | CS Leadership |

**Support Ticket Tagging Schema**:
```
Category: [Bug] [Feature] [Billing] [UX] [How-To] [Performance]
Subcategory: [API] [Integrations] [Mobile] [Web] [Billing-Portal]
Sentiment: [Positive] [Neutral] [Negative] [Frustrated]
Urgency: [P1-Critical] [P2-High] [P3-Medium] [P4-Low]
Feature Request: [Feature-Name] (if applicable)
```

**Weekly Support Insights Report**:
```
Week of [DATE]

Total Tickets: [X]
Response Time: [X] hours (target: <4 hours)
Resolution Time: [X] hours (target: <24 hours)

Top 5 Issues:
1. [Issue] - [X] tickets - [Sentiment] - [Owner]
2. [Issue] - [X] tickets - [Sentiment] - [Owner]
...

Feature Requests (Top 10):
1. [Feature] - [X] requests - [X% of customers]
2. [Feature] - [X] requests - [X% of customers]
...

Churn Risk Alerts:
- [X] customers flagged (sentiment negative + churn keywords)
- [X] reached out for save attempts

Action Items:
- [ ] [Team]: [Action] - [Owner] - [Due Date]
```

**Success Metric**: 100% of tickets tagged, weekly report published

---

### Channel 5: Sales Call Intelligence (Active)

**Data Source**: Sales call recordings, notes, CRM entries

**Capture Framework**:

| Question Type | What to Capture | Frequency | Report To |
|---------------|-----------------|-----------|-----------|
| **Objections** | Price, features, competitor, timing | Every call | Sales, Marketing |
| **Pain Points** | Specific problems mentioned | Every call | Product, Marketing |
| **Competitor Mentions** | Which competitors, what features | Every call | Product, Marketing |
| **Feature Requests** | "If you had X, I'd buy" | Every call | Product |
| **Buying Criteria** | What made them decide | Won deals | Sales, Marketing |
| **Churn Reasons** | Why they didn't buy | Lost deals | Sales, Product |

**Sales Call VoC Template** (CRM field):
```
CUSTOMER FEEDBACK SUMMARY

Pain Points Mentioned:
- [ ] No-shows cost R$ [X]/month
- [ ] Leads ghost after first contact
- [ ] Payment collection issues
- [ ] Manual follow-up is time-consuming
- [ ] Other: _______________

Objections:
- [ ] Price: R$ [X] is too expensive
- [ ] Features: Missing [feature]
- [ ] Competitor: [Competitor] has [feature]
- [ ] Timing: Not right now
- [ ] Other: _______________

Competitor Mentions:
- [ ] [Competitor]: They said _______________
- [ ] [Competitor]: They said _______________

Feature Requests:
1. [Feature description]
2. [Feature description]

Key Quote (Customer's Words):
"[Quote]"

Would Buy If:
[ ] Price was R$ [X]
[ ] Had [feature]
[ ] [Other condition]
```

**Weekly Sales VoC Report**:
```
Week of [DATE]

Calls: [X] | Demos: [X] | Won: [X] | Lost: [X]

Top 5 Objections (Lost Deals):
1. [Objection] - [X]% of lost deals - [Counter-argument]
2. [Objection] - [X]% of lost deals - [Counter-argument]
...

Top 5 Pain Points (All Deals):
1. [Pain] - [X]% of deals mentioned - [Messaging angle]
2. [Pain] - [X]% of deals mentioned - [Messaging angle]
...

Feature Requests (Top 10):
1. [Feature] - [X] requests - [X] said "would buy if had this"
2. [Feature] - [X] requests - [X] said "would buy if had this"
...

Competitor Mentions:
- [Competitor]: [X] mentions - Feature: [feature] - [X]% won anyway
- [Competitor]: [X] mentions - Feature: [feature] - [X]% won anyway

Action Items:
- [ ] [Team]: [Action] - [Owner] - [Due Date]
```

**Success Metric**: 100% of sales calls logged with VoC data

---

### Channel 6: Churn Analysis (Passive)

**Data Source**: Exit surveys, churn interviews, cancellation reasons

**Churn Reason Taxonomy**:

| Category | Subcategory | Root Cause | Preventable? |
|----------|-------------|------------|--------------|
| **Price** | Too expensive | Price > value perceived | Yes (demonstrate value) |
| **Price** | Competitor cheaper | Competitor lower price | Yes (value differentiation) |
| **Product** | Missing feature | Need X to do job | Yes (roadmap) |
| **Product** | Poor UX | Hard to use | Yes (UX improvements) |
| **Product** | Technical issues | Bugs, downtime | Yes (fix bugs) |
| **Service** | Poor support | Slow/unhelpful support | Yes (CS training) |
| **Business** | Closed down | Company out of business | No |
| **Business** | Changed strategy | No longer need this | Maybe (pivot) |
| **Unknown** | No response | Didn't provide reason | No (uncontactable) |

**Exit Interview Template** (Phone/Zoom):
```
Introduction (2 min):
"Obrigado por usar o ConectaPay. Lamentos ver você partir.
Esta conversa de 30 min nos ajuda a melhorar para outros clientes."

Questions (25 min):
1. "O que motivou sua decisão de cancelar?"
   [Probe deeper: "What was the final straw?"]

2. "Se pudéssemos fazer uma coisa para você ficar, o que seria?"
   [This is the #1 insight]

3. "Como você nos descreveria para um colega?"
   [Test brand perception]

4. "O que você mais gostou no ConectaPay?"
   [Keep doing this]

5. "O que você menos gostou?"
   [Fix this]

6. "Você considerou outras opções? Qual? Por que escolheu elas?"
   [Competitive intelligence]

7. "Em que situação você voltaria a ser cliente?"
   [Win-back signals]

8. "O que mais você gostaria de dizer?"
   [Open mic]

Closing (3 min):
"Obrigado por sua honestidade. Vamos compartilhar isso com o time de produto.
Se mudar de ideia, você é sempre bem-vindo de volta."
```

**Monthly Churn Report**:
```
Month: [DATE]

Total Churn: [X] customers | [X]% churn rate

Churn by Category:
- Price: [X]% ([X] customers)
- Product (Missing Feature): [X]% ([X] customers)
- Product (Poor UX): [X]% ([X] customers)
- Product (Technical): [X]% ([X] customers)
- Service (Poor Support): [X]% ([X] customers)
- Business (Closed): [X]% ([X] customers)
- Unknown: [X]% ([X] customers)

Preventable Churn: [X]%

Top 5 Reasons (with counts):
1. [Reason] - [X] customers - [X]% of churn
2. [Reason] - [X] customers - [X]% of churn
...

Feature Requests from Churned Customers:
1. [Feature] - [X] requests - [X] said "would stay if had this"
2. [Feature] - [X] requests - [X] said "would stay if had this"
...

Competitor Switching:
- [Competitor]: [X] customers switched - Reason: [reason]
- [Competitor]: [X] customers switched - Reason: [reason]

Win-Back Opportunities:
- [X] customers said they'd return if [condition]
- [X] customers open to re-engagement in 30 days

Action Items:
- [ ] [Team]: [Action] - [Owner] - [Due Date]
```

**Success Metric**: 80%+ of churned customers complete exit interview

---

### Channel 7: Social Media Listening (Passive)

**Data Sources**: LinkedIn, Instagram, Facebook, Twitter/X, YouTube, Reddit, review sites (Google Maps, Trustpilot, Capterra)

**Monitoring Tools**:
- Free: Google Alerts, Mention.com (free tier), Social Search
- Paid: Brandwatch, Sprout Social, Hootsuite Insights

**Listen For**:

| Signal Type | Examples | Response Time | Owner |
|-------------|----------|---------------|-------|
| **Mentions** | @ConectaPay, #ConectaPay | <4 hours | CS/Social |
| **Sentiment Spikes** | Sudden negative/positive trends | <1 hour | Executive |
| **Viral Content** | Post with 10K+ impressions | <2 hours | Marketing |
| **Competitor Mentions** | Competitors mentioned with us | Weekly | Marketing |
| **Industry Trends** | Topics: "automação WhatsApp", "no-show" | Weekly | Product |
| **Reviews** | Google, Trustpilot, Capterra | <24 hours | CS |

**Social VoC Template** (for tracking):
```
Platform: [LinkedIn/Instagram/etc.]
Date: [DATE]
Post/Tweet/Review: [Link]
Author: [Name] ([Type: Customer/Prospect/Influencer/Other])
Sentiment: [Positive/Neutral/Negative]
Reach: [X] impressions | [X] engagements
Topic: [No-shows/Leads/Payments/Support/Price/Feature]
Key Quote: "[Quote]"
Action Taken: [Responded/Forwarded/Nothing]
Owner: [Name]
Status: [Open/Closed]
```

**Weekly Social Listening Report**:
```
Week of [DATE]

Total Mentions: [X] | Sentiment: [X]% Positive

Top 5 Topics:
1. [Topic] - [X] mentions - [Sentiment] - [Example quote]
2. [Topic] - [X] mentions - [Sentiment] - [Example quote]
...

Sentiment Trend:
- Week 1: [X]% positive
- Week 2: [X]% positive
- Week 3: [X]% positive
- Week 4: [X]% positive
- Direction: [↗️ Improving / ↘️ Declining / → Stable]

Viral Content:
- [Post] - [X] impressions - [X]% engagement - [Action]

Review Sites:
- Google Maps: [X]/5 stars ([X] reviews) - [Last review summary]
- Trustpilot: [X]/5 stars ([X] reviews) - [Last review summary]
- Capterra: [X]/5 stars ([X] reviews) - [Last review summary]

Action Items:
- [ ] [Team]: [Action] - [Owner] - [Due Date]
```

**Success Metric**: <4 hour response time to all mentions, 0 viral negative posts unaddressed

---

### Channel 8: App Store & Review Sites (Passive)

**Data Sources**:
- **Mobile**: Apple App Store, Google Play Store (if mobile app exists)
- **Software**: Capterra, G2, Software Advice, GetApp
- **Brazilian**: Kekanto, Apontador, Google Meu Negócio

**Track**:

| Metric | Current | Target | Frequency |
|--------|---------|--------|-----------|
| Overall Rating | [X]/5 | 4.5+/5 | Weekly |
| Review Count | [X] | 100+ | Weekly |
| Response Rate | [X]% | 100% | Weekly |
| Response Time | [X] hours | <24 hours | Weekly |

**Review Response Templates**:

**5-Star Review**:
```
Obrigado, [Nome]! 😊

Ficamos felizes em saber que está tendo ótimos resultados com o ConectaPay.
Se conhecer alguém que também precisa recuperar vendas, indicamos a gente!

Abraço,
Equipe ConectaPay
```

**4-Star Review (with suggestions)**:
```
Obrigado pelo feedback, [Nome]! 🙏

Que bom que está gostando do ConectaPay!
Sobre [sugestão]: Já passamos isso para o time de produto.
Vamos te avisar quando implementarmos.

Abraço,
Equipe ConectaPay
```

**3-Star or Lower**:
```
Obrigado pelo feedback, [Nome].

Sinto muito que sua experiência não foi 100% positiva.
Gostaria de entender melhor o que aconteceu para podermos ajudar.

Pode responder aqui ou chamar no WhatsApp: [LINK]

Abraço,
[CSM Name]
Equipe ConectaPay
```

**Monthly Review Analysis Report**:
```
Month: [DATE]

Total Reviews: [X] | Average Rating: [X]/5

Rating Distribution:
⭐⭐⭐⭐⭐: [X] reviews ([X]%)
⭐⭐⭐⭐: [X] reviews ([X]%)
⭐⭐⭐: [X] reviews ([X]%)
⭐⭐: [X] reviews ([X]%)
⭐: [X] reviews ([X]%)

Top 5 Praise Points:
1. [Topic] - [X] reviews mentioned
2. [Topic] - [X] reviews mentioned
...

Top 5 Complaint Points:
1. [Topic] - [X] reviews mentioned - [Owner: [Team]]
2. [Topic] - [X] reviews mentioned - [Owner: [Team]]
...

Feature Requests from Reviews:
1. [Feature] - [X] requests
2. [Feature] - [X] requests

Action Items:
- [ ] [Team]: [Action] - [Owner] - [Due Date]
```

**Success Metric**: 4.5+/5 average rating, 100% response rate, <24 hour response time

---

### Channel 9: Behavioral Data (Passive)

**Data Source**: In-app analytics, usage patterns

**What Behavior Says**:

| Behavior | Insight | Action |
|----------|---------|--------|
| **Feature Adoption** | Which features are used/ignored | Product investment |
| **Drop-off Points** | Where users abandon flows | UX improvements |
| **Power User Patterns** | How top 10% use the product | Best practices, templates |
| **Churn Precursors** | Behaviors before churn | Early warning, intervention |
| **Aha Moments** | Behaviors correlated with retention | Optimize for early adoption |

**Behavioral VoC Framework**:

**Feature Adoption Tracking**:
```
Feature Name: [Feature]
Total Users: [X]
Users Who Used: [X] ([X]%)
Used 5+ Times: [X] ([X]% of users)
Used 10+ Times: [X] ([X]% of users)
Adoption Rate Trend: [↗️ Growing / ↘️ Declining / → Stable]

Correlation with Retention:
- Users who use this feature retain at [X]%
- Users who don't use this feature retain at [X]%
- Impact: [X] percentage points

Conclusion: [This is a retention driver / This is unused / This needs improvement]

Action: [Keep investing / Deprecate / Improve UX / Add training]
```

**Drop-off Analysis**:
```
Flow: [Flow Name - e.g., Onboarding, Campaign Creation]

Step 1: [Action] - [X]% complete
Step 2: [Action] - [X]% complete ([X]% drop-off)
Step 3: [Action] - [X]% complete ([X]% drop-off)
Step 4: [Action] - [X]% complete ([X]% drop-off)

Biggest Drop-off: Step [X] - [X]% of users abandon here

Hypothesis: [Why they drop off]

Validation: [Survey users who dropped off]

Action: [Fix flow / Add guidance / Remove friction]
```

**Power User Pattern Mining**:
```
Top 10% Users (by revenue recovered):

Common Behaviors:
- [X]% use [Feature A] (vs [X]% of all users)
- [X]% use [Feature B] (vs [X]% of all users)
- [X]% created [X]+ automations (vs [X]+ for all users)
- [X]% sent [X]+ messages (vs [X]+ for all users)

Conclusion: Power users do [X], [Y], [Z]

Action: Teach all new users to do [X], [Y], [Z] in onboarding
```

**Churn Precursor Analysis**:
```
Churned Customers ([X] total):

Behaviors in 30 days before churn:
- [X]% decreased usage by >50%
- [X]% had 0 successful automations
- [X]% had [X]+ support tickets
- [X]% logged in <5 times
- [X]% never used [Feature]

Predictive Model:
If customer shows [X] + [Y] + [Z] → [X]% churn risk

Action: Create alert when customers show these behaviors
```

**Success Metric**: 100% of users tracked, monthly behavioral insights report

---

### Channel 10: Advisory Board (Active)

**Purpose**: Strategic guidance from top customers

**Structure**:
- **Size**: 12 customers (by invitation only)
- **Criteria**: 6+ months tenure, Pro plan, NPS 60+, advocate
- **Term**: 12 months (renewable)
- **Compensation**: Free Pro plan + early feature access + annual event

**Cadence**:
- **Quarterly Meetings**: 2 hours, virtual
- **Quarterly Surveys**: Strategic priorities (15 min)
- **Ad-hoc Feedback**: Beta testing, feature validation

**Meeting Agenda**:
1. Product roadmap preview (30 min)
   - "Here's what we're planning next quarter"
   - "What do you think?"

2. Strategic priorities discussion (45 min)
   - "What are YOUR biggest challenges?"
   - "Where should we invest?"

3. Feature feedback (30 min)
   - "Here's a feature we're building"
   - "Does this solve your problem?"

4. Open Q&A (15 min)
   - "Anything else?"

**Advisory Board Application Template**:
```
ConectaPay Customer Advisory Board

Nome: [Nome]
Empresa: [Empresa]
Tempo como cliente: [X] meses
Plano: [Starter/Pro]

Por que você quer participar?
[Open text]

Quais são seus 3 maiores desafios hoje?
1. [Desafio]
2. [Desafio]
3. [Desafio]

Se você fosse o CEO do ConectaPay por um dia,
o que você mudaria primeiro?
[Open text]

Compromissos:
- [ ] Participar de 4 reuniões virtuais por ano (2 horas cada)
- [ ] Fornecer feedback honesto e construtivo
- [ ] Testar recursos beta antes do lançamento
- [ ] Participar de 1 pesquisa por trimestre

Benefícios:
- [X] Plano Pro gratuito enquanto estiver no conselho
- [X] Acesso antecipado a novos recursos
- [X] Influência direta no roadmap do produto
- [X] Evento anual exclusivo para membros (em São Paulo)

Enviar para: cab@conectapay.com.br
```

**Quarterly CAB Report**:
```
Quarter: [Q1 2026]

Attendees: [X]/12 ([X]% attendance)

Agenda Items Discussed:
1. [Topic] - Consensus: [Agreement/Disagreement] - Action: [Action]
2. [Topic] - Consensus: [Agreement/Disagreement] - Action: [Action]
...

Feature Validations:
- [Feature]: [X]% said "build this now" → [Priority: High]
- [Feature]: [X]% said "build this later" → [Priority: Medium]
- [Feature]: [X]% said "don't build this" → [Priority: Low]

Strategic Priorities Identified:
1. [Priority] - [X]% of members mentioned - [Owner: [Team]]
2. [Priority] - [X]% of members mentioned - [Owner: [Team]]
...

Action Items:
- [ ] [Team]: [Action] - [Owner] - [Due Date]
```

**Success Metric**: 80%+ CAB meeting attendance, 100% of feedback addressed

---

# Part 3: Feedback Analysis Framework

## Thematic Coding System

### Category Taxonomy

```
Level 1: 6 Main Categories
├── Product (Features, UX, Performance)
├── Price (Pricing, Plans, Discounts)
├── Service (Support, Onboarding, CS)
├── Billing (Invoicing, Payments, Refunds)
├── Technical (Bugs, Downtime, Integration)
└── Market (Competitors, Industry Trends)

Level 2: 30 Subcategories (5 per category)
├── Product: [Missing Feature], [Poor UX], [Feature Request], [Enhancement], [Removal Request]
├── Price: [Too Expensive], [Competitor Cheaper], [Value Misalignment], [Plan Limitations], [Discount Request]
├── Service: [Slow Response], [Unhelpful], [Rude], [Language Barrier], [Availability]
├── Billing: [Invoice Issues], [Payment Failed], [Refund Request], [Transparency], [Currency]
├── Technical: [Bug], [Downtime], [Integration Failed], [Performance], [Data Loss]
└── Market: [Competitor Mention], [Industry Shift], [Regulatory Change], [Alternative Solution], [Partnership]

Level 3: Specific Tags (unlimited)
├── e.g., [WhatsApp API], [Pix Integration], [Campaign Builder], [Analytics Dashboard], [Mobile App]
└── e.g., [R$ 297/month], [Annual Plan], [Startup Discount], [Education Pricing]
```

### Sentiment Analysis

**5-Point Scale**:
- **+2 (Very Positive)**: "Amazing!", "Love it!", "Best decision ever"
- **+1 (Somewhat Positive)**: "Good", "Helpful", "Works well"
- **0 (Neutral)**: "It's okay", "Fine", "No strong feelings"
- **-1 (Somewhat Negative)**: "Could be better", "Not great", "Disappointed"
- **-2 (Very Negative)**: "Terrible!", "Hate it!", "Worst mistake"

**Sentiment Scoring by Channel**:
| Channel | Positive Weight | Negative Weight | Reason |
|---------|----------------|-----------------|--------|
| In-app microsurvey | 1x | 2x | Negative = churn risk |
| Email NPS | 1x | 1x | Balanced feedback |
| Customer interview | 2x | 2x | Deep insights |
| Support ticket | 1x | 3x | Very negative = urgent |
| Sales call | 2x | 2x | Buying signals |
| Churn interview | 1x | 2x | Exit insights |
| Social media | 3x | 5x | Public sentiment |
| Reviews | 2x | 3x | Public record |
| Behavioral data | 2x | 1x | Actions > words |
| Advisory board | 3x | 3x | Strategic insight |

### Priority Scoring System

**VoC Priority Score (0-100)**:
```
Priority Score = (Frequency × 20) + (Impact × 30) + (Urgency × 25) + (Feasibility × 25)

Frequency (0-100):
- 100: 50+ customers mentioned in 30 days
- 80: 30-49 customers mentioned in 30 days
- 60: 20-29 customers mentioned in 30 days
- 40: 10-19 customers mentioned in 30 days
- 20: 5-9 customers mentioned in 30 days
- 10: 1-4 customers mentioned in 30 days

Impact (0-100):
- 100: Affects 100% of customers, mission-critical
- 80: Affects 50%+ of customers, high impact
- 60: Affects 20-49% of customers, medium impact
- 40: Affects 5-19% of customers, low impact
- 20: Affects <5% of customers, minimal impact

Urgency (0-100):
- 100: Churning customers, revenue loss, PR crisis
- 80: High churn risk, competitive disadvantage
- 60: Medium churn risk, customer frustration
- 40: Low churn risk, mild annoyance
- 20: No urgency, nice-to-have

Feasibility (0-100):
- 100: Quick win (<1 week, low cost, high confidence)
- 80: Easy (1-4 weeks, medium cost, high confidence)
- 60: Medium (1-3 months, medium cost, medium confidence)
- 40: Hard (3-6 months, high cost, medium confidence)
- 20: Very Hard (6+ months, very high cost, low confidence)
```

**Priority Matrix**:
```
HIGH IMPACT + HIGH FEASIBILITY = DO NOW (80-100 points)
HIGH IMPACT + LOW FEASIBILITY = PLAN (60-79 points)
LOW IMPACT + HIGH FEASIBILITY = QUICK WIN (40-59 points)
LOW IMPACT + LOW FEASIBILITY = BACKLOG (0-39 points)
```

---

## Weekly VoC Analysis Meeting

**Attendees**: CMO, Head of Product, Head of CS, Head of Sales (30 min, every Monday)

**Agenda**:

1. **Review Last Week's Feedback** (5 min)
   - Total feedback received: [X]
   - Top 3 themes: [Theme 1], [Theme 2], [Theme 3]
   - Sentiment trend: [↗️ Improving / ↘️ Declining / → Stable]

2. **Deep Dive on Top 3 Issues** (15 min, 5 min each)
   - Issue: [Name]
   - Frequency: [X] customers mentioned
   - Impact: [X]% of customers affected
   - Sentiment: [Positive/Negative/Mixed]
   - Priority Score: [X]/100
   - Owner: [Team]
   - Action: [What we're doing]
   - Timeline: [When]

3. **Close the Loop Updates** (5 min)
   - [X] items completed last week
   - [X] customers notified
   - [X] items still in progress

4. **Assign This Week's Actions** (5 min)
   - [ ] [Team]: [Action] - [Owner] - [Due Date]
   - [ ] [Team]: [Action] - [Owner] - [Due Date]
   - ...

**Weekly VoC Summary Email** (sent to all company):
```
Subject: Weekly VoC Summary - Week of [DATE]

Hi Team,

Here's what customers told us last week:

📊 Feedback Received: [X] customers
📈 Sentiment: [X]% positive (↗️ +[X]% from last week)
🎯 Top 3 Issues:
1. [Issue] - [X] customers - [Owner: [Name]]
2. [Issue] - [X] customers - [Owner: [Name]]
3. [Issue] - [X] customers - [Owner: [Name]]

✅ Closed the Loop:
- [Feature/Improvement] - [X] customers notified
- [Feature/Improvement] - [X] customers notified

🚧 In Progress:
- [Feature/Improvement] - ETA: [Date] - [X] customers waiting

📋 This Week's Actions:
- [ ] [Team]: [Action] - [Owner]
- [ ] [Team]: [Action] - [Owner]

Keep the feedback coming!

CMO Team
```

---

# Part 4: Feedback Routing System

## Team Responsibilities

### Product Team
**Receives**:
- Feature requests (all channels)
- UX feedback (in-app, interviews, reviews)
- Product improvement suggestions
- Competitive intelligence (sales, churn)

**Responsible For**:
- Roadmap prioritization
- Feature design and build
- UX improvements
- A/B testing new features

**Response SLA**: Acknowledge within 7 days, act within 90 days (if approved)

**Feedback → Product Pipeline**:
```
Request → Review (Product Manager) → Prioritize (Roadmap Meeting) →
Design (Product Designer) → Build (Engineering) → Test (QA) →
Launch (Product Marketing) → Notify Customers (CS)
```

---

### Marketing Team
**Receives**:
- Messaging feedback (sales calls, social media)
- Content suggestions (customers asking for X)
- Objections (sales, churn)
- Brand perception (reviews, interviews)

**Responsible For**:
- Messaging refinement
- Content creation
- Objection handling materials
- Brand positioning

**Response SLA**: Acknowledge within 3 days, act within 30 days

**Feedback → Marketing Pipeline**:
```
Request → Review (Marketing Lead) → Validate (A/B Test) →
Implement (Update Content) → Measure (Performance) →
Report (Results)
```

---

### Customer Success Team
**Receives**:
- Onboarding friction (interviews, in-app)
- Support issues (tickets, sentiment)
- Churn risk (behavioral, sentiment)
- Customer training needs

**Responsible For**:
- Customer health management
- Churn prevention
- Customer education
- Support quality

**Response SLA**: Acknowledge within 24 hours, act within 7 days

**Feedback → CS Pipeline**:
```
Request → Review (CSM) → Classify (Health Impact) →
Intervene (Save/Risk Mitigation) → Monitor (Health Check) →
Close Loop (Notify Customer)
```

---

### Sales Team
**Receives**:
- Objections (sales calls)
- Competitive intelligence (churn, sales)
- Buying criteria (won deals)
- Lost deal reasons

**Responsible For**:
- Objection handling scripts
- Competitive battle cards
- Sales collateral updates
- Win/loss analysis

**Response SLA**: Acknowledge within 3 days, act within 14 days

**Feedback → Sales Pipeline**:
```
Request → Review (Sales Lead) → Validate (Top 5 Objections) →
Create (Collateral/Script) → Distribute (Sales Team) →
Train (Role Play) → Measure (Win Rate)
```

---

### Engineering Team
**Receives**:
- Bug reports (support, in-app)
- Performance issues (support, behavioral)
- Integration requests (sales, advisory board)
- Technical debt (internal metrics)

**Responsible For**:
- Bug fixes
- Performance optimization
- API/integration development
- Technical stability

**Response SLA**: Acknowledge within 24 hours, fix within 14 days (P1), 30 days (P2)

**Feedback → Engineering Pipeline**:
```
Request → Review (Tech Lead) → Triage (Severity) →
Schedule (Sprint) → Build (Developer) → Test (QA) →
Deploy (Release) → Verify (Customer)
```

---

## Escalation Matrix

**When Feedback Crosses Teams**:

| Scenario | Primary Owner | Escalation Path | SLA |
|----------|---------------|-----------------|-----|
| **Feature Request + Pricing** | Product → Marketing | Product Lead + CMO | 7 days |
| **Bug + Churn Risk** | Engineering → CS | Tech Lead + CS Lead | 24 hours |
| **Competitor Loss** | Sales → Product | Sales Lead + Product Lead | 3 days |
| **PR Crisis (Viral Negative)** | Marketing → Executive | CMO + CEO | <1 hour |
| **Data Breach** | Engineering → Executive | CTO + CEO + Legal | <1 hour |

---

# Part 5: Close-the-Loop Framework

## The Close-the-Loop Promise

**Rule**: Every customer who gives feedback deserves a response.

**3 Levels of Closing the Loop**:

### Level 1: Individual Response (Required)

**When**: Every customer who provides feedback

**Timeline**: Within 7 days of feedback receipt

**Templates**:

**For Feature Requests**:
```
Olá [Nome],

Obrigado por sugerir [Feature]!

Nós adicionamos sua ideia à nossa lista de prioridades.
Vamos avaliar junto com outras solicitações de clientes.

Te avisaremos quando:
- Começarmos a construir (Você será beta tester!)
- Lançarmos (Você será o primeiro a saber)

Agradecemos por nos ajudar a construir um produto melhor.

Abraço,
Equipe ConectaPay
```

**For Bugs Reported**:
```
Olá [Nome],

Obrigado por reportar este problema.

Nossa equipe de engenharia está investigando.
Você pode acompanhar o status aqui:
[Link: Status do Ticket]

Estimativa de correção: [X] dias.

Te avisaremos quando for corrigido.

Desculpe pelo inconveniente.
Equipe ConectaPay
```

**For Negative Feedback**:
```
Olá [Nome],

Obrigado pelo feedback honesto.

Sinto muito que sua experiência não foi ideal.
Gostaria de entender melhor para podermos ajudar.

Posso te ligar rapidamente (10 min) para entender melhor?
[Agendar Ligação]

O que você prefere:
- [ ] Ligação (agende aqui)
- [ ] WhatsApp (clique aqui)
- [ ] Email (responda aqui)

Abraço,
[CSM Name]
Equipe ConectaPay
```

**For Positive Feedback**:
```
Oi [Nome],

Que ótimo saber que você está gostando do ConectaPay! 🎉

Se você tem 2 minutos, poderia nos deixar um avaliação no Google?
Ajuda outros pequenos negócios a nos encontrarem.

[Link: Deixar Avaliação]

Obrigado por fazer parte da nossa jornada!

Abraço,
Equipe ConectaPay
```

---

### Level 2: Segment Notification (Best Practice)

**When**: Multiple customers request same feature/report same issue

**Timeline**: When action is taken (before launch)

**Template**:
```
Subject: Você pediu, nós fizemos! 🚀

Olá [Nome],

Você mencionou que [Feature/Idea] seria útil para você.

Adivinha só? Nós lançamos [Feature]!

[O que faz]: [Descrição]
[Como usar]: [Link: Tutorial]
[Por que importa]: [Benefício]

[X] clientes como você pediram este recurso.
Obrigado por nos guiar!

Aproveite,
Equipe ConectaPay

P.S. Quer ser beta tester de futuros recursos?
[Cadastre-se aqui: Beta Program]
```

**Segmentation**:
- All who requested X feature
- All who reported X bug
- All who gave X feedback score
- All in X lifecycle stage (onboarding, expansion, etc.)

---

### Level 3: Public Communication (Optional)

**When**: Major feature launch, significant improvement, crisis resolution

**Channels**:
- Product update email (all customers)
- Blog post
- Social media announcement
- Release notes

**Template** (Product Update Email):
```
Subject: Novidades do ConectaPay: [Feature Name] 🚀

Olá [Nome],

Estamos felizes em anunciar [Feature Name]!

[O que é]: [Descrição]
[Por que criamos]: [X] clientes pediram, incluindo você se...
[Como funciona]: [Explicação simples]
[Como usar]: [Link: Tutorial]

Isso resolve o problema de [Problem] que muitos de vocês mencionaram.

Lançamento gradual:
- Disponível para: [Segment]
- Disponível para todos em: [Date]

O que acham? Conte para nós no WhatsApp!
[Link: WhatsApp Feedback]

Abraço,
Equipe ConectaPay
```

---

## Close-the-Loop Tracking

**Close-the-Loop Rate Metric**:
```
Close-the-Loop Rate = (Customers Notified / Customers Who Requested) × 100%

Target:
- Month 3: 50%
- Month 6: 75%
- Month 12: 90%
```

**Tracking Template**:
```
Feature/Improvement: [Name]
Request Date: [DATE]
Customers Who Requested: [X]
Customers Notified: [X] ([X]%)
Notification Date: [DATE]
Notification Channel: [Email/WhatsApp/In-app/All]
Status: [Notified / Partially Notified / Not Notified]
Reason if Not Notified: [Reason]
```

---

# Part 6: VoC Metrics & Reporting

## North Star Metrics

| Metric | Definition | Target | Frequency |
|--------|------------|--------|-----------|
| **Feedback Collection Rate** | % of customers who provided feedback in last 30 days | 80% | Monthly |
| **NPS** | % Promoters - % Detractors | 60 | Quarterly |
| **Close-the-Loop Rate** | % of feedback recipients notified of action | 90% | Monthly |
| **Analysis Response Time** | Days from feedback receipt to analysis complete | 3 days | Weekly |
| **Action Closure Rate** | % of analyzed feedback items acted upon | 90% | Monthly |
| **Feedback-to-Feature Rate** | % of shipped features originated from customer feedback | 15% | Quarterly |

## Operational Metrics

| Metric | Target | Frequency | Owner |
|--------|--------|-----------|-------|
| In-app survey response rate | 40%+ | Weekly | Product |
| Email survey response rate | 25%+ | Monthly | Marketing |
| Support ticket tagging | 100% | Daily | CS |
| Social media response time | <4 hours | Daily | Marketing |
| Review response rate | 100% | Weekly | CS |
| Churn interview completion | 80%+ | Monthly | CS |

## VoC Dashboard Structure

**Real-Time (Always Visible)**:
- NPS (current)
- Feedback collection rate (last 30 days)
- Close-the-loop rate (last 30 days)
- Sentiment trend (last 7 days)

**Weekly (Updated Monday)**:
- Top 5 feedback themes
- Top 5 feature requests
- Top 5 complaints
- Action items with owners

**Monthly (Published 1st of month)**:
- NPS trend (last 6 months)
- Feedback collection by channel
- Close-the-loop rate by channel
- Feedback-to-feature ship rate
- Churn analysis (top reasons)
- Competitive intelligence summary

**Quarterly (Published first week of quarter)**:
- Comprehensive VoC report
- Customer sentiment deep dive
- Feature request impact analysis
- ROI of VoC program (revenue saved/earned)
- Roadmap informed by VoC
- Next quarter priorities

---

# Part 7: Implementation Roadmap

## 90-Day Launch Plan

### Month 1: Foundation (Weeks 1-4)

**Week 1: System Setup**
- [ ] Select VoC tools (Typeform/SurveyMonkey for surveys, Brandwatch for social, Mixpanel for behavior)
- [ ] Configure in-app survey tool (integration required)
- [ ] Set up feedback database (Airtable/Notion/CRM)
- [ ] Create feedback tagging schema
- [ ] Build Slack/Discord channel for VoC alerts

**Week 2: Template Creation**
- [ ] Write all survey templates (in-app, email, interview)
- [ ] Create close-the-loop email templates
- [ ] Build weekly VoC meeting agenda template
- [ ] Design VoC dashboard (in data tool)
- [ ] Create feedback routing flowchart

**Week 3: Integration**
- [ ] Integrate in-app survey tool (requires engineering)
- [ ] Set up email survey automation (Day 7, 30, 90)
- [ ] Configure support ticket tagging (CS team)
- [ ] Set up social listening alerts (marketing team)
- [ ] Create review tracking (Google, Trustpilot, Capterra)

**Week 4: Team Training**
- [ ] Train CS team on close-the-loop (all templates)
- [ ] Train sales team on VoC capture (CRM fields)
- [ ] Train product team on feedback triage
- [ ] Train marketing team on social listening
- [ ] Launch weekly VoC meeting (Monday 30 min)

**Success Criteria**:
- [ ] In-app surveys configured
- [ ] Email surveys automated (Day 7, 30, 90)
- [ ] Support tickets 100% tagged
- [ ] Social listening active
- [ ] Weekly VoC meeting established

---

### Month 2: Launch (Weeks 5-8)

**Week 5: Soft Launch**
- [ ] Launch in-app microsurveys (10% of users)
- [ ] Send Day 7 NPS survey (all new customers from Week 5)
- [ ] Begin support ticket sentiment analysis
- [ ] Start social listening monitoring
- [ ] Track baseline metrics

**Week 6: Scale Up**
- [ ] Scale in-app surveys to 50% of users
- [ ] Send Day 30 NPS survey (all eligible customers)
- [ ] Conduct first 5 customer interviews (onboarding focus)
- [ ] Publish first weekly VoC summary
- [ ] Close first loop (notify customers of action)

**Week 7: Full Launch**
- [ ] Launch in-app surveys to 100% of users
- [ ] Implement exit survey for churned customers
- [ ] Launch review response protocol (respond to all)
- [ ] Conduct first churn interview (all churned from Week 7)
- [ ] Publish first monthly VoC report

**Week 8: Optimization**
- [ ] Analyze first 4 weeks of data
- [ ] Optimize low-performing surveys (response rate <20%)
- [ ] Iterate on close-the-loop templates based on responses
- [ ] Adjust feedback routing based on volume
- [ ] Conduct CAB recruitment outreach (20 invitations)

**Success Criteria**:
- [ ] 40%+ feedback collection rate
- [ ] 50%+ close-the-loop rate
- [ ] Weekly VoC meeting established
- [ ] Monthly VoC report published
- [ ] 5 customer interviews completed

---

### Month 3: Scale & Automate (Weeks 9-12)

**Week 9: Advisory Board**
- [ ] Select 12 CAB members from applicants
- [ ] Schedule first quarterly CAB meeting (Week 12)
- [ ] Send CAB pre-meeting survey (strategic priorities)
- [ ] Prepare roadmap preview for CAB meeting

**Week 10: Automation**
- [ ] Automate sentiment analysis (AI/NLP integration)
- [ ] Build automated alerts (churn risk, viral sentiment)
- [ ] Create auto-assignment for feedback routing
- [ ] Implement behavioral churn prediction
- [ ] Set up VoC dashboard auto-refresh

**Week 11: Deep Dive**
- [ ] Conduct 10 customer interviews (feature validation focus)
- [ ] Analyze first 8 weeks of VoC data (trends, patterns)
- [ ] Calculate VoC ROI (revenue impact of closed loops)
- [ ] Identify top 5 requested features for roadmap
- [ ] Publish first quarterly VoC report

**Week 12: Review & Plan**
- [ ] Host first CAB meeting (2 hours, virtual)
- [ ] Present VoC program results to company
- [ ] Create Q2 VoC roadmap (improvements, new channels)
- [ ] Celebrate wins (notify customers of shipped features)
- [ ] Document lessons learned

**Success Criteria**:
- [ ] 60%+ feedback collection rate
- [ ] 75%+ close-the-loop rate
- [ ] 10 customer interviews completed
- [ ] First CAB meeting conducted
- [ ] Quarterly VoC report published

---

## Beyond 90 Days

### Month 4-6: Optimization
- Optimize survey response rates (A/B test subject lines, timing)
- Automate more feedback analysis (AI/NLP for themes)
- Expand social listening (more platforms, deeper analysis)
- Launch customer advisory board recruitment (CAB v2)

### Month 7-12: Maturity
- Achieve 80%+ feedback collection rate
- Achieve 90%+ close-the-loop rate
- Ship 10+ features from customer feedback
- Publish VoC case study (how we built the program)

---

# Part 8: Tools & Technology Stack

## Recommended Tools by Budget

### Bootstrap Phase (<R$ 500/month)

| Function | Tool | Cost | Why |
|----------|------|------|-----|
| **Surveys** | Typeform | Free (up to 100 responses/month) | Beautiful, easy |
| **In-App Surveys** | Hotjar | Free (up to 1,000 pageviews/day) | Heatmaps + surveys |
| **Social Listening** | Google Alerts | Free | Basic mention tracking |
| **Reviews** | Manual (Google, Trustpilot) | Free | Check weekly |
| **Support** | Gmail + Labels | Free | Basic ticket tracking |
| **Database** | Airtable | Free (up to 1,000 records) | Flexible, easy |
| **Analytics** | PostHog | Free (up to 1M events/month) | Product analytics |
| **Meetings** | Google Meet | Free | Interviews, CAB |
| **Total**: ~R$ 0/month |

### Growth Phase (R$ 500-2.000/month)

| Function | Tool | Cost | Why |
|----------|------|------|-----|
| **Surveys** | Typeform Pro | ~R$ 200/month | Unlimited responses |
| **In-App Surveys** | Sprig | ~R$ 300/month | Microsurveys, beautiful |
| **Social Listening** | Mention.com | ~R$ 400/month | Comprehensive monitoring |
| **Reviews** | ReviewTrackers | ~R$ 300/month | Aggregates all review sites |
| **Support** | Front | ~R$ 400/month | Shared inbox, analytics |
| **Database** | Notion | ~R$ 100/month | Wiki, docs, databases |
| **Analytics** | Amplitude | ~R$ 200/month | Advanced product analytics |
| **Meetings** | Zoom | ~R$ 100/month | Reliable, recording |
| **Total**: ~R$ 2.000/month |

### Scale Phase (R$ 2.000-5.000/month)

| Function | Tool | Cost | Why |
|----------|------|------|-----|
| **Surveys** | Qualtrics | ~R$ 600/month | Enterprise survey platform |
| **In-App Surveys** | Medallia | ~R$ 800/month | VoC specialized |
| **Social Listening** | Brandwatch | ~R$ 1.000/month | Best-in-class |
| **Reviews** | Birdeye | ~R$ 500/month | Review management |
| **Support** | Zendesk | ~R$ 800/month | Enterprise support |
| **Database** | Salesforce | ~R$ 600/month | CRM + custom objects |
| **Analytics** | Mixpanel | ~R$ 500/month | Advanced analytics |
| **Meetings** | Zoom Enterprise | ~R$ 200/month | Large meetings |
| **Total**: ~R$ 5.000/month |

---

# Part 9: Team Structure & Roles

## VoC Team Responsibilities

### Phase 1: Bootstrap (0-500 customers)

**VoC Lead** (CMO owns):
- Owns: NPS, close-the-loop rate, feedback collection rate
- Manages: Weekly VoC meeting, monthly report
- Reports: CEO
- Time: 5 hours/week

**Support Analyst** (CS team member):
- Owns: Support ticket tagging, close-the-loop responses
- Manages: Daily VoC triage
- Reports: Head of CS
- Time: 2 hours/day

**Product Manager**:
- Owns: Feature request triage, roadmap prioritization
- Manages: Product feedback analysis
- Reports: CPO/CEO
- Time: 3 hours/week

### Phase 2: Growth (500-2.000 customers)

**VoC Manager** (Full-time hire):
- Owns: VoC program operations, all VoC metrics
- Manages: Weekly VoC meeting, all reports, CAB
- Reports: CMO
- Team: 1 analyst

**VoC Analyst**:
- Owns: Feedback analysis, thematic coding, reporting
- Manages: Daily VoC triage, data quality
- Reports: VoC Manager
- Time: Full-time

**Product Manager** (VoC-focused):
- Owns: Feature request triage, feedback-to-product pipeline
- Manages: Product feedback analysis, roadmap
- Reports: CPO
- Time: 50% of role

### Phase 3: Scale (2.000+ customers)

**Head of Voice of Customer**:
- Owns: VoC strategy, all VoC metrics, team management
- Manages: VoC team, CAB, executive reporting
- Reports: CMO
- Team: 3-5 people

**VoC Analysts** (2-3):
- Owns: Feedback analysis, thematic coding, reporting
- Manages: Daily VoC triage, data quality
- Reports: Head of VoC
- Time: Full-time each

**Product Manager** (VoC-focused):
- Owns: Feature request triage, feedback-to-product pipeline
- Manages: Product feedback analysis, roadmap
- Reports: CPO
- Time: Dedicated role

---

# Part 10: ROI of VoC Program

## Quantify the Impact

### Revenue Impact

**Scenario 1: Prevent Churn** (Conservative)
- 100 customers, R$ 300/month ARPU
- 5% monthly churn without VoC → 5 customers churn/month
- VoC program reduces churn by 20% → 4 customers churn/month
- **Savings**: 1 customer × R$ 300 × 12 months = R$ 3.600/year
- **VoC Program Cost**: R$ 2.000/month (Phase 2 tools + team)
- **ROI**: (R$ 3.600 - R$ 24.000) / R$ 24.000 = **-85%** (wait, this is wrong...)

**Corrected Calculation**:
- 1.000 customers, R$ 300/month ARPU = R$ 300.000 MRR
- 5% monthly churn without VoC → 50 customers churn/month = R$ 15.000 MRR lost
- VoC program reduces churn by 20% → 40 customers churn/month = R$ 12.000 MRR lost
- **Savings**: R$ 3.000 MRR × 12 months = R$ 36.000/year
- **VoC Program Cost**: R$ 2.000/month × 12 months = R$ 24.000/year
- **ROI**: (R$ 36.000 - R$ 24.000) / R$ 24.000 = **50% ROI**

**Scenario 2: Expansion Revenue** (Moderate)
- 1.000 customers, R$ 300/month ARPU
- 5% expand to Pro plan (R$ 497/month) per year without VoC
- VoC program increases expansion by 50% → 7.5% expand
- **Additional Revenue**: 25 customers × (R$ 497 - R$ 300) × 12 months = R$ 59.100/year
- **VoC Program Cost**: R$ 24.000/year
- **ROI**: (R$ 59.100 - R$ 24.000) / R$ 24.000 = **146% ROI**

**Scenario 3: Combined Impact** (Realistic)
- Churn reduction savings: R$ 36.000/year
- Expansion revenue increase: R$ 59.100/year
- **Total Impact**: R$ 95.100/year
- **VoC Program Cost**: R$ 24.000/year
- **Net ROI**: R$ 71.100/year
- **ROI %**: (R$ 95.100 - R$ 24.000) / R$ 24.000 = **296% ROI**

### Non-Revenue Impact

**Employee Engagement**:
- Companies with mature VoC programs see 3x higher employee engagement
- Engaged employees stay 2x longer, perform 2x better
- Impact: Reduced hiring costs, increased productivity

**Product-Market Fit**:
- VoC accelerates PMF by 50% (faster learning)
- Faster PMF = faster growth, less capital burned
- Impact: Reach profitability 6 months earlier

**Brand Equity**:
- NPS 60+ = organic growth through referrals
- 70% of buying experiences are based on how customers feel they're treated
- Impact: Lower CAC, higher LTV

---

# Part 11: Common Mistakes to Avoid

## Mistake 1: Collecting But Not Acting
**Problem**: Survey fatigue, customer resentment
**Solution**: Don't ask if you can't/won't act. Close the loop always.

## Mistake 2: Only Collecting Negative Feedback
**Problem**: Skewed perception, demoralized team
**Solution**: Celebrate positive feedback too. Share wins broadly.

## Mistake 3: Asking Leading Questions
**Problem**: Biased data, wrong insights
**Solution**: Use neutral language. Test surveys internally first.

## Mistake 4: Surveying Too Frequently
**Problem**: Annoyed customers, lower response rates
**Solution**: Space out surveys. Minimum 30 days between major surveys.

## Mistake 5: Ignoring Silent Customers
**Problem**: Missing insights from majority who don't speak up
**Solution**: Behavioral data + proactive outreach to silent customers.

## Mistake 6: Only Collecting, Not Analyzing
**Problem**: Data overload, no insights
**Solution**: Thematic coding, sentiment analysis, prioritize by impact.

## Mistake 7: Siloing VoC in One Team
**Problem**: Limited impact, slow action
**Solution**: VoC is everyone's job. Distribute insights to all teams.

## Mistake 8: Focusing on Vanity Metrics
**Problem**: Good scores but no business impact
**Solution**: Track NPS, close-the-loop rate, feedback-to-feature rate.

## Mistake 9: Not Closing the Loop
**Problem**: Customers feel unheard, lower NPS
**Solution**: Every customer who gives feedback deserves a response.

## Mistake 10: Treating All Feedback Equally
**Problem**: Noise drowns signal, analysis paralysis
**Solution**: Priority scoring. Focus on high-impact, high-frequency issues.

---

# Part 12: Quick Reference Guides

## VoC Program Launch Checklist

```
Phase 1: Setup (Week 1)
□ Select survey tools (Typeform, Hotjar)
□ Configure feedback database (Airtable)
□ Create tagging schema
□ Build Slack/Discord alerts
□ Write survey templates
□ Create close-the-loop templates
□ Build weekly meeting agenda
□ Design VoC dashboard

Phase 2: Integrate (Week 2-3)
□ Integrate in-app survey tool
□ Set up email surveys (Day 7, 30, 90)
□ Configure support ticket tagging
□ Set up social listening
□ Create review tracking

Phase 3: Train (Week 4)
□ Train CS team (close-the-loop)
□ Train sales team (VoC capture)
□ Train product team (triage)
□ Train marketing team (social listening)
□ Launch weekly VoC meeting

Phase 4: Launch (Week 5-8)
□ Launch in-app surveys (10% → 100%)
□ Send Day 7 NPS survey
□ Implement exit survey
□ Conduct customer interviews
□ Publish weekly VoC summary
□ Close first loop

Phase 5: Optimize (Week 9-12)
□ Analyze first 4 weeks of data
□ Optimize low-performing surveys
□ Iterate on close-the-loop templates
□ Conduct CAB recruitment
□ Publish quarterly VoC report
```

---

## Survey Timing Cheat Sheet

```
In-App Microsurveys:
- After signup: Instant
- After first automation: Instant
- After first recovery: Instant
- After support ticket closed: 1 hour
- After feature used 5x times: Instant
- After churn initiated: Instant

Email Surveys:
- Day 7 NPS: Exactly 7 days after signup
- Day 30 NPS: Exactly 30 days after signup
- Day 90 NPS: Exactly 90 days after signup
- Quarterly NPS: First week of each quarter
- Win-back survey: 30 days after churn

Interviews:
- Onboarding: Day 14-30
- Quarterly check-in: Every 90 days
- Churn interview: Within 7 days of churn
- Feature validation: Before building feature
- Advisory board: Quarterly (2 hours)

Support Analysis:
- Daily: Ticket tagging, sentiment
- Weekly: Top issues report
- Monthly: Churn analysis, feature requests

Sales Analysis:
- Weekly: Objections, feature requests
- Monthly: Win/loss analysis
- Quarterly: Competitive intelligence

Social Listening:
- Real-time: Mentions, sentiment spikes
- Daily: Review sites
- Weekly: Social summary report

Behavioral Analysis:
- Daily: Churn risk alerts
- Weekly: Feature adoption
- Monthly: Power user patterns, churn precursors
```

---

## Close-the-Loop Response Time SLAs

```
Individual Feedback:
- Positive: Within 7 days
- Negative: Within 24 hours
- Feature request: Within 7 days
- Bug report: Within 24 hours (acknowledge), 7 days (update)

Segment Notification:
- Before feature launch: All who requested
- After bug fix: All who reported
- After improvement: All who suggested

Public Communication:
- Major feature: All customers (email)
- Significant improvement: All customers (email)
- Crisis resolution: Public statement + affected customers (email)
```

---

## VoC Dashboard Structure

```
Real-Time (Always Visible):
├── NPS (current)
├── Feedback Collection Rate (last 30 days)
├── Close-the-Loop Rate (last 30 days)
└── Sentiment Trend (last 7 days)

Weekly (Updated Monday):
├── Top 5 Feedback Themes
├── Top 5 Feature Requests
├── Top 5 Complaints
└── Action Items (with owners)

Monthly (Published 1st of month):
├── NPS Trend (last 6 months)
├── Feedback Collection by Channel
├── Close-the-Loop Rate by Channel
├── Feedback-to-Feature Ship Rate
├── Churn Analysis (top reasons)
└── Competitive Intelligence Summary

Quarterly (Published first week of quarter):
├── Comprehensive VoC Report
├── Customer Sentiment Deep Dive
├── Feature Request Impact Analysis
├── ROI of VoC Program
├── Roadmap Informed by VoC
└── Next Quarter Priorities
```

---

**Document Version**: 1.0
**Created**: 2026-04-25
**Author**: CMO Agent (55827422-a849-41d3-9286-0b5b8b002079)
**Task**: CON-107 - Customer Feedback Loop and Voice of Customer Program

---

## Next Steps

1. **Review with Leadership** (Week 1)
   - Present VoC program strategy
   - Approve budget for tools
   - Approve team structure
   - Align on metrics and targets

2. **Select Tools** (Week 1)
   - Survey platform (Typeform, SurveyMonkey, or Qualtrics)
   - In-app survey tool (Hotjar, Sprig, or Medallia)
   - Social listening (Mention.com, Brandwatch, or manual)
   - Feedback database (Airtable, Notion, or CRM)

3. **Hire/Assign VoC Lead** (Week 2)
   - Internal promotion or external hire
   - Train on VoC program
   - Begin Week 1 setup tasks

4. **Launch Foundation** (Week 3-4)
   - Configure all tools
   - Create all templates
   - Train all teams
   - Launch weekly VoC meeting

5. **Start Collecting Feedback** (Week 5+)
   - Launch in-app surveys
   - Send Day 7 NPS survey
   - Begin support ticket analysis
   - Start social listening

6. **Analyze & Act** (Week 6+)
   - First weekly VoC summary
   - Close first loop
   - Publish first monthly VoC report
   - Ship first feature from customer feedback

---

**Success Metric**: 90% close-the-loop rate, 60 NPS, 15% feedback-to-feature rate by Month 12
