# ConectaPay - Daily Smoke Test Monitoring & Iteration Framework

## Purpose
Daily monitoring system to track smoke test performance, identify issues early, and iterate rapidly based on real data.

## Scope
- **Campaigns**: Meta Ads (Clínicas + Imobiliárias)
- **Channels**: Facebook + Instagram Feed/Stories
- **Budget**: R$ 80/week (R$ 40 per campaign)
- **Duration**: 4 weeks (with weekly GO/NO-GO checkpoints)

---

## Part 1: Daily Monitoring Checklist

### ☀️ Morning Check (9:00 AM - Daily)

**Campaign Health**:
- [ ] Ads are running (no disapprovals or account issues)
- [ ] Budget is being spent (not pacing too slow/fast)
- [ ] No spikes in CPC (should be R$ 0.50-2.50)
- [ ] Pixel/GA4 firing correctly (test conversions)

**Alert Thresholds** (Red Flags 🚨):
- Ad spend = R$ 0 for >12 hours → Check account/billing
- CPC > R$ 4.00 → Pause ad set, investigate
- Impressions < 100 in 24h → Increase budget or widen audience
- CTR < 1.0% after 500 impressions → Test new creative

---

### 🌆 Evening Review (6:00 PM - Daily)

**Performance Metrics** (Log in daily report):

| Metric | Value | Target | Status |
|--------|-------|--------|--------|
| **Spend Today** | R$ ___ | R$ 10-15 | ✅/❌ |
| **Impressions** | ___ | 500+ | ✅/❌ |
| **Clicks** | ___ | 15+ | ✅/❌ |
| **CTR** | ___% | 2.0%+ | ✅/❌ |
| **CPC** | R$ ___ | R$ 0.50-2.50 | ✅/❌ |
| **Landing Page Visits** | ___ | 90%+ of clicks | ✅/❌ |
| **Leads Today** | ___ | 2+ | ✅/❌ |
| **CPL** | R$ ___ | <R$ 50 | ✅/❌ |

**Per-Ad Set Breakdown**:

| Ad Set | Spend | Impr | Clicks | CTR | CPC | Leads | CPL | Action |
|--------|-------|------|--------|-----|-----|-------|-----|--------|
| Clínicas - Pain | R$ | | | % | R$ | | R$ | |
| Clínicas - Time | R$ | | | % | R$ | | R$ | |
| Imobiliárias - Pain | R$ | | | % | R$ | | R$ | |
| Imobiliárias - Time | R$ | | | % | R$ | | R$ | |

---

## Part 2: Automated Alert Rules

### 🚨 Immediate Action Alerts (Act within 2 hours)

**1. Zero Spend Alert**
- Trigger: Spend = R$ 0 for 12+ hours
- Action: Check ad status, billing, account limits
- Severity: Critical (stops learning)

**2. CPC Explosion Alert**
- Trigger: CPC > R$ 4.00 for 50+ clicks
- Action: Pause ad set, check audience competition
- Severity: High (burns budget fast)

**3. CTR Collapse Alert**
- Trigger: CTR < 0.8% after 1,000 impressions
- Action: Kill ad, test new creative/hook
- Severity: High (wastes impressions)

**4. Landing Page Broken Alert**
- Trigger: 0 conversions OR 95%+ bounce rate
- Action: Test page immediately, check pixel/links
- Severity: Critical (100% waste)

---

### ⚠️ Warning Alerts (Review within 24 hours)

**5. Slow Pace Alert**
- Trigger: Spend < 50% of daily budget by 6 PM
- Action: Consider increasing budget or widening audience
- Severity: Medium (slows learning)

**6. Expensive Leads Alert**
- Trigger: CPL > R$ 75 for 48+ hours
- Action: Pause bottom performers, reallocate budget
- Severity: Medium (check unit economics)

**7. Low Conversion Alert**
- Trigger: Landing page visit → Lead < 10% (50+ visits)
- Action: A/B test value prop, simplify form
- Severity: Medium (funnel issue)

---

## Part 3: Daily Iteration Protocols

### 🔄 Daily Optimization Actions

**Kill These Immediately** (No hesitation):
- CTR < 1.0% after 1,000 impressions
- CPC > R$ 4.00 for 50+ clicks
- CPL > R$ 100 after 10 leads
- Landing page conversion < 5% (100+ visits)

**Scale These Aggressively** (Double budget):
- CTR > 3.0% AND CPL < R$ 30
- Conversion rate > 15% (visit → lead)
- Positive feedback (comments, shares)

**Test These Tomorrow** (One variation at a time):
- New headline (if CTR < 2%)
- New creative format (image → video)
- New audience interest (if current saturates)

---

### 📊 Daily Testing Cadence

**Week 1: Find Winning Angle** (Test 4 hooks)
- Day 1-2: Let all 4 ad sets run (equal budget)
- Day 3: Kill bottom 2 (lowest CTR + CPL)
- Day 4-5: Double budget on top 2
- Day 6-7: Test 1 new variation vs. winner

**Week 2: Optimize Funnel** (Test landing page)
- Day 8-10: Scale winner to 3 cities (BH, Curitiba, Salvador)
- Day 11-12: A/B test landing page elements (CTA, social proof)
- Day 13-14: Kill losing page, scale winner

**Week 3: Maximize Scale** (Test creatives)
- Day 15-17: Expand to all top 20 cities
- Day 18-19: Refresh creative (prevent ad fatigue)
- Day 20-21: Test lookalike audiences (1%, 2%, 3%)

**Week 4: Final Push** (Test retargeting)
- Day 22-24: Retarget website visitors (warm audience)
- Day 25-26: Test email follow-up sequence
- Day 27-28: Final optimization, prepare GO/NO-GO analysis

---

## Part 4: Daily Report Template

### 📋 Smoke Test Daily Report - Day X

**Date**: 2026-04-__
**Campaign Week**: __
**Total Spend**: R$ ____ / R$ ____ (planned)

---

#### Budget Pacing
| Campaign | Planned | Actual | Variance | Status |
|----------|---------|--------|----------|--------|
| Clínicas | R$ 40 | R$ __ | ±__% | ✅/⚠️/❌ |
| Imobiliárias | R$ 40 | R$ __ | ±__% | ✅/⚠️/❌ |
| **TOTAL** | **R$ 80** | **R$ __** | **±__%** | ✅/⚠️/❌ |

---

#### Traffic Performance
| Metric | Clínicas | Imobiliárias | Total | Target | Status |
|--------|----------|--------------|-------|--------|--------|
| Impressions | __ | __ | __ | 500+ | ✅/❌ |
| Clicks | __ | __ | __ | 15+ | ✅/❌ |
| CTR | __% | __% | __% | 2.0%+ | ✅/❌ |
| CPC | R$ __ | R$ __ | R$ __ | R$ 0.50-2.50 | ✅/❌ |

---

#### Funnel Performance
| Stage | Count | Rate | Target | Status |
|-------|-------|------|--------|--------|
| Landing Page Visits | __ | 100% | - | - |
| Form Views | __ | __% | 80%+ | ✅/❌ |
| Form Starts | __ | __% | 50%+ | ✅/❌ |
| Leads | __ | __% | 10%+ | ✅/❌ |

**Bottleneck**: ______ (highest drop-off point)

---

#### Lead Quality (Today's Leads: __)

| Question | Response | Target | Status |
|----------|----------|--------|--------|
| Problem Recognition | __% | 70%+ | ✅/❌ |
| Monthly Loss (avg) | R$ __ | R$ 2.000+ | ✅/❌ |
| WTP > R$ 300/mo | __% | 50%+ | ✅/❌ |
| Ready to Buy Now | __% | 20%+ | ✅/❌ |

**Lead Quality Score**: __/10

---

#### Top Performers Today

**Winning Ad Set**: ______ (CTR: __%, CPL: R$ __)
**Winning Creative**: ______ (CTR: __%)
**Winning Headline**: ______ (CTR: __%)

---

#### Action Items Today

**Kill** (pause immediately):
- [ ] ______ (CPL: R$ __, CTR: __%)

**Scale** (increase budget):
- [ ] ______ (CPL: R$ __, CTR: __%) → Double to R$ __

**Test** (launch tomorrow):
- [ ] ______ (new variation of ______)

**Fix** (technical issue):
- [ ] ______ (broken pixel, form, etc.)

---

#### Notes & Observations

**Unexpected Insights**:
- ______

**Customer Feedback**:
- "______________________"

**Technical Issues**:
- ______

---

## Part 5: Weekly Review Framework

### 📅 Weekly GO/NO-GO Checkpoint

**Every Sunday evening**, review full week and decide: CONTINUE, PIVOT, or STOP.

---

#### Week 1 Review (Day 7)

**CONTINUE if**:
- [ ] 20+ leads generated (CPL < R$ 40)
- [ ] CTR > 1.5% across campaigns
- [ ] 50%+ lead quality score (5-7/10)
- [ ] Clear winner emerging (1 angle > others)

**PIVOT if**:
- [ ] 10-20 leads (marginal volume)
- [ ] CTR 1.0-1.5% (weak engagement)
- [ ] CPL R$ 40-75 (expensive but workable)
- [ ] Mixed results (no clear winner)

**STOP if**:
- [ ] < 10 leads (insufficient data)
- [ ] CTR < 1.0% (nobody clicking)
- [ ] CPL > R$ 100 (too expensive)
- [ ] Technical issues unresolved

---

#### Week 2 Review (Day 14)

**CONTINUE if**:
- [ ] 50+ leads total (CPL < R$ 30)
- [ ] 30%+ lead quality score (7-10/10)
- [ ] 1 clear winning angle validated
- [ ] Landing page conversion > 10%

**PIVOT if**:
- [ ] 30-50 leads (volume OK but expensive)
- [ ] CPL R$ 30-50 (acceptable but not great)
- [ ] Lead quality 20-30% (needs improvement)
- [ ] Funnel issues (low conversion)

**STOP if**:
- [ ] < 30 leads total
- [ ] CPL > R$ 50 consistently
- [ ] Lead quality < 20%
- [ ] No clear winner after 2 weeks

---

#### Week 3 Review (Day 21)

**CONTINUE if**:
- [ ] 100+ leads total (CPL < R$ 25)
- [ ] 40%+ lead quality score (7-10/10)
- [ ] Scaling successfully across cities
- [ ] Positive unit economics (CAC < LTV × 3)

**PIVOT if**:
- [ ] 60-100 leads (growing but slow)
- [ ] CPL R$ 25-40 (marginal)
- [ ] Lead quality 30-40% (some validation)
- [ ] Early traction but needs refinement

**STOP if**:
- [ ] < 60 leads total
- [ ] CPL > R$ 40 consistently
- [ ] Lead quality < 30%
- [ ] Cannot scale beyond 1-2 cities

---

#### Week 4 Review (Day 28) - Final Decision

**GO (Build Product)** if:
- [ ] 150+ leads total
- [ ] 50%+ lead quality score (7-10/10)
- [ ] CAC < R$ 100
- [ ] LTV:CAC > 3x projected
- [ ] 20+ qualified beta candidates
- [ ] Clear ICP defined

**PIVOT (Refine Strategy)** if:
- [ ] 80-150 leads (some validation)
- [ ] CAC R$ 100-150 (workable)
- [ ] Lead quality 30-50% (mixed signals)
- [ ] Some channels work, others don't
- [ ] Need second smoke test

**STOP (Not Validated)** if:
- [ ] < 80 leads total
- [ ] CAC > R$ 150
- [ ] Lead quality < 30%
- [ ] No clear ICP or value prop
- [ ] Return to interviews or pivot niche

---

## Part 6: Iteration Decision Trees

### 🌳 Decision Tree: Low CTR (< 1.5%)

**Step 1: Check impressions**
- < 500 → Wait for more data (don't act yet)
- 500-1.000 → Proceed to Step 2
- > 1.000 → Proceed to Step 2

**Step 2: Check creative**
- Creative low quality or unclear → Redesign creative
- Creative looks good → Proceed to Step 3

**Step 3: Check headline/hook**
- Headline weak or generic → Test new hook (pain-driven)
- Headline strong → Proceed to Step 4

**Step 4: Check audience**
- Audience too broad → Narrow interests
- Audience too narrow → Widen targeting
- Audience looks good → Proceed to Step 5

**Step 5: Kill ad**
- Pause ad set
- Create 2 new variations (different hook + creative)
- Test tomorrow

---

### 🌳 Decision Tree: High CPC (> R$ 3.00)

**Step 1: Check competition**
- High competition niche → Accept higher CPC or pivot niche
- Normal competition → Proceed to Step 2

**Step 2: Check ad relevance**
- Relevance score < 5 → Improve creative + headline alignment
- Relevance score 7+ → Proceed to Step 3

**Step 3: Check audience targeting**
- Audience too narrow → Expand interests
- Audience looks good → Proceed to Step 4

**Step 4: Check bid strategy**
- Bid cap too low → Increase bid cap 10-20%
- Lowest cost bid → Proceed to Step 5

**Step 5: Kill or accept**
- CPL still good (< R$ 40) → Accept higher CPC
- CPL bad (> R$ 75) → Pause ad set

---

### 🌳 Decision Tree: Low Conversion (< 10%)

**Step 1: Check landing page traffic**
- < 100 visits → Wait for more data
- 100+ visits → Proceed to Step 2

**Step 2: Check funnel leaks**
- High bounce (>70%) → Fix page load speed, mobile experience
- Low form view (<50%) → Improve CTA placement
- Low form start (<30%) → Simplify form, reduce fields
- Low submit (<10%) → Test value prop, add social proof

**Step 3: Check lead quality**
- Wrong audience → Revisit targeting
- Right audience, wrong messaging → Test new copy
- Price too high → Test pricing page (or hide price)

**Step 4: A/B test**
- Test 1 element at a time (CTA, headline, social proof)
- Run test for 48-72 hours
- Keep winner, kill loser

---

### 🌳 Decision Tree: Poor Lead Quality (WTP < R$ 200)

**Step 1: Check targeting**
- Wrong audience interests → Update targeting
- Too broad → Narrow by job titles, behaviors
- Looks right → Proceed to Step 2

**Step 2: Check messaging**
- Attracting wrong prospects → Test problem-driven hooks
- Value prop unclear → Test benefit-focused copy
- Messaging looks right → Proceed to Step 3

**Step 3: Check landing page**
- No price filter → Add pricing (filters out cheap leads)
- No qualifying questions → Add "Budget" field
- Page looks right → Proceed to Step 4

**Step 4: Accept or pivot**
- Niche not viable → Pause campaign, test other niche
- Early signal → Keep testing, refine targeting

---

## Part 7: Crisis Protocols

### 🚨 Crisis: Zero Leads for 48 Hours

**Immediate Actions (within 2 hours)**:
1. Check ads are running (Meta Ads Manager)
2. Check landing page is live (visit URL)
3. Check form is working (test submit)
4. Check pixel is firing (Meta Pixel Helper)

**Root Cause Analysis**:
- Ads not running → Fix billing/policy issue
- Page not loading → Fix hosting/SSL issue
- Form broken → Fix form/integration issue
- Pixel not firing → Reinstall pixel/CAPI

**Prevention**:
- Set up Meta Ads notifications (email + push)
- Test complete flow daily (morning check)
- Use UTM tracking to diagnose issues
- Have developer on standby

---

### 🚨 Crisis: CPL Exploded to > R$ 100

**Immediate Actions**:
1. Pause all ad sets immediately
2. Review per-ad set performance
3. Kill worst performers (top 50% of CPL)
4. Reallocate budget to winners only

**Root Cause Analysis**:
- Competition increased → Check auction insights
- Ad fatigue → Refresh creative
- Audience saturated → Expand to new cities/interests
- Seasonality → Wait or adjust messaging

**Recovery Strategy**:
- Scale back to proven winners only
- Reduce daily budget 30% temporarily
- Test 1-2 new variations (not full overhaul)
- Wait 48 hours for stabilization

---

### 🚨 Crisis: Technical Issue (Pixel, Form, Page)

**Immediate Actions**:
1. Pause all campaigns immediately
2. Document issue (screenshot + description)
3. Escalate to developer/technical support
4. Create tracking workaround (manual if needed)

**While Fixing**:
- Keep campaigns paused (don't waste budget)
- Test fix thoroughly before resuming
- Update all tracking/monitoring systems
- Document lessons learned

**After Fixing**:
- Resume campaigns gradually (start at 50% budget)
- Monitor closely for 24 hours
- Verify all data is accurate
- Update crisis protocol with learnings

---

## Part 8: Success Metrics & Targets

### 📊 Daily Targets (Per Campaign)

| Metric | Minimum | Target | Stretch |
|--------|---------|--------|----------|
| Spend | R$ 8 | R$ 10-12 | R$ 15 |
| Impressions | 300 | 500+ | 800+ |
| Clicks | 8 | 15+ | 25+ |
| CTR | 1.5% | 2.0%+ | 3.0%+ |
| CPC | R$ 0.50 | R$ 0.80-1.50 | R$ 0.50 |
| Leads | 1 | 2+ | 4+ |
| CPL | < R$ 50 | < R$ 30 | < R$ 20 |

---

### 📊 Weekly Targets (Aggregated)

| Metric | Week 1 | Week 2 | Week 3 | Week 4 |
|--------|--------|--------|--------|--------|
| Total Spend | R$ 80 | R$ 160 | R$ 320 | R$ 480 |
| Total Leads | 15+ | 40+ | 80+ | 150+ |
| Avg CPL | < R$ 40 | < R$ 35 | < R$ 30 | < R$ 25 |
| Lead Quality (7-10) | 30%+ | 40%+ | 50%+ | 60%+ |
| WTP > R$ 300 | 40%+ | 50%+ | 60%+ | 70%+ |

---

### 📊 Final Decision Thresholds (Day 28)

**GO (Build Product)**:
- ✅ 150+ leads total
- ✅ 50%+ score 7-10 (high quality)
- ✅ 60%+ WTP > R$ 300/month
- ✅ CAC < R$ 100
- ✅ LTV:CAC > 3x projected

**PIVOT (Refine Strategy)**:
- ⚠️ 80-150 leads
- ⚠️ 30-50% score 7-10
- ⚠️ CAC R$ 100-150
- ⚠️ Some validation but unclear

**STOP (Not Validated)**:
- ❌ < 80 leads
- ❌ < 30% score 7-10
- ❌ CAC > R$ 150
- ❌ No clear ICP or value prop

---

## Part 9: Tools & Resources

### 🛠️ Required Tools

**Meta Ads Manager**:
- Campaign monitoring
- Ad set performance
- Creative testing
- Audience insights

**Meta Pixel Helper** (Chrome Extension):
- Verify pixel firing
- Test events
- Debug tracking issues

**Google Analytics 4**:
- Traffic source analysis
- User behavior
- Funnel visualization
- UTM tracking

**Hotjar** (Optional):
- Heat maps
- Session recordings
- Form analytics
- Conversion funnel

**Google Sheets / Airtable**:
- Lead tracking
- Qualification data
- Daily performance log
- Weekly summary

---

### 📱 Daily Monitoring Dashboard (Template)

**Tab 1: Daily Performance**
- Date, Spend, Impr, Clicks, CTR, CPC, Leads, CPL
- Filter by Campaign, Ad Set, Creative
- Sparkline charts for trends

**Tab 2: Lead Quality**
- Lead source, problem recognition, WTP, readiness
- Scoring calculator (0-10)
- Qualification status

**Tab 3: Weekly Summary**
- Week number, total spend, total leads, avg CPL
- Lead quality distribution
- Top performers (winners/losers)

**Tab 4: Action Items**
- Date, Campaign, Action (Kill/Scale/Test)
- Reason, Expected Impact, Result
- Follow-up date

---

## Part 10: Execution Checklist

### ✅ Pre-Launch Checklist (Before Day 1)

**Technical Setup**:
- [ ] Meta Pixel installed and verified
- [ ] GA4 property connected and receiving data
- [ ] Landing page live and tested (mobile + desktop)
- [ ] Form tested end-to-end (submission + storage)
- [ ] UTM tracking template configured
- [ ] Google Sheets database connected

**Campaign Setup**:
- [ ] Meta Ads account configured (billing verified)
- [ ] 2 campaigns created (Clínicas + Imobiliárias)
- [ ] 4 ad sets created (Pain + Time angles)
- [ ] 8-12 ads uploaded (creatives + headlines)
- [ ] Budget set (R$ 40/campaign/week)
- [ ] Targeting configured (location, interests, age)
- [ ] Conversion events tracked (Lead, Purchase)

**Monitoring Setup**:
- [ ] Daily report template created
- [ ] Google Sheets dashboard set up
- [ ] Alert notifications configured (Meta + GA4)
- [ ] Crisis protocols documented
- [ ] Developer contact confirmed

---

### ✅ Daily Monitoring Checklist (Every Day)

**Morning (9:00 AM)**:
- [ ] Check ad status (running/paused)
- [ ] Check spend pacing (not too fast/slow)
- [ ] Check for disapprovals or policy issues
- [ ] Verify pixel/CAPI firing
- [ ] Test landing page load time

**Evening (6:00 PM)**:
- [ ] Log daily metrics in report
- [ ] Calculate per-ad set performance
- [ ] Identify winners (scale) and losers (kill)
- [ ] Check lead quality (sample 5-10 leads)
- [ ] Plan tomorrow's actions (test/pause/scale)

**Weekly (Sunday 6:00 PM)**:
- [ ] Review full week performance
- [ ] Calculate weekly averages (CPL, CTR, quality)
- [ ] Make GO/NO-GO decision for next week
- [ ] Document learnings and insights
- [ ] Update strategy based on data

---

## Part 11: Quick Reference Guide

### 🚨 Red Flags (Act Immediately)

| Flag | Threshold | Action |
|------|-----------|--------|
| Zero Spend | R$ 0 for 12h | Check billing/account |
| CPC Explosion | > R$ 4.00 | Pause ad set |
| CTR Collapse | < 1.0% (1k+ impr) | Kill ad, test new |
| Broken Page | 0 conversions | Test page, pause ads |
| Expensive Leads | CPL > R$ 100 | Pause, reallocate |

---

### ✅ Green Flags (Scale Aggressively)

| Flag | Threshold | Action |
|------|-----------|--------|
| High CTR | > 3.0% | Double budget |
| Cheap Leads | CPL < R$ 20 | Double budget |
| High Quality | > 50% score 7-10 | Scale to new cities |
| Viral Signal | Shares/comments | Boost post organically |

---

### ⚠️ Yellow Flags (Monitor Closely)

| Flag | Threshold | Action |
|------|-----------|--------|
| Slow Pace | < 50% budget by 6 PM | Consider increasing budget |
| Marginal CTR | 1.0-1.5% | Test new creative tomorrow |
| Expensive OK | CPL R$ 50-75 | Kill losers, keep winners |
| Low Conversion | 5-10% | A/B test landing page |

---

## Part 12: Logging & Documentation

### 📝 Daily Log Entry Format

```
## Daily Log - DD Month YYYY

### Morning Check (9:00 AM)
- Ad Status: ✅ All running / ❌ Issue: ______
- Spend Pacing: ✅ On track / ⚠️ Behind / ⚠️ Ahead
- Alerts: 🚨 ______ / ✅ None

### Evening Review (6:00 PM)
**Performance**:
- Spend: R$ __ / R$ __ (planned)
- Impressions: __ (target: 500+)
- Clicks: __ (target: 15+)
- CTR: __% (target: 2.0%+)
- Leads: __ (target: 2+)
- CPL: R$ __ (target: < R$ 50)

**Top Performer**: ______ (CTR: __%, CPL: R$ __)
**Bottom Performer**: ______ (CTR: __%, CPL: R$ __)

**Actions Taken**:
- [KILL] ______ (reason: ______)
- [SCALE] ______ (new budget: R$ __)
- [TEST] ______ (variation: ______)

**Lead Quality** (sample: __ leads):
- Problem Recognition: __%
- WTP > R$ 300: __%
- Ready to Buy: __%

**Notes/Observations**: ______

**Tomorrow's Plan**:
- ______
- ______

---

**Agent**: CMO (55827422-a849-41d3-9286-0b5b8b002079)
**Task**: CON-63 - Monitor Smoke Test Performance & Iterate Daily
**Time**: __:__ UTC-3
```

---

## Appendix: Troubleshooting Guide

### Issue: Ads Not Delivering

**Symptoms**: Spend = R$ 0, Impressions = 0

**Possible Causes**:
1. Ad under review (wait 24 hours)
2. Billing issue (check payment method)
3. Ad rejected (check policy guidelines)
4. Audience too small (widen targeting)
5. Bid too low (increase bid cap)

**Solutions**:
- Check Meta Ads Manager for status
- Verify payment method is valid
- Review ad against policies
- Expand audience size (> 500k)
- Increase bid cap 10-20%

---

### Issue: Low CTR (< 1.0%)

**Symptoms**: Impressions high, clicks low

**Possible Causes**:
1. Weak headline/hook
2. Poor creative quality
3. Wrong audience (not interested)
4. Ad fatigue (seen too many times)

**Solutions**:
- Test pain-driven hooks ("Perdendo R$ 5.000/mês?")
- Improve creative (high-quality image/video)
- Narrow audience targeting
- Refresh creative every 3-5 days

---

### Issue: High CPC (> R$ 3.00)

**Symptoms**: Cost per click very expensive

**Possible Causes**:
1. High competition niche
2. Low ad relevance score
3. Narrow audience (auction competition)
4. Bid cap too high (algorithm bidding up)

**Solutions**:
- Improve ad relevance (align creative + headline)
- Widen audience targeting
- Switch to "Lowest Cost" bid strategy
- Accept higher CPC if CPL still good

---

### Issue: Low Landing Page Conversion (< 10%)

**Symptoms**: Clicks high, leads low

**Possible Causes**:
1. Weak value proposition
2. Form too long/complex
3. No social proof
4. Poor mobile experience
5. Wrong expectations (ad vs. page mismatch)

**Solutions**:
- Strengthen headline/benefit statement
- Reduce form fields (name, email, phone only)
- Add testimonials, logos, reviews
- Test mobile responsiveness
- Align ad messaging with landing page

---

### Issue: Poor Lead Quality (WTP < R$ 200)

**Symptoms**: Leads coming in, but not qualified

**Possible Causes**:
1. Wrong audience (attracting wrong prospects)
2. Messaging too generic
3. No price filter (attracts tire-kickers)
4. Value prop unclear

**Solutions**:
- Narrow audience targeting (job titles, behaviors)
- Test problem-driven hooks (filters for pain)
- Add pricing to landing page
- Add qualifying questions (budget, authority)

---

*Prepared by: CMO Agent (55827422-a849-41d3-9286-0b5b8b002079)*
*Linked Task: [CON-63](/PAP/issues/CON-63)*
*Goal: Monitor smoke test performance daily, iterate rapidly based on real data*
*Status: Framework ready for smoke test launch*

**Next Step**: Begin daily monitoring when smoke test launches (CON-49 + CON-51)
