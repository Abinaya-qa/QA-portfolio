# Bug Report — BUG-002

**Bug ID:** BUG-002

**Title:** No confirmation message shown after saving DNS record

**Reported by:** Abinaya

**Date:** May 2026

**Status:** New

**Severity:** Minor

**Priority:** Medium

---

## Environment
- **URL:** https://www.namecheap.com/myaccount/domains/
- **Browser:** Chrome
- **OS:** Windows

---

## Steps to Reproduce
1. Log in to Namecheap account
2. Go to domain DNS settings
3. Click Add New Record
4. Fill in all required fields with valid values
5. Click Save

---

## Expected Result
A clear confirmation message should appear after saving —
for example "DNS record saved successfully" — so the user
knows their changes were applied.

---

## Actual Result
No confirmation message is displayed after clicking Save.
The record appears in the list but the user receives no
visual confirmation that the save was successful.

---

## Impact
- User is unsure whether their DNS record was saved
- May click Save multiple times creating duplicate records
- Creates anxiety for users making critical DNS changes
- Increases support tickets from users asking if their
  changes were applied

---

## Recommendation
Display a clear success message immediately after saving
a DNS record — for example a green banner saying
"DNS record saved successfully."
