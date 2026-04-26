# ConectaPay - Customer Testimonial and Case Study Production Pipeline

## Purpose
This document defines the end-to-end production pipeline for systematically creating, managing, and distributing customer testimonials and case studies at scale.

**Use this document when:**
- Managing the case study production workflow
- Onboarding team members to case study operations
- Scaling case study production
- Tracking pipeline performance and KPIs
- Troubleshooting bottlenecks in the production process

---

## Pipeline Overview

### The Case Study Production Funnel

```
┌─────────────────────────────────────────────────────────────────────────┐
│                    CASE STUDY PRODUCTION PIPELINE                      │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                         │
│  IDENTIFY → QUALIFY → OUTREACH → INTERVIEW → DRAFT → APPROVE → PRODUCE │
│    (500)      (200)      (100)       (50)      (25)      (20)      (15) │
│                                                                         │
│  PUBLISH → DISTRIBUTE → TRACK → REPURPOSE → ARCHIVE                    │
│    (15)       (15)        (15)       (45)       (15)                   │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘

Time from Identify to Publish: 14-21 days per case study
Team Capacity: 4-6 case studies per month (solo CMO)
```

### Pipeline Stages Summary

| Stage | Goal | Output | Owner | Time |
|-------|------|--------|-------|------|
| **1. Identify** | Find potential candidates | Candidate list (50+) | CMO/Customer Success | Ongoing |
| **2. Qualify** | Prioritize best opportunities | Qualified list (20) | CMO | Weekly |
| **3. Outreach** | Secure participation | Scheduled interviews (10) | CMO | 1-2 weeks |
| **4. Interview** | Capture story and metrics | Interview notes + recording | CMO | 30-45 min each |
| **5. Draft** | Write compelling narrative | Draft case study | CMO/Content Writer | 2-3 days |
| **6. Approve** | Get customer sign-off | Approved content | CMO + Customer | 3-5 days |
| **7. Produce** | Create final assets | Web, PDF, social versions | Designer + CMO | 3-5 days |
| **8. Publish** | Go live | Published case study | CMO | 1 day |
| **9. Distribute** | Maximize reach | Multi-channel distribution | CMO | Ongoing |
| **10. Track** | Measure impact | Performance report | CMO | 30+ days |
| **11. Repurpose** | Extract maximum value | 5+ content pieces | Content Team | Ongoing |
| **12. Archive** | Organize for reuse | Indexed library | CMO | Immediate |

---

## Stage 1: Candidate Identification

### Automated Candidate Detection System

**Data Sources to Monitor:**

1. **Product Analytics**
   - Revenue recovery > R$ 2.000/month
   - No-show reduction > 50%
   - Pix adoption rate > 30%
   - Active usage > 30 days
   - NPS score: 9-10

2. **Customer Success Signals**
   - Quick implementation (< 7 days)
   - Feature requests (shows engagement)
   - Support tickets closed as "delighted"
   - Refers other customers
   - Responds to check-in emails

3. **Manual Identification**
   - Sales team nominations
   - Customer mentions on social media
   - Industry awards or recognition
   - Unique use cases
   - Geographic representation needs

### Candidate Scoring Card

Use this scorecard to prioritize case study candidates:

```
CASE STUDY CANDIDATE SCORECARD

Customer: _____________________________  Date: _________

Section 1: Results (40 points)
□ Revenue recovery > R$ 5.000/month (15 pts)
□ Revenue recovery R$ 2.000-5.000/month (10 pts)
□ Revenue recovery < R$ 2.000/month (5 pts)
□ No-show reduction > 70% (10 pts)
□ No-show reduction 50-70% (7 pts)
□ No-show reduction < 50% (3 pts)
□ ROI > 10x (10 pts)
□ ROI 5-10x (7 pts)
□ ROI < 5x (3 pts)
□ Time to results < 7 days (5 pts)
□ Time to results 7-30 days (3 pts)

Section 2: Story Quality (25 points)
□ Clear before/after transformation (10 pts)
□ Emotional pain point (10 pts)
□ Unexpected benefit (5 pts)

Section 3: Representation Value (20 points)
□ Target ICP segment (Clinics/Real Estate) (10 pts)
□ Emerging segment we want to validate (7 pts)
□ Unique geography (SP/RJ/BH之外) (3 pts)
□ Business size representative of ICP (5 pts)
□ Industry authority/influencer (5 pts)

Section 4: Customer Willingness (15 points)
□ Previously expressed interest (10 pts)
□ Active on social media (3 pts)
□ Professional photo available (2 pts)

TOTAL SCORE: _____ / 100

QUALIFICATION THRESHOLDS:
- 80+ points: IMMEDIATE PRIORITY (Tier 1)
- 60-79 points: HIGH PRIORITY (Tier 2)
- 40-59 points: MEDIUM PRIORITY (Tier 3)
- < 40 points: LOW PRIORITY (backlog)
```

### Monthly Identification Targets

| Timeframe | New Candidates Identified | Cumulative Pipeline |
|-----------|---------------------------|---------------------|
| Month 1 | 20 | 20 |
| Month 2 | 15 | 35 |
| Month 3 | 15 | 50 |
| Month 4+ | 10 | 60+ |

**Sources breakdown:**
- Product analytics: 50%
- Customer Success referrals: 30%
- Sales team nominations: 15%
- Social monitoring: 5%

---

## Stage 2: Qualification & Prioritization

### Weekly Qualification Process

**Every Monday:**
1. Review new candidates from past week
2. Score each candidate using scorecard
3. Assign Tier (1, 2, or 3)
4. Update Candidate Tracker
5. Select top 5 for outreach this week

### Tier-Based Outreach Strategy

| Tier | Description | Outreach Priority | Target Conversion |
|------|-------------|-------------------|-------------------|
| **Tier 1** | 80+ points, perfect fit | Immediate outreach (within 48 hours) | 70% → interview |
| **Tier 2** | 60-79 points, strong fit | Outreach within 1 week | 50% → interview |
| **Tier 3** | 40-59 points, good fit | Outreach within 2 weeks | 30% → interview |

### Portfolio Balance Strategy

Ensure case study portfolio represents:

**By Segment:**
- Clínicas: 40%
- Imobiliárias: 40%
- Academias: 10%
- Óticas: 10%

**By Geography:**
- São Paulo: 30%
- Rio de Janeiro: 20%
- Belo Horizonte: 15%
- Curitiba: 15%
- Other capitals: 20%

**By Business Size:**
- Small (1-5 employees): 30%
- Medium (6-20 employees): 50%
- Large (21+ employees): 20%

---

## Stage 3: Outreach & Scheduling

### Outreach Sequence

**Touch 1: Email (Day 0)**
- Personalized based on their specific results
- Offer clear incentive
- Link to calendar

**Touch 2: WhatsApp (Day 2)**
- Casual follow-up
- Reinforce incentive
- Make it easy to say yes

**Touch 3: Phone Call (Day 5)**
- For Tier 1 candidates only
- Personal connection
- Answer questions

**Touch 4: Break-up (Day 10)**
- "Not the right time?"
- Keep door open for future

### Incentive Menu

Offer choice of incentives:

| Incentive | Value | Cost to ConectaPay | Appeal |
|-----------|-------|-------------------|--------|
| 1 month free | R$ 149-397 | R$ 60-160 (marginal cost) | ⭐⭐⭐⭐⭐ |
| Feature request priority | N/A | Engineering time | ⭐⭐⭐⭐ |
| R$ 200 Amazon gift card | R$ 200 | R$ 200 | ⭐⭐⭐⭐⭐ |
| Co-marketing (social feature) | N/A | Time + reach | ⭐⭐⭐ |
| Lifetime discount (20%) | Ongoing value | Ongoing margin reduction | ⭐⭐⭐⭐ |
| Premium support (3 months) | N/A | CS time | ⭐⭐⭐ |

**Recommended:** Offer choice of 1 month free OR R$ 200 gift card

### Scheduling Best Practices

**Timing:**
- Best times: Tuesday-Thursday, 10am-12pm or 2pm-4pm
- Avoid: Mondays (busy), Fridays (checked out)
- Lead time: Schedule 1-2 weeks out

**Preparation:**
- Send questions 48 hours in advance
- Confirm appointment 24 hours before
- Research their business (website, social)

**Tools:**
- Calendly (configured with Brazil business hours)
- Zoom (record with permission)
- Backup: Phone call + note-taking

---

## Stage 4: Interview Execution

### Interview Preparation Checklist

**Before the Interview:**
- [ ] Review customer's usage data
- [ ] Research their business online
- [ ] Prepare specific questions based on their segment
- [ ] Test recording equipment
- [ ] Have interview guide printed/open
- [ ] Prepare opening script

**Interview Setup:**
```
OPENING SCRIPT:
"Olá [Nome]! Tudo bem?

Obrigado por fazer um tempo pra conversar. Vou gravar nossa conversa
pra garantir que não perco nenhum detalhe, tá bom? Depois eu te mando
o rascunho do case study pra você aprovar antes de publicar qualquer
coisa.

A conversa vai levar uns 30-40 minutos. Vou te fazer algumas perguntas
sobre sua experiência com a ConectaPay — como era antes, como funciona
agora, e os resultados que você conseguiu.

Qualquer momento que você quiser pausar ou tiver alguma dúvida, pode falar!

Vamos começar?"
```

### Interview Question Flow

Use the interview guide from `customer-success-case-study-template-framework.md`

**Key Probing Techniques:**

| Vague Answer | Probe Question |
|--------------|----------------|
| "Melhorou muito" | "Em números? 10%? 50%? 100%?" |
| "Recuperei dinheiro" | "Consegue estimar? R$ 1.000? R$ 3.000?" |
| "Foi rápido" | "Quanto tempo? 15 minutos? 1 hora?" |
| "Minha equipe gostou" | "Quantas horas por semana economizam?" |
| "Vale a pena" | "Pagou-se em quanto tempo? 3 dias? Uma semana?" |

### Post-Interview Actions (Within 24 hours)

1. **Send Thank You Email**
   - Thank them for their time
   - Attach recording (if requested)
   - Set expectations for timeline
   - Deliver on incentive promise

2. **Transcribe & Organize**
   - Transcribe interview (AI tool or manual)
   - Highlight key quotes
   - Extract all metrics
   - Identify story arc

3. **Create Interview Brief**
   - Customer profile
   - Key metrics summary
   - Best quotes
   - Recommended angle
   - Visual opportunities

---

## Stage 5: Draft Creation

### Draft Assignment Matrix

| Format | When to Use | Writer | Time Investment |
|--------|-------------|--------|-----------------|
| Full Case Study (web) | Primary format | CMO / Content Writer | 2-3 hours |
| Social Media Mini-Case | LinkedIn/Instagram | CMO / Social Media Manager | 1 hour |
| Video Script | Video testimonial | CMO | 1 hour |
| One-Pager | Sales materials | CMO / Designer | 1 hour |

### Draft Creation Workflow

**Step 1: Interview Brief Review (15 min)**
- Identify the "hook" (transformation statement)
- Select best quote for headline
- Verify all metrics
- Choose primary format

**Step 2: Outline (15 min)**
- Structure: Problem → Solution → Results
- Insert metrics at each stage
- Plan visual elements
- Draft headline options

**Step 3: First Draft (60-90 min)**
- Write without editing
- Follow template structure
- Insert placeholders for [bracketed] items
- Include at least 3 customer quotes

**Step 4: Metrics Verification (15 min)**
- Cross-check with interview
- Verify against internal data
- Calculate ROI
- Ensure all numbers add up

**Step 5: Polish (30 min)**
- Apply brand voice guidelines
- Check mobile readability
- Optimize for SEO (if web)
- Add visual directions

### Draft Quality Checklist

Before sending to customer:

**Content:**
- [ ] Specific R$ amounts included
- [ ] Before/after comparison clear
- [ ] ROI calculated and shown
- [ ] Customer quote authentic and powerful
- [ ] Problem clearly defined with pain
- [ ] Solution simply explained
- [ ] Results quantified with 3+ metrics

**Formatting:**
- [ ] Mobile-optimized paragraphs
- [ ] Scannable with subheadings
- [ ] Visual directions clear
- [ ] Customer name spelled correctly
- [ ] Business details accurate

**Compliance:**
- [ ] No exaggerated claims
- [ ] All metrics verifiable
- [ ] Customer context complete
- [ ] Implementation time specified
- [ ] Honest about challenges (if any)

---

## Stage 6: Customer Approval

### Approval Process Flow

```
DRAFT → CUSTOMER REVIEW → FEEDBACK → REVISION → FINAL APPROVAL → PRODUCTION
```

### Customer Review Email Template

**Subject:** Seu case study da ConectaPay — revisão e aprovação

**Body:**

Olá [Customer Name]!

Segue o rascunho do seu case study da ConectaPay.

📄 **Em anexo:** Case study completo em [PDF/Doc]

O que eu preciso de você:
1. Ler com atenção
2. Verificar se está tudo correto
3. Me enviar suas correções ou comentários
4. Aprovar para publicação

**Prazo:** [3-5 dias úteis]

Algumas observações:
- ✅ Você pode alterar qualquer parte que quiser
- ✅ Se quiser adicionar/remover algo, me fala
- ✅ Vou te mandar a versão final antes de publicar
- ✅ Te aviso quando sair (e te mamo o link pra compartilhar!)

Muito obrigado por fazer parte da história da ConectaPay! 🚀

Abraço,
[Seu Nome]

---

### Handling Common Feedback

| Feedback Type | Response |
|---------------|----------|
| "Está perfeito!" | Ótimo! Vou pra produção e te aviso quando publicar. |
| "Pode ser mais curto" | Vou criar uma versão compacta mantendo os resultados principais. |
| "Quero mudar este número" | Me confirma o número correto e eu ajusto. |
| "Não gostei desta frase" | Pode me sugerir como prefere que eu escreva? |
| "Preciso mostrar para meu sócio" | Sem problemas! Me fala quando tiverem o feedback conjunto. |
| "Está muito vendido" | Vou suavizar e focar mais na sua história e menos no produto. |
| Radio silence (5 days) | Envio follow-up amigável. "Deu uma olhada? Precisa de mais tempo?" |

### Approval Timeline Management

| Day | Action |
|-----|--------|
| 0 | Send draft for review |
| 3 | Check-in if no response |
| 5 | Final follow-up |
| 7 | If no response, pause and revisit later |

**Red Flags:**
- No response after 2 follow-ups → table for now
- Customer asks for changes that violate compliance → negotiate
- Customer wants to remove all metrics → explain impact, may not be worth publishing

---

## Stage 7: Production & Design

### Production Handoff Package

When sending to designer, include:

```
PRODUCTION BRIEF

Case Study: [Customer Name]
Format: [Web / PDF / Social / Video]

DELIVERABLES:
□ Web case study (600-800 words)
□ PDF one-pager
□ LinkedIn carousel (6 slides)
□ Instagram carousel (6 slides)
□ Instagram story graphics (3)
□ Quote graphic (for social)
□ Email header image

CONTENT PROVIDED:
□ Final approved text
□ Customer photo (high-res)
□ Business logo (vector if possible)
□ Customer headshot (professional)
□ Metrics for data visualization
□ Brand guidelines reference

VISUAL DIRECTIONS:
□ Color scheme: [specify]
□ Tone: [professional/friendly/energetic]
□ Key metric to highlight: [metric]
□ Chart type needed: [bar/donut/line]

DEADLINE: [date]
```

### Design Production Timeline

| Asset | Time | Dependencies |
|-------|------|--------------|
| Web case study | 2 hours | Final text, customer photo |
| PDF one-pager | 1 hour | Web version complete |
| Social carousel | 2 hours | Key metrics extracted |
| Story graphics | 1 hour | Quote selected |
| Video edit (if applicable) | 4-6 hours | Raw footage |

**Total production time: 1-2 business days**

### Visual Requirements Checklist

**For Web Case Study:**
- [ ] Hero image with customer photo + headline
- [ ] Before/After comparison chart
- [ ] ROI donut chart or infographic
- [ ] Customer quote pull-out
- [ ] Metrics sidebar
- [ ] Mobile responsive
- [ ] SEO meta tags

**For Social Carousel:**
- [ ] Slide 1: Hook + customer photo
- [ ] Slide 2: Problem (with numbers)
- [ ] Slide 3: Solution (simple)
- [ ] Slide 4: Results (big metrics)
- [ ] Slide 5: Customer quote
- [ ] Slide 6: CTA
- [ ] Branded cover frame

**For PDF One-Pager:**
- [ ] Customer logo
- [ ] Before/After comparison table
- [ ] ROI callout
- [ ] Customer photo
- [ ] Contact CTA

---

## Stage 8: Publication

### Pre-Publication Checklist (Final Gate)

**Content:**
- [ ] Customer final approval received
- [ ] All facts verified
- [ ] Links tested
- [ ] Contact info correct

**Technical:**
- [ ] SEO optimized (title, meta description, alt text)
- [ ] Mobile responsive tested
- [ ] Page load speed < 3 seconds
- [ ] Analytics tracking installed

**Legal:**
- [ ] Customer permission documented
- [ ] Photo usage rights confirmed
- [ ] No confidential information exposed
- [ ] No competitor references

### Publication Day Process

**Step 1: Website Publish (Morning)**
- Publish to case studies section
- Test on mobile
- Verify analytics firing
- Shorten URL for social

**Step 2: Social Launch (Mid-day)**
- LinkedIn: Carousel + tag customer
- Instagram: Reel teaser + carousel
- Stories: Day-long announcement

**Step 3: Email Feature (Afternoon)**
- Add to newsletter
- Send dedicated segment email
- Notify sales team

**Step 4: Customer Notification**
- Send published case study link
- Provide social share copy
- Encourage them to share
- Thank them again

### Publication Calendar Template

```
WEEK OF [DATE]: [Customer Name] Case Study Launch

Monday:
□ 9am: Website publish
□ 10am: LinkedIn carousel
□ 11am: Instagram carousel
□ 2pm: Customer notification
□ 4pm: Email newsletter feature

Tuesday:
□ 10am: LinkedIn text post (key stat)
□ All day: Instagram stories (metrics)

Wednesday:
□ 10am: Video testimonial clip (if available)
□ 2pm: Quote graphic

Thursday-Sunday:
□ Ongoing: Respond to comments
□ Ongoing: Sales team uses in calls
```

---

## Stage 9: Distribution & Amplification

### Multi-Channel Distribution Matrix

| Channel | Format | Frequency | Goal |
|---------|--------|-----------|------|
| **Website** | Full case study | One-time | SEO, inbound leads |
| **LinkedIn** | Carousel + article | Launch + 2x/month | Professional reach |
| **Instagram** | Carousel + Reel | Launch + weekly | Visual engagement |
| **Email** | Newsletter feature | Launch + nurture sequence | Lead conversion |
| **Sales** | One-pager PDF | Ongoing | Sales enablement |
| **YouTube** | Video testimonial | Launch | Social proof |
| **Medium** | Long-form article | Launch + evergreen | SEO, thought leadership |
| **Paid Ads** | Retargeting creative | Ongoing (30 days) | Conversion |

### 30-Day Distribution Timeline

**Week 1: Launch Blitz**
- Day 1: All channels (website, social, email)
- Day 2: LinkedIn text post with key stat
- Day 3: Instagram story series
- Day 5: Video testimonial clip

**Week 2: Sustained Promotion**
- Day 8: Quote graphic on all social
- Day 10: Sales team spotlight in internal comms
- Day 12: Repost in relevant LinkedIn groups
- Day 14: Customer re-share encouragement

**Week 3: Targeted Outreach**
- Day 15: Share with similar prospects (1:1 DMs)
- Day 17: Include in nurture email sequence
- Day 19: Feature in partner newsletter
- Day 21: LinkedIn article version

**Week 4: Long-Term Amplification**
- Day 22: Add to sales deck
- Day 24: Create Thread from key insights
- Day 26: Update website homepage slider
- Ongoing: Use in retargeting ads

### Sales Enablement Package

For each case study, create:

1. **One-Pager PDF** (for meetings)
2. **5-Minute Pitch Script** (for calls)
3. **3-Question Objection Handler** (common concerns)
4. **WhatsApp Forward Template** (easy sharing)
5. **Vertical-Specific Version** (if applicable)

---

## Stage 10: Performance Tracking

### Tracking Dashboard Template

```
CASE STUDY PERFORMANCE TRACKER

Case Study: [Customer Name]
Published: [Date]
Segment: [Clinics/Real Estate/etc]

CHANNEL PERFORMANCE (30 Days):
┌─────────────────────┬──────────┬──────────┬──────────┐
│ Channel             │ Views    │ Engagement│ Leads    │
├─────────────────────┼──────────┼──────────┼──────────┤
│ Website             │    0     │    0%    │    0     │
│ LinkedIn            │    0     │    0%    │    0     │
│ Instagram           │    0     │    0%    │    0     │
│ Email               │    0     │    0%    │    0     │
│ Sales Usage         │    0     │    N/A   │    0     │
└─────────────────────┴──────────┴──────────┴──────────┘

BUSINESS IMPACT:
├── Leads Generated: ___
├── Sales Calls Mentioning: ___
├── Opportunities Created: R$ ___
├── Closed Won: R$ ___
└── ROI on Production: [X]x

CUSTOMER IMPACT:
├── Customer shared on social: YES/NO
├── Customer referred new leads: ___
├── Customer became advocate: YES/NO
└── NPS after case study: ___

QUALITATIVE FEEDBACK:
├── Sales team feedback: ___________
├── Best performing element: ___________
├── Worst performing element: ___________
└── Lessons learned: ___________
```

### Monthly Performance Report

Track aggregate performance monthly:

```
MONTHLY CASE STUDY PERFORMANCE - [MONTH]

Case Studies Published: ___
Total Views: ___
Total Engagement Rate: ___%
Total Leads Generated: ___
Total Revenue Attributed: R$ ___

TOP PERFORMING CASE STUDY:
[Customer Name] - [Key stat] views, [X]% engagement

UNDERPERFORMING CASE STUDY:
[Customer Name] - [Key stat] views, [X]% engagement
Action plan: ___________

SEGMENT BREAKDOWN:
├── Clínicas: ___ case studies, ___ avg engagement
├── Imobiliárias: ___ case studies, ___ avg engagement
├── Academias: ___ case studies, ___ avg engagement
└── Óticas: ___ case studies, ___ avg engagement

FORMAT BREAKDOWN:
├── Full case study: ___ avg views
├── Social carousel: ___ avg engagement
├── Video testimonial: ___ avg views
└── One-pager: ___ sales uses

PIPELINE HEALTH:
├── Candidates identified: ___
├── Interviews scheduled: ___
├── Drafts in progress: ___
├── Awaiting approval: ___
└── In production: ___

NEXT MONTH'S FOCUS:
1. ___________
2. ___________
3. ___________
```

---

## Stage 11: Content Repurposing

### The 1:10 Content Rule

Every 1 case study should produce 10+ pieces of content:

```
INPUT: 1 Case Study
│
├── 1. Full case study (web)
├── 2. PDF one-pager
├── 3. LinkedIn carousel
├── 4. Instagram carousel
├── 5. Video testimonial
├── 6. Quote graphic
├── 7. Email newsletter feature
├── 8. LinkedIn text post (key stat)
├── 9. Twitter/X thread
├── 10. Medium article
├── 11. Sales one-pager (vertical-specific)
├── 12. WhatsApp forward template
└── 13. Retargeting ad creative

OUTPUT: 10+ pieces of content
```

### Repurposing Templates

**From Case Study to LinkedIn Text Post:**
```
[Dra. Dr. Name], [City] → recuperou R$ 3.200 no primeiro mês.

Antes: 12 no-shows por semana
Depois: 3 no-shows por semana

Redução de 75% em 30 dias.

ROI de 10x. Pagou-se em 3 dias.

Link completo nos comentários 👇

#conectapay #saúde #no-show #pix
```

**From Case Study to Twitter Thread:**
```
1/7
Como uma clínica em São Paulo reduziu no-shows em 75%...

Thread 🧵👇

2/7
O problema:
Dra. Ana perdia 12 pacientes por semana.
R$ 2.500 por mês no buraco negro.

3/7
A solução:
ConectaPay automatizou lembretes via WhatsApp.
Pix antecipado para garantir presença.

4/7
[Continue thread...]
```

**From Case Study to Email:**
```
Assunto: Como [Customer] recuperou R$ [amount] em 30 dias

Olá [Name],

[Customer Name], [industry] em [city], estava perdendo [pain point].

Implementou ConectaPay. Resultados:
✅ [Result 1]
✅ [Result 2]
✅ ROI de [X]x

Veja o case completo: [link]

Quer resultados parecidos? [CTA]
```

---

## Stage 12: Archiving & Organization

### Case Study Library Structure

```
/conectapay-docs/case-studies/
│
├── /published/
│   ├── /clinics/
│   │   ├── customer-name-1/
│   │   │   ├── case-study-web.md
│   │   │   ├── case-study-pdf.pdf
│   │   │   ├── linkedin-carousel.pdf
│   │   │   ├── interview-recording.mp4
│   │   │   ├── interview-transcript.md
│   │   │   ├── customer-photo.jpg
│   │   │   ├── customer-logo.svg
│   │   │   └── performance-data.csv
│   │   └── customer-name-2/
│   │       └── ...
│   ├── /real-estate/
│   ├── /academies/
│   └── /opticals/
│
├── /in-production/
│   ├── customer-name-a/
│   │   ├── interview-notes.md
│   │   ├── draft-v1.md
│   │   ├── draft-v2.md
│   │   └── feedback-from-customer.md
│   └── ...
│
├── /templates/
│   ├── full-case-study-template.md
│   ├── social-carousel-template.fig
│   └── one-pager-template.indd
│
└── /assets/
    ├── customer-photos/
    ├── logos/
    └── charts/
```

### Metadata Index

Maintain a master index of all case studies:

```csv
Customer,Segment,City,Revenue Recovery,ROI,Published Date,Views,Leads,Status
Dra. Ana Silva,Clinics,São Paulo,R$ 3.200,10x,2026-04-15,1250,23,Published
Imobiliária ABC,Real Estate,Rio de Janeiro,R$ 5.800,8x,2026-04-20,980,17,Published
...
```

---

## Pipeline Management

### Weekly Rhythm

**Monday:**
- Review new candidates (20 min)
- Score and prioritize (30 min)
- Select 5 for outreach (10 min)
- Send outreach emails (30 min)

**Tuesday:**
- Follow up on last week's outreach (20 min)
- Conduct 1-2 interviews (60 min)
- Send thank you emails (15 min)

**Wednesday:**
- Conduct 1-2 interviews (60 min)
- Create interview briefs (30 min)
- Start drafting top priority (60 min)

**Thursday:**
- Complete drafts (90 min)
- Send for customer approval (30 min)
- Design handoff for approved (30 min)

**Friday:**
- Review published performance (30 min)
- Update tracker (15 min)
- Plan next week (15 min)
- Repurpose top content (60 min)

### Monthly Review

At the end of each month, review:

1. **Pipeline Health**
   - Candidates identified vs. target
   - Conversion rate at each stage
   - Bottlenecks identified

2. **Content Performance**
   - Best performing case studies
   - Worst performing case studies
   - Patterns in success

3. **Process Efficiency**
   - Time from interview to publish
   - Customer approval rate
   - Production quality issues

4. **Business Impact**
   - Leads generated
   - Revenue attributed
   - Sales team feedback

### Roles and Responsibilities

| Role | Responsibilities | Time Commitment |
|------|------------------|-----------------|
| **CMO** | Overall pipeline, interviews, drafts, distribution | 10-15 hrs/week |
| **Content Writer** | Draft creation, repurposing | 5-8 hrs/week |
| **Designer** | Visual production (carousel, PDF, graphics) | 4-6 hrs/week |
| **Customer Success** | Candidate identification, outreach support | 2-3 hrs/week |
| **Sales** | Feedback, usage tracking, prospect sharing | Ongoing |

---

## KPIs and Targets

### Pipeline KPIs

| Metric | Target | Measurement |
|--------|--------|-------------|
| Candidates identified/month | 15-20 | Tracker count |
| Outreach conversion rate | 50% | Interviews scheduled ÷ outreach |
| Interview → Draft rate | 90% | Drafts created ÷ interviews |
| Customer approval rate | 95% | Approved ÷ submitted |
| Identify → Publish time | 14-21 days | Days from identification to publish |
| Case studies published/month | 4-6 | Published count |

### Content Performance KPIs

| Metric | Target | Measurement |
|--------|--------|-------------|
| Website case study views | 500+/month | Analytics |
| Social engagement rate | 5%+ | Social analytics |
| Leads generated per case study | 15+/month | CRM attribution |
| Sales team usage | 80% use weekly | Internal survey |
| Customer share rate | 60% share on social | Social monitoring |

### Business Impact KPIs

| Metric | Target | Measurement |
|--------|--------|-------------|
| Revenue attributed to case studies | R$ 10k+/month | Closed-won attribution |
| Case study influence on pipeline | 20% of opportunities | CRM source tracking |
| Customer advocacy from case studies | 40% refer new customers | Referral tracking |
| Production ROI | 10x+ | Revenue ÷ production cost |

---

## Automation Opportunities

### Tools to Streamline Pipeline

1. **Candidate Identification**
   - Automate: Product analytics alerts
   - Tool: Mixpanel/Amplitude dashboards
   - Trigger: Revenue recovery > R$ 2.000

2. **Outreach Scheduling**
   - Automate: Email sequences
   - Tool: HubSpot sequences / Lemlist
   - Trigger: Candidate added to Tier 1 list

3. **Interview Scheduling**
   - Automate: Calendly
   - Tool: Calendly + Google Calendar
   - Trigger: Customer says yes

4. **Transcription**
   - Automate: Interview to text
   - Tool: Otter.ai / Descript
   - Trigger: Recording uploaded

5. **Draft Creation**
   - Semi-automate: Template population
   - Tool: Custom script / AI writing assistant
   - Trigger: Interview transcript ready

6. **Approval Tracking**
   - Automate: Follow-up reminders
   - Tool: HubSpot workflows / Trello
   - Trigger: Draft sent, no response in 3 days

7. **Distribution Scheduling**
   - Automate: Social posts
   - Tool: Buffer / Hootsuite
   - Trigger: Case study published

8. **Performance Reporting**
   - Automate: Monthly dashboard
   - Tool: Google Data Studio
   - Trigger: End of month

---

## Troubleshooting Guide

### Common Bottlenecks

**Problem: Low customer acceptance rate ( < 30%)**

Diagnosis:
- Incentive not compelling enough?
- Outreach message too salesy?
- Wrong timing (busy season)?
- Customer relationship weak?

Solutions:
1. Increase incentive (offer R$ 200 gift card)
2. Soften outreach (focus on "sharing your story" not "case study")
3. Time outreach better (avoid tax season, holidays)
4. Build relationship first (check-in call, value add)

**Problem: Slow customer approval ( > 7 days)**

Diagnosis:
- Customer too busy?
- Draft too long?
- Unclear expectations?

Solutions:
1. Send friendly reminder (not pushy)
2. Offer to hop on call to review together
3. Send shorter version for quick approval
4. Set clear deadline upfront

**Problem: Poor case study performance ( < 200 views)**

Diagnosis:
- Weak headline/hook?
- Not distributed enough?
- Not relevant to audience?

Solutions:
1. A/B test headline
2. Increase distribution (add more channels)
3. Check segment alignment (is this ICP-relevant?)
4. Boost with paid promotion

**Problem: Production bottleneck (designer overloaded)**

Diagnosis:
- Too many case studies in pipeline?
- Designer not prioritized?
- Inefficient handoff?

Solutions:
1. Use templates (less custom work)
2. Hire freelancer for overflow
3. Create design system (faster production)
4. Prioritize Tier 1 case studies only

---

## First 90-Day Execution Plan

### Month 1: Foundation

**Week 1: Setup**
- [ ] Create Candidate Tracker sheet
- [ ] Set up Calendly for interviews
- [ ] Build scoring card
- [ ] Document outreach templates
- [ ] Identify first 20 candidates

**Week 2: First Outreach**
- [ ] Score and prioritize candidates
- [ ] Send outreach to top 5
- [ ] Schedule 2-3 interviews
- [ ] Conduct first interview
- [ ] Create interview brief template

**Week 3: Production Begins**
- [ ] Complete 2-3 interviews
- [ ] Write first case study draft
- [ ] Send for customer approval
- [ ] Set up design file structure

**Week 4: First Publication**
- [ ] Get customer approval
- [ ] Design and produce assets
- [ ] Publish first case study
- [ ] Distribute across all channels
- [ ] Track initial performance

### Month 2: Ramping Up

**Weeks 5-6:**
- [ ] Publish 2 more case studies
- [ ] Refine templates based on learnings
- [ ] Build repurposing workflow
- [ ] Create sales enablement package

**Weeks 7-8:**
- [ ] Publish 2 more case studies
- [ ] Analyze performance data
- [ ] Identify best-performing format
- [ ] Optimize outreach based on conversion

### Month 3: Scaling

**Weeks 9-10:**
- [ ] Publish 3 case studies
- [ ] Automate candidate identification
- [ ] Build email sequences
- [ ] Train sales team on usage

**Weeks 11-12:**
- [ ] Publish 3 case studies
- [ ] Complete 90-day review
- [ ] Document lessons learned
- [ ] Create Month 4-6 plan

**End of Month 3 Targets:**
- ✅ 10 case studies published
- ✅ 2.000+ total views
- ✅ 100+ leads generated
- ✅ Pipeline of 20+ candidates
- ✅ Production time < 14 days

---

## Appendix: Quick Reference

### Candidate Qualification Thresholds
- **Tier 1 (80+ points):** Outreach within 48 hours
- **Tier 2 (60-79 points):** Outreach within 1 week
- **Tier 3 (40-59 points):** Outreach within 2 weeks

### Standard Incentives
- 1 month free OR R$ 200 gift card
- Feature request priority
- Co-marketing (social feature)

### Timeline Expectations
- Identify → Publish: 14-21 days
- Interview → Draft: 2-3 days
- Customer Approval: 3-5 days
- Production: 1-2 days

### File Naming Convention
```
case-study-[customer-name]-[segment]-[date].md
Example: case-study-dra-ana-silva-clinics-2026-04-15.md
```

### Must-Have Metrics
1. Revenue recovery (R$ amount)
2. No-show reduction (%)
3. ROI (multiple)
4. Payback period (days)
5. Time to results (days/weeks)

---

## Document Updates

### Version History
- **v1.0** (April 26, 2026): Initial production pipeline

### Next Review
- Update after 10 case studies published
- Incorporate performance data
- Refine based on bottlenecks encountered

---

*Prepared by: CMO Agent (55827422-a849-41d3-9286-0b5b8b002079)*
*Linked Task: CON-164*
*Goal: Build operational pipeline for scalable case study production*
*Created: April 26, 2026*
*Dependencies: customer-success-case-study-template-framework.md*
