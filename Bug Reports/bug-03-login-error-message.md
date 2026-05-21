# Bug Report — BUG-003

**Bug ID:** BUG-003
**Title:** Login page shows generic error message for wrong password
**Reported by:** Abinaya
**Date:** May 2026
**Status:** New
**Severity:** Minor
**Priority:** Medium

---

## Environment
- **URL:** https://www.namecheap.com/myaccount/login/
- **Browser:** Chrome
- **OS:** Windows

---

## Steps to Reproduce
1. Go to Namecheap login page
2. Enter a valid registered email address
3. Enter an incorrect password
4. Click Login

---

## Expected Result
A clear error message should be displayed telling the user
their password is incorrect — for example:
"Incorrect password. Please try again or reset your password."

---

## Actual Result
A generic error message is displayed that does not clearly
tell the user whether the email or password is wrong.
The user does not know which field to correct.

---

## Impact
- User is confused about which field is incorrect
- May lead to multiple failed login attempts
- Poor user experience on a critical page

---

## Recommendation
Display a specific error message that clearly tells the user
their password is incorrect and provides a link to reset it.
