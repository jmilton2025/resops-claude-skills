# Skill: /resops-screener-review

**For:** Research Operations team (Megan, Anna, Emanuelle)
**Purpose:** Review a researcher-submitted screener for logic errors, gaps, and inconsistencies before it goes live — so ops can catch issues before they affect recruitment.

> **Note:** Researchers write their own screener questions. This skill is for the *ops review* step — not drafting. If you need to draft screener content, that's a researcher-facing tool.

---

## When to use this skill

Invoke when a researcher has submitted their screener questions and you need to:
1. Check for logic errors (branching, skip logic, contradictory criteria)
2. Verify the screener will actually surface the right participants
3. Flag any questions that are leading, unclear, or likely to cause drop-off
4. Confirm the screener matches the study's stated participant criteria

---

## How to invoke

Paste the screener questions (copy from the doc, Ethnio draft, or Slack), then type:

```
/resops-screener-review
```

Also provide (if available):
- The study's participant criteria (from the intake or kickoff doc)
- The target platform (Ethnio or User Interviews)
- The target participant count

---

## What Claude will do

### Step 1 — Criteria alignment check

Compare the screener questions against the stated participant criteria. Flag any gaps:

- Are all key inclusion criteria captured in a screener question?
- Are all key exclusion criteria captured?
- Is Instacart usage (or non-usage) verified correctly?
- For B2B: is the advertiser/business type screened for properly?
- For shoppers: is the shopper status question present and correct?

### Step 2 — Logic & flow review

Check the screener structure for:

| Issue type | What to look for |
|---|---|
| Dead-end branching | A "disqualify" path that doesn't actually end the screener |
| Missing skip logic | A question that should only appear based on a prior answer but doesn't branch |
| Contradictory criteria | Two questions that could qualify and disqualify the same person |
| Order problems | Sensitive or qualifying questions appearing too early (increases drop-off) |
| Double-barreled questions | One question asking two things at once |
| Leading questions | Wording that signals the "right" answer to participants |
| Vague response options | Answer choices that could be interpreted multiple ways |

### Step 3 — Drop-off risk assessment

Flag any questions likely to cause participants to abandon:
- Questions that feel invasive before trust is established
- Very long multi-select lists
- Open-text fields early in the flow
- No clear sense of how long the screener takes

Recommend reordering if needed.

### Step 4 — Platform-specific checks

**Ethnio:**
- Confirm skip logic is set up correctly for Ethnio's branching rules
- Check that disqualify screens are configured (not just a dead branch)
- Verify incentive messaging is not included in the screener itself

**User Interviews:**
- Confirm eligibility criteria match the screener filter settings
- Check that the screener length is appropriate for the incentive offered
- Verify auto-approval vs. manual review setting matches the study needs

### Step 5 — Output: Review summary

Produce a clear, numbered review for the coordinator to share back with the researcher:

```
## Screener Review — [Study Name]
Reviewed by: Claude (via /resops-screener-review)
Date: [Date]
Platform: [Ethnio / User Interviews]

### ✅ Looks good
[List what's working well]

### ⚠️ Issues to fix before launch
1. [Issue — specific question or section — what's wrong and why]
2. [Issue]
3. [Issue]

### 💡 Optional improvements
[Lower-priority suggestions — wording tweaks, order changes, etc.]

### Criteria coverage
- Inclusion criteria covered: [Yes / Partially / No — with specifics]
- Exclusion criteria covered: [Yes / Partially / No — with specifics]

### Recommendation
[Ready to launch / Fix issues above before launching / Needs researcher clarification on X]
```

---

## Output format

Always produce in this order:
1. **Criteria alignment check** (inclusion + exclusion)
2. **Logic & flow issues** (numbered, specific)
3. **Drop-off risk flags** (if any)
4. **Platform-specific checks**
5. **Review summary** (ready to share with researcher)

---

## References

- [Research Ops Main Doc](https://docs.google.com/document/d/1jzoICKM6iQxlfHam44rkPILhBm9NdS1aZxiBSoCZnCw/edit) — master index of all processes and linked documentation
- [Research Operations Recruiting Playbook](https://docs.google.com/document/d/1qC8Y39YW_DIE6bu8WoNgTh7OUSaKMCcAKIlnWv_gnAM/edit) — screener setup process and platform guidance
- [WIP Screener Bank](https://docs.google.com/document/d/1VTnNVLGIeuuMMLTF93ZfAdoJpeeguMXgq6V5Ay8b2V4/edit) — existing screener questions organized by audience type (reference for common patterns and known good logic)
