# ICP Lead Qualification Scorecard

**Purpose**: Qualify leads and determine if they fit ConectaPay's Ideal Customer Profile (ICP)
**Threshold**: 70+ points = Sales qualified | 50-69 points = Nurture | <50 points = Disqualify

---

## Scoring Dimensions (0-100 Total)

### 1. Industry Fit (0-30 points)

| Industry | Points | Notes |
|----------|--------|-------|
| **Clínica Médica** (Medical Clinic) | 30 | Primary ICP - highest no-show problem |
| **Imobiliária** (Real Estate) | 30 | Primary ICP - highest lead conversion problem |
| **Academia** (Fitness/Gym) | 20 | Secondary ICP - class booking reminders |
| **Ótica** (Optical Store) | 15 | Secondary ICP - appointment reminders |
| Outro (Other) | 0 | Not in target segments |

**Scoring**: Select ONE industry based on lead's primary business type

---

### 2. Company Size (0-20 points)

| Employee Count | Points | Notes |
|----------------|--------|-------|
| 10-50 employees | 20 | Ideal size - has volume but not too complex |
| 5-9 employees | 15 | Small but viable - can grow with us |
| 51-100 employees | 10 | Larger - may require enterprise approach |
| 2-4 employees | 5 | Very small - limited budget |
| 1 or 100+ employees | 0 | Too small or too large |

**Scoring**: Select based on current employee count

---

### 3. Pain Severity (0-25 points)

| Problem Frequency | Points | Notes |
|-------------------|--------|-------|
| **Daily abandoned sales** | 25 | Critical pain - urgent need |
| **Weekly abandoned sales** | 20 | High pain - clear ROI case |
| **Monthly abandoned sales** | 15 | Moderate pain - solution valuable |
| **Rarely lose sales** | 5 | Low pain - harder to close |
| **Don't track/Not sure** | 10 | Need discovery to uncover pain |

**Follow-up Questions**:
- "How many sales do you lose per week to no-response?"
- "What's the typical time between first contact and purchase?"
- "Do you currently follow up automatically?"

**Scoring**: Select based on stated frequency of lost sales

---

### 4. WhatsApp Usage (0-15 points)

| Usage Level | Points | Notes |
|-------------|--------|-------|
| **Primary customer channel** | 15 | Perfect fit - WhatsApp is main communication |
| **Secondary channel** | 8 | Good fit - uses WhatsApp regularly |
| **Rarely use** | 0 | Wrong channel - won't get value |

**Follow-up Questions**:
- "How do you currently communicate with customers?"
- "What percentage of your customers prefer WhatsApp?"
- "Do you have WhatsApp Business?"

**Scoring**: Select based on importance of WhatsApp in their business

---

### 5. Budget Authority (0-10 points)

| Role | Points | Notes |
|------|--------|-------|
| **Owner/CEO/Decision Maker** | 10 | Can approve immediately |
| **Manager/Influencer** | 5 | Can recommend but not decide |
| **Employee/No Authority** | 0 | Wrong contact - need decision maker |

**Follow-up Questions**:
- "Who would approve a R$ 200-500/month investment?"
- "What's your budget for tools that increase sales?"
- "Are you the person who makes purchasing decisions?"

**Scoring**: Select based on contact's authority level

---

## Total Score Calculation

```
Industry Fit (30) +
Company Size (20) +
Pain Severity (25) +
WhatsApp Usage (15) +
Budget Authority (10)
=
TOTAL SCORE (0-100)
```

---

## Qualification Decision Matrix

| Score Range | Action | Next Steps |
|-------------|--------|------------|
| **80-100** | **HIGH PRIORITY** | Immediate outreach, fast-track to demo |
| **70-79** | **QUALIFIED** | Add to sales sequence, schedule call |
| **50-69** | **NURTURE** | Add to email nurture, monitor engagement |
| **0-49** | **DISQUALIFY** | Politely decline, don't invest time |

---

## Example Scores

### Example 1: Perfect Fit (90 points)
- Industry: Clínica Médica (30)
- Company Size: 25 employees (20)
- Pain: Daily abandoned sales (25)
- WhatsApp: Primary channel (15)
- Authority: Owner (10)
- **Total: 90/100** → IMMEDIATE OUTREACH

### Example 2: Good Fit (75 points)
- Industry: Imobiliária (30)
- Company Size: 8 employees (15)
- Pain: Weekly abandoned sales (20)
- WhatsApp: Secondary channel (8)
- Authority: Manager (5)
- **Total: 78/100** → SALES QUALIFIED

### Example 3: Nurture (55 points)
- Industry: Academia (20)
- Company Size: 40 employees (20)
- Pain: Monthly abandoned sales (15)
- WhatsApp: Primary channel (15)
- Authority: Employee (0)
- **Total: 70/100** → NURTURE (wrong contact)

### Example 4: Disqualify (25 points)
- Industry: Restaurant (0)
- Company Size: 3 employees (5)
- Pain: Rarely lose sales (5)
- WhatsApp: Rarely use (0)
- Authority: Owner (10)
- **Total: 20/100** → DISQUALIFY

---

## Quick Reference Card

### Red Flags (Auto-Disqualify)
- ❌ Industry outside 4 target segments
- ❌ <5 employees or >100 employees
- ❌ No WhatsApp usage
- ❌ No decision-making authority
- ❌ Can't articulate pain/lost sales

### Green Flags (Fast-Track)
- ✅ Clínica or Imobiliária
- ✅ 10-50 employees
- ✅ Daily/weekly abandoned sales
- ✅ WhatsApp is primary channel
- ✅ Owner/CEO decision maker

---

## Usage Instructions

### During Outreach (ICP Discovery)
1. **Before DM**: Research industry and company size (LinkedIn, website)
2. **During DM**: Ask about WhatsApp usage and pain
3. **After Interview**: Calculate full score, assign to track

### For Smoke Test Signups
1. **On signup form**: Collect industry, company size, WhatsApp usage
2. **In welcome email**: Ask about pain severity
3. **Before demo call**: Verify budget authority
4. **Score in CRM**: Tag based on total points

### In HubSpot CRM
Create these property fields:
- `icp_score` (number field, 0-100)
- `icp_industry_fit` (dropdown: Clínica/Imobiliária/Academia/Ótica/Outro)
- `icp_company_size` (number field)
- `icp_pain_severity` (dropdown: Daily/Weekly/Monthly/Rare)
- `icp_whatsapp_usage` (dropdown: Primary/Secondary/Rare)
- `icp_authority` (dropdown: Decision Maker/Influencer/None)
- `qualification_status` (dropdown: Qualified/Nurture/Disqualified)

Set up automation:
- Score ≥70 → Add to "Sales Qualified" list
- Score 50-69 → Add to "Nurture" list
- Score <50 → Add to "Disqualified" list

---

**Template Version**: 1.0
**Last Updated**: April 27, 2026
**Next Review**: After 50 leads scored
