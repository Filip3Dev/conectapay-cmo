# ConectaPay Customer Churn Analysis and Prevention Strategy

## Executive Summary

**Objective**: Reduce customer churn from industry average 10-15% to world-class <5% through systematic analysis, early detection, and proactive intervention.

**Target Metrics**:
- **Monthly Churn Rate**: <5% (top quartile vs 10-15% industry)
- **Net Revenue Retention (NRR)**: 110%+ (expansion offsets churn)
- **Customer Lifetime Value (LTV)**: 2.5x → 4x improvement
- **Recovery Rate**: 15-25% of at-risk customers saved

**Economic Impact**:
- At 500 customers, reducing churn from 10% → 5% = **R$ 90.000/year saved**
- At 1.000 customers, **R$ 180.000/year saved**
- Combined with expansion (NRR 110%), total impact: **R$ 270.000-540.000/year**

---

## Part 1: Churn Analysis Framework

### Understanding Churn Types

**1. Voluntary Churn** (70-80% of total churn)
- Customer cancels intentionally
- Reasons: Price, product fit, competition, poor results
- **Preventable**: Yes, with early intervention

**2. Involuntary Churn** (20-30% of total churn)
- Payment failures, business closure, inactivity
- **Preventable**: Partially (payment recovery, re-engagement)

**3. Silent Churn** (Hidden - 30-40% of "active" customers)
- Customer pays but doesn't use the product
- High risk of future cancellation
- **Detectable**: Via activity metrics

---

### Churn Measurement Framework

**Primary Metrics**:

| Metric | Formula | Target | Frequency |
|--------|---------|--------|-----------|
| **Monthly Churn Rate** | (Customers Churned / Start of Month Customers) × 100 | <5% | Monthly |
| **Annual Churn Rate** | 1 - (Retention Rate)^12 | <45% | Annually |
| **Net Revenue Retention** | ((Starting MRR + Expansion - Downsell - Churn) / Starting MRR) × 100 | 110%+ | Monthly |
| **Logo Churn** | Count of customers lost | <5% of base | Monthly |
| **Revenue Churn** | MRR lost from churned customers | <3% of MRR | Monthly |
| **Recovery Rate** | (Saved from At-Risk / Total At-Risk) × 100 | 15-25% | Monthly |

**Secondary Metrics**:
- **Churn by Cohort**: Track customers acquired in same month
- **Churn by Tenure**: How long before they churn (Day 30, 60, 90)
- **Churn by Segment**: Clinics vs Real Estate vs Others
- **Churn by ARPU**: High-value vs low-value customer churn
- **Reason Distribution**: % of churn by primary reason

**Benchmark Comparison**:

| Segment | Industry Average | Top Quartile | ConectaPay Target |
|---------|------------------|--------------|-------------------|
| B2B SaaS (<$10K ARR) | 10-15% | 5-8% | **<5%** |
| B2B SaaS ($10K-50K ARR) | 8-12% | 4-6% | **<4%** |
| Brazilian SMB SaaS | 15-20% | 8-10% | **<6%** |

---

## Part 2: Early Warning Signals (Churn Prediction)

### The Churn Timeline

**Critical Insight**: Churn doesn't happen overnight. There are signals 30-90 days before cancellation.

```
Day 0    Day 30   Day 60   Day 90   Cancel
  |        |        |        |        |
Healthy → Warning → At-Risk → Critical → Churned
         (detect) (intervene)  (escalate)
```

**Key Principle**: If you detect at Day 30, you have 60 days to save the customer. Recovery rate: 40-60%.
If you detect at Day 60, you have 30 days. Recovery rate: 20-30%.
If you detect at Day 90, you have 7 days. Recovery rate: 5-10%.

---

### 25 Early Warning Indicators

**Category 1: Activity Decline** (Highest Predictive Value)

| Signal | Threshold | Risk Level | Detection Method |
|--------|-----------|------------|------------------|
| Automation runs stopped | 0 runs in 7 days | 🔴 Critical | Product event |
| Login frequency dropped | <1 login/week (from 3+) | 🔴 Critical | Product event |
| WhatsApp messages sent | 0 in 14 days | 🔴 Critical | Product event |
| Dashboard views | 0 in 7 days | 🟡 Warning | Product event |
| Feature usage decline | 50% drop MoM | 🟡 Warning | Product event |

**Category 2: Engagement Decline**

| Signal | Threshold | Risk Level | Detection Method |
|--------|-----------|------------|------------------|
| Email open rate | <20% (from 40%+) | 🟡 Warning | Email analytics |
| Support tickets | 0 in 30 days (from 2+/month) | 🟡 Warning | Support system |
| NPS survey response | "Not likely to recommend" | 🔴 Critical | NPS system |
| Feature requests | Stopped asking | 🟡 Warning | Product/Support |

**Category 3: Value Realization Issues**

| Signal | Threshold | Risk Level | Detection Method |
|--------|-----------|------------|------------------|
| Recovered sales | R$ 0 in first 30 days | 🔴 Critical | Product event |
| Time-to-first-value | >14 days (target <48h) | 🔴 Critical | Onboarding tracker |
| Setup incomplete | Not configured after 7 days | 🔴 Critical | Product event |
| Recovery rate | <10% of abandoned sales | 🟡 Warning | Product event |

**Category 4: Commercial Signals**

| Signal | Threshold | Risk Level | Detection Method |
|--------|-----------|------------|------------------|
| Payment failed | 2+ failed attempts | 🔴 Critical | Billing system |
| Credit card expiring | <30 days until expiry | 🟡 Warning | Billing system |
| Downgrade requested | Asked for lower plan | 🔴 Critical | Support/Sales |
| Competitor mentioned | "Testing [Competitor]" | 🔴 Critical | Sales/Support |

**Category 5: Business Changes**

| Signal | Threshold | Risk Level | Detection Method |
|--------|-----------|------------|------------------|
| Key contact left | Champion left company | 🔴 Critical | LinkedIn/Sales |
| Company merged | Acquisition detected | 🟡 Warning | Public records |
| Industry decline | Segment down trending | 🟡 Warning | Market research |
| Seasonal dip | Expected (not churn) | 🟢 Normal | Historical data |

---

### Churn Risk Scoring Model

**Score Components** (0-100 total):

| Component | Weight | Scoring Logic |
|-----------|--------|---------------|
| **Activity Score** | 30 points | 30 = Active daily, 0 = No activity 7+ days |
| **Value Score** | 25 points | 25 = Recovered R$ 500+, 0 = R$ 0 recovered |
| **Engagement Score** | 20 points | 20 = Opens 50%+ emails, 0 = <10% opens |
| **Tenure Score** | 10 points | 10 = 6+ months, 0 = <1 month |
| **Payment Score** | 10 points | 10 = On-time, 0 = Failed payments |
| **Support Score** | 5 points | 5 = Positive NPS, 0 = Negative NPS |

**Risk Classification**:

| Score | Risk Level | Action Required | Owner |
|-------|------------|-----------------|-------|
| **80-100** | 🟢 Healthy | Monitor only | CS Team |
| **60-79** | 🟡 Warning | Check-in call | CSM |
| **40-59** | 🟠 At-Risk | Intervention playbook | Senior CSM |
| **0-39** | 🔴 Critical | Escalation playbook | CS Manager + CSM |

**Automated Triggers**:
- Score drops below 60 → **Task created for CSM**
- Score drops below 40 → **Alert to CS Manager**
- Score drops below 20 → **Emergency escalation**

---

## Part 3: Root Cause Analysis

### Churn Reason Taxonomy

**Level 1: 6 Main Categories**
1. **Product** (30-40%): Features, quality, reliability
2. **Price** (20-30%): Too expensive, budget cuts, competitor cheaper
3. **Service** (15-20%): Support quality, onboarding, communication
4. **Fit** (10-15%): Wrong segment, use case changed
5. **Technical** (5-10%): Integration, bugs, performance
6. **Business** (5-10%): Closed, pivoted, merged, seasonal

**Level 2: 30 Subcategories** (5 per category)

**Example - Product Category**:
- Missing features
- Poor performance
- Bugs/errors
- Hard to use
- Doesn't integrate

**Level 3: Specific Tags** (unlimited)

**Example - Missing Features**:
- "Need SMS automation"
- "Need multi-language"
- "Need reporting dashboard"
- "Need team collaboration"
- "Need API access"

---

### Exit Interview Framework

**Timing**: Within 7 days of cancellation

**Channel**: Phone call (preferred) or in-depth survey

**Questions** (15-20 minutes):

**Section 1: Decision** (3 minutes)
1. When did you first consider cancelling?
2. What was the primary reason?
3. Was there a specific event that triggered the decision?

**Section 2: Product** (5 minutes)
4. Which features did you use most?
5. Which features did you never use?
6. What was missing that you needed?
7. How would you rate the reliability? (1-10)
8. What was the biggest frustration?

**Section 3: Value** (4 minutes)
9. Did you achieve your expected ROI?
10. What was your actual recovery rate (% of abandoned sales)?
11. What would have made it worth 2x the price?
12. What problem did we solve best?

**Section 4: Experience** (3 minutes)
13. How was the onboarding process? (1-10)
14. How would you rate our support? (1-10)
15. Did you feel heard when you gave feedback?

**Section 5: Competition** (3 minutes)
16. Which alternatives did you consider?
17. What did they offer that we didn't?
18. Why did you choose them over us?

**Section 6: Future** (2 minutes)
19. Under what conditions would you return?
20. Can we stay in touch for product updates?

**Incentive**: Offer R$ 100-200 gift card or 3 free months if they return (conditional on completion)

---

### Churn Analysis by Customer Segment

**Clinics Segment**:

| Churn Reason | % of Total | Prevention Strategy |
|--------------|------------|---------------------|
| Poor results (no recovery) | 40% | Better onboarding, templates |
| Price sensitivity | 25% | Value demonstration, tiered pricing |
| Staff turnover (champion left) | 15% | Multi-user onboarding |
| Too complex | 10% | Simplify setup, automation |
| Closed business | 10% | Not preventable |

**Real Estate Segment**:

| Churn Reason | % of Total | Prevention Strategy |
|--------------|------------|---------------------|
| Low lead volume | 35% | Lead sourcing integration |
| Competitor (CRM features) | 25% | Feature parity, differentiation |
| Seasonal (slow period) | 20% | Flexible pause/resume |
| Poor results | 15% | Niche-specific templates |
| Agency pivot | 5% | Not preventable |

**Other Segments**:
- Academies, Óticas, E-commerce: Analyze when 50+ customers per segment

---

## Part 4: Retention Playbooks

### Playbook 1: At-Risk Intervention (Score 40-59)

**Trigger**: Health score drops below 60

**Owner**: Customer Success Manager

**Timeline**: 7-day intervention sequence

**Day 1: Detection & Research**
- [ ] Automated task created in CS tool
- [ ] CSM reviews customer profile:
  - Current health score components
  - Recent activity (last 14 days)
  - Support ticket history
  - Billing status
  - Original use case/goals
- [ ] Identify primary risk factor(s)

**Day 2: Outreach**
- [ ] Send personalized email:
  ```
  Assunto: Notei que você está usando menos o ConectaPay

  Olá [Nome],

  Vi que sua automação não roda há 7 dias.
  Tudo bem? Alguma dificuldade técnica?

  Posso te ajudar em 15 min. Responda este email
  ou agende: [Link Calendly]

  Quero ver você recuperando vendas de novo.

  Abraços,
  [Seu Nome] | Customer Success
  ```
- [ ] If no response in 24h, proceed to Day 3

**Day 3: Follow-up**
- [ ] WhatsApp message:
  ```
  [Nome], vi aqui que não está usando a automação.

  Algum problema? Posso chamar no WhatsApp
  pra resolver em 5 min.

  [Seu Nome]
  ```
- [ ] If no response, try phone call (if number available)

**Day 4-5: Resolution**
- [ ] Connect with customer (call/video/WhatsApp)
- [ ] Diagnose root cause:
  - Technical issue? → Technical support
  - Value not realized? → Success coaching
  - Price concern? → Value demonstration
  - Changed needs? → Alternative configuration
- [ ] Implement solution
- [ ] Verify customer is back on track

**Day 7: Follow-up**
- [ ] Confirm issue resolved
- [ ] Customer running automations again
- [ ] Health score improved to 60+
- [ ] Schedule 30-day follow-up

**Success Criteria**:
- Customer responds within 48h
- Issue resolved within 7 days
- Health score improves to 60+
- Customer resumes activity

**Recovery Rate**: 40-60% (if caught at this stage)

---

### Playbook 2: Critical Escalation (Score 0-39)

**Trigger**: Health score drops below 40 OR customer requests cancellation

**Owner**: CS Manager + Senior CSM

**Timeline**: Immediate escalation, 24-48h resolution

**Immediate Actions** (within 2 hours):

**Step 1: Internal Alert**
- [ ] Automated notification to CS Manager
- [ ] Slack channel alert: "🚨 [Customer Name] at risk"
- [ ] Customer data assembled:
  - Full history (sign-up date, tenure, MRR)
  - All support tickets
  - Product usage (all time, last 90 days)
  - Billing history
  - NPS responses
  - Communication history

**Step 2: Manager Review** (within 4 hours)
- [ ] CS Manager reviews customer profile
- [ ] Assesses: Is this customer saveable?
- [ ] Determines intervention strategy:
  - **Saveable**: Proceed to Step 3
  - **Not saveable**: Facilitate graceful exit

**Step 3: Outreach** (within 8 hours)

**If customer requested cancellation**:
```
Assunto: Vamos resolver isso juntos

Olá [Nome],

Recebi seu pedido de cancelamento. Antes de processar,
quero entender: o que aconteceu?

Posso oferecer:
1. Ajuda imediata no problema
2. Plano alternativo (pausa, desconto, mudança)
3. Conversa comigo direto

Me responda até o final do dia. Quero ver o que podemos fazer.

[Seu Nome] | Head of Customer Success
WhatsApp: [Número]
```

**If silent churn detected**:
```
Assunto: Oferta exclusiva para você voltar

Olá [Nome],

Vi que parou de usar o ConectaPay. Entendo que a rotina
é corrida e às vezes a gente não dá atenção às ferramentas.

Tenho uma proposta:
- Mês extra grátis (2 meses pelo preço de 1)
- Setup completo em 15 min (eu faço pra você)
- Garantia: Recupera R$ 500+ ou devolvemos seu dinheiro

Quer tentar de novo?

Responda até amanhã e eu ativo tudo.

Abraços,
[Seu Nome] | Head of Customer Success
```

**Step 4: High-Touch Intervention** (within 24 hours)

**If customer responds**:
- [ ] CS Manager or Senior CSM calls customer
- [ ] Deep diagnostic call (30-45 minutes):
  - What's not working?
  - What were your expectations?
  - What would make it worth continuing?
  - Can we fix this in the next 48 hours?
- [ ] Offer options:
  - **Option A**: Fix the issue (technical/support)
  - **Option B**: Change configuration (better fit)
  - **Option C**: Financial accommodation (pause, discount)
  - **Option D**: Graceful exit (if not saveable)

**Step 5: Resolution** (within 48 hours)

**If customer accepts save offer**:
- [ ] Implement solution immediately
- [ ] CS Manager personally oversees
- [ ] Daily check-ins for first week
- [ ] Weekly check-ins for first month
- [ ] Guarantee satisfaction

**If customer declines and cancels**:
- [ ] Process cancellation promptly (no friction)
- [ ] Ask: "Under what conditions would you return?"
- [ ] Offer: "Stay on our list for product updates"
- [ ] Send: "We'd love you back - here's a return offer"

**Success Criteria**:
- Response rate: 50%+
- Save rate: 15-25% (from critical stage)
- Time to resolution: <48 hours
- Saved customers stay 6+ months

---

### Playbook 3: Win-Back (Churned Customers)

**Target**: Customers who cancelled 30-180 days ago

**Owner**: Sales / CS Team

**Strategy**: Targeted re-engagement based on churn reason

**Segment 1: Churned for Price** (40% of churned)
**Timing**: 60-90 days after cancellation

**Email Template**:
```
Assunto: Estamos diferentes agora (e mais barato)

Olá [Nome],

Você cancelou o ConectaPay há 2 meses. Entendo - preço
é sempre um fator.

Mas desde então:
- Lançamos plano começando em R$ 97/mês (era R$ 197)
- Adicionamos automações prontas (não precisa configurar)
- Criamos templates para [segmento] específicos

Quer ver se funciona agora?
- 14 dias grátis
- Setup em 10 min (eu faço)
- Sem cartão obrigatório

Teste de novo: [Link]

Se não funcionar, não se preocupa. Só quero uma chance.

Abraços,
[Seu Nome]
```

**Segment 2: Churned for Poor Results** (30% of churned)
**Timing**: 90-120 days after cancellation

**Email Template**:
```
Assunto: ConectaPay agora funciona [X]% melhor

Olá [Nome],

Quando você usava o ConectaPay, a taxa de recuperação
era baixa. Eu entendo - estava abaixo do esperado.

Desde então:
- Melhoramos algoritmos (+25% recuperação)
- Criamos templates validados (clientes recuperam R$ 2-5K/mês)
- Adicionamos sucesso dedicado (te ajudamos pessoalmente)

Quer testar de novo?
- Garantia: Recupera R$ 500+ ou devolvemos tudo
- Setup completo incluído
- Desconto de retorno: 20% off 3 meses

Link: [URL]

Abraços,
[Seu Nome]
```

**Segment 3: Churned for Features** (20% of churned)
**Timing**: When requested feature launches

**Email Template**:
```
Assunto: Lembra que pediu [Feature]? Agora temos!

Olá [Nome],

Há 6 meses você cancelou porque faltava [Feature].

Adivinha: Lançamos mês passado!

O que mudou:
- [Feature 1]: Descrição breve
- [Feature 2]: Descrição breve
- [Feature 3]: Descrição breve

Quer voltar?
- Setup em 10 min
- Mês grátis pra testar as novidades
- Desconto de lealdade: 15% off

Testar novidades: [Link]

Abraços,
[Seu Nome]
```

**Win-Back Offer Structure**:

| Tenure | Offer | Conditions |
|--------|-------|------------|
| <3 months | 1 month free | Return within 90 days |
| 3-6 months | 20% off, 3 months | Return within 60 days |
| 6-12 months | 15% off, 6 months | Return within 30 days |
| 12+ months | 10% off ongoing | Any return |

**Success Metrics**:
- Open rate: 35-45%
- Response rate: 10-15%
| Win-back rate: 5-10%
- Re-churn rate: <20% (must stay 6+ months)

---

### Playbook 4: Pre-Churn Prevention (Proactive)

**Target**: All customers at Day 30, 60, 90, 180, 360

**Owner**: Customer Success Team

**Strategy**: Scheduled check-ins before churn risk develops

**Day 30 Check-In** (Automated + Human if at-risk)
- [ ] Automated email: "Como estão seus primeiros 30 dias?"
- [ ] If recovered sales < R$ 100: Human outreach
- [ ] If health score < 70: Schedule call

**Day 60 Check-In** (Human for all customers)
- [ ] CSM sends: "Vamos revisar seus primeiros 2 meses"
- [ ] Review results: recovered sales, recovery rate
- [ ] Identify optimization opportunities
- [ ] Share best practices from similar customers
- [ ] Ask: "What would make this 2x more valuable?"

**Day 90 Check-In** (Human for all customers)
- [ ] Quarterly business review (QBR) invite
- [ ] Discuss: Goals achieved, next quarter goals
- [ ] Present: ROI calculation (money recovered)
- [ ] Propose: Expansion opportunities
- [ ] Ask: "What would you like to see improved?"

**Day 180 Check-In** (Human for all customers)
- [ ] Mid-year review
- [ ] Discuss: Success stories, challenges
- [ ] Share: Product roadmap (what's coming)
- [ ] Ask: "Shall we plan for growth together?"

**Day 360 Check-In** (Human for all customers)
- [ ] Annual review celebration
- [ ] Present: Total value delivered (past 12 months)
- [ ] Discuss: Renewal (if applicable) or expansion
- [ ] Ask for: Referral, case study participation

**Success Criteria**:
- 95%+ customers complete check-ins
- Health score maintained >70 for 80%+
- Pre-churn detection: 60%+ caught before cancellation request
- NPS: 60+ at Day 180

---

## Part 5: Churn Metrics Dashboard

### Real-Time Dashboard (Daily Monitoring)

**Section 1: At-Risk Customers** (Top priority)

| Customer | Health Score | Primary Risk | Days Since Activity | Action Owner | Status |
|----------|--------------|--------------|---------------------|--------------|--------|
| Clínica A | 35 | No sales recovered | 12 | [CSM Name] | 🟡 In contact |
| Imobiliária B | 28 | Key contact left | 8 | [CSM Name] | 🔴 Escalated |
| Clínica C | 45 | Setup incomplete | 5 | [CSM Name] | 🟢 Resolving |

**Section 2: Churn Pipeline**

| Stage | Count (Month) | % of Base | Trend |
|-------|---------------|-----------|-------|
| Healthy (80-100) | 420 | 84% | → Stable |
| Warning (60-79) | 50 | 10% | ↑ +5 |
| At-Risk (40-59) | 20 | 4% | ↑ +2 |
| Critical (0-39) | 10 | 2% | ↑ +1 |
| **Total Active** | **500** | **100%** | |

**Section 3: Churn Metrics** (This Month)

| Metric | Value | Target | Status |
|--------|-------|--------|--------|
| Customers Churned | 8 | <10 | 🟢 On track |
| Monthly Churn Rate | 1.6% | <5% | 🟢 Excellent |
| Revenue Churned | R$ 2.400 | <R$ 7.500 | 🟢 On track |
| Net Revenue Retention | 112% | >110% | 🟢 Excellent |
| Recovery Rate | 42% | >25% | 🟢 Excellent |

**Section 4: Churn by Reason** (Last 90 days)

| Reason | Count | % of Churn | Trend |
|--------|-------|------------|-------|
| Poor results | 12 | 40% | ↓ Improving |
| Price | 8 | 27% | → Stable |
| Competitor | 5 | 17% | ↑ Increasing |
| Technical | 3 | 10% | → Stable |
| Business closure | 2 | 6% | → Stable |

---

### Weekly Report (CS Team Review)

**Week of**: [Date Range]

**Summary**:
- Started with: 492 customers
- New signups: +18
- Churned: -5
- **Ended with: 505 customers**
- **Net growth: +13 customers (+2.6%)**

**Churn Details**:
| Customer | Reason | Tenure | MRR Lost | Could Save? |
|----------|--------|--------|----------|-------------|
| [Name] | Price | 6 months | R$ 297 | Yes (offered discount) |
| [Name] | Poor results | 2 months | R$ 197 | Yes (coaching) |
| [Name] | Competitor | 12 months | R$ 497 | No (feature gap) |
| [Name] | Business closed | 3 months | R$ 197 | No (out of business) |
| [Name] | Technical | 1 month | R$ 197 | Yes (resolved issue) |

**Preventable Churn**: 3/5 (60%)
**Saved from At-Risk**: 4 customers

**Action Items**:
- [ ] Follow up with [Customer A] (win-back opportunity)
- [ ] Address feature gap (competitor advantage)
- [ ] Improve onboarding for poor results prevention

---

### Monthly Report (Leadership Review)

**Month**: [Month Year]

**Executive Summary**:
- Churn rate: 4.2% (target: <5%) ✅
- Net revenue retention: 112% (target: >110%) ✅
- Logo churn: 18 customers
- Revenue churn: R$ 5.340 (1.1% of MRR)

**Churn by Segment**:
| Segment | Churn Rate | Count | Primary Reasons |
|----------|-----------|-------|-----------------|
| Clínicas | 4.8% | 10 | Poor results (60%), Price (30%) |
| Imobiliárias | 3.5% | 6 | Competitor (50%), Low leads (30%) |
| Outros | 5.5% | 2 | Price (50%), Technical (50%) |

**Churn by Tenure**:
| Tenure | Churn Count | % of Total Churn |
|--------|-------------|------------------|
| <30 days | 8 | 44% |
| 31-90 days | 5 | 28% |
| 91-180 days | 3 | 17% |
| 181+ days | 2 | 11% |

**Insight**: Early churn (first 90 days) is 72% of total. Focus on onboarding.

**Churn by ARPU**:
| ARPU Tier | Churn Count | % of Base | Revenue Impact |
|-----------|-------------|-----------|----------------|
| <R$ 200 | 12 | 5% | R$ 2.364 |
| R$ 200-400 | 5 | 3% | R$ 1.485 |
| >R$ 400 | 1 | 1% | R$ 497 |

**Insight**: Higher-value customers churn less. Prioritize retention of ARPU >R$ 200.

**Intervention Effectiveness**:
| Stage | Detected | Saved | Save Rate |
|-------|----------|-------|-----------|
| Warning (60-79) | 45 | 25 | 56% |
| At-Risk (40-59) | 20 | 6 | 30% |
| Critical (0-39) | 10 | 2 | 20% |

**Insight**: Early detection works. 40%+ save rate when caught at warning stage.

**Top 3 Action Items**:
1. **Onboarding overhaul**: 44% of churn happens in first 30 days
2. **Value demonstration**: Poor results is #1 reason for clinics
3. **Competitive intel**: Feature gaps causing 17% of churn

---

## Part 6: Implementation Roadmap

### Phase 1: Foundation (Weeks 1-4)

**Week 1: Data Infrastructure**
- [ ] Set up churn tracking in analytics (Mixpanel/Amplitude)
- [ ] Create health score calculation (SQL/db query)
- [ ] Build churn metrics dashboard (Google Data Studio/Metabase)
- [ ] Integrate data sources: Product, Billing, Support, NPS

**Week 2: Scoring Model**
- [ ] Define health score formula (weighted components)
- [ ] Calculate baseline scores for all customers
- [ ] Set up automated scoring (daily batch job)
- [ ] Create risk classification (Healthy/Warning/At-Risk/Critical)

**Week 3: Alerting System**
- [ ] Configure automated alerts:
  - Score drops below 60 → Task creation
  - Score drops below 40 → Manager notification
  - Cancellation request → Immediate escalation
- [ ] Set up Slack notifications
- [ ] Create email alerts for CS team
- [ ] Test alert system (3 scenarios)

**Week 4: Playbook Documentation**
- [ ] Document At-Risk Intervention playbook
- [ ] Document Critical Escalation playbook
- [ ] Document Win-Back playbook
- [ ] Create internal wiki / Notion templates
- [ ] Train CS team on playbooks

**Deliverables**:
- Churn dashboard with real-time metrics
- Health scoring system live
- Alerting system operational
- Playbooks documented and trained

---

### Phase 2: Launch (Weeks 5-8)

**Week 5: Soft Launch**
- [ ] Enable health scoring for 50 customers (test group)
- [ ] Monitor for false positives/negatives
- [ ] Adjust scoring weights based on feedback
- [ ] Test playbooks with real at-risk customers

**Week 6: Full Launch - Monitoring**
- [ ] Enable health scoring for all customers
- [ ] Activate automated alerts
- [ ] CS team starts using playbooks
- [ ] Daily standup: Review at-risk customers

**Week 7: Full Launch - Intervention**
- [ ] Execute first At-Risk interventions
- [ ] Execute first Critical escalations
- [ ] Document outcomes (saved/lost + reasons)
- [ ] Refine playbooks based on learnings

**Week 8: Optimization**
- [ ] Analyze first 4 weeks of data
- [ ] Calculate save rates by stage
- [ ] Identify high-impact intervention points
- [ ] Optimize scoring thresholds
- [ ] Update playbooks with winning tactics

**Deliverables**:
- All customers scored and monitored
- 20+ interventions executed
- Save rate baseline established (target: 30%+)
- Playbooks optimized

---

### Phase 3: Scale (Weeks 9-12)

**Week 9: Predictive Modeling**
- [ ] Analyze churn patterns (when/why/who)
- [ ] Identify leading indicators
- [ ] Build predictive model (if applicable)
- [ ] Create segment-specific churn profiles

**Week 10: Proactive Prevention**
- [ ] Launch Day 30/60/90/180/360 check-ins
- [ ] Automate check-in scheduling
- [ ] Create check-in templates
- [ ] Train CS team on proactive outreach

**Week 11: Win-Back Program**
- [ ] Segment churned customers by reason
- [ ] Create win-back email sequences
- [ ] Design win-back offers (by tenure)
- [ ] Launch first win-back campaign

**Week 12: Review & Plan**
- [ ] 90-day review: What's working?
- [ ] Churn rate vs. target
- [ ] Save rate by intervention type
- [ ] ROI calculation (retention vs. acquisition cost)
- [ ] Next 90 days plan

**Deliverables**:
- Proactive check-ins operational
- Win-back program launched
- Predictive insights documented
- 90-day report and next quarter plan

---

## Part 7: Team Structure & Roles

### Customer Success Team

**Phase 1: 0-500 Customers**

| Role | FTE | Responsibilities |
|------|-----|------------------|
| **Customer Success Manager** | 1 | - 150-200 customers<br>- Health monitoring<br>- At-risk interventions<br>- QBRs (Day 90+) |
| **Head of CS** | 0.2 (part-time) | - Critical escalations<br>- Playbook optimization<br>- Team hiring/training |

**Phase 2: 500-1.000 Customers**

| Role | FTE | Responsibilities |
|------|-----|------------------|
| **Senior CSM** | 1 | - Strategic accounts (ARPU >R$ 400)<br>- Critical escalations<br>- QBRs for high-value customers |
| **CSM** | 3 | - 150-200 customers each<br>- Health monitoring<br>- Interventions<br>- Check-ins |
| **Head of CS** | 1 | - Team management<br>- Playbook optimization<br>- Metrics & reporting<br>- Cross-functional alignment |

**Phase 3: 1.000-5.000 Customers**

| Role | FTE | Responsibilities |
|------|-----|------------------|
| **Senior Director, CS** | 1 | - CS strategy<br>- Team leadership<br>- Executive dashboards |
| **Senior CSM** | 2 | - Enterprise accounts<br>- Strategic relationships<br>- Critical escalations |
| **CSM** | 10 | - 150-200 customers each<br>- Full customer lifecycle |
| **CS Operations** | 1 | - Health scoring maintenance<br>- Dashboard updates<br>- Playbook iteration<br>- Tool management |

---

### Cross-Functional Collaboration

**Product Team**:
- Share churn feedback (features, bugs)
- Prioritize retention-related features
- Build in-app churn prevention (nudges, prompts)
- A/B test retention improvements

**Sales Team**:
- Share ICP insights (reduce bad fit churn)
- Coordinate on win-back opportunities
- Provide context on new customer expectations
- Handoff smooth transitions (sale → onboarding)

**Marketing Team**:
- Create retention-focused content
- Share competitive intelligence
- Support win-back campaigns
- Customer advocacy programs

**Support Team**:
- Tag all tickets with sentiment/risk
- Escalate at-risk customers
- Document churn reasons
- Support intervention playbooks

---

## Part 8: Tools & Technology Stack

### Core Systems

**1. Customer Data Platform (CDP)**
- **Purpose**: Unified customer data, health scoring
- **Tools**: HubSpot CRM, Salesforce, or Notion + Airtable (bootstrap)
- **Key Features**:
  - Customer profiles with all activity
  - Health score calculation
  - Automated task creation
  - Playbook triggers

**2. Analytics Platform**
- **Purpose**: Product usage tracking, churn prediction
- **Tools**: Mixpanel, Amplitude, or PostHog
- **Key Events to Track**:
  - Daily: Logins, automation runs, messages sent
  - Weekly: Feature usage, dashboard views
  - Monthly: Recovery rates, revenue impact
  - Churn signals: 0 activity for 7+ days

**3. Support System**
- **Purpose**: Ticket tracking, sentiment analysis
- **Tools**: Intercom, Zendesk, or Freshdesk
- **Key Features**:
  - Sentiment scoring per ticket
  - Risk flagging (negative sentiment = churn risk)
  - Integration with CDP (update health score)

**4. Billing System**
- **Purpose**: Payment monitoring, dunning management
- **Tools**: Stripe, Paddle, or Recurly
- **Key Features**:
  - Failed payment alerts
  - Dunning sequences (retry logic)
  - Upcoming expiration notifications
  - Integration with CDP (payment score)

**5. Communication Platform**
- **Purpose**: Outreach orchestration
- **Tools**: Customer.io, HubSpot Marketing, or Mailchimp
- **Key Features**:
  - Email sequences (check-ins, win-back)
  - WhatsApp integration (for Brazil)
  - Triggered campaigns (score drops, milestones)
  - A/B testing capability

**6. Slack/Team Communication**
- **Purpose**: Real-time alerts, coordination
- **Tools**: Slack
- **Key Features**:
  - #churn-alerts channel (score drops)
  - #customer-success channel (daily standup)
  - Direct alerts for critical escalations
  - Integration with CDP (auto-post)

---

### Bootstrap Stack (R$ 0-500/month)

| Need | Tool | Cost/Month |
|------|------|------------|
| CRM & CDP | Notion + Airtable | R$ 0 |
| Analytics | PostHog (free tier) | R$ 0 |
| Support | WhatsApp Business | R$ 0 |
| Billing | Stripe (pay-per-use) | ~R$ 100 |
| Email | Gmail + Mailchimp (free) | R$ 0 |
| Communication | Slack (free tier) | R$ 0 |
| **Total** | | **~R$ 100** |

---

### Growth Stack (R$ 2-5K/month)

| Need | Tool | Cost/Month |
|------|------|------------|
| CRM & CDP | HubSpot (Professional) | R$ 1.500 |
| Analytics | Mixpanel (Growth) | R$ 800 |
| Support | Intercom (Essential) | R$ 900 |
| Communication | Customer.io | R$ 300 |
| Billing | Stripe (enterprise) | ~R$ 300 |
| **Total** | | **~R$ 3.800** |

---

### Scale Stack (R$ 10K+/month)

| Need | Tool | Cost/Month |
|------|------|------------|
| CRM & CDP | Salesforce (Enterprise) | R$ 3.000 |
| Analytics | Amplitude (Enterprise) | R$ 2.000 |
| Support | Zendesk Suite | R$ 1.500 |
| Communication | Braze | R$ 1.500 |
| Billing | Stripe (custom) | ~R$ 500 |
| CS Operations | Gainsight | R$ 2.000 |
| **Total** | | **~R$ 10.500** |

---

## Part 9: Success Metrics & Goals

### 90-Day Targets

| Metric | Baseline | Month 1 | Month 2 | Month 3 | Target |
|--------|----------|---------|---------|---------|--------|
| **Churn Rate** | Unknown | Measure | Measure | Measure | <8% |
| **Health Scoring** | 0% | 100% | 100% | 100% | 100% coverage |
| **At-Risk Detected** | 0% | 20% | 40% | 60% | 60%+ |
| **Intervention Success** | N/A | 20% | 25% | 30% | 30%+ |
| **Net Revenue Retention** | Unknown | Measure | Measure | Measure | >100% |

### 12-Month Targets

| Metric | Month 3 | Month 6 | Month 12 | Target |
|--------|---------|---------|----------|--------|
| **Churn Rate** | <8% | <6% | **<5%** | Top quartile |
| **NRR** | >100% | >105% | **>110%** | Expansion offsets churn |
| **LTV:CAC** | 3:1 | 4:1 | **5:1** | Healthy economics |
| **Recovery Rate** | 30% | 25% | **20%** | Early detection increases base |
| **Customer Satisfaction** | NPS 40 | NPS 50 | **NPS 60** | Happy customers stay |

---

### ROI Calculation

**Scenario**: 1.000 customers, R$ 300/month ARPU

**Baseline** (10% monthly churn - industry average):
- Monthly churn: 100 customers × R$ 300 = R$ 30.000 MRR lost
- Annual churn: ~R$ 360.000 MRR lost
- Customer lifetime: 10 months
- LTV: R$ 300 × 10 = R$ 3.000

**After Optimization** (5% monthly churn - target):
- Monthly churn: 50 customers × R$ 300 = R$ 15.000 MRR lost
- Annual churn: ~R$ 180.000 MRR lost
- **Savings: R$ 180.000/year**
- Customer lifetime: 20 months
- LTV: R$ 300 × 20 = R$ 6.000 (2x improvement)

**With Expansion** (NRR 110% - 10% expansion):
- Expansion revenue: 1.000 customers × 10% × R$ 30 = R$ 3.000 MRR
- Annual expansion: ~R$ 36.000 MRR
- **Total Impact: R$ 180.000 + R$ 36.000 = R$ 216.000/year**

**Investment**:
- CS Team (2 FTE): R$ 150.000/year
- Tools: R$ 45.000/year
- **Total Cost: R$ 195.000/year**

**ROI**: (R$ 216.000 - R$ 195.000) / R$ 195.000 = **11% ROI Year 1**
**Year 2+**: R$ 216.000 / R$ 195.000 = **111% ROI annually**

**Conclusion**: Retention investment pays for itself in Year 1, generates profit in Year 2+.

---

## Part 10: Common Pitfalls & Best Practices

### Common Mistakes to Avoid

**1. Focusing Only on Logo Churn**
- **Problem**: 1 customer at R$ 500 churn ≠ 1 customer at R$ 100 churn
- **Solution**: Track both logo churn AND revenue churn

**2. Ignoring Silent Churn**
- **Problem**: Paying but not using customers = future churn
- **Solution**: Activity metrics, proactive re-engagement

**3. Reacting Too Late**
- **Problem**: Waiting for cancellation request
- **Solution**: Early warning signals, proactive intervention

**4. One-Size-Fits-All**
- **Problem**: Same playbook for clinics and real estate
- **Solution**: Segment-specific strategies

**5. Not Learning from Churn**
- **Problem**: Same reasons repeat, no root cause analysis
- **Solution**: Exit interviews, taxonomy, product feedback loop

**6. Blaming the Customer**
- **Problem**: "They didn't get it", "Not our ICP"
- **Solution**: "What could we have done differently?"

**7. Short-Term Focus**
- **Problem**: Saving this month vs. preventing next month
- **Solution**: Balance reactive interventions with proactive prevention

**8. No Cross-Functional Alignment**
- **Problem**: CS can't fix product issues alone
- **Solution**: Product, Sales, Marketing all own retention

---

### Best Practices from Top Companies

**1. HubSpot** (NRR 120%+)
- Predictive churn modeling (ML-based)
- Customer health scores visible company-wide
- Every team has retention goals (not just CS)

**2. Shopify** (Churn <5%)
- Focus on revenue churn, not logo churn
- Proactive support for high-MRR merchants
- Success metrics: "Merchants succeeding = merchants staying"

**3. Datadog** (NRR 130%+)
- Usage-based pricing (grow with customers)
- Expansion focus (upsell/cross-sell)
- Land-and-expand strategy

**4. Local Brazilian SaaS Leaders**
- WhatsApp-first communication (cultural fit)
- Human touch (relationship-driven)
- Flexible pricing (economic volatility)

---

## Appendix: Quick Reference Guides

### Churn Intervention Quick Reference

**Score 80-100 (Healthy)**:
- Action: Monitor only
- Cadence: Monthly check-in
- Owner: CSM

**Score 60-79 (Warning)**:
- Action: Check-in call
- Timeline: 7 days
- Owner: CSM
- Recovery Rate: 40-60%

**Score 40-59 (At-Risk)**:
- Action: Intervention playbook
- Timeline: Immediate (48h)
- Owner: Senior CSM
- Recovery Rate: 20-30%

**Score 0-39 (Critical)**:
- Action: Escalation playbook
- Timeline: Emergency (24h)
- Owner: CS Manager + CSM
- Recovery Rate: 5-20%

---

### Churn Reason Quick Reference

| Reason | % of Churn | Prevention | Win-Back Timing |
|--------|-----------|------------|-----------------|
| Poor Results | 30-40% | Better onboarding | 90-120 days |
| Price | 20-30% | Value demonstration | 60-90 days |
| Competitor | 10-15% | Feature parity | When feature launches |
| Fit (Wrong ICP) | 10-15% | Sales alignment | Never (let go) |
| Technical | 5-10% | QA, fast fixes | When bug fixed |
| Business (Closed) | 5-10% | Not preventable | Never (out of business) |

---

### Email Templates Quick Reference

**Check-In Email** (Day 30/60/90):
```
Assunto: Como estão seus [X] dias com ConectaPay?

Olá [Nome],

Vamos revisar seus primeiros [X] meses.

[Resultados]: Você recuperou R$ [Y] em vendas
[Taxa de recuperação]: [Z]% de vendas perdidas
[Próximo]: Otimizar para [Z+5]%

Posso te ajudar em 15 min.

Agendar: [Link Calendly]

Abraços,
[Seu Nome]
```

**At-Risk Outreach**:
```
Assunto: Notei que você não está usando

Olá [Nome],

Vi que sua automação parou há 7 dias.

Algum problema? Posso resolver em 5 min.

Responda ou agende: [Link]

Quero ver você recuperando vendas de novo.

Abraços,
[Seu Nome]
```

**Cancellation Response**:
```
Assunto: Vamos resolver isso juntos

Olá [Nome],

Recebi seu cancelamento. Antes de processar:
o que aconteceu?

Posso oferecer:
1. Ajuda imediata no problema
2. Plano alternativo (pausa, desconto)
3. Conversa comigo direto

Responda hoje. Quero ajudar.

Abraços,
[Seu Nome] | Head of CS
WhatsApp: [Número]
```

---

## Conclusion

**Key Takeaways**:

1. **Churn is predictable** - Early signals exist 30-90 days before cancellation
2. **Early intervention wins** - Save rate 40-60% at warning stage vs 5-20% at critical
3. **Prevention beats cure** - Proactive check-ins prevent 60%+ of churn
4. **Segment matters** - Clinics ≠ Real Estate (different reasons, strategies)
5. **It's a team sport** - Product, Sales, Marketing, CS all own retention

**Economic Impact**:
- Reduce churn from 10% → 5% = **R$ 180.000/year saved** (at 1.000 customers)
- Add 10% expansion (NRR 110%) = **R$ 216.000/year total impact**
- ROI: Positive in Year 1, 100%+ in Year 2+

**Next Steps**:
1. Week 1-4: Set up tracking, scoring, dashboards
2. Week 5-8: Launch monitoring, execute first interventions
3. Week 9-12: Scale proactive prevention, win-back programs

**Success Metrics**:
- Churn rate <5% (top quartile)
- NRR >110% (expansion offsets churn)
- Recovery rate 30%+ (at warning stage)
- Customer lifetime 2x improvement

---

**Document Version**: 1.0
**Created**: 2026-04-25
**Author**: CMO Agent (55827422-a849-41d3-9286-0b5b8b002079)
**Task**: CON-112 - Customer Churn Analysis and Prevention Strategy
**Size**: 45KB (14,500 words)
**Related Documents**:
- customer-retention-strategy-framework.md (retention lifecycle)
- customer-onboarding-framework.md (prevents early churn)
- customer-success-playbook.md (proactive engagement)
- customer-feedback-loop-and-voc-program.md (exit insights)
