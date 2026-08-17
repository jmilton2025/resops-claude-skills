# Skill: /resops-no-show-response

**For:** Research Operations team (Megan, Anna, Emanuelle)
**Purpose:** Draft a no-show follow-up message to the participant and a backup outreach message to a replacement candidate — so the coordinator can act quickly without starting from scratch.

---

## When to use this skill

Invoke when a participant doesn't show up for their scheduled session. Covers:
- Follow-up message to the no-show participant
- Backup outreach to a replacement from the waitlist or backup pool
- Internal note for the ops tracking dashboard

---

## How to invoke

Provide the following, then type:

```
/resops-no-show-response
```

Input to provide:
- Participant's first name (or "participant" if unknown)
- Study name
- Missed session date and time
- Study format (remote / in-person / shop-along)
- Whether a backup participant is available (yes / no / unknown)
- Whether to reschedule or close the slot

---

## What Claude will do

### Step 1 — Draft the no-show follow-up

Tone: warm but clear. Don't guilt-trip. Leave the door open to reschedule if slots are available — close it if not.

**If rescheduling is possible:**
```
Subject: We missed you today — [Study Name]

Hi [First Name],

We noticed you weren't able to make your session today at [Time]. No worries — things come up!

If you're still interested in participating, we have [a few slots / one more slot] available:
- [Option 1: Day, Date, Time]
- [Option 2: Day, Date, Time]

Reply to this message to grab one of these times, or let us know if you'd like to be considered for a future study.

Thanks for your understanding!

[Coordinator Name]
Instacart Research Team
```

**If no rescheduling is available:**
```
Subject: We missed you today — [Study Name]

Hi [First Name],

We noticed you weren't able to join your session today at [Time]. Unfortunately we don't have any remaining slots for this study, but we appreciate your interest in participating.

We'd love to include you in a future study — we'll keep you in mind!

Thanks,

[Coordinator Name]
Instacart Research Team
```

### Step 2 — Draft the backup outreach message

Reach out to a backup participant from the waitlist or pool.

**Backup outreach (remote):**
```
Subject: Research session opportunity — [Study Name]

Hi [First Name],

A spot has just opened up in an upcoming research session, and we thought you might be interested!

📅 [Day, Date] at [Time] [Timezone]
⏱ About [X] minutes
💻 Remote via Zoom

[Brief 1-sentence study description, if shareable: e.g., "We're looking for Instacart users to share their experience with our app."]

If you're available and interested, reply to this message and we'll send you the details right away.

Thanks!

[Coordinator Name]
Instacart Research Team
```

**Backup outreach (in-person / shop-along):**
```
Subject: In-person research session opportunity — [Study Name]

Hi [First Name],

A spot has just opened up for an in-person research session!

📅 [Day, Date] at [Time]
📍 [Location]
⏱ About [X] minutes

[Brief description if shareable.]

Reply to this message if you're interested and we'll get you confirmed right away.

Thanks!

[Coordinator Name]
Instacart Research Team
```

### Step 3 — Internal tracking note

Produce a short log entry for the ops dashboard or study tracker:

```
No-show log — [Study Name]
Date: [Date]
Participant: [ID or first name]
Scheduled time: [Time]
Action taken: [Follow-up sent / Slot closed / Backup outreach sent to [Name]]
Rescheduled: [Yes — new time: X / No]
Notes: [Any relevant context]
```

---

## Cooldown note

If the no-show participant was a first contact, they remain in the pool. If this is their second no-show, flag for Megan to review before re-inviting — repeated no-shows may warrant removal from the active pool.

---

## References

- [Research Ops Main Doc](https://docs.google.com/document/d/1jzoICKM6iQxlfHam44rkPILhBm9NdS1aZxiBSoCZnCw/edit) — master index of all processes and linked documentation
- [Research Operations Recruiting Playbook](https://docs.google.com/document/d/1qC8Y39YW_DIE6bu8WoNgTh7OUSaKMCcAKIlnWv_gnAM/edit) — participant outreach templates and no-show handling guidance
- [How to Work with ResOps](https://docs.google.com/document/d/1qLF_HZZlr4ICQsIXr4LueqO8JLIzvvZV1Dg_eWmw0_4/edit) — process overview and SLAs

---

## Output format

Always produce in this order:
1. **No-show follow-up message** (with or without reschedule option, clearly labeled)
2. **Backup outreach message** (if applicable)
3. **Internal tracking note**
4. **Cooldown flag** (if second no-show)
