# Namecheap Login Page — Test Cases

**Feature:** Login Page  
**URL:** https://www.namecheap.com/myaccount/login/  
**Prepared by:** Abinaya  
**Test Types:** Positive, Negative, Edge  

---

## Format 1 — Detailed (Point-wise)
> This format is used when documenting a single test case in detail.

---

**TC_001 — Valid Login with Correct Credentials**

- **Precondition:** User has a registered Namecheap account
- **Steps:**
  1. Go to https://www.namecheap.com/myaccount/login/
  2. Enter registered email or username
  3. Enter correct password
  4. Click Sign In
- **Expected Result:** User is redirected to the account dashboard
- **Actual Result:** User is redirected to the account dashboard
- **Status:** Pass

---

**TC_004 — Login with Wrong Password**

- **Precondition:** User has a registered Namecheap account
- **Steps:**
  1. Go to login page
  2. Enter valid registered email
  3. Enter an incorrect password
  4. Click Sign In
- **Expected Result:** Error message is displayed — "Incorrect username or password". User is not logged in.
- **Actual Result:** The password does not match the user account or the account does not exist. Please verify both the user name and password and try again.
- **Status:** Pass

---

**TC_008 — Account Locked After Multiple Failed Attempts**

- **Precondition:** User has a registered Namecheap account
- **Steps:**
  1. Go to login page
  2. Enter valid registered email
  3. Enter wrong password
  4. Repeat step 3 five times in a row
- **Expected Result:** Account is temporarily locked. A lockout message is displayed.
- **Actual Result:** Your account has been locked for 24 hours for three consecutive failed password or username entry attempts. Please use Password Reset option. Once the password is reset your account will be unlocked automatically.
- **Status:** Pass
---

## Format 2 — Tabular (All Test Cases)
> This format is used in test management tools like Jira, TestRail, or Excel to manage multiple test cases together.

---

### Positive Cases

| TC ID | Title | Precondition | Steps | Expected Result | Actual Result | Status |
|-------|-------|--------------|-------|-----------------|---------------|--------|
| TC_001 | Valid login with correct credentials | Registered account exists | 1. Go to login page 2. Enter valid email 3. Enter correct password 4. Click Sign In | User redirected to dashboard | | |
| TC_002 | Login using username instead of email | Account with username exists | 1. Go to login page 2. Enter username 3. Enter correct password 4. Click Sign In | Login succeeds, user lands on dashboard | | |
| TC_003 | Successful redirect after login | Registered account exists | 1. Access a page requiring login 2. Enter valid credentials 3. Click Sign In | User taken back to originally requested page | | |

---

### Negative Cases

| TC ID | Title | Precondition | Steps | Expected Result | Actual Result | Status |
|-------|-------|--------------|-------|-----------------|---------------|--------|
| TC_004 | Login with wrong password | Registered account exists | 1. Go to login page 2. Enter valid email 3. Enter wrong password 4. Click Sign In | Error shown: "Incorrect username or password" | | |
| TC_005 | Login with unregistered email | Email not registered | 1. Go to login page 2. Enter unregistered email 3. Enter any password 4. Click Sign In | Error shown, login blocked | | |
| TC_006 | Submit with empty email field | None | 1. Go to login page 2. Leave email blank 3. Enter any password 4. Click Sign In | Validation error shown, form not submitted | | |
| TC_007 | Submit with empty password field | None | 1. Go to login page 2. Enter valid email 3. Leave password blank 4. Click Sign In | Validation error shown, form not submitted | | |
| TC_008 | Account locked after multiple failed attempts | Registered account exists | 1. Go to login page 2. Enter valid email 3. Enter wrong password 5 times | Account temporarily locked, lockout message shown | | |

---

### Edge Cases

| TC ID | Title | Precondition | Steps | Expected Result | Actual Result | Status |
|-------|-------|--------------|-------|-----------------|---------------|--------|
| TC_009 | Password is case-sensitive | Registered account exists | 1. Go to login page 2. Enter valid email 3. Enter password in wrong case 4. Click Sign In | Login fails — password must match exact case | | |
| TC_010 | Email with leading/trailing spaces | Registered account exists | 1. Go to login page 2. Enter email with spaces e.g. " user@test.com " 3. Enter correct password 4. Click Sign In | System trims spaces and login succeeds OR shows clear error | | |
| TC_011 | Forgot password link works | None | 1. Go to login page 2. Click "Forgot Password" | User redirected to password reset page | | |
| TC_012 | Show/hide password toggle works | None | 1. Go to login page 2. Type in password field 3. Click eye icon to show 4. Click again to hide | Password toggles correctly between visible and hidden | | |
