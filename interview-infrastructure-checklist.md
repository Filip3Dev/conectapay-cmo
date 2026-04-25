# Customer Interview Infrastructure - Setup Checklist

## Overview
Complete step-by-step checklist to set up all interview infrastructure components. Use this to track progress.

---

## Phase 1: Scheduling Setup (Est. 30 min)

### Step 1.1: Create Calendly Account
- [ ] Go to calendly.com and sign up (Google account recommended)
- [ ] Complete basic profile
- [ ] Choose Free Tier (sufficient for initial phase)

**Account Created**: ☐ Yes ☐ No
**Username**: _______________

### Step 1.2: Configure Event Type
- [ ] Create new event type
- [ ] Name: "Entrevista de Descoberta ICP - ConectaPay (20 min)"
- [ ] Duration: 20 minutes
- [ ] Location: Google Meet (enable auto-record)

**Event Type Created**: ☐ Yes ☐ No
**Booking Link**: _______________

### Step 1.3: Set Availability
- [ ] Business hours: Mon-Fri, 9:00-18:00 BRT
- [ ] Time zone: America/Sao_Paulo
- [ ] Buffer: 15 minutes between meetings
- [ ] Min notice: 4 hours
- [ ] Future limit: 4 weeks

**Availability Configured**: ☐ Yes ☐ No

### Step 1.4: Add Questions
- [ ] Name (required)
- [ ] Email (required)
- [ ] WhatsApp (required)
- [ ] Company (optional)
- [ ] Segment (optional)
- [ ] Main challenge (optional)

**Questions Added**: ☐ Yes ☐ No

### Step 1.5: Customize Emails
- [ ] Configure confirmation email template
- [ ] Enable 24h reminder email
- [ ] Add cancellation/reschedule policy

**Emails Configured**: ☐ Yes ☐ No

### Step 1.6: Test Booking Flow
- [ ] Book test appointment with yourself
- [ ] Verify confirmation email arrives
- [ ] Test Google Meet link
- [ ] Verify calendar sync works

**Test Completed**: ☐ Yes ☐ No

---

## Phase 2: Recording Setup (Est. 20 min)

### Step 2.1: Google Meet Setup (Recommended)
- [ ] Go to meet.google.com
- [ ] Enable "Record to cloud" in settings
- [ ] Create "ConectaPay Interviews" folder in Google Drive
- [ ] Set auto-save location to that folder

**Recording Enabled**: ☐ Yes ☐ No
**Folder Created**: ☐ Yes ☐ No

### Step 2.2: Alternative: Zoom Setup
- [ ] Enable cloud recording in Zoom settings
- [ ] Set auto-record for all meetings
- [ ] Create dedicated folder for recordings

**Zoom Configured**: ☐ Yes ☐ N/A

### Step 2.3: Test Recording
- [ ] Start 5-min test meeting
- [ ] Verify recording works
- [ ] Check file saves to correct folder
- [ ] Test on mobile device

**Recording Tested**: ☐ Yes ☐ No

---

## Phase 3: Database Setup (Est. 25 min)

### Step 3.1: Create Google Sheets Database
- [ ] Go to sheets.google.com
- [ ] Create new spreadsheet: "ConectaPay - Customer Interviews"
- [ ] Create 4 sheets:
  - [ ] Sheet 1: "Master Tracker"
  - [ ] Sheet 2: "Outreach Pipeline"
  - [ ] Sheet 3: "Weekly Summary"
  - [ ] Sheet 4: "Quotes Collection"

**Spreadsheet Created**: ☐ Yes ☐ No
**URL**: _______________

### Step 3.2: Set Up Master Tracker Columns
- [ ] Copy column headers from interview-database-schema.md
- [ ] Set up data validation for dropdowns
- [ ] Format currency columns (R$)
- [ ] Format date columns (DD/MM/YYYY)

**Master Tracker Ready**: ☐ Yes ☐ No

### Step 3.3: Create Dropdown Menus
- [ ] Status: Not Contacted, Sent, Responded, Booked, Completed, No-show
- [ ] Segment: Clínica, Imobiliária, Outro
- [ ] Company Size: 1-5, 6-20, 21-50, 51+
- [ ] Beta Interest: Hot Lead, Warm Lead, Cold Lead, Not a fit

**Dropdowns Created**: ☐ Yes ☐ No

### Step 3.4: Create Dashboard (Optional)
- [ ] Create chart: Interviews per week
- [ ] Create chart: Avg ICP score trend
- [ ] Create chart: WTP distribution
- [ ] Create funnel: Outreach → Interview → Beta

**Dashboard Created**: ☐ Yes ☐ No

### Step 3.5: Share with Team
- [ ] Add team members with edit access
- [ ] Set up notification rules
- [ ] Test simultaneous editing

**Team Access**: ☐ Yes ☐ No

---

## Phase 4: Email Templates Setup (Est. 20 min)

### Step 4.1: Choose Email Method
- [ ] Calendly built-in emails (easiest)
- [ ] Manual drafts (for now)
- [ ] Mailchimp/ActiveCampaign (advanced)

**Method Chosen**: _______________

### Step 4.2: Set Up Confirmation Email
- [ ] Use template from email-communication-templates.md
- [ ] Configure in Calendly or save as draft
- [ ] Test with sample data

**Confirmation Email**: ☐ Ready ☐ Not needed

### Step 4.3: Set Up Reminder Email
- [ ] Enable in Calendly (automated)
- [ ] Customize content
- [ ] Test timing

**Reminder Email**: ☐ Ready ☐ Not needed

### Step 4.4: Prepare Manual Templates
- [ ] Thank you email (save as draft)
- [ ] Beta invitation (save as draft)
- [ ] Referral request (save as draft)
- [ ] Re-engagement (save as draft)
- [ ] No-show follow-up (save as draft)

**Manual Templates**: ☐ All saved ☐ Partial

---

## Phase 5: Interview Materials (Est. 15 min)

### Step 5.1: Print/Save Interview Guides
- [ ] icp-interview-guide-clinics.md
- [ ] icp-interview-guide-real-estate.md
- [ ] interview-note-template.md

**Guides Accessible**: ☐ Yes ☐ No

### Step 5.2: Prepare Analysis Framework
- [ ] Review interview-analysis-framework.md
- [ ] Print coding system reference
- [ ] Set up ROI calculator spreadsheet

**Analysis Framework**: ☐ Reviewed ☐ Not started

### Step 5.3: Tech Check Before First Interview
- [ ] Test microphone quality
- [ ] Test camera/video
- [ ] Test internet connection
- [ ] Have backup phone ready
- [ ] Open all necessary tabs:
  - [ ] Google Meet
  - [ ] Interview guide
  - [ ] Note template
  - [ ] Database for data entry

**Tech Check Complete**: ☐ Yes ☐ No

---

## Phase 6: Integration Testing (Est. 15 min)

### Step 6.1: End-to-End Test
- [ ] Simulate booking (use test contact)
- [ ] Receive confirmation email
- [ ] Join test meeting
- [ ] Test recording (3 min)
- [ ] End meeting and verify recording saves
- [ ] Enter data in database
- [ ] Send thank you email (to self)

**Full Test Passed**: ☐ Yes ☐ No

### Step 6.2: Fix Any Issues
- [ ] Document any problems found
- [ ] Fix or work around issues
- [ ] Re-test if needed

**Issues Resolved**: ☐ Yes ☐ N/A

---

## Phase 7: Launch Preparation (Est. 10 min)

### Step 7.1: Update Outreach Materials
- [ ] Add booking link to outreach messages CSV
- [ ] Update outreach-execution-guide if needed
- [ ] Verify all links work

**Outreach Updated**: ☐ Yes ☐ No

### Step 7.2: Prepare Week 1 Schedule
- [ ] Block interview slots in calendar
- [ ] Set target: 3-5 interviews first week
- [ ] Plan daily review time (30 min)

**Schedule Ready**: ☐ Yes ☐ No

### Step 7.3: Set Reminders
- [ ] Calendar reminder 15 min before each interview
- [ ] Weekly review reminder (Friday 5pm)
- [ ] Daily data entry reminder

**Reminders Set**: ☐ Yes ☐ No

---

## Quick Launch Checklist

### Minimum Viable Setup (1 hour)
- [ ] Calendly account created
- [ ] Booking link generated
- [ ] Google Meet recording enabled
- [ ] Google Sheets database created
- [ ] Interview guides accessible
- [ ] Thank you email saved as draft

**Ready for Interviews**: ☐ Yes ☐ No

### Complete Setup (2 hours)
- All above PLUS:
- [ ] Email templates configured
- [ ] Dashboard created
- [ ] Analysis framework reviewed
- [ ] End-to-end test completed
- [ ] Outreach materials updated

**Fully Prepared**: ☐ Yes ☐ No

---

## Launch Day Checklist

### Before First Interview
- [ ] Calendly link shared in outreach
- [ ] First booking received
- [ ] Confirmation email verified
- [ ] Interview guide open
- [ ] Note template open
- [ ] Database open for data entry
- [ ] Water/coffee ready 😊

### During Interview
- [ ] Recording started
- [ ] Consent obtained
- [ ] Notes taken (or transcription running)
- [ ] Time tracked (max 20 min)

### Immediately After
- [ ] Recording saved
- [ ] Thank you email sent
- [ ] Data entered in database
- [ ] Key insights documented
- [ ] Follow-up scheduled (if needed)

---

## Weekly Maintenance

### Every Friday
- [ ] Review all interviews from week
- [ ] Update weekly summary sheet
- [ ] Identify top 3 insights
- [ ] Calculate avg ICP score
- [ ] Count hot/warm/cold leads
- [ ] Plan next week's outreach

### End of Interview Cycle (After 15-20)
- [ ] Complete final analysis
- [ ] Generate insights report
- [ ] Make GO/NO-GO decision
- [ ] Share insights with all participants
- [ ] Plan beta program based on findings

---

## Troubleshooting Guide

| Problem | Solution |
|---------|----------|
| No bookings coming in | Test link yourself, verify it's being shared correctly |
| High no-show rate | Add SMS reminder, reduce lead time to 15 min |
| Recording failed | Take detailed notes as backup, offer to reschedule |
| Database not syncing | Check Google Drive permissions, refresh page |
| Emails not sending | Verify spam folder, check email settings |
| Poor audio quality | Use headset, test before interview, offer phone backup |

---

## File Locations Quick Reference

### Setup Guides
- Scheduling: `interview-scheduling-setup.md`
- Database: `interview-database-schema.md`
- Templates: `email-communication-templates.md`
- Analysis: `interview-analysis-framework.md`

### Interview Materials
- Clinics Guide: `icp-interview-guide-clinics.md`
- Real Estate Guide: `icp-interview-guide-real-estate.md`
- Note Template: `interview-note-template.md`

### Outreach Materials
- Execution Guide: `outreach-execution-guide-instagram-linkedin.md`
- Contact List: `contact-list-outreach.csv`

---

## Success Metrics

### Week 1 Targets
- [ ] 3-5 interviews completed
- [ ] 0 no-shows
- [ ] All data entered in database
- [ ] Thank you emails sent within 1h

### Full Cycle Targets (2 weeks)
- [ ] 15-20 interviews completed
- [ ] <10% no-show rate
- [ ] 100% data completeness
- [ ] Clear ICP pattern identified
- [ ] GO/NO-GO decision made

---

## Support Contacts

### Technical Issues
- Calendly Support: help.calendly.com
- Google Meet: support.google.com/meet
- Google Sheets: support.google.com/docs

### Content Questions
- Interview guides: See CMO Agent
- Analysis help: See CMO Agent
- Strategy questions: See CEO Agent

---

**Checklist Version**: 1.0
**Created**: 2025-04-25
**Purpose**: CON-57 - Customer Interview Infrastructure
**Estimated Setup Time**: 1-2 hours total
**Status**: Ready for execution
