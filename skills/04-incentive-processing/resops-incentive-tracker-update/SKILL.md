# Skill: /resops-incentive-tracker-update

**For:** Research Operations team (Megan, Anna, Emanuelle)
**Purpose:** Format a clean, consistent incentive log entry (or batch of entries) for the ops tracking dashboard or spreadsheet — from raw session notes or a list of participants.

---

## When to use this skill

Invoke after sessions are complete and incentives need to be logged. Works for:
- A single participant post-session
- A batch of participants after a study wraps
- Cleaning up messy or inconsistent log entries

---

## How to invoke

Paste your raw session data (names, times, statuses, amounts), then type:

```
/resops-incentive-tracker-update
```

Input can be in any format — a Slack message, a copy-pasted table, bullet points, or free text. Claude will extract and structure it.

---

## What Claude will do

### Step 1 — Extract participant data

From the raw input, pull out for each participant:
- Participant ID or first name
- Session date and time
- Study name
- Participant type (customer / shopper / B2B / non-IC user)
- Session status (completed / no-show / partial)
- Incentive amount
- Processing path (Ethnio / Admin / User Interviews / Custom)
- Incentive status (pending / processed / N/A)

### Step 2 — Format as tracker rows

Produce a clean table ready to paste into the ops tracker:

```
| Participant | Study | Date | Session Type | Status | Incentive | Platform | Processed? |
|---|---|---|---|---|---|---|---|
| [Name/ID] | [Study] | [Date] | [Moderated/Unmod] | Completed | $[X] | Ethnio | ☐ Pending |
| [Name/ID] | [Study] | [Date] | [Moderated/Unmod] | No-show | N/A | — | N/A |
```

### Step 3 — Flag anything that needs action

Surface a flag for:
- Any participant marked "completed" with no incentive amount noted
- Any no-show where incentive status is unclear
- B2B participants (confirm processing method before marking complete)
- Partial sessions (flagged for coordinator review on amount)
- Any entry where participant type is missing

### Step 4 — Produce a processing summary

If processing a batch, add a quick summary at the top:

```
## Incentive Processing Summary — [Study Name]
Date processed: [Date]
Coordinator: [Name]

Total participants: [N]
  - Completed: [N]
  - No-shows: [N]
  - Partial: [N]

Total incentives to process: $[X]
  - Via Ethnio: [N] participants / $[X]
  - Via Admin tool: [N] participants / $[X]
  - Via User Interviews: [N] participants / $[X] (auto-processed)
  - Custom / pending confirmation: [N] participants

Action needed: [List any flagged items — or "None, all entries ready to process"]
```

---

## References

- [Research Ops Main Doc](https://docs.google.com/document/d/1jzoICKM6iQxlfHam44rkPILhBm9NdS1aZxiBSoCZnCw/edit) — master index of all processes and linked documentation
- [Research Operations Recruiting Playbook](https://docs.google.com/document/d/1qC8Y39YW_DIE6bu8WoNgTh7OUSaKMCcAKIlnWv_gnAM/edit) — incentive processing procedures and tracker format
- [How to Work with ResOps](https://docs.google.com/document/d/1qLF_HZZlr4ICQsIXr4LueqO8JLIzvvZV1Dg_eWmw0_4/edit) — incentive policy overview

---

## Output format

Always produce in this order:
1. **Processing summary** (totals by platform + action items)
2. **Formatted tracker table** (paste-ready)
3. **Flags** (any entries needing review before processing)
