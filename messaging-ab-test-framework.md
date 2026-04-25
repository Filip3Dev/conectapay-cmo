# ConectaPay - Messaging A/B Test Framework
## Smoke Test Validation (No Interviews)

**Task**: CON-82 - Messaging Optimization
**Owner**: CMO Agent (55827422-a849-41d3-9286-0b5b8b002079)
**Purpose**: Validate messaging through A/B testing in smoke test (real traffic)
**Status**: Framework Ready | Execution Pending Smoke Test

---

## 🎯 Objective

Validate messaging assumptions through **real market data** instead of interviews:

1. **Create message variations** for each assumption
2. **A/B test variations** in smoke test ads/landing page
3. **Measure performance** (CTR, conversion, lead quality)
4. **Let data decide** which messaging resonates
5. **Scale winners** and kill losers

---

## 📊 6 Core Messaging Assumptions to Test

### Test 1: Financial Pain Angle
**Hypothesis**: "Focusing on money lost (R$ X/mês) outperforms other angles"

**Variation A (Current)**: "Sua clínica perde R$ 2.500-R$ 5.000 por mês com no-shows"

**Variation B (Specific)**: "Pare de perder R$ 3.200 todo mês com pacientes que marcam e não aparecem"

**Variation C (Urgency)**: "Sua clínica já perdeu R$ 400 esta semana com no-shows"

**Metrics**:
- CTR (impressões → cliques)
- Landing page conversion (cliques → leads)
- Lead quality (WTP, problem recognition)

**Success Criteria**: Variation with highest conversion rate wins

---

### Test 2: Time Savings Angle
**Hypothesis**: "Focusing on time saved resonates with busy clinic owners"

**Variation A (Current)**: "Sua secretária gasta 3-5 horas/semana em ligações"

**Variation B (Opportunity Cost)**: "Sua secretária volta a focar em atendimento, não em ligações repetidas"

**Variation C (Efficiency)**: "De 3 horas/semana em ligações para 5 minutos/dia com automação"

**Metrics**:
- CTR
- Conversion rate
- Lead quality (business size, role)

**Success Criteria**: Variation with highest conversion rate wins

---

### Test 3: WhatsApp Channel Angle
**Hypothesis**: "Messaging emphasizing WhatsApp as channel resonates most"

**Variation A (Feature)**: "Lembretes automáticos via WhatsApp"

**Variation B (Benefit)**: "99% dos seus pacientes usam WhatsApp - use isso a seu favor"

**Variation C (Solution)**: "Envie lembretes no WhatsApp. Receba via Pix. Pronto."

**Metrics**:
- CTR
- Conversion rate
- Lead quality (current WhatsApp usage)

**Success Criteria**: Variation with highest conversion rate wins

---

### Test 4: Pix Payment Angle
**Hypothesis**: "Pix payment messaging increases perceived value"

**Variation A (Feature)**: "Receba via Pix antes da consulta"

**Variation B (Problem)**: "Pare de perder dinheiro: receba via Pix antes da consulta"

**Variation C (Benefit)**: "45% dos pacientes pagam antes da consulta com Pix antecipado"

**Metrics**:
- CTR
- Conversion rate
- Lead quality (payment methods, WTP)

**Success Criteria**: Variation with highest conversion rate wins

---

### Test 5: Ease of Setup Angle
**Hypothesis**: "Emphasizing ease reduces perceived friction"

**Variation A (Time)**: "Configure em 15 minutos"

**Variation B (Simplicity)**: "Se você sabe usar WhatsApp, sabe usar ConectaPay"

**Variation C (No Tech)**: "Zero conhecimento técnico necessário. Configure em 15 min."

**Metrics**:
- CTR
- Conversion rate
- Lead quality (tech comfort, role)

**Success Criteria**: Variation with highest conversion rate wins

---

### Test 6: Pricing/Value Angle
**Hypothesis**: "Clear value proposition at R$ 297/month converts best"

**Variation A (ROI)**: "Por R$ 297/mês, recupere R$ 3.000+ em no-shows"

**Variation B (Payback)**: "Em 30 dias você já lucrou R$ 2.900. ROI de 10x no primeiro mês"

**Variation C (Comparison)**: "Menos que 1 secretária por dia, mas recupera R$ 3.000/mês em no-shows"

**Metrics**:
- CTR
- Conversion rate
- Lead WTP (actual willingness to pay)

**Success Criteria**: Variation with highest WTP and conversion wins

---

## 🧪 A/B Test Setup

### Week 1: Broad Testing (Exploration)

**Ad Level Tests** (Meta Ads + Google Ads):

| Test | Variations | Budget | Duration |
|------|------------|--------|----------|
| Headline Angle | 4 variations (pain, time, WhatsApp, Pix) | R$ 200 | 3 days |
| Value Prop | 3 variations (feature, benefit, problem) | R$ 200 | 3 days |
| CTA | 3 variations ("Começar", "Testar Grátis", "Ver Como Funciona") | R$ 150 | 2 days |

**Landing Page Level Tests**:

| Test | Variations | Traffic Source | Duration |
|------|------------|----------------|----------|
| Hero Section | 3 headline variations | Top ad winner | 4 days |
| Social Proof | With vs. Without testimonials | Top ad winner | 4 days |
| Pricing | R$ 297 vs. R$ 397 anchor test | Top ad winner | 3 days |

### Week 2: Optimization (Exploitation)

**Scale Winners**:
- Take winning variations from Week 1
- Increase budget by 3x
- Test secondary elements (images, descriptions)

**Budget**: R$ 600-800/week

### Week 3-4: Maximum Scale

**Final Validation**:
- Run only winning messaging
- Budget: R$ 1.000-1.500/week
- Final conversion metrics

---

## 📈 Measurement Framework

### Ad-Level Metrics

| Metric | Target | Winner Criteria |
|--------|--------|-----------------|
| CTR | 2.5-4% | Highest CTR |
| CPC | R$ 1-3 | Lowest CPC |
| Impressions | 10K+ | Sufficient data |
| Clicks | 300+ | Statistical significance |

### Landing Page Metrics

| Metric | Target | Winner Criteria |
|--------|--------|-----------------|
| Visit → Form View | 80%+ | Highest |
| Form View → Submit | 45-55% | Highest |
| Visit → Lead | 35-45% | Highest |
| Time on Page | 2+ min | Highest |

### Lead Quality Metrics

| Metric | Target | Winner Criteria |
|--------|--------|-----------------|
| Problem Recognition | 80%+ | Highest |
| WTP > R$ 300 | 60%+ | Highest |
| Ready to Buy Now | 30%+ | Highest |
| ICP Fit Score | 70+/100 | Highest |

---

## 🎯 Statistical Significance

### Minimum Sample Sizes

- **Ad variations**: 300+ clicks each
- **Landing page**: 200+ visitors each
- **Confidence level**: 95%
- **Minimum detectable effect**: 20%

### When to Declare a Winner

- ✅ **Winner**: 95% confidence + 20%+ improvement
- ⚠️ **Inconclusive**: After 7 days without clear winner
- ❌ **Loser**: 95% confidence + 20%+ worse

### Early Stopping Rules

Stop a test early if:
- CTR < 1% (message not resonating at all)
- CPC > R$ 5 (too expensive)
- Conversion < 10% (major disconnect)

---

## 📋 Test Execution Checklist

### Pre-Launch (Day 0)
- [ ] Create all ad variations in Meta Ads Manager
- [ ] Create all ad variations in Google Ads
- [ ] Build landing page variations (or use A/B testing tool)
- [ ] Set up conversion tracking (pixel, GA4)
- [ ] Set up UTM parameters for each variation
- [ ] Create tracking sheet for results
- [ ] Define budget allocation per test

### Launch (Day 1)
- [ ] Launch all tests simultaneously
- [ ] Verify tracking is working
- [ ] Check ads are approved
- [ ] Monitor first 4 hours for issues

### Daily Monitoring (Days 2-7)
- [ ] Check CTR by variation
- [ ] Check CPC by variation
- [ ] Check landing page conversion by variation
- [ ] Check lead quality by variation
- [ ] Document insights daily
- [ ] Kill obvious losers (CTR < 1%)
- [ ] Scale tentative winners (CTR > 3%)

### Weekly Review (Days 7, 14, 21, 28)
- [ ] Aggregate all data
- [ ] Calculate statistical significance
- [ ] Declare winners/losers
- [ ] Document learnings
- [ ] Plan next week's tests
- [ ] Update messaging framework with winners

---

## 📊 Results Tracking Template

### Ad Variation Results

```
Test Name: _________________ | Date: ___/___/___

Variation | Impressions | Clicks | CTR | CPC | Conv. | Conv. Rate | CPA | Winner?
----------|-------------|--------|-----|-----|--------|------------|-----|--------
A         |             |        |     |     |        |            |     |
B         |             |        |     |     |        |            |     |
C         |             |        |     |     |        |            |     |
```

### Landing Page Results

```
Test Name: _________________ | Date: ___/___/___

Variation | Visitors | Form Views | Submit | Lead | Conv. Rate | Avg WTP | Winner?
----------|----------|------------|--------|------|------------|---------|--------
A         |          |            |        |      |            |         |
B         |          |            |        |      |            |         |
```

### Lead Quality by Variation

```
Test Name: _________________ | Date: ___/___/___

Variation | Leads | Prob. Recog | WTP>R$300 | Ready Now | Avg ICP Fit | Winner?
----------|-------|-------------|-----------|-----------|-------------|--------
A         |       |             |           |           |             |
B         |       |             |           |           |             |
```

---

## 🔄 Iteration Process

### After Week 1 (Day 7)
1. **Identify winners** from each test
2. **Kill losers** (pause ads, remove landing pages)
3. **Document insights** (what worked, what didn't)
4. **Create new variations** based on learnings
5. **Plan Week 2** focused on scaling winners

### After Week 2 (Day 14)
1. **Final validation** of Week 1 winners
2. **Secondary element testing** (images, descriptions)
3. **Budget reallocation** to best performers
4. **Prepare Week 3** maximum scale

### After Week 4 (Day 28)
1. **Final messaging** determined by data
2. **Update messaging-framework.md** with validated copy
3. **Document all learnings** for future campaigns
4. **Create messaging playbook** based on winners

---

## 🎯 Success Criteria

### Week 1 Success
- ✅ 4 headline variations tested
- ✅ Clear winner identified (statistically significant)
- ✅ 1+ message angle validated (CTR > 3%, conversion > 40%)

### Week 2 Success
- ✅ Winner scaled 3x
- ✅ Conversion rate maintained or improved at scale
- ✅ CPA stable or decreased

### Week 3-4 Success
- ✅ Final messaging converts at 40%+ (visit → lead)
- ✅ CAC < R$ 100
- ✅ 60%+ of leads have WTP > R$ 300
- ✅ Messaging framework updated with validated language

---

## 📚 Related Documents

- `messaging-framework.md` - Current messaging (to be updated after tests)
- `smoke-test-ad-copy.md` - Ad copy variations
- `smoke-test-landing-page-copy.md` - Landing page copy
- `smoke-test-execution-guide.md` - 4-week smoke test playbook
- `daily-smoke-test-monitoring-framework.md` - Daily monitoring system

---

## 🚀 Next Steps

1. ✅ Framework complete
2. ⏳ Awaiting smoke test launch (CON-61 - hosting access)
3. ⏳ Create A/B test variations in Meta/Google Ads
4. ⏳ Build landing page variations
5. ⏳ Launch Week 1 tests
6. ⏳ Monitor, iterate, scale winners

---

*Prepared by: CMO Agent (55827422-a849-41d3-9286-0b5b8b002079)*
*Date: 2026-04-25*
*Task: CON-82 - Messaging Optimization (A/B Testing Approach)*
*Note: Adapted from interview-based to A/B test validation approach*
