# Skill: /resops-screener-select

**For:** Research Operations team (Megan, Anna, Emanuelle)
**Purpose:** Given a study's participant criteria, recommend the correct recruitment platform (Ethnio or User Interviews) and explain why.

---

## When to use this skill

Invoke during intake or kickoff prep when the platform hasn't been confirmed yet. This skill resolves the Ethnio vs. User Interviews decision quickly and flags any edge cases.

---

## How to invoke

Share the study type and participant criteria, then type:

```
/resops-screener-select
```

Example input:
> Study type: Moderated. 8 participants. Must be Instacart shoppers, active in the last 30 days.

---

## What Claude will do

### Step 1 — Apply the platform decision rules

Use this decision logic (based on the ResOps Recruiting Playbook):

| Participant type | Platform |
|---|---|
| Instacart customers (app users) | **Ethnio** |
| Instacart shoppers | **Ethnio** (via shopper app intercept) or **Admin tool** |
| Non-Instacart users (general public) | **User Interviews** |
| B2B / Advertisers | **User Interviews** (or direct outreach — see `/resops-b2b-recruit`) |
| Mixed (IC users + non-users) | Flag for ops team — may require two separate recruitment streams |

### Step 2 — Apply study-type modifiers

| Study type | Platform notes |
|---|---|
| Moderated (remote) | Either platform works — default by participant type above |
| Unmoderated | User Interviews preferred for non-IC users; Ethnio for IC users |
| Shop-along / in-person | Ethnio for IC users; coordinate logistics separately |
| Benchmarking (30+ participants) | User Interviews handles scale better; flag if Ethnio is preferred |
| HQ visit | Ethnio for IC users; confirm greeter and location logistics |

### Step 3 — Surface any edge cases

Flag if any of the following apply:

- **Overlap / cooldown risk:** Has this participant type been recruited recently? Ethnio pool may be fatigued — check cooldown period before launching.
- **Small pool:** If B2B or a very narrow segment, flag low pool size and suggest timeline buffer.
- **Multi-platform needed:** If the study needs both IC users and non-users, note that two screeners and two recruitment streams are required.
- **Shopper studies:** Confirm whether the shopper app intercept is available or if the Admin tool path is needed for this segment.
- **International participants:** User Interviews supports international recruiting; Ethnio is US-focused.

### Step 4 — Output: Platform recommendation

```
## Platform Recommendation — [Study Name]

**Recommended platform:** [Ethnio / User Interviews / Both]
**Reason:** [One sentence explaining why based on participant type + study type]

**Setup notes:**
- [Any edge cases or flags from Step 3]
- [Any special configuration needed for this platform/study combo]

**Next step:** [e.g., "Set up Ethnio screener — share questions via Slack when ready for review" or "Create User Interviews project and set eligibility filters"]
```

---

## References

- [Research Ops Main Doc](https://docs.google.com/document/d/1jzoICKM6iQxlfHam44rkPILhBm9NdS1aZxiBSoCZnCw/edit) — master index of all processes and linked documentation
- [Research Operations Recruiting Playbook](https://docs.google.com/document/d/1qC8Y39YW_DIE6bu8WoNgTh7OUSaKMCcAKIlnWv_gnAM/edit) — full platform decision rules and recruitment lifecycle
- [How to Work with ResOps](https://docs.google.com/document/d/1qLF_HZZlr4ICQsIXr4LueqO8JLIzvvZV1Dg_eWmw0_4/edit) — SLAs and submission requirements by study type
- [WIP Screener Bank](https://docs.google.com/document/d/1VTnNVLGIeuuMMLTF93ZfAdoJpeeguMXgq6V5Ay8b2V4/edit) — existing screener questions organized by audience type

---

## Output format

Always produce in this order:
1. **Platform recommendation** (Ethnio / User Interviews / Both + reason)
2. **Edge case flags** (cooldown, pool size, multi-stream, shopper path, international)
3. **Next step** (one clear action for the coordinator)
