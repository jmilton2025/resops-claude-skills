# Skill: /resops-kickoff-prep

**For:** Research Operations team (Megan, Anna, Emanuelle)
**Purpose:** Given an incoming research brief, generate a pre-kickoff checklist and a structured alignment doc to share with the researcher before or during the kickoff call.

---

## When to use this skill

Invoke after `/resops-intake-triage` has confirmed a request is complete (or after gaps have been filled). Use it to:
1. Make sure the ops team is fully prepared before the kickoff call
2. Give the researcher a clear view of what to expect and what decisions need to be made
3. Set SLA expectations upfront so there are no surprises on timeline

---

## How to invoke

Paste the research brief or the completed intake summary, then type:

```
/resops-kickoff-prep
```

---

## What Claude will do

### Step 1 — Internal ops prep checklist

Generate a checklist for Anna or Emanuelle to complete *before* the kickoff call:

```
## Pre-Kickoff Ops Checklist — [Study Name]
Coordinator: [Name]
Kickoff date: [Date/TBD]

### Before the call
- [ ] Confirm study type (moderated / unmoderated / in-person / benchmarking / B2B)
- [ ] Identify correct recruitment platform (Ethnio or User Interviews — see /resops-screener-select)
- [ ] Verify query is ready or DS has been looped in
- [ ] Check participant pool size and flag if pool is small (B2B / advertiser)
- [ ] Review SLA table and calculate realistic fielding start date
- [ ] Check cooldown period — confirm participants haven't been contacted in the last [X] days
- [ ] Flag if participant count >30 (benchmarking pacing strategy needed)
- [ ] Confirm incentive amount and processing path for this participant type
- [ ] Set up screener shell in Ethnio or User Interviews (if researcher has shared screener)
- [ ] Add study to ops tracking dashboard
```

### Step 2 — SLA calculation

Based on the study type and requested fielding date, calculate whether the timeline is achievable. Use these standard SLAs:

| Study type | Typical ops lead time |
|---|---|
| Standard moderated (Ethnio, IC users) | 5–7 business days from kickoff |
| Unmoderated (User Interviews) | 3–5 business days from kickoff |
| B2B / Advertiser | 10–14 business days (smaller pool, monthly cadence) |
| Benchmarking / high count (30+) | 10–14 business days |
| Shop-along / in-person | 10+ business days (logistics-heavy) |
| Non-Instacart users (User Interviews) | 5–7 business days |

If the requested timeline is too tight, flag it and suggest a revised date. Example:

> ⚠️ **Timeline flag:** Researcher is requesting fielding to start [date], but kickoff is [date] — that's only 3 business days. Standard SLA for this study type is 5–7 days. Suggest pushing fielding start to [revised date] or discuss what can be expedited.

### Step 3 — Researcher-facing alignment doc

Produce a short doc the coordinator can paste into Slack or share as a Google Doc before or after the kickoff call:

```
## Kickoff Alignment — [Study Name]
Date sent: [Date]
Coordinator: [Name] | Researcher: [Name]

### What we'll recruit
- Study type: [Moderated / Unmoderated / etc.]
- Platform: [Ethnio / User Interviews]
- Participant type: [IC user / non-user / shopper / B2B]
- Target count: [N participants + N backups recommended]

### Timeline
- Screener live by: [Date]
- Fielding window: [Start – End]
- Sessions scheduled by: [Date]
- Ops lead time needed: [N business days]

### What we need from you
- [ ] Finalized screener questions
- [ ] Zoom link (if moderated)
- [ ] Confirmed datasheet / research schedule
- [ ] DS query (or DS contact)
- [ ] Incentive amount confirmation

### SLA note
[Insert any timeline flag here, or "Timeline looks achievable — we'll aim to have the screener live by [date]."]

Questions? Ping [coordinator name] in #researchops.
```

---

## Segment-specific notes

- **B2B / Advertiser:** Remind researcher of monthly cadence and smaller pool size. Confirm whether this is a new contact or re-engage.
- **Shop-alongs / in-person:** Add location, greeter, and travel logistics to the "what we need from you" list.
- **Benchmarking:** Flag backup pool strategy — ops will need to recruit 20–30% over target count.
- **Unmoderated:** No scheduling needed, but confirm auto-approval settings and completion rate targets.

---

## Output format

Always produce in this order:
1. **Internal ops checklist** (coordinator use only)
2. **SLA calculation + any timeline flags**
3. **Researcher-facing alignment doc** (ready to copy-paste into Slack)

---

## References

- [Research Ops Main Doc](https://docs.google.com/document/d/1jzoICKM6iQxlfHam44rkPILhBm9NdS1aZxiBSoCZnCw/edit) — master index of all processes and linked documentation
- [Research Operations Recruiting Playbook](https://docs.google.com/document/d/1qC8Y39YW_DIE6bu8WoNgTh7OUSaKMCcAKIlnWv_gnAM/edit) — full recruitment lifecycle and SLA detail
- [How to Work with ResOps](https://docs.google.com/document/d/1qLF_HZZlr4ICQsIXr4LueqO8JLIzvvZV1Dg_eWmw0_4/edit) — SLAs and submission requirements by study type
