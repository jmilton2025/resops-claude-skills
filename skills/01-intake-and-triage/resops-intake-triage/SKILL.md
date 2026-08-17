# Skill: /resops-intake-triage

**For:** Research Operations team (Megan, Anna, Emanuelle)
**Purpose:** Review an incoming research request, interactively collect any missing information via pop-up questions, then produce a complete intake summary, follow-up draft, and kickoff agenda.

---

## Workflow

### Step 1 — Parse the request

Read the research request provided. Extract whatever is already present:

- Study name / project name
- Researcher name
- Study type (moderated / unmoderated / in-person / shop-along / HQ visit / benchmarking / B2B)
- Participant criteria (who they need)
- Participant count
- Timeline / fielding dates
- Zoom link
- Datasheet (full research schedule)
- Query (Mode / DS query)
- Incentive info
- Participant type (IC customer / shopper / non-IC user / B2B)

### Step 2 — Identify missing fields

Check which of the above are absent or unclear. Do NOT produce a summary yet.

### Step 3 — Ask for missing info interactively

For each missing field, use the AskUserQuestion tool to collect it via a pop-up with selectable options. Group questions in batches of up to 4 at a time.

**Question set A** (always ask first if any of these are missing):

- **Study type** — options: Moderated (remote), Unmoderated (self-paced), In-person / HQ visit, Shop-along, Benchmarking (30+ participants), B2B / Advertiser
- **Participant type** — options: Instacart customers, Instacart shoppers, Non-Instacart users (general public), B2B / Advertisers (multiSelect: true)
- **Participant count** — options: 5, 8, 10, 12, 15, 20, 30+
- **Timeline** — options: This week, Next 1–2 weeks, 3–4 weeks out, More than a month out

**Question set B** (ask second, for logistics fields):

- **Zoom link** — options: Already have one, Need to create one, Not needed (in-person)
- **Datasheet status** — options: Shared and complete, Shared but incomplete, Not yet shared, Not applicable
- **Query status** — options: Query is ready, Need to loop in a DS, Not sure — need guidance
- **Incentive** — options: Use standard rate for this study type, Custom amount (will specify), Not confirmed yet

Only ask about fields that are actually missing. If a field was provided in the request, skip its question entirely.

### Step 4 — Produce the full output

Once all missing fields are filled in, produce the following in order:

---

#### Intake Summary

| Field | Status | Value |
|---|---|---|
| Study name | ✅ | [value] |
| Researcher | ✅/❌ | [value or Missing] |
| Study type | ✅ | [value] |
| Participant type | ✅ | [value] |
| Participant count | ✅ | [value] |
| Timeline | ✅ | [value] |
| Zoom link | ✅/N/A | [value or N/A] |
| Datasheet | ✅/❌ | [value] |
| Query | ✅/❌ | [value] |
| Incentive | ✅/❌ | [value or TBD] |

If everything is now filled in: "This request looks complete — ready to proceed to screener setup."

---

#### Draft Follow-Up Slack Message (only if any field is still unresolved after the pop-ups)

Write a short, warm Slack message to the researcher listing only the remaining unresolved items (numbered for easy reply). Match the ResOps team's voice — direct, friendly, no corporate-speak.

---

#### Kickoff Agenda

```
Kickoff Agenda — [Study Name]
Researcher: [Name]
Date/Time: TBD | Duration: 30 min

1. Study overview (5 min)
   - Goals, methodology, participant profile

2. Participant criteria alignment (10 min)
   - Who we're recruiting and why
   - Confirm participant type and any behavioral criteria
   - Confirm study format

3. Timeline & logistics (10 min)
   - Fielding window, session dates
   - Zoom / location setup
   - Screener review and launch date

4. Data sourcing (5 min)
   - Query readiness
   - Any PII handling considerations

5. Open questions / next steps
   - [auto-populate any remaining unknowns here]
```

---

## Segment-specific reminders

- **B2B / Advertiser:** Smaller pool, monthly cadence, no cooldown rule — flag if timeline doesn't account for this.
- **Shop-alongs / in-person:** No Zoom needed; confirm location, greeter, and travel logistics.
- **Unmoderated:** No scheduling needed; confirm platform (Ethnio vs. User Interviews) and auto-approval setting.
- **Benchmarking (30+):** Flag that a backup pool and pacing strategy are needed.

---

## References

- [Research Ops Main Doc](https://docs.google.com/document/d/1jzoICKM6iQxlfHam44rkPILhBm9NdS1aZxiBSoCZnCw/edit) — master index of all processes and linked documentation
- [Research Operations Recruiting Playbook](https://docs.google.com/document/d/1qC8Y39YW_DIE6bu8WoNgTh7OUSaKMCcAKIlnWv_gnAM/edit) — full recruitment lifecycle
- [How to Work with ResOps](https://docs.google.com/document/d/1qLF_HZZlr4ICQsIXr4LueqO8JLIzvvZV1Dg_eWmw0_4/edit) — SLAs and submission requirements for researchers
