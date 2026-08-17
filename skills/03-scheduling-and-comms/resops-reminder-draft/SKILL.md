# Skill: /resops-reminder-draft

**For:** Research Operations team (Megan, Anna, Emanuelle)
**Purpose:** Draft participant reminder messages (pre-session and day-of) in the ResOps team's warm, direct voice — ready to send via Ethnio, User Interviews, or email.

---

## When to use this skill

Invoke when sessions are confirmed and you need to send reminders to participants. Covers:
- 24-hour pre-session reminder
- Day-of / 1-hour reminder
- Custom reminders for in-person, shop-along, or HQ visit studies

---

## How to invoke

Provide the following details, then type:

```
/resops-reminder-draft
```

Input to provide:
- Study name
- Session date and time (with timezone)
- Study format (remote / in-person / shop-along / HQ)
- Zoom link (if remote)
- Location + any logistics (if in-person)
- Incentive amount (optional — include if confirmed)
- Any study-specific instructions (e.g., "please be in a quiet space," "have the Instacart app open")

---

## What Claude will do

### Step 1 — Determine reminder types needed

Based on study format, produce the relevant reminder set:

| Format | Reminders to draft |
|---|---|
| Remote (moderated) | 24-hour + 1-hour |
| Unmoderated | 24-hour only (link-based, no scheduling) |
| In-person / HQ visit | 48-hour + day-of |
| Shop-along | 48-hour + day-of (includes logistics) |

### Step 2 — Draft reminders

Follow the ResOps voice: warm, clear, and concise. No corporate-speak. Participants should feel informed and welcomed, not processed.

**24-hour reminder (remote):**
```
Subject: Reminder: Your research session is tomorrow — [Study Name]

Hi [First Name],

Just a quick reminder that your research session is scheduled for tomorrow:

📅 [Day, Date] at [Time] [Timezone]
🔗 Zoom link: [Link]

The session will take about [X] minutes. [Any specific instructions, e.g., "Please join from a quiet space with your Instacart app open."]

If anything comes up and you can't make it, please let us know as soon as possible by replying to this message.

Looking forward to chatting with you!

[Coordinator Name]
Instacart Research Team
```

**Day-of / 1-hour reminder (remote):**
```
Subject: Your session starts in 1 hour — [Study Name]

Hi [First Name],

Your session is coming up in about an hour!

📅 Today at [Time] [Timezone]
🔗 Zoom link: [Link]

[Any last-minute instructions, e.g., "Make sure you're in a quiet spot and your Instacart app is ready to go."]

See you soon!

[Coordinator Name]
Instacart Research Team
```

**48-hour reminder (in-person / HQ / shop-along):**
```
Subject: Reminder: Your in-person research session — [Study Name]

Hi [First Name],

Your in-person session is in two days — here are the details:

📅 [Day, Date] at [Time]
📍 Location: [Full address or office location + room/floor]
🚗 Parking: [Parking info if applicable]

[Any logistics, e.g., "Please check in at the front desk and ask for [Coordinator Name]."]

The session will take about [X] minutes. [Include any prep instructions specific to shop-along, etc.]

Questions? Reply to this message and we'll help.

See you soon,

[Coordinator Name]
Instacart Research Team
```

**Day-of reminder (in-person / HQ / shop-along):**
```
Subject: See you today! — [Study Name]

Hi [First Name],

Today's the day! Here's a quick recap:

📅 [Time] [Timezone]
📍 [Location / address]

[Any last-minute logistics, e.g., "Head to the 3rd floor reception and ask for [Name]."]

We're looking forward to meeting you!

[Coordinator Name]
Instacart Research Team
```

### Step 3 — Flag any missing info

If the input is missing anything needed to complete the reminder (e.g., no Zoom link provided for a remote study), flag it clearly rather than leaving a blank placeholder.

---

## Customization notes

- **Incentive mention:** Only include if confirmed and if the platform allows it. Never mention specific amounts in Ethnio messages unless ops practice allows it.
- **Unmoderated reminders:** Simpler — just include the study link and estimated time. No session time needed.
- **Multiple sessions same day:** Produce one template with [First Name] and [Time] as variables — don't draft individual messages for each participant.

---

## References

- [Research Ops Main Doc](https://docs.google.com/document/d/1jzoICKM6iQxlfHam44rkPILhBm9NdS1aZxiBSoCZnCw/edit) — master index of all processes and linked documentation
- [Research Operations Recruiting Playbook](https://docs.google.com/document/d/1qC8Y39YW_DIE6bu8WoNgTh7OUSaKMCcAKIlnWv_gnAM/edit) — participant outreach templates and communication standards
- [How to Work with ResOps](https://docs.google.com/document/d/1qLF_HZZlr4ICQsIXr4LueqO8JLIzvvZV1Dg_eWmw0_4/edit) — SLAs and process overview

---

## Output format

Always produce in this order:
1. **List of reminder types being drafted** (based on study format)
2. **Each reminder draft** (clearly labeled: 24-hour, 1-hour, 48-hour, day-of)
3. **Any flags** (missing info, incentive handling notes)
