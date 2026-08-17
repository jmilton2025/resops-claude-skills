# Skill: /resops-scheduling-checklist

**For:** Research Operations team (Megan, Anna, Emanuelle)
**Purpose:** Generate a complete scheduling checklist tailored to the study type — remote, in-person, shop-along, or HQ visit — so nothing falls through the cracks between kickoff and sessions going live.

---

## When to use this skill

Invoke after the screener is live and recruitment is underway, when the coordinator is ready to begin scheduling confirmed participants.

---

## How to invoke

Provide the following, then type:

```
/resops-scheduling-checklist
```

Input to provide:
- Study name
- Study format (remote / in-person / shop-along / HQ visit)
- Session dates and times
- Number of participants to schedule
- Researcher name and Zoom link (if remote)
- Location details (if in-person)

---

## What Claude will do

Produce a format-specific checklist the coordinator can work through and check off as sessions are confirmed.

---

### Remote (moderated) checklist

```
## Scheduling Checklist — [Study Name] (Remote)
Coordinator: [Name] | Researcher: [Name]

### Setup
- [ ] Researcher has confirmed Zoom link is active and waiting room is ON
- [ ] Session slots added to scheduling tool (Ethnio / Calendly / manual)
- [ ] Screener completions reviewed and participants qualified
- [ ] Backup list identified (recommend 20–30% over target count)

### Per participant (repeat for each confirmed participant)
- [ ] Slot confirmed with participant
- [ ] Calendar invite sent with Zoom link
- [ ] Confirmation message sent (via Ethnio or email)
- [ ] Participant added to session tracker with: name, contact, time slot, backup status
- [ ] Incentive amount noted in tracker

### Before sessions begin
- [ ] 24-hour reminder sent to all confirmed participants
- [ ] 1-hour reminder scheduled or queued
- [ ] Researcher briefed on participant count and any flags
- [ ] Backup participants on standby and aware they may be called

### Day-of
- [ ] 1-hour reminder sent
- [ ] Monitor for no-shows — trigger /resops-no-show-response if needed
- [ ] Note actual attendance in tracker
```

---

### In-person / HQ visit checklist

```
## Scheduling Checklist — [Study Name] (In-Person / HQ)
Coordinator: [Name] | Researcher: [Name]
Location: [Address / Room]

### Setup
- [ ] Location confirmed and booked (room, floor, building access)
- [ ] Greeter assigned (who will meet participants at reception)
- [ ] Parking or transit info prepared
- [ ] Building access / visitor pass process confirmed
- [ ] Session slots confirmed with researcher
- [ ] Backup participants identified

### Per participant (repeat for each confirmed participant)
- [ ] Slot confirmed with participant
- [ ] Confirmation message sent with full location details
- [ ] Calendar invite sent
- [ ] Participant added to session tracker with: name, contact, time slot, backup status
- [ ] Any special access needs noted (accessibility, dietary if food provided, etc.)

### Before sessions begin
- [ ] 48-hour reminder sent with location details
- [ ] Day-of reminder sent
- [ ] Greeter briefed on participant names and arrival times
- [ ] Researcher briefed on schedule and participant count
- [ ] Backup participants on standby

### Day-of
- [ ] Coordinator or greeter at location before first session
- [ ] Monitor for no-shows — trigger /resops-no-show-response if needed
- [ ] Note actual attendance in tracker
- [ ] Collect any required consent forms on-site if not done digitally
```

---

### Shop-along checklist

```
## Scheduling Checklist — [Study Name] (Shop-Along)
Coordinator: [Name] | Researcher: [Name]

### Setup
- [ ] Store location(s) confirmed with researcher
- [ ] Store manager or contact notified (if required)
- [ ] Session slots confirmed — allow extra buffer time between sessions for travel
- [ ] Equipment confirmed: recording device, consent forms, researcher materials
- [ ] Backup participants identified

### Per participant (repeat for each confirmed participant)
- [ ] Slot confirmed with participant
- [ ] Meeting point confirmed (store entrance, specific section, parking lot)
- [ ] Confirmation message sent with meeting point details and what to expect
- [ ] Calendar invite sent
- [ ] Participant added to tracker

### Before sessions begin
- [ ] 48-hour reminder sent with meeting point and logistics
- [ ] Day-of reminder sent
- [ ] Researcher briefed on participant schedule
- [ ] Confirm researcher has all materials (consent form, recording setup, etc.)
- [ ] Backup participants on standby

### Day-of
- [ ] Coordinator available by phone in case of issues
- [ ] Monitor for no-shows — trigger /resops-no-show-response if needed
- [ ] Note attendance in tracker
```

---

## Flags to surface

- If participant count is >30, note that staggered scheduling may be needed to avoid overlap
- If any participant flagged a special need during screener, surface it here
- If the study is B2B, confirm that the monthly cadence and pool size have been accounted for

---

## References

- [Research Ops Main Doc](https://docs.google.com/document/d/1jzoICKM6iQxlfHam44rkPILhBm9NdS1aZxiBSoCZnCw/edit) — master index of all processes and linked documentation
- [Research Operations Recruiting Playbook](https://docs.google.com/document/d/1qC8Y39YW_DIE6bu8WoNgTh7OUSaKMCcAKIlnWv_gnAM/edit) — scheduling process and logistics guidance
- [How to Work with ResOps](https://docs.google.com/document/d/1qLF_HZZlr4ICQsIXr4LueqO8JLIzvvZV1Dg_eWmw0_4/edit) — SLAs and researcher expectations

---

## Output format

Produce the checklist matching the study format. If format is unclear, ask before generating. Always surface any flags at the end.
