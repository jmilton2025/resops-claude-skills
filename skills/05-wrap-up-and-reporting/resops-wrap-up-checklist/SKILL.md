# Skill: /resops-wrap-up-checklist

**For:** Research Operations team (Megan, Anna, Emanuelle)
**Purpose:** Generate a study wrap-up checklist covering all post-fielding tasks — incentive processing, data archiving, dashboard updates, and researcher close-out — so nothing is missed after sessions end.

---

## When to use this skill

Invoke when all sessions for a study are complete and it's time to close out the study on the ops side.

---

## How to invoke

Provide the following, then type:

```
/resops-wrap-up-checklist
```

Input to provide:
- Study name
- Study format (remote / in-person / unmoderated / shop-along)
- Participant type (customer / shopper / B2B / non-IC user)
- Total sessions completed / no-shows
- Coordinator name

---

## What Claude will do

Generate a complete wrap-up checklist tailored to the study type.

---

### Standard wrap-up checklist (all studies)

```
## Study Wrap-Up Checklist — [Study Name]
Coordinator: [Name] | Researcher: [Name]
Wrap-up date: [Date]

### Incentive Processing
- [ ] All completed sessions logged in tracker — use /resops-incentive-tracker-update if needed
- [ ] Incentives processed for all completed participants (Ethnio / Admin / User Interviews)
- [ ] No-show entries marked N/A in tracker
- [ ] B2B incentives confirmed with Megan before processing
- [ ] Incentive processing summary saved to study folder

### Participant Data & Privacy
- [ ] Participant PII (names, emails, contact info) removed from active tracking sheets per data privacy policy
- [ ] Participant IDs retained in tracker (no identifying info)
- [ ] Any CCPA deletion requests noted and queued — use /resops-ccpa-deletion if applicable
- [ ] Recording files (if any) moved to secure storage per researcher's instructions

### Platform Close-Out
- [ ] Ethnio intercept paused or closed (if used)
- [ ] User Interviews project closed (if used)
- [ ] Screener archived in screener bank — use /resops-screener-bank-add if it's worth keeping
- [ ] Any remaining invites or outreach emails stopped

### Ops Dashboard Update
- [ ] Study marked "Complete" in the ops tracking dashboard
- [ ] Final participant counts recorded: [completed / no-show / backup used]
- [ ] Notes added to dashboard: any issues, unusual patterns, or recommendations for next time
- [ ] Study added to monthly impact tracking — use /resops-impact-update

### Researcher Close-Out
- [ ] Researcher notified that ops wrap-up is complete
- [ ] Any outstanding questions from the researcher addressed
- [ ] Confirm researcher has all session recordings / notes they need
- [ ] Debrief note sent to researcher if there were any ops-side issues (no-show rate, pool size, timeline flags)
```

---

### Additional items for in-person / shop-along studies

```
### In-Person / Shop-Along Add-Ons
- [ ] Any physical materials returned or disposed of (consent forms, printed guides)
- [ ] Room or location booking cancelled or released
- [ ] Store contact thanked / notified of completion (if applicable)
- [ ] Researcher travel or logistics expenses logged (if applicable)
```

---

### Additional items for B2B / Advertiser studies

```
### B2B Add-Ons
- [ ] Advertiser contacts logged separately from consumer tracker
- [ ] Confirm cooldown period applied to B2B participants (monthly cadence)
- [ ] Any follow-up from the advertiser team addressed
```

---

## References

- [Research Ops Main Doc](https://docs.google.com/document/d/1jzoICKM6iQxlfHam44rkPILhBm9NdS1aZxiBSoCZnCw/edit) — master index of all processes and linked documentation
- [Research Operations Recruiting Playbook](https://docs.google.com/document/d/1qC8Y39YW_DIE6bu8WoNgTh7OUSaKMCcAKIlnWv_gnAM/edit) — wrap-up process and data handling guidance
- [How to Work with ResOps](https://docs.google.com/document/d/1qLF_HZZlr4ICQsIXr4LueqO8JLIzvvZV1Dg_eWmw0_4/edit) — SLAs and researcher expectations at study close

---

## Output format

Always produce in this order:
1. **Standard wrap-up checklist** (all studies)
2. **Format-specific add-ons** (in-person, B2B — only if applicable)
3. **Any flags** (outstanding actions, missing info)
