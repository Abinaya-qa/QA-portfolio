
# Spaceship Domain Search — Test Cases

**Feature:** Domain Search
**URL:** https://www.spaceship.com/domains/
**Prepared by:** QA Portfolio
**Test Types:** Positive, Negative, Edge

---

## Format 1 — Detailed (Point-wise)
> This format is used when documenting a single test case in detail.

---

**TC_SP_001 — Search for an Available Domain**

- **Precondition:** User is on Spaceship homepage or domain search page
- **Steps:**
  1. Go to https://www.spaceship.com
  2. Type an available domain name e.g. "testdomain99887.com"
  3. Click Search
- **Expected Result:** Domain is shown as "Available" with a price and an "Add to Cart" button
- **Actual Result:** *(to be filled after execution)*
- **Status:** *(Pass / Fail / Blocked)*

---

**TC_SP_004 — Search for a Taken Domain**

- **Precondition:** User is on Spaceship homepage or domain search page
- **Steps:**
  1. Go to https://www.spaceship.com
  2. Type a well-known taken domain e.g. "google.com"
  3. Click Search
- **Expected Result:** Domain shown as "Unavailable". Alternative domain suggestions are displayed.
- **Actual Result:** *(to be filled after execution)*
- **Status:** *(Pass / Fail / Blocked)*

---

**TC_SP_007 — Search with Empty Input**

- **Precondition:** None
- **Steps:**
  1. Go to https://www.spaceship.com
  2. Leave the search field empty
  3. Click Search
- **Expected Result:** Validation error is shown. Search is not executed.
- **Actual Result:** *(to be filled after execution)*
- **Status:** *(Pass / Fail / Blocked)*

---

## Format 2 — Tabular (All Test Cases)
> This format is used in test management tools like Jira, TestRail, or Excel to manage multiple test cases together.

---

### Positive Cases

| TC ID | Title | Precondition | Steps | Expected Result | Actual Result | Status |
|-------|-------|--------------|-------|-----------------|---------------|--------|
| TC_SP_001 | Search for an available domain | User is on search page | 1. Go to spaceship.com 2. Enter an available domain name 3. Click Search | Domain shown as "Available" with price and Add to Cart button | | |
| TC_SP_002 | Available domain can be added to cart | User is on search results page | 1. Search for an available domain 2. Click "Add to Cart" | Domain added to cart successfully | | |
| TC_SP_003 | Alternative TLDs shown in results | User is on search results page | 1. Search for any domain name 2. Check results below main result | Alternative TLDs like .net .org .io .co shown with prices | | |

---

### Negative Cases

| TC ID | Title | Precondition | Steps | Expected Result | Actual Result | Status |
|-------|-------|--------------|-------|-----------------|---------------|--------|
| TC_SP_004 | Search for a taken domain | User is on search page | 1. Go to spaceship.com 2. Enter "google.com" 3. Click Search | Domain shown as "Unavailable". Alternative suggestions displayed. | | |
| TC_SP_005 | Search with empty input | None | 1. Go to spaceship.com 2. Leave search field empty 3. Click Search | Validation error shown, search not executed | | |
| TC_SP_006 | Search with only spaces | None | 1. Go to spaceship.com 2. Enter only spaces in search field 3. Click Search | Validation error shown OR no results found message displayed | | |

---

### Edge Cases

| TC ID | Title | Precondition | Steps | Expected Result | Actual Result | Status |
|-------|-------|--------------|-------|-----------------|---------------|--------|
| TC_SP_007 | Search with special characters | None | 1. Go to spaceship.com 2. Enter "test@domain!.com" 3. Click Search | Error shown or invalid input message. Search handled gracefully. | | |
| TC_SP_008 | Search with very long domain name | None | 1. Go to spaceship.com 2. Enter a domain name with 63+ characters 3. Click Search | System handles it gracefully — error shown or result returned | | |
| TC_SP_009 | Search with numeric only domain | None | 1. Go to spaceship.com 2. Enter "1234567.com" 3. Click Search | Results shown correctly — available or unavailable | | |
| TC_SP_010 | Search with hyphen in domain name | None | 1. Go to spaceship.com 2. Enter "my-domain.com" 3. Click Search | Results shown correctly — hyphens are valid in domain names | | |
| TC_SP_011 | Search returns multiple TLD options | None | 1. Go to spaceship.com 2. Search for any domain 3. Check results page | Multiple TLD options shown e.g. .com .net .org .io .co | | |
| TC_SP_012 | Search with uppercase letters | None | 1. Go to spaceship.com 2. Enter "GOOGLE.COM" in uppercase 3. Click Search | System converts to lowercase and returns correct results | | |
| TC_SP_013 | Search result shows correct pricing | None | 1. Go to spaceship.com 2. Search for an available domain 3. Check price displayed | Price shown matches the price on Spaceship pricing page | | |
