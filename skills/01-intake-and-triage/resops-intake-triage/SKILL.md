# Skill: /resops-intake-triage

**For:** Research Operations team (Megan, Anna, Emanuelle)
**Purpose:** Review an incoming research request, flag any missing information, and draft a kickoff agenda.

---

## When to use this skill

Invoke when a new research request has come in via Slack or the intake form and you need to:
1. Quickly assess whether the request is complete enough to act on
2. Identify exactly what's missing before reaching out to the researcher
3. Draft a kickoff meeting agenda to align on criteria and timeline

---

## How to invoke

Paste the research request (Slack message, form submission, or email) directly into the chat, then type:

```
/resops-intake-triage
```

Or paste the request and ask:
```
/resops-intake-triage [paste request here]
```

---

## What Claude will do

### Step 1 — Parse the request

Extract and surface the following fields (mark each as ✅ present or ❌ missing):

| Field | What to look for |
|---|---|
| Study type | Moderated / Unmoderated / Shop-along / In-person / Benchmarking / B2B |
| Participant criteria | Who they need (demographics, behavior, Instacart user vs. non-user) |
| Participant count | How many participants |
| Timeline | Fielding dates, session dates, or deadline |
| Zoom link | Session link or note that it's not needed (e.g., in-person) |
| Datasheet | Confirmation that a complete research schedule has been shared |
| Query | Mode / DS query for pulling the participant pool |
| Incentive info | Amount and type (if known) |
| Researcher name | Who submitted the request |
| Project / study name | What to call this study in tracking |

### Step 2 — Flag gaps

List every ❌ missing field clearly, with a plain-English note on why it's needed. Example:

> ❌ **Zoom link** — Needed before scheduling participant sessions. If in-person, confirm location instead.
> ❌ **Query** — Required to pull the participant pool from Mode. Share the query or tag the DS who will run it.

If nothing is missing, confirm: "This request looks complete — ready to proceed to screener setup."

### Step 3 — Draft a follow-up message (if gaps exist)

Write a short, friendly Slack message to the researcher that:
- Thanks them for submitting
- Lists the specific missing items (numbered, not bulleted — easier to respond to)
- Gives a clear ask ("Can you share these before [date] so we can hit your [fielding date] target?")

Match the Research Ops team's warm, direct tone. No corporate-speak.

### Step 4 — Draft a kickoff agenda

Regardless of gaps, produce a kickoff agenda the team can use to align with the researcher. Include:

```
## Kickoff Agenda — [Study Name]
Researcher: [Name]
Date/Time: [TBD or scheduled]
Duration: 30 min

1. Study overview (5 min)
   - Goals, methodology, participant profile

2. Participant criteria alignment (10 min)
   - Who we're recruiting and why
   - Confirm Instacart user vs. non-user
   - Confirm moderated vs. unmoderated

3. Timeline & logistics (10 min)
   - Fielding window, session dates
   - Zoom / location setup
   - Screener review and launch date

4. Data sourcing (5 min)
   - Query readiness
   - Any PII handling considerations

5. Open questions / next steps
   - [auto-populated from flagged gaps]
```

---

## Segment-specific reminders

- **B2B / Advertiser requests:** Smaller pool, monthly cadence, no cooldown rule applies — flag if the researcher hasn't accounted for this in their timeline.
- **Shop-alongs / in-person / HQ visits:** No Zoom needed, but confirm location, travel logistics, and whether a greeter is needed.
- **Unmoderated studies:** No scheduling needed, but confirm the platform (User Interviews vs. Ethnio) and whether auto-approval is on.
- **Benchmarking / high-count studies:** Flag if participant count is >30 — pacing strategy and backup pool needed.

---

## Output format

Always produce in this order:
1. **Intake summary table** (fields + ✅/❌ status)
2. **Gap list** (only if gaps exist)
3. **Draft follow-up Slack message** (only if gaps exist)
4. **Kickoff agenda**

Keep the tone warm and practical — this is internal team use, not a formal report.

---

## References

- [Research Ops Main Doc](https://docs.google.com/document/d/1jzoICKM6iQxlfHam44rkPILhBm9NdS1aZxiBSoCZnCw/edit) — master index of all processes and linked documentation
- [Research Operations Recruiting Playbook](https://docs.google.com/document/d/1qC8Y39YW_DIE6bu8WoNgTh7OUSaKMCcAKIlnWv_gnAM/edit) — full recruitment lifecycle: request → prepare → recruit → monitor → wrap
- [How to Work with ResOps](https://docs.google.com/document/d/1qLF_HZZlr4ICQsIXr4LueqO8JLIzvvZV1Dg_eWmw0_4/edit) — process overview, SLAs, and submission requirements for researchers
