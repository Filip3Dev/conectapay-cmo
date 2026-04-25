# Interview Tracking Database Schema

## Overview
Complete database schema for tracking all customer interviews across Google Sheets or Airtable.

---

## Option 1: Google Sheets (Recommended - Free)

### Sheet 1: Master Interview Tracker

#### Column Structure (A-Z)

| Column | Type | Description | Example |
|--------|------|-------------|---------|
| A | Text | Interview ID | INT-001 |
| B | Date | Interview Date | 25/04/2026 |
| C | Text | Contact Name | João Silva |
| D | Text | Email | joao@clinica.com |
| E | Text | WhatsApp | (11) 99999-9999 |
| F | Text | Company | Clínica Saúde |
| G | Dropdown | Segment | Clínica |
| H | Dropdown | Company Size | 6-20 |
| I | Text | Location | São Paulo, SP |
| J | Dropdown | Status | Completed |
| K | Dropdown | ICP Fit Score | 85/100 |
| L | Number | WTP (R$/month) | 500 |
| M | Number | Estimated Impact (R$/month) | 5000 |
| M | Number | ROI Multiple | 10x |
| O | Dropdown | Beta Interest | Hot Lead |
| N | Checkbox | Recording Available | TRUE |
| O | URL | Recording Link | https://meet.google.com/... |
| P | URL | Transcription Link | https://docs.google.com/... |
| Q | Text | Key Problem | No-shows |
| R | Text | Key Insight | Values automation |
| S | Text | Main Objection | Price concern |
| T | Date | Follow-up Date | 02/05/2026 |
| U | Text | Follow-up Action | Send beta invite |
| V | Text | Interviewer | CMO Agent |
| W | Number | Duration (minutes) | 22 |
| X | Text | Tags | high-value, quick-win |
| Y | Date | Date Added | 25/04/2026 |
| Z | Text | Notes | Excellent fit, ready for beta |

---

### Sheet 2: Outreach Pipeline

#### For Tracking Before Interview

| Column | Type | Description | Example |
|--------|------|-------------|---------|
| A | Text | Contact ID | CT-001 |
| B | Text | Contact Name | Maria Santos |
| C | Text | Company | Imobiliária X |
| D | Dropdown | Segment | Imobiliária |
| E | Text | Source | Instagram |
| F | Date | Outreach Date | 25/04/2026 |
| G | Dropdown | Status | Sent |
| H | Date | Response Date | 26/04/2026 |
| I | Dropdown | Response | Positive |
| J | Date | Booking Date | 27/04/2026 |
| K | Text | Interview ID | INT-003 |
| L | Text | Notes | Replied within 24h |

---

### Sheet 3: Weekly Summary

#### Aggregated Metrics

| Column | Type | Description | Example |
|--------|------|-------------|---------|
| A | Date | Week Start | 20/04/2026 |
| B | Number | Interviews Completed | 8 |
| C | Number | Avg ICP Score | 72/100 |
| D | Number | Avg WTP | 450 |
| E | Number | Hot Leads | 3 |
| F | Number | Warm Leads | 4 |
| G | Number | Cold Leads | 1 |
| H | Text | Key Insights | Clinics value speed |
| I | Text | Top Problems | No-shows, follow-up |
| J | Text | Next Week Focus | More real estate outreach |

---

### Sheet 4: Quotes Collection

#### For Copywriting and Testimonials

| Column | Type | Description | Example |
|--------|------|-------------|---------|
| A | Date | Interview Date | 25/04/2026 |
| B | Text | Interview ID | INT-001 |
| C | Text | Contact Name | João Silva |
| D | Text | Segment | Clínica |
| E | Text | Quote | "Perco 20% das consultas..." |
| F | Text | Context | About no-shows |
| G | Text | Use Case | Landing page copy |
| H | Checkbox | Used in Marketing | FALSE |

---

### Google Sheets Setup Instructions

#### Step 1: Create Spreadsheet
1. Go to [sheets.google.com](https://sheets.google.com)
2. Click "Blank spreadsheet"
3. Name: "ConectaPay - Customer Interviews"

#### Step 2: Create Sheets
- Sheet 1: "Master Tracker"
- Sheet 2: "Outreach Pipeline"
- Sheet 3: "Weekly Summary"
- Sheet 4: "Quotes Collection"

#### Step 3: Set Up Dropdowns
Use Data > Data Validation for:
- Status: Not Contacted, Sent, Responded, Booked, Completed, No-show
- Segment: Clínica, Imobiliária, Outro
- Company Size: 1-5, 6-20, 21-50, 51+
- Beta Interest: Hot Lead, Warm Lead, Cold Lead, Not a fit

#### Step 4: Create Dashboard
Use Insert > Chart to visualize:
- Interviews per week
- Avg ICP score trend
- WTP distribution by segment
- Conversion funnel (Outreach → Interview → Beta)

#### Step 5: Set Up Form (Optional)
Use Forms > Create Form to quickly add interviews:
- Link form to "Master Tracker" sheet
- Create form with key fields
- Share form link with interviewers

---

## Option 2: Airtable (Advanced - $10/month)

### Base Structure

#### Table 1: Interviews
| Field | Type | Options |
|-------|------|---------|
| Interview ID | Single Line Text | Auto-number INT-001 |
| Contact Name | Single Line Text | Required |
| Email | Email | Required |
| WhatsApp | Phone | Format: Brazil |
| Company | Single Line Text | |
| Segment | Single Select | Clínica, Imobiliária, Outro |
| Company Size | Single Select | 1-5, 6-20, 21-50, 51+ |
| Location | Single Line Text | |
| Status | Single Select | Booked, Completed, No-show |
| ICP Fit Score | Rating | 0-100 |
| WTP | Currency | R$ |
| Estimated Impact | Currency | R$ |
| ROI Multiple | Formula | `{Estimated Impact}/{WTP}` |
| Beta Interest | Single Select | Hot Lead, Warm Lead, Cold Lead, Not a fit |
| Recording Link | URL | |
| Transcription | Attachment | PDF/DOC |
| Key Problem | Single Line Text | |
| Key Insight | Long Text | |
| Follow-up Date | Date | |
| Follow-up Action | Single Line Text | |
| Interview Date | Date | |
| Duration | Number | Minutes |
| Tags | Multiple Select | high-value, quick-win, reference-candidate |

#### Table 2: Contacts
| Field | Type | Options |
|-------|------|---------|
| Contact ID | Single Line Text | Auto-number CT-001 |
| Name | Single Line Text | |
| Email | Email | |
| WhatsApp | Phone | |
| Company | Single Line Text | |
| Segment | Single Select | |
| Source | Single Select | Instagram, LinkedIn, Referral |
| Status | Single Select | New, Contacted, Replied, Booked |
| Linked Interviews | Link to Interviews | Multiple records |

#### Table 3: Weekly Reports
| Field | Type | Options |
|-------|------|---------|
| Week Start | Date | |
| Interviews Completed | Count | Rollup from Interviews |
| Avg ICP Score | Average | Rollup from Interviews |
| Avg WTP | Average | Rollup from Interviews |
| Hot Leads | Count | Rollup from Interviews |
| Key Insights | Long Text | |
| Top Problems | Long Text | |

---

## Airtable Setup Instructions

### Step 1: Create Base
1. Go to [airtable.com](https://airtable.com)
2. Click "Add a base"
3. Start from scratch
4. Name: "ConectaPay - Customer Interviews"

### Step 2: Create Tables
- Create 3 tables: Interviews, Contacts, Weekly Reports
- Set up fields as specified above
- Create linked records between Contacts and Interviews

### Step 3: Create Views

#### Views for Interviews Table
- **All Interviews**: Grid view
- **This Week**: Filter by Interview Date (next 7 days)
- **Completed**: Filter by Status = Completed
- **Hot Leads**: Filter by Beta Interest = Hot Lead
- **By Segment**: Group by Segment

#### Views for Contacts Table
- **All Contacts**: Grid view
- **New Contacts**: Filter by Status = New
- **Replied**: Filter by Status = Replied
- **Booked**: Filter by Status = Booked

### Step 4: Create Forms
- **Interview Entry Form**: For quick data entry after interviews
- Share form with interviewers
- Set up notifications on form submission

### Step 5: Automations (Optional)
- When status changes to "Completed", send Slack notification
- when "Beta Interest" = "Hot Lead", send email to sales team
- When interview date is today, send reminder notification

---

## Data Backup Strategy

### Google Sheets
- **Auto-save**: Enabled by default
- **Version history**: 30 days (free) or unlimited (Workspace)
- **Export**: Weekly download as Excel
- **Share**: Team access with edit permissions

### Airtable
- **Auto-save**: Enabled by default
- **Snapshot**: Weekly base snapshots
- **Export**: Monthly CSV export
- **Sync**: Use Airtable Sync for backup

---

## Quick Start Checklist

### For Google Sheets
- [ ] Create spreadsheet
- [ ] Set up column headers
- [ ] Configure dropdown menus
- [ ] Create charts for dashboard
- [ ] Share with team
- [ ] Set up notifications
- [ ] Test with sample data

### For Airtable
- [ ] Create base
- [ ] Set up tables and fields
- [ ] Create linked records
- [ ] Build views and filters
- [ ] Create forms
- [ ] Set up automations
- [ ] Invite team members

---

## Integration with Other Tools

### Calendly Integration
- **Google Sheets**: Use Zapier or native Calendly integration
- **Airtable**: Native Calendly integration available

### Google Meet Recordings
- Auto-save to Google Drive
- Link to recording in database
- Use transcription API (optional)

### Slack Notifications
- New interview booked → #interviews channel
- Interview completed → #results channel
- Hot lead identified → #sales channel

---

## Recommended: Google Sheets for Initial Phase

**Why Google Sheets?**
- ✅ Free
- ✅ Familiar interface
- ✅ Real-time collaboration
- ✅ Integrates with Google Meet
- ✅ Sufficient for 15-20 interviews

**Upgrade to Airtable when:**
- 50+ interviews
- Multiple team members
- Complex workflows needed
- Advanced reporting required

---

**Schema Version**: 1.0
**Created**: 2025-04-25
**Purpose**: CON-57 - Customer Interview Infrastructure
**Status**: Ready for implementation
