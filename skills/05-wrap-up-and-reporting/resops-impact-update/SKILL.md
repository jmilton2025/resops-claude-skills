# Skill: /resops-impact-update

**For:** Research Operations team (Megan, Anna, Emanuelle)
**Purpose:** Format a weekly or monthly research impact tracking entry from study data — ready to add to the ops dashboard or share with leadership.

---

## When to use this skill

Invoke at the end of the week or month to compile completed study data into a clean impact entry. Also useful after a single study closes if Megan wants to capture it immediately.

---

## How to invoke

Paste your raw study data (completed studies, participant counts, study types, researchers) then type:

```
/resops-impact-update
```

Specify: **weekly** or **monthly** entry.

Input can be in any format — a Slack message, copy-pasted tracker rows, bullet points, or free text.

---

## What Claude will do

### Step 1 — Extract study data

From the raw input, pull out for each completed study:
- Study name
- Researcher(s)
- Study type (moderated / unmoderated / shop-along / benchmarking / B2B)
- Participant type (customer / shopper / B2B / non-IC)
- Sessions completed
- No-show count
- Fielding dates (start → end)
- Any notable ops flags or learnings

### Step 2 — Format the impact entry

**Weekly entry:**
```
## Research Ops Weekly Impact — Week of [Date]
Prepared by: [Coordinator Name]

### Studies active this week
| Study | Researcher | Type | Participants completed | No-shows |
|---|---|---|---|---|
| [Study name] | [Name] | [Type] | [N] | [N] |

### Studies closed this week
| Study | Researcher | Total completed | Fielding window |
|---|---|---|---|
| [Study name] | [Name] | [N] | [Start – End] |

### Totals
- Studies active: [N]
- Studies closed: [N]
- Total participants recruited this week: [N]
- Total no-shows: [N] ([X]% no-show rate)

### Ops notes
[Any recurring issues, pool fatigue signals, timeline flags, or process improvements to surface]
```

**Monthly entry:**
```
## Research Ops Monthly Impact — [Month Year]
Prepared by: [Coordinator Name]

### Studies completed this month
| Study | Researcher | Type | Participants | No-shows | Fielding window |
|---|---|---|---|---|---|
| [Study name] | [Name] | [Type] | [N] | [N] | [Dates] |

### Monthly totals
- Studies completed: [N]
- Total participants recruited: [N]
- Total no-shows: [N] ([X]% no-show rate)
- Participant breakdown:
  - Instacart customers: [N]
  - Instacart shoppers: [N]
  - B2B / Advertisers: [N]
  - Non-IC users: [N]

### Study type breakdown
- Moderated (remote): [N]
- Unmoderated: [N]
- In-person / shop-along: [N]
- Benchmarking: [N]
- B2B: [N]

### Platform usage
- Ethnio: [N] studies
- User Interviews: [N] studies
- Both: [N] studies

### Ops highlights & learnings
[Surface any process improvements, recurring issues, unusual patterns, or wins from the month]
```

### Step 3 — Flag anything missing

If key data is absent (no-show counts, participant types, study names), flag what's needed to complete the entry rather than leaving blanks.

---

## References

- [Research Ops Main Doc](https://docs.google.com/document/d/1jzoICKM6iQxlfHam44rkPILhBm9NdS1aZxiBSoCZnCw/edit) — master index of all processes and linked documentation
- [Research Operations Recruiting Playbook](https://docs.google.com/document/d/1qC8Y39YW_DIE6bu8WoNgTh7OUSaKMCcAKIlnWv_gnAM/edit) — ops tracking and reporting guidance
- [How to Work with ResOps](https://docs.google.com/document/d/1qLF_HZZlr4ICQsIXr4LueqO8JLIzvvZV1Dg_eWmw0_4/edit) — SLAs and process overview

---

## Output format

Always produce in this order:
1. **Weekly or monthly impact entry** (clearly labeled, paste-ready)
2. **Any flags** (missing data needed to complete the entry)
