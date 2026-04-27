# Lead Tracking Dashboard Setup Guide

**Purpose**: Track all marketing leads, sources, and conversion metrics in one place
**Tool**: Google Sheets (free, collaborative, importable to HubSpot later)

---

## Sheet Structure (4 Tabs)

### Tab 1: Master Lead Database
All leads in one place with full details

### Tab 2: Daily Metrics Summary
Key KPIs updated automatically

### Tab 3: Weekly Trends
Week-over-week comparisons

### Tab 4: Source & Segment Breakdown
Funnel analysis by source and ICP segment

---

## Tab 1: Master Lead Database

**Purpose**: Single source of truth for all leads

### Column Structure (A-Z)

| Column | Header | Type | Description |
|--------|--------|------|-------------|
| A | Lead ID | Text | Unique identifier (e.g., L-001, L-002) |
| B | Date Added | Date | When lead was captured |
| C | Source | Dropdown | How they found us |
| D | Industry | Dropdown | Which segment |
| E | Company Size | Number | Employee count |
| F | Contact Name | Text | Person's name |
| G | Contact Role | Dropdown | Decision maker/Influencer/Other |
| H | WhatsApp | Text | Phone number |
| H | Email | Text | Email address |
| I | ICP Score | Number | 0-100 qualification score |
| J | Qualification | Dropdown | Qualified/Nurture/Disqualified |
| K | Stage | Dropdown | Lead/Interviewed/Demo/Customer/Churned |
| L | Interview Date | Date | Calendly booking (if scheduled) |
| M | Interview Status | Dropdown | Scheduled/Completed/No-show |
| N | Notes | Text | Qualitative insights |
| O | Last Contact | Date | Most recent touchpoint |
| P | Next Action | Dropdown | DM sent/Call booked/Email sent/Follow-up |
| Q | Assigned To | Text | Who owns this lead |
| R | Created Waitlist | Date | If they signed up for waitlist |
| S | Smoke Test Signup | Date | If they signed up during smoke test |
| T | Converted to Customer | Date | First payment date |
| U | LTV | Currency | Customer lifetime value (if customer) |

### Example Rows (First 5 Leads)

| Lead ID | Date Added | Source | Industry | Company Size | ICP Score | Qualification | Stage |
|---------|------------|--------|----------|--------------|-----------|---------------|-------|
| L-001 | 2026-04-27 | Instagram DM | Clínica | 25 | 85 | Qualified | Interviewed |
| L-002 | 2026-04-27 | LinkedIn Outreach | Imobiliária | 8 | 72 | Qualified | Demo |
| L-003 | 2026-04-28 | Waitlist | Academia | 40 | 68 | Nurture | Lead |
| L-004 | 2026-04-28 | Referral | Clínica | 15 | 90 | Qualified | Customer |
| L-005 | 2026-04-29 | Meta Ads | Outro | 3 | 25 | Disqualified | Lead |

---

## Tab 2: Daily Metrics Summary

**Purpose**: Quick daily view of key performance indicators

### Layout

| Metric | Today | Yesterday | Week Ago | % Change |
|--------|-------|-----------|----------|----------|
| **Total Leads** | =COUNTA(Master!A:A) | =B2-<today's new> | =INDEX(...,7) | =(B2-C2)/C2 |
| **New Leads (Today)** | =COUNTIF(Master!B:B,TODAY()) | =COUNTIF(Master!B:B,TODAY()-1) | =COUNTIF(Master!B:B,TODAY()-7) | =(B2-C2)/C2 |
| **Qualified Leads** | =COUNTIF(Master!J:J,"Qualified") | =B3-<new qualified> | =INDEX(...,7) | =(B3-C3)/C3 |
| **Qualification Rate** | =B3/B2 | =C3/C2 | =D3/D2 | =B4-C4 |
| **Interviews Scheduled** | =COUNTIF(Master!L:L,"<>") | =B5-<new> | =INDEX(...,7) | =(B5-C5)/C5 |
| **Interviews Completed** | =COUNTIF(Master!M:M,"Completed") | =B6-<new> | =INDEX(...,7) | =(B6-C6)/C6 |
| **Show Rate** | =B6/B5 | =C6/C5 | =D6/D5 | =B7-C7 |
| **Waitlist Signups** | =COUNTIF(Master!R:R,"<>") | =B8-<new> | =INDEX(...,7) | =(B8-C8)/C8 |
| **Smoke Test Signups** | =COUNTIF(Master!S:S,"<>") | =B9-<new> | =INDEX(...,7) | =(B9-C9)/C9 |
| **Customers** | =COUNTIF(Master!T:T,"<>") | =B10-<new> | =INDEX(...,7) | =(B10-C10)/C10 |

### Key Metrics to Track Daily

1. **Lead Velocity**: New leads per day
2. **Qualification Rate**: % of leads that score 70+
3. **Interview Conversion**: % of leads that book interviews
4. **Show Rate**: % of interviews that actually happen
5. **Waitlist Growth**: Total waitlist signups
6. **Conversion to Customer**: % of leads that become customers

---

## Tab 3: Weekly Trends

**Purpose**: Track week-over-week progress and spot trends

### Layout

| Week Starting | Total Leads | New Leads | Qualified | Interviews | Show Rate | Waitlist | Customers |
|---------------|-------------|-----------|-----------|------------|-----------|----------|-----------|
| 2026-04-20 | 0 | 0 | 0 | 0 | - | 0 | 0 |
| 2026-04-27 | 50 | 50 | 35 | 8 | 62.5% | 12 | 0 |
| 2026-05-04 | 85 | 35 | 22 | 12 | 75% | 28 | 2 |
| 2026-05-11 | 120 | 35 | 28 | 15 | 80% | 45 | 5 |

### Formulas (Auto-Calculate Each Week)

- **Total Leads (cumulative)**: `=COUNTIF(Master!B:B,"<="&[Week Ending])`
- **New Leads (weekly)**: `=COUNTIFS(Master!B:B,">="&[Week Start],Master!B:B,"<="&[Week Ending])`
- **Qualified**: `=COUNTIFS(Master!J:J,"Qualified",Master!B:B,">="&[Week Start],Master!B:B,"<="&[Week Ending])`
- **Interviews**: `=COUNTIFS(Master!L:L,"<>",Master!B:B,">="&[Week Start],Master!B:B,"<="&[Week Ending])`
- **Show Rate**: `=[Interviews Completed]/[Interviews Scheduled]`
- **Waitlist**: `=COUNTIFS(Master!R:R,"<>",Master!B:B,">="&[Week Start],Master!B:B,"<="&[Week Ending])`
- **Customers**: `=COUNTIFS(Master!T:T,"<>",Master!B:B,">="&[Week Start],Master!B:B,"<="&[Week Ending])`

---

## Tab 4: Source & Segment Breakdown

**Purpose**: Understand which channels and segments perform best

### Section A: Funnel by Source

| Source | Leads | % of Total | Qualified | Qual Rate | Interviews | Int Rate | Customers | Conv Rate |
|--------|-------|------------|-----------|-----------|------------|----------|-----------|-----------|
| Instagram DM | 25 | 50% | 18 | 72% | 5 | 28% | 0 | 0% |
| LinkedIn Outreach | 15 | 30% | 12 | 80% | 3 | 25% | 1 | 33% |
| Waitlist | 5 | 10% | 3 | 60% | 0 | 0% | 0 | 0% |
| Meta Ads | 3 | 6% | 1 | 33% | 0 | 0% | 0 | 0% |
| Referral | 2 | 4% | 2 | 100% | 0 | 0% | 0 | 0% |
| **TOTAL** | **50** | **100%** | **36** | **72%** | **8** | **22%** | **1** | **12.5%** |

### Section B: Funnel by Segment

| Segment | Leads | % of Total | Qualified | Qual Rate | Interviews | Int Rate | Customers | Conv Rate |
|---------|-------|------------|-----------|-----------|------------|----------|-----------|-----------|
| Clínicas | 20 | 40% | 16 | 80% | 4 | 25% | 1 | 25% |
| Imobiliárias | 18 | 36% | 14 | 78% | 3 | 21% | 0 | 0% |
| Academias | 7 | 14% | 4 | 57% | 1 | 25% | 0 | 0% |
| Óticas | 3 | 6% | 2 | 67% | 0 | 0% | 0 | 0% |
| Outro | 2 | 4% | 0 | 0% | 0 | 0% | 0 | 0% |
| **TOTAL** | **50** | **100%** | **36** | **72%** | **8** | **22%** | **1** | **12.5%** |

### Pivot Table Formulas

- **Leads by Source**: `=COUNTIF(Master!C:C,"[Source Name]")`
- **Leads by Segment**: `=COUNTIF(Master!D:D,"[Segment Name]")`
- **Qualification Rate**: `=[Qualified]/[Leads]`
- **Interview Rate**: `=[Interviews]/[Qualified]`
- **Conversion Rate**: `=[Customers]/[Interviews]`

---

## Setup Instructions

### Step 1: Create Google Sheet
1. Go to `sheets.google.com`
2. Create new sheet: "ConectaPay Lead Dashboard"
3. Create 4 tabs: "Master", "Daily Metrics", "Weekly Trends", "Source Analysis"

### Step 2: Set Up Master Tab
1. Add column headers A-Z (see Tab 1 structure)
2. Format columns:
   - Date columns: Format → Number → Date
   - Number columns: Format → Number
   - Dropdown columns: Data → Data Validation → Dropdown
3. Freeze first row: View → Freeze → 1 row
4. Add filter: Data → Create a filter

### Step 3: Add Formulas to Daily Metrics
1. Copy formulas from Tab 2 structure
2. Update cell references to match your sheet
3. Test with sample data

### Step 4: Set Up Weekly Trends
1. Add week start dates in Column A
2. Copy formulas for each metric
3. Create chart: Insert → Chart → Line chart

### Step 5: Create Source & Segment Analysis
1. Use pivot tables or COUNTIF formulas
2. Add conditional formatting:
   - Green: >70% (good performance)
   - Yellow: 40-70% (average)
   - Red: <40% (needs improvement)

### Step 6: Add Automations (Optional)
1. **Import from HubSpot**: Extensions → Add-ons → HubSpot → Import
2. **Import from Calendly**: Use Zapier or Make.com
3. **Import from waitlist form**: Google Forms → Link to sheet

### Step 7: Share with Team
1. Click Share → Add people
2. Add CMO, CS hire (when hired), Founder
3. Permission: Editor

---

## Daily Review Process (5 minutes)

### Every Morning (9:00 AM)
1. Open "Daily Metrics" tab
2. Check "New Leads (Today)" - should be >0
3. Check "Qualification Rate" - should be >60%
4. Check "Interview Show Rate" - should be >50%
5. Identify any drops from yesterday
6. Investigate issues (e.g., low show rate = reminder needed)

### Weekly Review (Every Monday 10:00 AM)
1. Check "Weekly Trends" tab
2. Compare this week vs last week
3. Identify best-performing sources
4. Double down on what's working
5. Pause or fix underperforming channels

---

## Integration with HubSpot

### When Ready to Migrate
1. Export Master tab to CSV
2. Import to HubSpot: Contacts → Import → CSV
3. Map columns to HubSpot properties:
   - Lead ID → External ID
   - Source → Lead Source
   - Industry → Industry
   - ICP Score → ICP Score
   - Qualification → Lead Status
   - Stage → Lifecycle Stage
4. Keep Google Sheet as backup/quick view

---

## Target Metrics (Week 4)

| Metric | Week 1 | Week 2 | Week 3 | Week 4 | Target |
|--------|--------|--------|--------|--------|--------|
| Total Leads | 50 | 100 | 150 | 200 | 200 |
| Qualification Rate | 60% | 65% | 70% | 75% | 75% |
| Interviews Scheduled | 10 | 20 | 30 | 40 | 40 |
| Show Rate | 50% | 60% | 70% | 75% | 75% |
| Waitlist Signups | 10 | 25 | 40 | 60 | 60 |

---

**Template Version**: 1.0
**Last Updated**: April 27, 2026
**Maintained By**: CMO Agent
**Review Frequency**: Daily
