# ConectaPay Smoke Test Launch Checklist

**Version**: 1.0
**Created**: 2026-04-26
**Status**: Ready for Execution
**Issue**: [CON-186](/conectapay/issues/CON-186)
**Timeline**: Day 1-4 (4-6 hours total)

---

## Purpose

This checklist provides a step-by-step guide for launching ConectaPay's smoke test campaign. It ensures all infrastructure is in place, all integrations are working, and nothing is missed before going live.

**Use This Checklist When**:
- Launching smoke test campaigns (Meta Ads, Google Ads)
- Setting up new landing pages
- Configuring analytics and tracking
- Preparing for paid media campaigns

**Prerequisites**:
- 90-Day Marketing Execution Calendar reviewed (CON-185)
- Smoke Test Execution Guide reviewed (CON-25)
- Landing page copy finalized (smoke-test-landing-page-copy.md)
- Ad copy finalized (smoke-test-ad-copy.md)

---

## Launch Timeline

```
Day 1 (Monday): Infrastructure Setup (4-6 hours)
  ├─ Platform selection & setup (2 hours)
  ├─ Analytics configuration (2 hours)
  └─ Form builder setup (1 hour)

Day 2 (Tuesday): Landing Page Copy & Design (8 hours)
  ├─ Copy finalization (2 hours)
  ├─ Visual design (4 hours)
  └─ Page build (2 hours)

Day 3 (Wednesday): Integration & Testing (4 hours)
  ├─ Analytics integration (2 hours)
  ├─ Form integration (1 hour)
  └─ Cross-browser testing (1 hour)

Day 4 (Thursday): QA & Launch (4 hours)
  ├─ Final QA (2 hours)
  ├─ Launch 🚀 (30 minutes)
  └─ Post-launch verification (1.5 hours)
```

---

## Day 1: Infrastructure Setup (Monday)

### Step 1.1: Landing Page Platform Selection (30 minutes)

**Objective**: Choose and set up landing page platform

**Options**:
- **Webflow** (Recommended): Visual design, powerful, R$ 180-420/month
- **Framer**: Fast, modern, limited customization, R$ 0-70/month
- **Unbounce**: Optimized for conversions, expensive, R$ 270-740/month
- **Carrd**: Simple, cheap, limited, R$ 0-49/month

**Decision Framework**:
| Factor | Webflow | Framer | Unbounce | Carrd |
|--------|---------|--------|----------|-------|
| Ease of use | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| Customization | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐ |
| Analytics | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ |
| Speed | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| Price | R$ 180-420 | R$ 0-70 | R$ 270-740 | R$ 0-49 |
| **Recommended** | ✅ | ✅ (budget) | ❌ | ❌ (limited) |

**Action Items**:
- [ ] Select platform (Webflow recommended)
- [ ] Create account
- [ ] Choose subscription plan
- [ ] Connect custom domain (if available)

**Time Estimate**: 30 minutes
**Owner**: Growth Marketing

---

### Step 1.2: Domain Configuration (30 minutes)

**Objective**: Configure custom domain for landing page

**Domain Options**:
- **Primary**: `get.conectapay.com.br` (subdomain of conectapay.com.br)
- **Secondary**: `lp.conectapay.com.br` (alternative subdomain)
- **Tertiary**: `conectapay.com.br/oferta` (directory on main site)

**Action Items**:
- [ ] Log in to domain registrar (GoDaddy, Namecheap, etc.)
- [ ] Create subdomain: `get.conectapay.com.br`
- [ ] Configure DNS records:
  - Type: **CNAME**
  - Name: **get**
  - Value: **proxy-ssl.webflow.com** (if using Webflow)
  - TTL: **3600** (1 hour)
- [ ] Verify DNS propagation (use: https://www.whatsmydns.net/)
- [ ] Enable SSL certificate (automatic on Webflow/Framer)

**Verification**:
- [ ] Visit `https://get.conectapay.com.br` - should show landing page (after build)

**Time Estimate**: 30 minutes
**Owner**: Growth Marketing
**Notes**: DNS propagation can take 24-48 hours, start early!

---

### Step 1.3: Google Analytics 4 Setup (45 minutes)

**Objective**: Set up GA4 property and tracking

**Action Items**:

1. **Create GA4 Property**:
   - [ ] Log in to https://analytics.google.com/
   - [ ] Click "Admin" → "Create Account"
   - [ ] Account name: **ConectaPay Marketing**
   - [ ] Property name: **ConectaPay Smoke Test**
   - [ ] Reporting time zone: **America/Sao Paulo (GMT-3)**
   - [ ] Currency: **BRL (R$ Brazilian Real)**
   - [ ] Click "Next" and accept terms

2. **Set Up Data Stream**:
   - [ ] Click "Admin" → "Data Streams" → "Add stream"
   - [ ] Platform: **Web**
   - [ ] Stream URL: **https://get.conectapay.com.br**
   - [ ] Stream name: **Smoke Test Landing Page**
   - [ ] Enhanced measurement: **Enabled** (page views, scrolls, outbound clicks, site search)

3. **Get Measurement ID**:
   - [ ] Copy **Measurement ID** (format: `G-XXXXXXXXXX`)
   - [ ] Save to notepad (needed for landing page integration)

4. **Configure Events** (after landing page is live):
   - [ ] Go to "Configure" → "Events"
   - [ ] Create custom events:
     - `waitlist_signup` (when form submitted)
     - `cta_click` (when CTA button clicked)
     - `video_play` (if video on page)
     - `link_click` (outbound links)

**Time Estimate**: 45 minutes
**Owner**: Growth Marketing
**Deliverable**: GA4 Measurement ID: `G-XXXXXXXXXX`

---

### Step 1.4: Meta Pixel Setup (45 minutes)

**Objective**: Set up Meta (Facebook) Pixel for tracking

**Action Items**:

1. **Create Meta Pixel**:
   - [ ] Log in to https://business.facebook.com/
   - [ ] Go to "Events Manager"
   - [ ] Click "Connect Data Sources" → "Web" → "Meta Pixel"
   - [ ] Pixel name: **ConectaPay Smoke Test**
   - [ ] Click "Create Pixel"

2. **Get Pixel ID**:
   - [ ] Copy **Pixel ID** (format: 16-digit number)
   - [ ] Save to notepad (needed for landing page integration)

3. **Configure Conversions** (after landing page is live):
   - [ ] Go to "Events Manager" → "Conversions" → "Create Custom Conversion"
   - [ ] Event: **Lead** (waitlist signup)
   - [ ] Conversion name: **Waitlist Signup**
   - [ ] Value: **R$ 50** (estimated lead value)
   - [ ] Conversion window: **7 days click, 1 day view**

4. **Test Pixel**:
   - [ ] Install Meta Pixel Helper Chrome Extension
   - [ ] Visit landing page
   - [ ] Verify Pixel fires (green checkmark in extension)

**Time Estimate**: 45 minutes
**Owner**: Growth Marketing
**Deliverable**: Meta Pixel ID: XXXXXXXXXXXXXXXX

---

### Step 1.5: Hotjar Setup (30 minutes)

**Objective**: Set up heatmaps and session recordings

**Action Items**:

1. **Create Hotjar Account**:
   - [ ] Log in to https://www.hotjar.com/
   - [ ] Sign up (free plan: up to 1.000 pageviews/day)
   - [ ] Site name: **ConectaPay Smoke Test**
   - [ ] Site URL: **https://get.conectapay.com.br**

2. **Install Hotjar Tracking Code**:
   - [ ] Copy **Hotjar Site ID** (format: 6-digit number)
   - [ ] Save to notepad (needed for landing page integration)

3. **Configure Heatmaps**:
   - [ ] Go to "Heatmaps" → "Add Heatmap"
   - [ ] Page type: **All pages**
   - [ ] Sample rate: **100%** (capture all visitors)
   - [ ] Devices: **Desktop + Tablet + Mobile**

4. **Configure Recordings**:
   - [ ] Go to "Recordings" → "Add Recording"
   - [ ] Page type: **All pages**
   - [ ] Sample rate: **10-20%** (10-20% of visitors)
   - [ ] Max recordings: **100/day** (free plan limit)

**Time Estimate**: 30 minutes
**Owner**: Growth Marketing
**Deliverable**: Hotjar Site ID: XXXXXX

---

### Step 1.6: Waitlist Form Setup (60 minutes)

**Objective**: Set up waitlist form to collect leads

**Options**:
- **Typeform** (Recommended): Beautiful, easy, R$ 0-70/month
- **Google Forms**: Free, basic, limited customization
- **Tally**: Free, open source, simpler than Typeform
- **Custom**: Build yourself (Webflow forms)

**Decision**: Use Typeform (better UX, higher conversion)

**Action Items**:

1. **Create Typeform Account**:
   - [ ] Log in to https://typeform.com/
   - [ ] Sign up (free plan: up to 3 forms, 100 responses/month)

2. **Build Waitlist Form**:
   - [ ] Create new form: **ConectaPay Waitlist**
   - [ ] Add questions:
     - **Q1**: Name (short text) - Required
     - **Q2**: Email (email) - Required
     - **Q3**: Company name (short text) - Required
     - **Q4**: Phone (short text) - Optional (for WhatsApp outreach)
     - **Q5**: Segment (dropdown: Clínica, Imobiliária, Academia, Ótica, Outro) - Required
     - **Q6**: Biggest challenge (long text: "Qual seu maior desafio hoje?") - Optional
   - [ ] Customize design:
     - Add ConectaPay logo
     - Use brand colors (if available)
     - Enable progress bar
     - Hide Typeform branding (paid plan only)

3. **Configure Thank You Screen**:
   - [ ] Message: "Obrigado por se juntar à lista de espera! Entraremos em contato em breve."
   - [ ] Redirect: None (keep on thank you screen)
   - [ ] Optional: Add social media links

4. **Get Form Embed Code**:
   - [ ] Go to "Share" → "Launch"
   - [ ] Copy **Embed code** (HTML snippet)
   - [ ] Save to notepad (needed for landing page integration)

**Form Fields Specification**:
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| Name | Short text | ✅ | Contact person name |
| Email | Email | ✅ | For follow-up communication |
| Company | Short text | ✅ | For account-based scoring |
| Phone | Short text | ❌ | For WhatsApp outreach |
| Segment | Dropdown | ✅ | For ICP segmentation |
| Challenge | Long text | ❌ | For pain point validation |

**Time Estimate**: 60 minutes
**Owner**: Growth Marketing
**Deliverable**: Typeform embed code

---

### Day 1 Completion Checklist

**Deliverables**:
- [ ] Landing page platform selected and account created
- [ ] Custom domain configured (get.conectapay.com.br)
- [ ] GA4 property created (Measurement ID: `G-XXXXXXXXXX`)
- [ ] Meta Pixel created (Pixel ID: XXXXXXXXXXXXXXXX)
- [ ] Hotjar account created (Site ID: XXXXXX)
- [ ] Waitlist form built (Typeform embed code ready)

**Verification**:
- [ ] All accounts created and accessible
- [ ] All tracking codes saved to notepad
- [ ] Domain DNS configured (may take 24-48h to propagate)
- [ ] Tech stack document finalized

**Time Invested**: 4-5 hours
**Next**: Day 2 - Landing page copy and design

---

## Day 2: Landing Page Copy & Design (Tuesday)

### Step 2.1: Landing Page Copy Finalization (2 hours)

**Objective**: Finalize landing page copy based on smoke-test-landing-page-copy.md

**Action Items**:

1. **Review Copy Template**:
   - [ ] Read `smoke-test-landing-page-copy.md` (CON-25 deliverable)
   - [ ] Identify key sections: Hero, Social Proof, Problem, Solution, Benefits, Pricing, FAQ, CTA
   - [ ] Confirm value proposition: "Recupere vendas abandonadas no WhatsApp"

2. **Finalize Headline** (test 3 variations):
   - [ ] **Variation A**: "Recupere R$ 3.000/mês em vendas perdidas no WhatsApp"
   - [ ] **Variation B**: "Automatize seu atendimento no WhatsApp e recupere vendas"
   - [ ] **Variation C**: "7 em cada 10 clientes abandonam compras no WhatsApp. Recupere eles."
   - [ ] Select primary headline (start with Variation A)

3. **Finalize Subheadline**:
   - [ ] Copy from template: "A plataforma que automatiza vendas, follow-ups e pagamentos via WhatsApp e Pix para pequenos negócios."
   - [ ] Edit for clarity and impact

4. **Finalize Benefits** (3-5 key benefits):
   - [ ] Benefit 1: "Recupere até 70% das vendas perdidas"
   - [ ] Benefit 2: "Automatize follow-ups no WhatsApp"
   - [ ] Benefit 3: "Receba pagamentos via Pix instantaneamente"
   - [ ] Benefit 4: "Reduza no-shows em até 80%" (for clínicas)
   - [ ] Benefit 5: "Setup em 15 minutos, sem código"

5. **Finalize Social Proof** (if available):
   - [ ] Add testimonial quote (if beta customer exists)
   - [ ] Add "Usado por 50+ negócios" (if true)
   - [ ] Add logos (if any partnerships exist)

6. **Finalize CTA** (Call-to-Action):
   - [ ] Primary CTA button: "Entrar na Lista de Espera"
   - [ ] Secondary CTA text: "Junte-se a 500+ negócios na fila"
   - [ ] CTA urgency: "Vagas limitadas para首批 usuários"

**Copy Review Checklist**:
- [ ] Headline is clear and compelling
- [ ] Subheadline explains what it is
- [ ] Benefits are specific and quantified
- [ ] Social proof is credible
- [ ] CTA is action-oriented
- [ ] Copy is in Portuguese (Brazilian)
- [ ] Copy length is 300-500 words (not too long)

**Time Estimate**: 2 hours
**Owner**: Growth Marketing + CMO (review)
**Deliverable**: Finalized landing page copy document

---

### Step 2.2: Visual Design (4 hours)

**Objective**: Create visual design for landing page

**Action Items**:

1. **Define Design System**:
   - [ ] **Colors**:
     - Primary: #00A884 (WhatsApp green)
     - Secondary: #25D366 (Meta green)
     - Accent: #32BCAD (ConectaPay teal)
     - Dark: #111827 (text)
     - Light: #F9FAFB (background)
   - [ ] **Typography**:
     - Headings: Inter or Poppins (bold, 32-48px)
     - Body: Inter or Roboto (regular, 16-18px)
     - CTA: Inter or Poppins (semibold, 18-20px)
   - [ ] **Spacing**: 8px grid system (8, 16, 24, 32, 48, 64px)
   - [ ] **Border radius**: 8px (buttons, cards)

2. **Create Wireframe** (Figma, Sketch, or paper):
   - [ ] **Hero Section**:
     - Headline (H1, centered, 48px)
     - Subheadline (H2, centered, 20px)
     - CTA button (centered, prominent)
     - Hero image (mockup or illustration)
   - [ ] **Social Proof Section**:
     - Logos strip or testimonial quote
     - "Used by 50+ businesses" badge
   - [ ] **Problem Section**:
     - "Você está perdendo vendas?" heading
     - 3 pain points (icons + text)
   - [ ] **Solution Section**:
     - "Como funciona" heading
     - 3-step process (1 → 2 → 3)
   - [ ] **Benefits Section**:
     - 3-5 benefit cards (icon + headline + text)
   - [ ] **Pricing Section** (optional):
     - "A partir de R$ 97/mês"
     - "Sem cartão, teste grátis"
   - [ ] **FAQ Section**:
     - 3-5 common questions
     - Accordion style
   - [ ] **Final CTA Section**:
     - "Pronto para recuperar vendas?"
     - CTA button (repeat primary CTA)
   - [ ] **Footer**:
     - ConectaPay logo
     - "© 2026 ConectaPay. Todos os direitos reservados."
     - Privacy policy link (placeholder)

3. **Design Hero Section** (most important):
   - [ ] Create eye-catching headline (48px, bold, centered)
   - [ ] Add supporting subheadline (20px, regular, centered)
   - [ ] Design CTA button:
     - Background: Primary green (#00A884)
     - Text: White (#FFFFFF)
     - Size: 200px wide × 56px tall
     - Border radius: 8px
     - Hover effect: Slightly darker green
   - [ ] Add hero image:
     - Option A: Product mockup (WhatsApp interface)
     - Option B: Illustration (person using phone)
     - Option C: Screenshot (if product exists)
   - [ ] Ensure mobile responsive (stack vertically on mobile)

4. **Design Social Proof Section**:
   - [ ] Add testimonial quote (if available)
   - [ ] Add "Usado por" logos strip (gray logos, 50% opacity)
   - [ ] Add star rating (★★★★★ 4.9/5)

5. **Design Benefits Section**:
   - [ ] Create 3-5 benefit cards in grid layout
   - [ ] Each card: Icon (emoji or SVG) + Headline + Text
   - [ ] 3 columns on desktop, 1 column on mobile

**Design Review Checklist**:
- [ ] Design is clean and uncluttered
- [ ] Color contrast is accessible (WCAG AA)
- [ ] Typography is readable (16px min body text)
- [ ] CTA button is prominent (high contrast)
- [ ] Mobile responsive (test on 375px width)
- [ ] Images are optimized (<200KB each)
- [ ] Design follows brand guidelines

**Time Estimate**: 4 hours
**Owner**: Growth Marketing + Designer (if available)
**Deliverable**: Figma file or design mockup

---

### Step 2.3: Landing Page Build (2 hours)

**Objective**: Build landing page in chosen platform

**Action Items**:

1. **Set Up Landing Page Project**:
   - [ ] Log in to platform (Webflow, Framer, etc.)
   - [ ] Create new project: **ConectaPay Smoke Test**
   - [ ] Select template: Blank canvas
   - [ ] Set canvas size: Desktop (1920px width)

2. **Build Hero Section**:
   - [ ] Add heading element (H1, 48px, bold, centered)
   - [ ] Add text element (subheadline, 20px, regular, centered)
   - [ ] Add button element (CTA, 200px × 56px, green background)
   - [ ] Add image element (hero image, right-aligned or centered)
   - [ ] Adjust spacing: 64px top padding, 48px bottom padding

3. **Build Social Proof Section**:
   - [ ] Add section container (light gray background: #F9FAFB)
   - [ ] Add testimonial quote (italic, 24px, centered)
   - [ ] Add logos strip (flexbox row, 50% opacity)
   - [ ] Adjust spacing: 48px padding

4. **Build Problem Section**:
   - [ ] Add heading (H2: "Você está perdendo vendas?")
   - [ ] Add 3 pain points (flexbox row, icon + text each)
   - [ ] Adjust spacing: 64px padding

5. **Build Solution Section**:
   - [ ] Add heading (H2: "Como funciona")
   - [ ] Add 3-step process (1 → 2 → 3, numbered)
   - [ ] Adjust spacing: 64px padding

6. **Build Benefits Section**:
   - [ ] Add heading (H2: "Benefícios")
   - [ ] Add 3-5 benefit cards (grid layout, 3 columns)
   - [ ] Each card: Icon + Headline (H3) + Text (p)
   - [ ] Adjust spacing: 64px padding

7. **Build FAQ Section**:
   - [ ] Add heading (H2: "Perguntas Frequentes")
   - [ ] Add 3-5 FAQ items (accordion style if possible)
   - [ ] Each FAQ: Question (H3) + Answer (p)
   - [ ] Adjust spacing: 64px padding

8. **Build Final CTA Section**:
   - [ ] Add heading (H2: "Pronto para recuperar vendas?")
   - [ ] Add CTA button (repeat primary CTA)
   - [ ] Add subtext ("Junte-se a 500+ negócios na fila")
   - [ ] Adjust spacing: 64px padding

9. **Build Footer**:
   - [ ] Add ConectaPay logo or text
   - [ ] Add copyright text
   - [ ] Add privacy policy link (placeholder: #)
   - [ ] Adjust spacing: 32px padding

**Mobile Responsive Check**:
- [ ] Test on 375px width (mobile)
- [ ] Ensure all sections stack vertically
- [ ] Reduce font sizes: H1 32px, H2 24px, body 14px
- [ ] Reduce padding: 32px instead of 64px
- [ ] Ensure CTA button is full width (100%)

**Time Estimate**: 2 hours
**Owner**: Growth Marketing
**Deliverable**: Functional landing page (not yet published)

---

### Day 2 Completion Checklist

**Deliverables**:
- [ ] Landing page copy finalized (300-500 words)
- [ ] Visual design complete (Figma file or mockup)
- [ ] Landing page built in platform (not yet live)
- [ ] Mobile responsive design verified
- [ ] Design system documented (colors, typography, spacing)

**Verification**:
- [ ] Copy reviewed by CMO
- [ ] Design follows brand guidelines
- [ ] Mobile view tested (375px width)
- [ ] All sections built (Hero → Footer)

**Time Invested**: 8 hours
**Next**: Day 3 - Integration and testing

---

## Day 3: Integration & Testing (Wednesday)

### Step 3.1: Analytics Integration (2 hours)

**Objective**: Integrate GA4, Meta Pixel, and Hotjar into landing page

**Action Items**:

1. **Add GA4 Tracking Code**:
   - [ ] Go to landing page project settings
   - [ ] Find "Custom Code" or "Scripts" section
   - [ ] Paste GA4 tracking code in `<head>` section:
     ```html
     <!-- Google tag (gtag.js) -->
     <script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
     <script>
       window.dataLayer = window.dataLayer || [];
       function gtag(){dataLayer.push(arguments);}
       gtag('js', new Date());
       gtag('config', 'G-XXXXXXXXXX');
     </script>
     ```
   - [ ] Replace `G-XXXXXXXXXX` with actual Measurement ID
   - [ ] Save and publish changes

2. **Add Meta Pixel Code**:
   - [ ] In same "Custom Code" section
   - [ ] Paste Meta Pixel script after GA4 code:
     ```html
     <!-- Meta Pixel Code -->
     <script>
       !function(f,b,e,v,n,t,s)
       {if(f.fbq)return;n=f.fbq=function(){n.callMethod?
       n.callMethod.apply(n,arguments):n.queue.push(arguments)};
       if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
       n.queue=[];t=b.createElement(e);t.async=!0;
       t.src=v;s=b.getElementsByTagName(e)[0];
       s.parentNode.insertBefore(t,s)}(window, document,'script',
       'https://connect.facebook.net/en_US/fbevents.js');
       fbq('init', 'XXXXXXXXXXXXXXX');
       fbq('track', 'PageView');
     </script>
     <noscript>
       <img height="1" width="1" style="display:none"
       src="https://www.facebook.com/tr?id=XXXXXXXXXXXXXXX&ev=PageView&noscript=1"/>
     </noscript>
     ```
   - [ ] Replace `XXXXXXXXXXXXXXX` with actual Pixel ID
   - [ ] Save and publish changes

3. **Add Hotjar Tracking Code**:
   - [ ] In same "Custom Code" section
   - [ ] Paste Hotjar script after Meta Pixel:
     ```html
     <!-- Hotjar Tracking Code -->
     <script>
       (function(h,o,t,j,a,r){
         h.hj=h.hj||function(){(h.hj.q=h.hj.q||[]).push(arguments)};
         h._hjSettings={hjid:XXXXXX,hjsv:6};
         a=o.getElementsByTagName('head')[0];
         r=o.createElement('script');r.async=1;
         r.src=t+h._hjSettings.hjid+j+h._hjSettings.hjsv;
         a.appendChild(r);
       })(window,document,'https://static.hotjar.com/c/hotjar-','.js?sv=');
     </script>
     ```
   - [ ] Replace `XXXXXX` with actual Hotjar Site ID
   - [ ] Save and publish changes

4. **Configure Custom Events** (GA4):
   - [ ] Go to GA4 → "Configure" → "Events" → "Create event"
   - [ ] Event name: `waitlist_signup`
   - [ ] Matching condition: `event_name` equals `form_submit`
   - [ ] Repeat for: `cta_click`, `scroll_depth_50`, `scroll_depth_100`

**Time Estimate**: 2 hours
**Owner**: Growth Marketing
**Verification**:
- [ ] All tracking codes added to `<head>` section
- [ ] Landing page republished with codes
- [ ] GA4 real-time report shows active users (test by visiting page)
- [ ] Meta Pixel Helper shows pixel firing
- [ ] Hotjar recordings show session data

---

### Step 3.2: Form Integration (1 hour)

**Objective**: Embed Typeform waitlist form into landing page

**Action Items**:

1. **Choose Integration Method**:
   - [ ] **Option A**: Embed inline (form shows on page)
   - [ ] **Option B**: Popup/overlay (form appears on CTA click)
   - [ ] **Option C**: Redirect (CTA button goes to Typeform URL)
   - [ ] **Recommended**: Option A (inline, highest conversion)

2. **Embed Form Inline** (Option A):
   - [ ] Copy Typeform embed code (from Day 1, Step 1.6)
   - [ ] Go to landing page project
   - [ ] Add "Embed" element to Final CTA section
   - [ ] Paste Typeform embed code
   - [ ] Adjust height: 400px (enough for full form)
   - [ ] Center the form
   - [ ] Test: Form should be visible and functional

3. **Or Redirect to Typeform** (Option C - simpler):
   - [ ] Select CTA button
   - [ ] Add link: https://form.typeform.com/to/XXXXXX
   - [ ] Check "Open in new tab" (better UX)
   - [ ] Test: Clicking CTA opens Typeform in new tab

4. **Test Form Submission**:
   - [ ] Submit test form entry
   - [ ] Verify data appears in Typeform responses
   - [ ] Check that all fields are captured
   - [ ] Verify thank you screen displays

**Time Estimate**: 1 hour
**Owner**: Growth Marketing
**Verification**:
- [ ] Form is visible on landing page
- [ ] Form is mobile responsive (fits on mobile screen)
- [ ] Test submission successful
- [ ] Data captured in Typeform

---

### Step 3.3: Cross-Browser Testing (1 hour)

**Objective**: Test landing page on all browsers and devices

**Action Items**:

1. **Desktop Browser Testing**:
   - [ ] **Google Chrome** (Windows/Mac): Test all sections
   - [ ] **Safari** (Mac): Test all sections
   - [ ] **Firefox** (Windows/Mac): Test all sections
   - [ ] **Edge** (Windows): Test all sections

2. **Mobile Browser Testing**:
   - [ ] **Safari iOS** (iPhone): Test on 375px width
   - [ ] **Chrome Android** (Samsung, etc.): Test on 360px width
   - [ ] Verify mobile responsive (all sections stack vertically)

3. **Functionality Testing**:
   - [ ] All links work (privacy policy, social media)
   - [ ] CTA button is clickable
   - [ ] Form submission works (test entry)
   - [ ] Images load correctly
   - [ ] No broken layout elements

4. **Performance Testing**:
   - [ ] Use Google PageSpeed Insights: https://pagespeed.web.dev/
   - [ ] Enter landing page URL
   - [ ] Target scores: 80+ on mobile, 90+ on desktop
   - [ ] If score <80, optimize images or reduce scripts

5. **Analytics Verification**:
   - [ ] Install Meta Pixel Helper (Chrome extension)
   - [ ] Visit landing page
   - [ ] Verify pixel fires (green checkmark)
   - [ ] Check GA4 real-time report (should show active user)
   - [ ] Check Hotjar recordings (should show session)

**Cross-Browser Testing Checklist**:
- [ ] Chrome: Layout OK, CTA works, form works
- [ ] Safari: Layout OK, CTA works, form works
- [ ] Firefox: Layout OK, CTA works, form works
- [ ] Edge: Layout OK, CTA works, form works
- [ ] Mobile (iOS): Layout OK, form responsive
- [ ] Mobile (Android): Layout OK, form responsive
- [ ] PageSpeed score: 80+ mobile, 90+ desktop
- [ ] All tracking codes firing

**Time Estimate**: 1 hour
**Owner**: Growth Marketing
**Deliverable**: Cross-browser tested landing page

---

### Day 3 Completion Checklist

**Deliverables**:
- [ ] GA4 tracking integrated and verified
- [ ] Meta Pixel integrated and verified
- [ ] Hotjar integrated and verified
- [ ] Waitlist form embedded and tested
- [ ] Cross-browser testing complete (Chrome, Safari, Firefox, Edge)
- [ ] Mobile responsive verified (iOS, Android)
- [ ] Performance tested (PageSpeed 80+ mobile, 90+ desktop)

**Verification**:
- [ ] All analytics firing (check with extensions)
- [ ] Form submission working (test entry)
- [ ] No bugs on any browser
- [ ] Mobile view looks good

**Time Invested**: 4 hours
**Next**: Day 4 - Final QA and launch 🚀

---

## Day 4: QA and Launch (Thursday)

### Step 4.1: Final QA Checklist (2 hours)

**Objective**: Complete final quality assurance check

**Action Items**:

1. **Content QA**:
   - [ ] Proofread all copy (check for typos, grammar)
   - [ ] Verify all links work (privacy policy, social media)
   - [ ] Check phone numbers (if any)
   - [ ] Verify email addresses (if any)
   - [ ] Ensure all text is in Portuguese (Brazilian)

2. **Design QA**:
   - [ ] Check color contrast (use https://webaim.org/resources/contrastchecker/)
   - [ ] Verify font sizes are readable (16px min body text)
   - [ ] Check spacing consistency (use 8px grid)
   - [ ] Ensure no layout breaks (elements overlapping, misaligned)
   - [ ] Verify images are high quality (not pixelated)

3. **Functionality QA**:
   - [ ] Test all buttons (CTA, links, social icons)
   - [ ] Test form submission (submit test entry)
   - [ ] Test form validation (try submitting without required fields)
   - [ ] Test mobile menu (if navigation exists)
   - [ ] Test scroll behavior (smooth scrolling to sections)

4. **Analytics QA**:
   - [ ] Use Meta Pixel Helper: Verify pixel fires on page load
   - [ ] Use GA4 Real-Time: Verify active users show up
   - [ ] Use Hotjar Recordings: Verify sessions are captured
   - [ ] Test custom events: Submit form → verify event fires

5. **Performance QA**:
   - [ ] Run PageSpeed Insights: Target 80+ mobile, 90+ desktop
   - [ ] Check image sizes: All <200KB
   - [ ] Check load time: Target <3 seconds on 3G
   - [ ] Minify CSS/JS (if platform doesn't auto-minify)

6. **Security QA**:
   - [ ] Verify SSL certificate is active (https://, not http://)
   - [ ] Check for mixed content (all resources use https://)
   - [ ] Verify privacy policy link exists (even if placeholder)
   - [ ] Ensure form data is collected securely (Typeform is GDPR-compliant)

**Final QA Checklist**:
- [ ] No typos or grammar errors
- [ ] All links work
- [ ] All buttons work
- [ ] Form works (submission + validation)
- [ ] Mobile responsive (iOS + Android)
- [ ] Cross-browser compatible (Chrome, Safari, Firefox, Edge)
- [ ] Analytics firing (GA4, Meta Pixel, Hotjar)
- [ ] Performance good (PageSpeed 80+)
- [ ] SSL active (https://)
- [ ] Privacy policy link exists

**Time Estimate**: 2 hours
**Owner**: Growth Marketing + CMO (final approval)

---

### Step 4.2: Launch 🚀 (30 minutes)

**Objective**: Publish landing page and make it live

**Action Items**:

1. **Pre-Launch Checks** (5 minutes):
   - [ ] Final QA complete (all items checked)
   - [ ] CMO approval received
   - [ ] DNS propagated (get.conectapay.com.br resolves)
   - [ ] Analytics codes verified
   - [ ] Form tested and working

2. **Publish Landing Page** (5 minutes):
   - [ ] Log in to platform (Webflow, Framer, etc.)
   - [ ] Click "Publish" or "Deploy"
   - [ ] Verify publish succeeded (green checkmark)
   - [ ] Test live URL: https://get.conectapay.com.br

3. **Verify Live Site** (10 minutes):
   - [ ] Visit https://get.conectapay.com.br (incognito mode)
   - [ ] Verify page loads correctly
   - [ ] Verify all images load
   - [ ] Verify form works (submit test entry)
   - [ ] Verify SSL certificate active (lock icon in browser)
   - [ ] Verify mobile view (use browser dev tools, mobile mode)

4. **Test Analytics on Live Site** (10 minutes):
   - [ ] Use Meta Pixel Helper on live site: Verify pixel fires
   - [ ] Check GA4 Real-Time: Verify your visit shows up
   - [ ] Check Hotjar Recordings: Verify session is captured
   - [ ] Submit form: Verify `waitlist_signup` event fires

**Launch Verification Checklist**:
- [ ] Landing page live at https://get.conectapay.com.br
- [ ] Page loads correctly (incognito mode)
- [ ] All images load
- [ ] Form works (test entry submitted)
- [ ] SSL active (https://, lock icon)
- [ ] Mobile view works
- [ ] GA4 tracking firing
- [ ] Meta Pixel firing
- [ ] Hotjar recording

**Time Estimate**: 30 minutes
**Owner**: Growth Marketing
**Deliverable**: LIVE LANDING PAGE 🚀

---

### Step 4.3: Post-Launch Verification (1.5 hours)

**Objective**: Verify everything is working after launch

**Action Items**:

1. **Final Analytics Check** (30 minutes):
   - [ ] GA4 Real-Time: Should show 1+ active users (you)
   - [ ] GA4 DebugView: Should show events firing
   - [ ] Meta Pixel Helper: Should show pixel firing
   - [ ] Hotjar Recordings: Should show 1+ session
   - [ ] Typeform Responses: Should show test entry

2. **Generate First 10 Test Signups** (30 minutes):
   - [ ] Share landing page with team/friends
   - [ ] Ask 5-10 people to submit waitlist form
   - [ ] Verify all submissions appear in Typeform
   - [ ] Check GA4: Should show 5-10 users
   - [ ] Check Meta Pixel: Should show 5-10 page views

3. **Create Shareable Assets** (30 minutes):
   - [ ] Create short link (bit.ly, tinyURL): https://bit.ly/conectapay-waitlist
   - [ ] Create QR code (use https://www.qrcode-generator.com/): Download PNG
   - [ ] Screenshot landing page (for social media)
   - [ ] Write launch tweet/post: "Acabamos de lançar! 🚀"

4. **Document Launch** (Optional, 10 minutes):
   - [ ] Screenshot analytics (GA4 real-time, Meta Pixel Helper)
   - [ ] Save screenshots to project folder
   - [ ] Note launch time and date
   - [ ] Celebrate! 🎉

**Post-Launch Verification Checklist**:
- [ ] Analytics verified (GA4, Meta Pixel, Hotjar)
- [ ] 10 test signups completed
- [ ] All test data captured correctly
- [ ] Shareable assets created (short link, QR code, screenshot)
- [ ] Launch documented

**Time Estimate**: 1.5 hours
**Owner**: Growth Marketing
**Deliverable**: Verified live landing page with initial traffic

---

## Day 4 Completion Checklist

**Deliverables**:
- [ ] Final QA complete (all items checked)
- [ ] Landing page published and live
- [ ] Live site verified (https://get.conectapay.com.br)
- [ ] Analytics verified on live site
- [ ] 10 test signups completed
- [ ] Shareable assets created
- [ ] Launch documented

**Verification**:
- [ ] Landing page accessible to public
- [ ] All tracking codes firing
- [ ] Form capturing data
- [ ] No critical bugs
- [ ] Mobile responsive

**Time Invested**: 4 hours
**Total Time Invested (Day 1-4)**: 20-24 hours
**Next**: Day 5 - Ad campaign setup (see 90-Day Execution Calendar, CON-185)

---

## Troubleshooting Guide

### Issue: DNS Not Propagating

**Symptoms**: get.conectapay.com.br doesn't resolve, shows "Server not found"

**Solutions**:
1. Wait 24-48 hours (DNS propagation takes time)
2. Check DNS records: Use https://www.whatsmydns.net/ to verify propagation
3. Clear browser cache and DNS cache:
   - Mac: `sudo dscacheutil -flushcache; sudo killall -HUP mDNSResponder`
   - Windows: `ipconfig /flushdns`
4. Verify DNS records are correct (CNAME, A record)

---

### Issue: Analytics Not Firing

**Symptoms**: GA4 shows 0 users, Meta Pixel Helper shows no pixel

**Solutions**:
1. Verify tracking codes are in `<head>` section (not `<body>`)
2. Check for typos in Measurement ID or Pixel ID
3. Use browser incognito mode (cache may block scripts)
4. Check browser extensions (ad blockers may block analytics)
5. Verify custom domain SSL is active (https:// required)

---

### Issue: Form Not Submitting

**Symptoms**: Submit button doesn't work, form doesn't submit

**Solutions**:
1. Verify Typeform embed code is correct
2. Check for JavaScript errors (use browser console: F12 → Console)
3. Verify form is not inside another form (nested forms don't work)
4. Try redirect method instead of embed (simpler)
5. Contact Typeform support if issue persists

---

### Issue: Low PageSpeed Score

**Symptoms**: PageSpeed score <80 on mobile or desktop

**Solutions**:
1. Optimize images: Compress to <200KB each (use https://tinypng.com/)
2. Reduce JavaScript: Remove unused scripts
3. Enable caching: Use platform's caching features
4. Use CDN: Most platforms have built-in CDN
5. Minify CSS/JS: Use platform's minification features

---

### Issue: Mobile Layout Broken

**Symptoms**: Landing page looks bad on mobile, elements overlapping

**Solutions**:
1. Test on real device (not just browser dev tools)
2. Reduce font sizes: H1 32px, body 14px on mobile
3. Stack elements vertically (flex-direction: column)
4. Reduce padding: 32px instead of 64px on mobile
5. Make CTA button full width (100%) on mobile

---

## Success Criteria

**Launch Successful IF**:
- [ ] Landing page live and accessible (https://get.conectapay.com.br)
- [ ] All analytics firing (GA4, Meta Pixel, Hotjar)
- [ ] Form capturing data (10+ test signups)
- [ ] No critical bugs (blocking functionality)
- [ ] Mobile responsive (iOS + Android)
- [ ] PageSpeed score 80+ mobile, 90+ desktop
- [ ] SSL active (https://)

**Launch Complete** 🎉

---

## Document Control

**Version**: 1.0
**Created**: 2026-04-26
**Owner**: CMO Agent (55827422-a849-41d3-9286-0b5b8b002079)
**Review Date**: 2026-05-26 (Monthly)

**Change Log**:
| Date | Version | Changes | Author |
|------|---------|---------|--------|
| 2026-04-26 | 1.0 | Initial launch checklist | CMO Agent |

---

*End of Document*
