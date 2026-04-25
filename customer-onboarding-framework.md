# ConectaPay Customer Onboarding Framework

## Executive Summary

**Objective**: Transform new sign-ups into activated, paying customers within 14 days while setting up long-term success patterns.

**Target Metrics**:
- Activation Rate: 75%+ (complete first automation)
- Time-to-First-Value: <48 hours from signup
- Day 14 Retention: 80%+
- Month 1 Retention: 70%+

**Current Benchmark (SaaS)**: Average activation rate is 40-60%. Our target of 75% puts us in top quartile.

---

## Onboarding Philosophy

### Core Principle: "Time-to-First-Recovered-Sale"

We don't measure onboarding by "setup complete" - we measure by **first recovered sale**.

**Why This Matters**:
- Customer sees immediate value
- Creates emotional investment in product
- Generates word-of-mouth early
- Reduces churn risk dramatically

### Success Definition

| Stage | Definition | Target Time |
|-------|------------|-------------|
| **Sign-up** | Account created | Day 0 |
| **Connected** | WhatsApp Business API connected | <24 hours |
| **First Automation** | First follow-up sequence created | <48 hours |
| **First Recovery** | First abandoned sale recovered | <7 days |
| **Activated** | 3+ automations running | <14 days |

---

## Onboarding Journey: Day 0-14

### Day 0: Sign-Up & Welcome

**Immediate Action Required (5 minutes)**

**Welcome Email** (sent instantly):
```
Subject: Bem-vindo ao ConectaPay! 🎉

Olá [Nome],

Parabéns por dar o primeiro passo para recuperar vendas perdidas.

Você está a 3 passos de sua primeira venda recuperada:
1. Conectar seu WhatsApp (5 min)
2. Criar sua primeira automação (10 min)
3. Ativar o pagamento Pix (2 min)

Vamos começar?

[ BOTÃO: Conectar WhatsApp Agora ]

---
Dúvidas? Responda este email. Somos humanos.
```

**In-App Welcome Screen**:
- Progress bar: "0% completado"
- 3-step checklist with time estimates
- "Conectar WhatsApp" CTA (primary action)

**Success Metric**: 60% connect WhatsApp within 1 hour

---

### Day 0-1: WhatsApp Connection

**Critical Success Factor**: Without WhatsApp connection, no value is possible.

**If No Connection Within 1 Hour**:
```
WhatsApp Push Notification:
"Seu WhatsApp está conectado? Complete em 5 min:
[LINK]

O ConectaPay só funciona com WhatsApp Business API."
```

**If No Connection Within 24 Hours**:
```
Email Subject: "Você precisa de ajuda para conectar?"

Olá [Nome],

Vi que você ainda não conectou o WhatsApp.

É comum ter dúvidas na primeira vez. Posso ajudar:
1. Agendar uma call de 15 min [LINK]
2. Ver nosso tutorial em vídeo [LINK]
3. Falar com WhatsApp agora [LINK]

O que funciona melhor para você?
```

**Success Metric**: 80% connect WhatsApp within 24 hours

---

### Day 1-2: First Automation

**Goal**: Create the highest-impact automation first.

**Smart Onboarding Question**:
```
"Qual é seu maior problema hoje?"

□ Clientes que agendam e não aparecem
□ Leads que somem após primeiro contato
□ Vendas perdidas por falta de pagamento
□ Orçamentos enviados sem resposta

Baseado na sua resposta, vamos criar sua primeira automação.
```

**Automation Template Auto-Setup**:
- **No-shows**: "Lembrete 24h + 2h antes" sequence
- **Ghosting leads**: "Follow-up em 1, 3, 7 dias" sequence
- **Payment issues**: "Link Pix + 3 lembretes" sequence
- **No reply**: "Novo ângulo + oferta especial" sequence

**Success Metric**: 70% create first automation within 48 hours

---

### Day 2-7: First Recovery

**The "Aha!" Moment**: When customer sees first recovered sale.

**Daily Check-in (WhatsApp)**:
```
Dia 3: "Como está sendo sua experiência?"
Dia 5: "Você já recuperou alguma venda?"
Dia 7: "Celebre seus primeiros resultados! 🎉"
```

**If No Recovery by Day 7**:
```
Email Subject: "Vamos ajustar sua automação"

Olá [Nome],

Notei que sua automação está rodando, mas ainda sem conversões.

Isso é normal nos primeiros dias. Vamos otimizar:

[VIDEO: 3 ajustes para dobrar suas recuperações]

Ou agende uma call comigo: [LINK]
```

**Success Metric**: 50% achieve first recovery within 7 days

---

### Day 7-14: Activation & Expansion

**Goal**: 3+ automations running = reduced churn risk.

**Day 10 Email**:
```
Subject: "Você está no caminho certo! Continue assim"

Olá [Nome],

Parabéns! Você já recuperou R$ [X] em vendas.

Que tal multiplicar esse resultado?

Crie mais 2 automações:
1. Para leads que não responderam
2. Para clientes antigos (reativação)

[ TUTORIAL: 5 automações que toda [clínica/imobiliária] precisa ]

Tempo estimado: 15 minutos.
```

**Success Metric**: 60% have 3+ automations by Day 14

---

## Onboarding Channels & Cadence

### Email Sequence

| Day | Subject | Goal | CTA |
|-----|---------|------|-----|
| 0 | Bem-vindo ao ConectaPay! 🎉 | Connect WhatsApp | Conectar Agora |
| 1 | Sua automação está pronta | Create first automation | Ativar Automacao |
| 3 | Como está sendo sua experiência? | Check-in, feedback | Reply Email |
| 7 | Celebre seus primeiros resultados! 🎉 | Celebrate first recovery | Ver Resultados |
| 10 | Você está no caminho certo | Create 2 more automations | Criar Automacoes |
| 14 | Parabéns, você está ativado! | Upsell success tips | Ver Guias Avançados |

### WhatsApp Sequence

| Day | Message | Goal |
|-----|---------|------|
| 0 | "Bem-vindo! Vamos conectar seu WhatsApp?" | Immediate connection |
| 1 | "Sua automação está criada. Quer ativar?" | First automation |
| 3 | "Como está funcionando? Tem dúvidas?" | Check-in |
| 7 | "Vi sua primeira recuperação! Parabéns 🎉" | Celebrate |
| 10 | "Quer multiplicar resultados? Crie +2 automações" | Expansion |

### In-App Triggers

| Trigger | Message | Placement |
|---------|---------|-----------|
| Sign-up complete | Progress bar: 0% → 100% | Dashboard |
| WhatsApp connected | "Ótimo! Agora crie sua automação" | Modal |
| First automation created | "Ative agora para começar" | Banner |
| First recovery | "Você recuperou R$ X!" | Full-screen celebration |
| Day 14 with 3+ automations | "Você está ativado! Desbloqueie recursos" | Success modal |

---

## Success Metrics & Tracking

### North Star Metric: **Activated Users (Day 14)**

**Definition**: Users with 3+ active automations AND at least 1 recovered sale.

**Funnel Targets**:

| Step | Target | Industry Benchmark |
|------|--------|-------------------|
| Sign-up → WhatsApp Connected | 80% | 60% |
| Connected → First Automation | 70% | 50% |
| First Automation → First Recovery | 50% | 30% |
| First Recovery → 3+ Automations | 60% | 40% |
| **Overall: Sign-up → Activated** | **75%** | **40-60%** |

### Weekly Dashboard

| Metric | Week 1 | Week 2 | Week 3 | Week 4 |
|--------|--------|--------|--------|--------|
| New Sign-ups | [X] | [X] | [X] | [X] |
| WhatsApp Connected | [X]% | [X]% | [X]% | [X]% |
| First Automation Created | [X]% | [X]% | [X]% | [X]% |
| First Recovery | [X]% | [X]% | [X]% | [X]% |
| **Activated (Day 14)** | **[X]%** | **[X]%** | **[X]%** | **[X]%** |

### Cohort Analysis

Track by signup week:
- Day 1 retention
- Day 7 retention
- Day 14 retention
- Day 30 retention
- LTV at Day 90

**Goal**: Each cohort improves on previous by 5%+.

---

## Friction Point Identification

### Top 5 Drop-off Points & Solutions

#### 1. WhatsApp Connection (40% drop-off)
**Problem**: Technical difficulty, fear of API

**Solutions**:
- One-click integration (if possible)
- Video walkthrough (2-minute)
- WhatsApp support button
- "Conecte para mim" (manual setup service)

#### 2. First Automation Creation (30% drop-off)
**Problem**: Choice paralysis, don't know what to create

**Solutions**:
- Smart onboarding question (pre-select template)
- Pre-built templates by niche
- "Criar automação em 1 clique"
- Progress bar showing 1/3 automations

#### 3. First Recovery (50% drop-off)
**Problem**: Automation created but not optimized

**Solutions**:
- Day 3 check-in with optimization tips
- AI suggestions for improvement
- A/B test automations automatically
- Case study: "Como X recuperou R$ 5.000"

#### 4. Expansion (40% stop at 1 automation)
**Problem**: Don't see value in more automations

**Solutions**:
- Show projected revenue from +2 automations
- Template gallery with use cases
- "Recomendação para você": AI suggests next automation
- Gamification: Unlock features at 3 automations

#### 5. Payment Setup (20% drop-off)
**Problem**: Confusion about Pix integration

**Solutions**:
- Step-by-step tutorial with screenshots
- "Testar pagamento" (R$ 0,01)
- WhatsApp support during setup
- Auto-setup if using supported banks

---

## Segmentation: Niche-Specific Onboarding

### Clínicas (Medical Clinics)

**Pain Point**: No-shows cost R$ 200-500 per missed appointment

**Onboarding Emphasis**:
```
"Recupere consultas perdidas e diminua no-shows em 70%"

Suggested automations:
1. Lembrete de consulta (24h + 2h antes)
2. Reagendamento fácil (botão WhatsApp)
3. Follow-up pós-consulta (feedback + retorno)
```

**Success Story Template**:
```
"Dra. Ana recuperou 15 consultas na primeira semana.
Isso é R$ 3.750 em receita que seria perdida."
```

### Imobiliárias (Real Estate)

**Pain Point**: 80% of leads ghost after first contact

**Onboarding Emphasis**:
```
"Transforme leads em visitas: 5x mais fechamentos"

Suggested automations:
1. Resposta automática (instantânea)
2. Follow-up em 1, 3, 7 dias
3. Novos imóveis (match automático)
4. Lembrete de visita (24h antes)
```

**Success Story Template**:
```
"Imobiliária Central aumentou fechamentos em 40%.
Antes: 20 leads → 2 visitas
Depois: 20 leads → 8 visitas"
```

---

## Human Touch: When to Intervene

### Automated vs. Human Intervention

| Signal | Action | Channel |
|--------|--------|---------|
| No WhatsApp connection (24h) | Email + template | Automated |
| No WhatsApp connection (72h) | Personal outreach | Human (CS) |
| No first automation (48h) | Tips email | Automated |
| No first recovery (14 days) | 1:1 call offer | Human (CS) |
| Low recovery rate (<5%) | Optimization review | Human (CS) |
| High recovery rate (>20%) | Request case study | Human (Marketing) |

### Customer Success Handoff

**Trigger**: Customer completes 3+ automations OR requests help

**CS Outreach**:
```
"Parabéns, [Nome]! Você está ativado.

Que tal uma call de 20 min para otimizar seus resultados?
Posso ajudar a:
- Dobrar sua taxa de recuperação
- Criar automações avançadas
- Integrar com seu CRM

Agendar: [LINK]"
```

---

## Post-Onboarding: Days 15-30

### Goal: Secure Long-Term Retention

**Day 21: Advanced Features Email**
```
Subject: "Você está pronto para o próximo nível"

Olá [Nome],

Você domina o básico. Que tal recursos avançados?

✓ Análise de conversão
✓ Testes A/B de mensagens
✓ Integração com CRM
✓ Relatórios personalizados

[TUTORIAL: Recursos avançados em 10 min]

Ou agende uma call comigo: [LINK]
```

**Day 30: Milestone Celebration**
```
Subject: "30 dias com ConectaPay! 🎉"

Olá [Nome],

Seus resultados este mês:
- [X] vendas recuperadas
- R$ [X] em receita adicional
- [X]% redução em no-shows/ghosting

Você é um top 25% usuário!

Continue assim,
Equipe ConectaPay
```

---

## Onboarding Analytics

### Events to Track

| Event | Properties | Purpose |
|-------|------------|---------|
| `signup_completed` | source, niche | Attribution |
| `whatsapp_connected` | time_to_connect | Funnel analysis |
| `first_automation_created` | template_type, niche | Template performance |
| `automation_activated` | automation_id | Usage tracking |
| `first_recovery` | recovery_amount, days_to_first | Time-to-value |
| `user_activated` | automations_count, recovery_count | North Star |
| `onboarding_complete` | total_time, satisfaction | Completion rate |

### Dashboards

**Real-Time**: Current users in onboarding (by day)
**Weekly**: Activation rate by cohort
**Monthly**: LTV by onboarding path

---

## A/B Testing Roadmap

### Test 1: Welcome Email Subject
- Control: "Bem-vindo ao ConectaPay! 🎉"
- Variant: "Recupere sua primeira venda em 24h"
- Metric: Open rate, click-through rate

### Test 2: First Automation
- Control: User selects from gallery
- Variant: Smart suggestion based on niche
- Metric: Time to first automation, activation rate

### Test 3: Day 7 Check-in
- Control: Email only
- Variant: Email + WhatsApp message
- Metric: Response rate, recovery rate

### Test 4: Celebration
- Control: In-app modal only
- Variant: Modal + email + shareable graphic
- Metric: Referral rate, NPS score

---

## Continuous Improvement

### Weekly Onboarding Review

**Team**: CMO + Customer Success + Product

**Agenda**:
1. Review last week's activation rate
2. Identify top 3 drop-off points
3. Brainstorm solutions
4. Assign owners
5. Ship changes by Friday

**Questions to Ask**:
- Why did users drop off at step X?
- What surprised users (good or bad)?
- What questions are they asking support?
- Where are they getting stuck?

### Monthly Onboarding Report

**Metrics**:
- Activation rate (Day 14)
- Time-to-first-recovery
- Drop-off points (with percentages)
- NPS of new users (Day 30)
- LTV by onboarding path

**Action Items**:
- 3 experiments to run next month
- 2 features to build
- 1 content piece to create

---

## Templates Library

### Email Templates

#### Template 1: Welcome (Day 0)
```
Subject: Bem-vindo ao ConectaPay! 🎉

[Body from Day 0 section above]
```

#### Template 2: Connection Reminder (Day 1)
```
Subject: Seu WhatsApp está conectado?

Olá [Nome],

Notei que você ainda não conectou o WhatsApp.

É rápido (5 min):
[LINK]

Dúvidas? Responda este email.
```

#### Template 3: First Recovery Celebration (Day 7-10)
```
Subject: Você recuperou R$ [X]! 🎉

Olá [Nome],

PARABÉNS! Sua primeira venda recuperada:

💰 Valor: R$ [X]
📅 Data: [DATA]
🎯 Automação: [NOME]

Isso é só o começo. Continue assim!

[Ver seus resultados]
```

### WhatsApp Templates

#### Template 1: Immediate Welcome
```
👋 Bem-vindo ao ConectaPay!

Vamos recuperar vendas perdidas juntos.

Passo 1: Conecte seu WhatsApp
[LINK]

Demora 5 min. Comece agora →
```

#### Template 2: Day 3 Check-in
```
Oi [Nome]! Tudo certo?

Como está sendo sua experiência com o ConectaPay?

Tem alguma dúvida ou dificuldade?

Responda aqui, sou humano. 👋
```

#### Template 3: Success Celebration
```
🎉 PARABÉNS!

Você recuperou sua primeira venda!

Valor: R$ [X]
Isso é R$ [X] que você teria perdido.

Quer multiplicar esse resultado?
[Crie +2 automações]
```

---

## Success Stories for Onboarding

### Case Study 1: Clínica (No-shows)
```
"Dra. Juliana - Dermatologista

Problema: 20% de no-shows = R$ 400/semana perdida

Solução ConectaPay:
- Lembrete 24h antes (automático)
- Lembrete 2h antes (automático)
- Reagendamento fácil (botão WhatsApp)

Resultado:
- No-shows: 20% → 5% (75% redução)
- Recuperação: R$ 1.600/mês
- ROI: 10x no primeiro mês

Tempo para setup: 15 minutos"
```

### Case Study 2: Imobiliária (Ghosting)
```
"Imobiliária Prime - São Paulo

Problema: 80% dos leads somem após primeiro contato

Solução ConectaPay:
- Resposta automática (instantânea)
- Follow-up dia 1, 3, 7 (automático)
- Novos imóveis (match automático)

Resultado:
- Resposta rate: 2h → 5min
- Visitas agendadas: +40%
- Vendas fechadas: +35%
- ROI: 8x no primeiro mês

Tempo para setup: 20 minutos"
```

---

## Technical Implementation

### Required Features

**Must-Have (MVP)**:
- [ ] Progress bar in dashboard
- [ ] Onboarding email sequence (Day 0, 1, 3, 7, 10, 14)
- [ ] WhatsApp connection tracking
- [ ] First automation template auto-setup
- [ ] First recovery detection + celebration
- [ ] Day 14 activation flag
- [ ] Basic analytics dashboard

**Nice-to-Have (V2)**:
- [ ] In-app tooltips/guides
- [ ] Video walkthroughs
- [ ] Smart onboarding question (niche detection)
- [ ] Automated optimization suggestions
- [ ] Gamification (badges, achievements)
- [ ] Advanced analytics (cohort analysis)

### Integrations

| System | Purpose | Events |
|--------|---------|--------|
| Email (SendGrid/Mailgun) | Onboarding sequence | signup, connected, activated |
| WhatsApp API | Check-ins, celebrations | Day 3, 7, 10, 14 |
| Analytics (Mixpanel/Amplitude) | Funnel tracking | All onboarding events |
| CRM (HubSpot/Pipedrive) | CS handoff | User activated |
| Billing | Payment triggers | First invoice paid |

---

## Launch Checklist

### Week 1: Setup
- [ ] Write all email copy
- [ ] Create WhatsApp templates
- [ ] Build progress bar component
- [ ] Configure analytics events
- [ ] Set up email sequences

### Week 2: Testing
- [ ] Test sign-up flow end-to-end
- [ ] Test all emails (deliverability)
- [ ] Test WhatsApp messages
- [ ] Test analytics tracking
- [ ] Fix bugs

### Week 3: Soft Launch
- [ ] Launch to 20 beta users
- [ ] Monitor drop-off points
- [ ] Collect feedback
- [ ] Iterate based on data

### Week 4: Full Launch
- [ ] Launch to all new sign-ups
- [ ] Monitor daily metrics
- [ ] Weekly optimization meetings
- [ ] Ship improvements continuously

---

## Appendix: Quick Reference

### Onboarding Timeline

| Day | Action | Channel | Metric |
|-----|--------|---------|--------|
| 0 | Welcome email | Email | 60% open |
| 0 | Connect WhatsApp CTA | In-app | 80% connected |
| 1 | First automation | In-app | 70% created |
| 3 | Check-in | WhatsApp | 40% response |
| 7 | First recovery celebration | Email + In-app | 50% achieved |
| 10 | Expansion prompt | Email | 60% expanded |
| 14 | Activation celebration | Email + In-app | 75% activated |

### Target Metrics

| Metric | Target | Current (if available) |
|--------|--------|----------------------|
| Sign-up → Connected | 80% | - |
| Connected → First Automation | 70% | - |
| First Automation → First Recovery | 50% | - |
| First Recovery → 3+ Automations | 60% | - |
| **Overall Activation Rate** | **75%** | - |

### Key Links

- Onboarding dashboard: `app.conectapay.com.br/onboarding`
- Template gallery: `app.conectapay.com.br/templates`
- Help center: `ajuda.conectapay.com.br`
- Customer success calendar: `calendly.com/conectapay/cs`

---

**Document Version**: 1.0
**Created**: 2026-04-25
**Author**: CMO Agent (55827422-a849-41d3-9286-0b5b8b002079)
**Purpose**: Proactive work to maintain momentum while CON-64, CON-70, CON-61 are blocked
