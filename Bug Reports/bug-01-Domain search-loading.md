
# Bug Report — BUG-001

**Bug ID:** BUG-001

**Title:** No loading indicator shown during domain search

**Reported by:** Abinaya

**Date:** May 2026

**Status:** New

**Severity:** Minor

**Priority:** Low

---

## Environment
- **URL:** https://www.namecheap.com
- **Browser:** Chrome
- **OS:** Windows

---

## Steps to Reproduce
1. Go to https://www.namecheap.com
2. Type any domain name in the search box
3. Click Search
4. Observe the page while results are loading

---

## Expected Result
A loading indicator such as a spinner or progress bar should
be displayed while the search results are being fetched.
This tells the user the system is working and they should wait.

---

## Actual Result
No loading indicator is shown after clicking Search.
The page appears static while results are loading which
makes the user think nothing happened or the search failed.

---

## Impact
- User thinks the search did not work and clicks Search again
- Creates confusion and poor user experience
- May lead to duplicate search requests being sent

---

## Recommendation
Add a loading spinner or progress indicator that appears
immediately after the user clicks Search and disappears
when results are displayed.
