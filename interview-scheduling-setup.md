# Interview Scheduling Setup Guide

## Overview
Complete guide to set up Calendly (or alternative) for customer interview scheduling.

---

## Step 1: Create Calendly Account

### Option A: Free Tier (Recommended for Initial Phase)
1. Go to [calendly.com](https://calendly.com)
2. Sign up with Google (for ease of setup)
3. Verify email address
4. Complete basic profile

**Free Tier Limitations:**
- 1 event type
- Limited customization
- Sufficient for 15-20 interviews

### Option B: Professional Tier ($16/month)
- Multiple event types
- Payment collection
- Advanced branding
- **Only upgrade if needed**

---

## Step 2: Configure Event Type

### Event Name
```
Entrevista de Descoberta ICP - ConectaPay (20 min)
```

### Event Details
- **Duration**: 20 minutes
- **Description**:
```
Uma conversa rápida para entender como você gerencia vendas e pagamentos no WhatsApp. Suas respostas nos ajudarão a construir uma solução que realmente resolve os problemas do seu negócio.

Não é venda. É pesquisa.
```

### Location
- **Google Meet** (recommended - automatic recording)
- OR **Zoom** (if preferred)

---

## Step 3: Set Availability

### Brazil Business Hours
- **Monday to Friday**: 9:00 - 18:00 (BRT)
- **Time Zone**: America/Sao_Paulo
- **Buffer Time**: 15 minutes between meetings

### Advanced Settings
- **Minimum scheduling notice**: 4 hours
- **Future scheduling limit**: 4 weeks
- **Cancel/reschedule**: Allowed up to 24 hours before

---

## Step 4: Customize Questions

### Required Questions
1. **Nome completo**
2. **Email**
3. **WhatsApp (com DDD)**

### Optional Questions
1. **Nome da empresa**
2. **Segmento** (Clínica / Imobiliária / Outro)
3. **Quantos funcionários?**
4. **Como você ouviu sobre a gente?**

### Question to Add to Calendly:
```
Por favor, conte brevemente: qual seu maior desafio hoje com vendas ou pagamentos no WhatsApp? (máx. 2 frases)
```

---

## Step 5: Booking Link Integration

### Your Booking Link
Once created, your link will be:
```
https://calendly.com/[your-username]/icp-discovery-interview
```

### Add to Outreach Messages
Update the outreach CSV to include this link in the booking invitation:
```
📅 Agende sua entrevista aqui: [CAL.COM/SEU-LINK]
```

---

## Step 6: Email Notifications

### Confirmation Email (Calendly Automatic)
Customize in Calendly settings:
```
Assunto: Entrevista Confirmada - ConectaPay

Olá {{name}}!

Obrigado por agendar sua entrevista de descoberta ICP.

📅 Data: {{date}}
⏰ Horário: {{time}}
🔗 Link da reunião: {{meeting_link}}

IMPORTANTE: A entrevista será gravada para análise. Ao participar, você consente com a gravação.

Se tiver alguma dúvida, responda a este email.

Te vejo logo!
Equipe ConectaPay
```

### Reminder Email (24h Before)
Enable in Calendly notifications:
```
Assunto: Lembrete: Entrevista Amanhã às {{time}}

Olá {{name}}!

Só um lembrete da nossa entrevista amanhã:

📅 Data: {{date}}
⏰ Horário: {{time}}
🔗 Link da reunião: {{meeting_link}}

Dica: Se puder, acesse 5 minutos antes para testar seu áudio/vídeo.

Até amanhã!
Equipe ConectaPay
```

---

## Step 7: Integration with Recording

### Google Meet Setup (Recommended)
1. Go to [meet.google.com](https://meet.google.com)
2. Enable automatic recording in settings
3. Create "ConectaPay Interviews" folder in Google Drive
4. Set recording save location

### Zoom Setup (Alternative)
1. Enable cloud recording in Zoom settings
2. Set "Record to cloud" as default
3. Enable auto-recording for all meetings
4. Set password protection

---

## Step 8: Calendar Integration

### Connect Your Calendar
1. In Calendly, go to **Integrations**
2. Connect **Google Calendar**
3. Enable **Two-way sync**
4. Set **Event detection**: 30 minutes before/after

### This Prevents:
- Double bookings
- Scheduling during conflicts
- Last-minute cancellations

---

## Step 9: Test Your Setup

### Pre-Launch Checklist
- [ ] Book a test appointment with yourself
- [ ] Verify email notifications arrive
- [ ] Test Google Meet link
- [ ] Test recording (5 min test)
- [ ] Verify recording saves to correct folder
- [ ] Test on mobile device
- [ ] Share link with team member for feedback

### What to Verify
- ✅ Booking flow works smoothly
- ✅ Questions appear correctly
- ✅ Meeting link works
- ✅ Recording saves to Drive
- ✅ Email notifications arrive on time
- ✅ Calendar sync prevents conflicts

---

## Alternative Tools

### If Not Calendly

#### Cal.com (Open Source)
- Free tier available
- More customization
- Self-hostable
- [cal.com](https://cal.com)

#### SavvyCal
- Better for B2B
- Visual scheduling
- $12/month
- [savvycal.com](https://savvycal.com)

#### Google Appointment Schedule
- Built into Google Calendar
- Free with Google Workspace
- Limited features
- [calendar.google.com](https://calendar.google.com)

---

## Step 10: Launch

### Go-Live Steps
1. **Double-check** all settings
2. **Test** complete flow end-to-end
3. **Share** booking link with outreach team
4. **Monitor** first 3 bookings closely
5. **Adjust** based on feedback

### Metrics to Track
- Booking conversion rate (visits → bookings)
- No-show rate
- Average booking lead time
- Cancellation rate

---

## Troubleshooting

### Common Issues

**Problem**: No bookings coming in
- **Solution**: Test the link yourself, verify it's shared correctly

**Problem**: High no-show rate
- **Solution**: Add SMS reminder, reduce lead time to 15 min

**Problem**: Technical issues during interview
- **Solution**: Always have backup option (phone call)

**Problem**: Recording failed
- **Solution**: Take detailed notes as backup, offer to reschedule

---

## Next Steps

After scheduling is set up:
1. ✅ Update outreach messages with booking link
2. ✅ Test recording and transcription
3. ✅ Set up interview tracking database
4. ✅ Prepare analysis framework
5. ✅ Launch outreach campaign

---

## Quick Reference

**Booking Link Format**: `https://calendly.com/[username]/icp-discovery-interview`
**Event Duration**: 20 minutes
**Time Zone**: America/Sao_Paulo
**Recording**: Google Meet auto-record
**Backup**: Phone notes

---

**Created**: 2025-04-25
**Purpose**: CON-57 - Customer Interview Infrastructure
**Status**: Ready for implementation
