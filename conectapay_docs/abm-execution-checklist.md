# ABM Execution Checklist
## ConectaPay Account-Based Marketing - Step-by-Step Implementation

**Document Version**: 1.0
**Created**: April 26, 2026
**Owner**: CMO Agent
**Related**: account-based-marketing-strategy.md

---

## Phase 1: Foundation (Weeks 1-4)

### Week 1: Setup & Planning

#### CRM Setup
- [ ] Create HubSpot/Pipedrive account
- [ ] Configure "Account" object
- [ ] Configure "Contact" object
- [ ] Create custom fields:
  - [ ] Segment (Clínica/Imobiliária/Academia/Ótica)
  - [ ] Tier (1/2/3)
  - [ ] ICP Score (0-100)
  - [ ] Engagement Score (0-100)
  - [ ] Stage (Identified/Engaged/Opportunity/Closed)
  - [ ] Owner (Sales Rep)
  - [ ] Marketing Owner
- [ ] Create pipeline stages
- [ ] Set up dashboards

#### Spreadsheet Setup
- [ ] Create Google Sheets for account research
- [ ] Create sheets: "All Accounts", "Tier 1", "Tier 2", "Tier 3"
- [ ] Share with team (edit access)
- [ ] Set up Airtable if preferred (optional)

#### LinkedIn Sales Navigator
- [ ] Purchase Sales Navigator Core (R$ 179/mês)
- [ ] Connect to CRM
- [ ] Set up saved searches for each segment
- [ ] Create account lists

#### Planning
- [ ] Finalize ICP scorecard for each segment
- [ ] Define Tier 1, 2, 3 criteria
- [ ] Set target: 50 accounts/segment (200 total)
- [ ] Assign sales owners to accounts

**Deliverable**: ABM infrastructure ready
**Time**: 5-10 hours
**Owner**: CMO + Sales Lead

---

### Week 2: Account Sourcing

#### Clínicas (50 accounts)
- [ ] Search LinkedIn Sales Navigator: "Clínica" + "São Paulo" + 11-50 employees
- [ ] Export to CSV
- [ ] Search Google Maps: "Clínica" + "São Paulo" + 4.0+ rating
- [ ] Search Doctoralia for clinics in SP
- [ ] Compile master list (50 accounts)

#### Imobiliárias (50 accounts)
- [ ] Search LinkedIn Sales Navigator: "Imobiliária" + "Rio de Janeiro" + 11-50 employees
- [ ] Search Portal do Imóvel, Zap Imóveis
- [ ] Search Google Maps: "Imobiliária" + "Rio de Janeiro"
- [ ] Compile master list (50 accounts)

#### Academias (50 accounts)
- [ ] Search LinkedIn Sales Navigator: "Academia" + "Belo Horizonte" + 11-50 employees
- [ ] Search Tecnofitness, Bodytech locations
- [ ] Search Google Maps: "Academia" + "Belo Horizonte"
- [ ] Compile master list (50 accounts)

#### Óticas (50 accounts)
- [ ] Search LinkedIn Sales Navigator: "Ótica" + "Curitiba" + 11-50 employees
- [ ] Search Google Maps: "Ótica" + "Curitiba" + 4.0+ rating
- [ ] Search shopping center directories
- [ ] Compile master list (50 accounts)

#### Verification & Scoring
- [ ] Verify all accounts have:
  - [ ] Company name
  - [ ] Website
  - [ ] City/State
  - [ ] Employee count (est.)
- [ ] Score all accounts using ICP scorecard
- [ ] Classify into Tier 1 (20-40), Tier 2 (60-80), Tier 3 (100-120)
- [ ] Load into CRM
- [ ] Assign owners

**Deliverable**: 200 scored accounts in CRM
**Time**: 15-20 hours
**Owner**: Market Research Agent

---

### Week 3: Account Research (Tier 1 Only)

#### For Each Tier 1 Account (2-3 hours/account)

##### Research Checklist
- [ ] **Company Website** (30 min)
  - [ ] Browse About page
  - [ ] Read last 3 blog posts
  - [ ] Check Careers page (hiring = growth)
  - [ ] Look for case studies/testimonials
  - [ ] Note: Company values, mission, tone

- [ ] **Social Media** (30 min)
  - [ ] Instagram: Last 20 posts, engagement rate
  - [ ] LinkedIn: Last 10 updates, employee count
  - [ ] Facebook: Last 5 posts, reviews
  - [ ] Note: Content themes, posting frequency

- [ ] **Google Search** (30 min)
  - [ ] News about company (last 6 months)
  - [ ] Press releases
  - [ ] Founder interviews/quotes
  - [ ] Awards/recognition
  - [ ] Note: Recent achievements, triggers

- [ ] **Reviews** (30 min)
  - [ ] Google Maps: Last 50 reviews
  - [ ] Facebook reviews
  - [ ] Reclame Aqui (check for complaints)
  - [ ] Note: Common praise themes, pain points

- [ ] **LinkedIn Deep Dive** (30 min)
  - [ ] Identify CEO/Owner (LinkedIn profile)
  - [ ] Identify Marketing Director/Manager
  - [ ] Identify Sales Manager
  - [ ] Note: Backgrounds, shared connections, recent posts

- [ ] **Stakeholder Mapping** (15 min)
  - [ ] Create stakeholder list (2-3 key people)
  - [ ] Find LinkedIn profiles
  - [ ] Find email addresses (Hunter.io, LinkedIn)
  - [ ] Note: Decision makers, influencers

- [ ] **Tech Stack** (15 min)
  - [ ] Identify CRM (HubSpot, Salesforce, etc.)
  - [ ] Identify payment processor (Mercado Pago, Stripe)
  - [ ] Check if WhatsApp Business API is used
  - [ ] Note: Integration opportunities

##### Documentation
- [ ] Complete Account Profile Template (see: abm-account-profile-template.md)
- [ ] Save in Google Drive folder: "ABM/Tier 1/Accounts"
- [ ] Update CRM with research findings
- [ ] Create personalization hooks document

**Deliverable**: Complete account profiles for 20-40 Tier 1 accounts
**Time**: 40-120 hours (can be parallelized)
**Owner**: Market Research Agent

---

### Week 4: Content & Creative Production

#### Tier 1 Content
- [ ] **Microsite Template**
  - [ ] Design microsite layout (Figma)
  - [ ] Write copy template (personalizable fields)
  - [ ] Create video placeholder script
  - [ ] Build in Webflow/Framer (1 page)
  - [ ] Test personalization tokens

- [ ] **Direct Mail Package**
  - [ ] Design custom report template (Canva/Indesign)
  - [ ] Write cover letter template
  - [ ] Source WhatsApp gadget (charging station, stand)
  - [ ] Design box layout
  - [ ] Get quote from printer (50 units)

- [ ] **Outreach Sequence** (8 touches)
  - [ ] Write LinkedIn InMail template (Week 1)
  - [ ] Write direct mail note template (Week 2)
  - [ ] Write phone script (Week 3)
  - [ ] Write WhatsApp video script (Week 4)
  - [ ] Write email case study template (Week 5)
  - [ ] Write LinkedIn engagement scripts (Week 6)
  - [ ] Write phone urgency script (Week 7)
  - [ ] Write email final template (Week 8)

- [ ] **Account-Based Ad Templates**
  - [ ] Meta Ads: 3 ad sets (company name targeting)
  - [ ] LinkedIn Ads: 2 sponsored content templates
  - [ ] Google Ads: 2 search ad templates
  - [ ] Set up UTM tracking structure

- [ ] **Sales Enablement Materials**
  - [ ] One-pager template (account-specific)
  - [ ] Slide deck template (5 slides)
  - [ ] ROI Calculator (pre-fillable)
  - [ ] Integration diagram template

#### Tier 2 Content
- [ ] **Cohort Landing Pages**
  - [ ] Create: conectapay.com.br/clinicas-sp
  - [ ] Create: conectapay.com.br/imobiliarias-rj
  - [ ] Create: conectapay.com.br/academias-bh
  - [ ] Create: conectapay.com.br/oticas-curitiba
  - [ ] Write copy for each (segment-relevant)
  - [ ] Embed ROI calculator (cohort averages)
  - [ ] Add 2-3 case studies per page

- [ ] **Cohort Content**
  - [ ] Plan webinar: "Clínicas em SP: Reduzindo No-Show"
  - [ ] Plan webinar: "Imobiliárias em RJ: Dobrando Conversão"
  - [ ] Write white paper: "No-Show em Clínicas SP (2026 Benchmark)"
  - [ ] Compile case study collection (5 per segment)

- [ ] **Outreach Sequence** (6 touches)
  - [ ] Write LinkedIn InMail template (Week 1)
  - [ ] Write email benchmark template (Week 2)
  - [ ] Write LinkedIn content scripts (Week 3)
  - [ ] Write phone webinar script (Week 4)
  - [ ] Write webinar follow-up template (Week 6)

#### Tier 3 Content
- [ ] **Segment Content** (reuse from CON-28)
  - [ ] LinkedIn posts (segment-specific)
  - [ ] Instagram carousels
  - [ ] Blog posts
  - [ ] Email nurture sequence

- [ ] **Outreach Sequence** (4 touches)
  - [ ] Write LinkedIn connection template (Week 1)
  - [ ] Write email waitlist template (Week 2)
  - [ ] Write LinkedIn engagement scripts (Week 3)
  - [ ] Write email case study template (Week 4)

#### Tracking & Analytics
- [ ] Set up GA4 for all landing pages
- [ ] Set up Meta Pixel
- [ ] Set up LinkedIn Insight Tag
- [ ] Set up UTM tracking sheet
- [ ] Create outreach tracker spreadsheet (see: abm-outreach-tracker-template.csv)

**Deliverable**: All content ready for launch
**Time**: 20-30 hours
**Owner**: Growth Marketing Agent

---

## Phase 2: Launch (Weeks 5-8)

### Week 5: Tier 1 Launch

#### Day 1-2: Direct Mail Setup
- [ ] Order 50 direct mail packages (or 20-40 for Tier 1 only)
- [ ] Personalize each package with:
  - [ ] Company name on report
  - [ ] Specific metrics (no-show rate, revenue lost)
  - [ ] Handwritten note (use service: Willa, Handwrytten)
- [ ] Schedule delivery (Week 6)

#### Day 3-4: Account-Based Ads
- [ ] Set up Meta Ads campaign:
  - [ ] Target: Upload company name lists
  - [ ] Creative: 3 ad variations
  - [ ] Budget: R$ 500-1.000 (Tier 1 only)
  - [ ] Duration: 4 weeks
- [ ] Set up LinkedIn Ads campaign:
  - [ ] Target: Account list upload
  - [ ] Creative: 2 sponsored content
  - [ ] Budget: R$ 500-1.000
  - [ ] Duration: 4 weeks
- [ ] Set up Google Ads campaign:
  - [ ] Target: Brand + competitor keywords
  - [ ] Negative: Broad segment terms
  - [ ] Budget: R$ 200-400
  - [ ] Duration: 4 weeks

#### Day 5: LinkedIn InMail (Wave 1)
- [ ] Send LinkedIn InMail to 50% of Tier 1 stakeholders
- [ ] Use template: abm-execution-checklist.md > Template 1.1
- [ ] Personalize with:
  - [ ] Company name
  - [ ] Stakeholder name
  - [ ] Specific metric (no-show rate, etc.)
  - [ ] Similar case study
- [ ] Track responses in outreach tracker

#### Ongoing (Week 5)
- [ ] Monitor ad performance daily
- [ ] Respond to LinkedIn InMails within 24 hours
- [ ] Update engagement scores in CRM
- [ ] Log all touches in tracker

**Deliverable**: Tier 1 campaign live
**Time**: 10-15 hours
**Owner**: Growth Marketing Agent

---

### Week 6: Tier 2 Launch

#### Day 1-2: Cohort Landing Pages
- [ ] Publish: conectapay.com.br/clinicas-sp
- [ ] Publish: conectapay.com.br/imobiliarias-rj
- [ ] Publish: conectapay.com.br/academias-bh
- [ ] Publish: conectapay.com.br/oticas-curitiba
- [ ] Test all forms, calculators, links
- [ ] Set up GA4 goals

#### Day 3-4: Cohort Ads
- [ ] Set up Meta Ads for cohorts:
  - [ ] Target: Location + Industry + Company size
  - [ ] Creative: 3 ad variations per cohort
  - [ ] Budget: R$ 200-400/cohort
  - [ ] Duration: 4 weeks
- [ ] Set up LinkedIn Ads for cohorts:
  - [ ] Target: Job titles + Location + Industry
  - [ ] Creative: 2 sponsored content per cohort
  - [ ] Budget: R$ 200-400/cohort
  - [ ] Duration: 4 weeks

#### Day 5: LinkedIn InMail (Wave 2)
- [ ] Send LinkedIn InMail to 50% of Tier 2 stakeholders
- [ ] Use template: abm-execution-checklist.md > Template 2.1
- [ ] Personalize with cohort name
- [ ] Track responses

#### Day 5: Email Benchmark (Wave 2)
- [ ] Send email benchmark report to Tier 2
- [ ] Use template: abm-execution-checklist.md > Template 2.2
- [ ] Attach: PDF benchmark report
- [ ] Track opens, clicks

#### Week 6-7: Tier 1 Follow-up
- [ ] Phone calls to Tier 1 (direct mail follow-up)
- [ ] Use template: abm-execution-checklist.md > Template 1.3
- [ ] Log outcomes in tracker

**Deliverable**: Tier 2 campaign live
**Time**: 8-12 hours
**Owner**: Growth Marketing Agent

---

### Week 7: Tier 3 Launch

#### Day 1-2: Segment Content
- [ ] Publish first LinkedIn posts (segment-specific)
- [ ] Publish first Instagram carousels
- [ ] Publish blog posts (if applicable)

#### Day 3-4: Segment Ads
- [ ] Set up Meta Ads for segments:
  - [ ] Target: Broad segment + location
  - [ ] Creative: 3 ad variations per segment
  - [ ] Budget: R$ 100-200/segment
  - [ ] Duration: 4 weeks

#### Day 5: LinkedIn Connections (Wave 3)
- [ ] Send LinkedIn connection requests to Tier 3
- [ ] Use template: abm-execution-checklist.md > Template 3.1
- [ ] Personalize with segment name

#### Day 5: Email Waitlist (Wave 3)
- [ ] Send email waitlist invitation to Tier 3
- [ ] Use template: abm-execution-checklist.md > Template 3.2
- [ ] Track signups

#### Ongoing: Tier 1 & Tier 2 Follow-up
- [ ] Continue phone outreach to Tier 1
- [ ] Send LinkedIn engagement (Tier 2)
- [ ] Respond to all inquiries within 24 hours

**Deliverable**: Tier 3 campaign live
**Time**: 5-8 hours
**Owner**: Growth Marketing Agent

---

### Week 8: First Tier 2 Webinar

#### Day 1-3: Webinar Setup
- [ ] Choose date/time (Thursday 14h or 15h)
- [ ] Set up Zoom (or Google Meet)
- [ ] Create registration page (Typeform, Landingi)
- [ ] Write invitation email
- [ ] Send invitations to Tier 2 accounts (email + LinkedIn)

#### Day 4-5: Webinar Content
- [ ] Create slide deck (10-15 slides)
  - [ ] Slide 1: Title + hook
  - [ ] Slide 2: Problem (benchmark data)
  - [ ] Slide 3: Solution (ConectaPay)
  - [ ] Slide 4: Case study 1
  - [ ] Slide 5: Case study 2
  - [ ] Slide 6: ROI calculator demo
  - [ ] Slide 7: Pilot offer
  - [ ] Slide 8: Q&A
- [ ] Rehearse 2-3 times
- [ ] Test tech (screen share, audio, video)

#### Day 6: Webinar Delivery
- [ ] Go live 15 min early
- [ ] Record session
- [ ] Engage with Q&A
- [ ] Send follow-up emails immediately after:
  - [ ] Attended: Demo offer + Calendly link
  - [ ] Registered but missed: Recording + demo offer
  - [ ] Didn't register: Second chance + recording link

#### Day 7: Follow-up
- [ ] Call all attendees within 48 hours
- [ ] Call all registrants who didn't attend
- [ ] Update pipeline with opportunities
- [ ] Log all touches in tracker

**Deliverable**: Webinar completed, 5-10 demos scheduled
**Time**: 10-15 hours
**Owner**: CMO + Sales Lead

---

## Phase 3: Optimization (Weeks 9-12)

### Week 9: Performance Review

#### Data Analysis
- [ ] Export data from:
  - [ ] CRM (pipeline, engagement scores)
  - [ ] GA4 (landing page visits)
  - [ ] Meta Ads Manager (impressions, CTR, CPC)
  - [ ] LinkedIn Ads Manager
  - [ ] Google Ads Manager
  - [ ] Outreach tracker

#### Calculate Metrics
- [ ] **Tier 1**:
  - [ ] Accounts engaged: _____ / 20-40 ( _____ %)
  - [ ] Opportunities created: _____ / engaged ( _____ %)
  - [ ] Pipeline generated: R$ _______
  - [ ] Deals closed: _____ / opportunities ( _____ %)
  - [ ] Revenue closed: R$ _______
  - [ ] Avg sales cycle: _____ days
  - [ ] CAC per account: R$ _______

- [ ] **Tier 2**:
  - [ ] Accounts engaged: _____ / 60-80 ( _____ %)
  - [ ] Webinar attendance: _____ / invited ( _____ %)
  - [ ] Opportunities from webinar: _____
  - [ ] Pipeline generated: R$ _______

- [ ] **Tier 3**:
  - [ ] Waitlist signups: _____ / 100-120 ( _____ %)
  - [ ] Accounts engaged: _____ / 100-120 ( _____ %)

#### Channel Performance
- [ ] Rank channels by conversion rate:
  1. _________________ ( _____ %)
  2. _________________ ( _____ %)
  3. _________________ ( _____ %)
  4. _________________ ( _____ %)

#### Identify Patterns
- [ ] **Winning patterns** (do more):
  - _________________________________________________
  - _________________________________________________
  - _________________________________________________

- [ ] **Losing patterns** (stop doing):
  - _________________________________________________
  - _________________________________________________
  - _________________________________________________

- [ ] **Stuck accounts** (need re-engagement):
  - _________________________________________________
  - _________________________________________________

#### Create Report
- [ ] Write performance report (2-3 pages)
- [ ] Create dashboard screenshot
- [ ] List optimization recommendations

**Deliverable**: Performance report + optimization plan
**Time**: 5-8 hours
**Owner**: CMO

---

### Week 10: Content Iteration

#### Double Down on Winners
- [ ] Identify top 3 performing content types
- [ ] Produce 2-3 more variations of each
- [ ] Test across all tiers

#### A/B Testing
- [ ] Test new subject lines (email/InMail)
- [ ] Test new hooks (first line)
- [ ] Test new case studies
- [ ] Test new ad creatives
- [ ] Set up proper A/B test structure (control vs variant)

#### Follow-up Content
- [ ] For engaged accounts (score 60+):
  - [ ] Create second-touch content
  - [ ] Deep-dive case studies
  - [ ] ROI calculator pre-filled

#### Refresh Ads
- [ ] Replace underperforming ad creatives
- [ ] Test new images/copy
- [ ] Adjust targeting based on data

**Deliverable**: Updated content library
**Time**: 8-12 hours
**Owner**: Growth Marketing Agent

---

### Week 11: Sales Alignment Review

#### Joint Account Review Meeting
- [ ] Schedule meeting: CMO + Sales Lead + SDRs
- [ ] Agenda:
  - [ ] Pipeline review by account (20 min)
  - [ ] Stuck accounts: Brainstorm tactics (20 min)
  - [ ] Assign next actions (10 min)
  - [ ] Set targets for next month (10 min)

#### Update Account Plans (Tier 1)
- [ ] For each Tier 1 account:
  - [ ] Review current stage
  - [ ] Update stakeholder map
  - [ ] Identify obstacles
  - [ ] Plan next 30 days
  - [ ] Assign resources needed

#### Re-assign Stalled Accounts
- [ ] Identify accounts with no engagement in 30+ days
- [ ] Decide: Re-engage or return to pool
- [ ] If re-engage: New tactic, new owner
- [ ] If return to pool: Document lessons learned

#### Brainstorm Tactics for Blocked Accounts
- [ ] For accounts stuck in "Engaged":
  - [ ] New channel (e.g., direct mail, executive outreach)
  - [ ] New stakeholder (find another decision maker)
  - [ ] New offer (pilot, discount, trial)

**Deliverable**: Updated account plans
**Time**: 5-8 hours
**Owner**: CMO + Sales Lead

---

### Week 12: Pipeline Review & Forecast

#### Pipeline Analysis
- [ ] Review all opportunities in CRM
- [ ] Categorize by stage:
  - [ ] Discovery: _____ accounts, R$ _______ pipeline
  - [ ] Demo: _____ accounts, R$ _______ pipeline
  - [ ] Proposal: _____ accounts, R$ _______ pipeline
  - [ ] Negotiation: _____ accounts, R$ _______ pipeline

#### Forecast Q2 Closes
- [ ] Identify likely closes (80%+ probability):
  - [ ] Account: _________________, R$ _______, Expected: [Month]
  - [ ] Account: _________________, R$ _______, Expected: [Month]
  - [ ] Account: _________________, R$ _______, Expected: [Month]
- [ ] Sum forecasted revenue: R$ _______

#### Identify At-Risk Opportunities
- [ ] Flag opportunities stalled 60+ days
- [ ] Flag opportunities with no engagement 30+ days
- [ ] Create re-engagement plan for each

#### Acceleration Tactics
- [ ] For opportunities stuck in "Demo":
  - [ ] Offer: Limited-time pilot (90 days free)
  - [ ] Offer: Executive call (CEO-to-CEO)
  - [ ] Offer: Case study call (existing customer reference)

- [ ] For opportunities stuck in "Proposal":
  - [ ] Offer: Discount for early commitment
  - [ ] Offer: Extended trial (6 months instead of 3)
  - [ ] Offer: Money-back guarantee

#### Report to Stakeholders
- [ ] Create Q2 forecast presentation
- [ ] Include: Pipeline, forecast, risks, requests
- [ ] Present to CEO/investors

**Deliverable**: Pipeline forecast + acceleration plan
**Time**: 5-8 hours
**Owner**: CMO + Sales Lead

---

## Phase 4: Scale (Months 4-12)

### Monthly Recurring Tasks

#### Each Month:
- [ ] **Add 20-30 new accounts**
  - [ ] Source accounts (repeat Week 2 process)
  - [ ] Score and classify
  - [ ] Research Tier 1 new accounts
  - [ ] Load into CRM

- [ ] **Launch campaigns for new accounts**
  - [ ] Tier 1: Direct mail + InMail + Ads
  - [ ] Tier 2: Landing page + Email + Webinar invite
  - [ ] Tier 3: Content + Waitlist email

- [ ] **Review and optimize existing campaigns**
  - [ ] Pause underperforming ads
  - [ ] Scale winning ads (increase budget)
  - [ ] Update content based on feedback

- [ ] **Report on KPIs**
  - [ ] Update dashboard
  - [ ] Share with team
  - [ ] Identify gaps vs targets

### Quarterly Reviews

#### Q1 Review (Months 1-3): Optimize
- [ ] Full program review (all tiers)
- [ ] Double down on winning segments
- [ ] Cut losing segments
- [ ] Adjust targets for Q2

#### Q2 Review (Months 4-6): Expand
- [ ] Add 100 new accounts (300 total)
- [ ] Launch in 2 new cities (e.g., Salvador, Brasília)
- [ ] Hire 1-2 SDRs if needed
- [ ] Consider ABM platform (6sense, Demandbase)

#### Q3 Review (Months 7-9): Deepen
- [ ] Add 50 more Tier 1 accounts (50 total)
- [ ] Launch customer marketing (upsell, cross-sell)
- [ ] Launch referral program (see CON-85)
- [ ] Optimize CAC

#### Q4 Review (Months 10-12): Full Year Review
- [ ] Review Year 1 performance vs targets
- [ ] Calculate ROI (ABM revenue / ABM investment)
- [ ] Document lessons learned
- [ ] Plan Year 2 strategy

---

## Quick Reference: Daily/Weekly Tasks

### Daily (15-30 min)
- [ ] Check LinkedIn for responses
- [ ] Check email for replies
- [ ] Respond within 24 hours
- [ ] Log touches in tracker
- [ ] Update engagement scores

### Weekly (2-3 hours)
- [ ] Review pipeline (all stages)
- [ ] Plan next week's touches
- [ ] Create content for next week
- [ ] Review ad performance
- [ ] Adjust budget if needed
- [ ] Report to team

---

## Appendix: File Organization

### Google Drive Structure
```
ConectaPay ABM/
├── 01-Strategy/
│   └── account-based-marketing-strategy.md
├── 02-Templates/
│   ├── abm-account-profile-template.md
│   ├── abm-account-scoring-template.csv
│   ├── abm-outreach-tracker-template.csv
│   └── abm-execution-checklist.md
├── 03-Accounts/
│   ├── Tier-1/
│   │   ├── Account-01-Clínica-SP/
│   │   │   ├── profile.md
│   │   │   ├── stakeholders.md
│   │   │   └── plan.md
│   │   └── ...
│   ├── Tier-2/
│   └── Tier-3/
├── 04-Content/
│   ├── Microsites/
│   ├── Landing-Pages/
│   ├── Email-Templates/
│   ├── LinkedIn-Scripts/
│   ├── Ad-Creatives/
│   └── Case-Studies/
├── 05-Performance/
│   ├── Weekly-Reports/
│   ├── Monthly-Reports/
│   └── Quarterly-Reviews/
└── 06-Tech/
    ├── CRM-Setup/
    ├── Analytics-Setup/
    └── Ad-Accounts/
```

---

**Next Step**: Execute Week 1 tasks (Setup & Planning)
**Timeline**: 12 weeks to full launch + optimization
**Budget**: R$ 3.000-8.000/mês (ads + tools + direct mail)
**Team**: CMO (strategy), Sales Lead (execution), Growth Marketing Agent (content/ads)

---

**Document Version**: 1.0
**Last Updated**: April 26, 2026
**Next Review**: May 26, 2026 (30-day review)
