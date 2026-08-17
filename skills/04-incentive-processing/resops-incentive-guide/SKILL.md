# Skill: /resops-incentive-guide

**For:** Research Operations team (Megan, Anna, Emanuelle)
**Purpose:** Given the participant type and study type, return the correct incentive amount and the exact processing path to follow (Ethnio, Admin tool, or other).

---

## When to use this skill

Invoke during kickoff prep or when processing incentives post-session. Quickly resolves: how much, what form, and through which system.

---

## How to invoke

Provide the following, then type:

```
/resops-incentive-guide
```

Input to provide:
- Participant type (customer / shopper / B2B / non-IC user)
- Study type (moderated / unmoderated / shop-along / benchmarking / in-person)
- Session length (in minutes)
- Number of participants being processed (optional)

---

## What Claude will do

### Step 1 — Return the incentive recommendation

Apply the standard ResOps incentive table. Claude will surface the amount and form based on participant type + session length.

> **Important:** Incentive amounts and policies are set by the ResOps team and may change. This skill applies the rates currently documented in the Recruiting Playbook. Always verify with Megan if a study falls outside the standard parameters.

**Standard rate reference (confirm current rates in the Recruiting Playbook):**

| Participant type | Session length | Incentive form |
|---|---|---|
| Instacart customer | 30 min | Gift card / Ethnio payout |
| Instacart customer | 60 min | Gift card / Ethnio payout |
| Instacart shopper | 30 min | Admin tool payout |
| Instacart shopper | 60 min | Admin tool payout |
| Non-IC user (general public) | 30 min | User Interviews payout |
| Non-IC user (general public) | 60 min | User Interviews payout |
| B2B / Advertiser | Any | Direct / custom — confirm with Megan |
| Unmoderated (any) | Self-paced | Platform payout (User Interviews / Ethnio) |

### Step 2 — Return the processing path

| Participant type | Processing path |
|---|---|
| Instacart customer (Ethnio) | Ethnio incentive payout — mark complete in Ethnio dashboard after session |
| Instacart shopper | Admin tool — submit shopper ID and session date for payout |
| Non-IC user (User Interviews) | User Interviews handles payout automatically on session completion |
| B2B / Advertiser | Confirm with Megan — typically direct or custom arrangement |
| Unmoderated (Ethnio) | Ethnio auto-pays on screener or task completion |
| Unmoderated (User Interviews) | User Interviews auto-pays on study completion |

### Step 3 — Flag any exceptions

Surface a flag if any of the following apply:
- **B2B participant:** Custom incentive — always confirm amount and method with Megan before processing
- **Session was partial or cut short:** Note that standard practice is to pay the full amount unless instructed otherwise
- **No-show:** Participants who did not attend are typically not paid — confirm with Megan if a partial no-show occurred
- **Study outside standard length:** Flag if session was significantly longer than booked (e.g., 90 min booked as 60) — researcher may need to approve adjusted incentive

### Step 4 — Output

```
## Incentive Guide — [Study Name]
Participant type: [Type]
Study type: [Type]
Session length: [X min]

Recommended incentive: [Amount + form]
Processing path: [Ethnio / Admin tool / User Interviews / Custom]

Steps to process:
1. [Step 1]
2. [Step 2]
3. [Step 3]

Flags: [Any exceptions — or "None"]
```

---

## References

- [Research Ops Main Doc](https://docs.google.com/document/d/1jzoICKM6iQxlfHam44rkPILhBm9NdS1aZxiBSoCZnCw/edit) — master index of all processes and linked documentation
- [Research Operations Recruiting Playbook](https://docs.google.com/document/d/1qC8Y39YW_DIE6bu8WoNgTh7OUSaKMCcAKIlnWv_gnAM/edit) — incentive rates and processing procedures by participant type
- [How to Work with ResOps](https://docs.google.com/document/d/1qLF_HZZlr4ICQsIXr4LueqO8JLIzvvZV1Dg_eWmw0_4/edit) — incentive policy overview for researchers

---

## Output format

Always produce in this order:
1. **Incentive recommendation** (amount + form)
2. **Processing path** (which system + steps)
3. **Any flags** (exceptions, custom cases)
