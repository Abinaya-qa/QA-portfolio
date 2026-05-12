# Test Cases — Namecheap Login Page

## Page details
- **URL:** https://www.namecheap.com/myaccount/login/
- **Tested by:** Abinaya
- **Date:** May 2026

---

## TC-01: Login with valid email and correct password

| Field | Details |
|---|---|
| Precondition | User has a registered Namecheap account |
| Steps | 1. Go to login page 2. Enter valid email 3. Enter correct password 4. Click Login |
| Expected result | User is redirected to account dashboard |
| Actual result | |
| Status | |

---

## TC-02: Login with valid email but wrong password

| Field | Details |
|---|---|
| Precondition | User has a registered account |
| Steps | 1. Go to login page 2. Enter valid email 3. Enter incorrect password 4. Click Login |
| Expected result | Error message shown, user stays on login page |
| Actual result | |
| Status | |

---

## TC-03: Login with empty email field

| Field | Details |
|---|---|
| Precondition | None |
| Steps | 1. Go to login page 2. Leave email empty 3. Enter any password 4. Click Login |
| Expected result | Validation error shown on email field, form not submitted |
| Actual result | |
| Status | |

---

## TC-04: Login with empty password field

| Field | Details |
|---|---|
| Precondition | None |
| Steps | 1. Go to login page 2. Enter valid email 3. Leave password empty 4. Click Login |
| Expected result | Validation error shown on password field, form not submitted |
| Actual result | |
| Status | |

---

## TC-05: Login with both fields empty

| Field | Details |
|---|---|
| Precondition | None |
| Steps | 1. Go to login page 2. Leave both fields empty 3. Click Login |
| Expected result | Validation errors shown on both fields |
| Actual result | |
| Status | |

---

## TC-06: Login with invalid email format

| Field | Details |
|---|---|
| Precondition | None |
| Steps | 1. Go to login page 2. Enter "usernamegmail.com" in email field 3. Enter any password 4. Click Login |
| Expected result | Email format validation error shown |
| Actual result | |
| Status | |

---

## TC-07: Login with unregistered email address

| Field | Details |
|---|---|
| Precondition | Email is not registered on Namecheap |
| Steps | 1. Go to login page 2. Enter unregistered email 3. Enter any password 4. Click Login |
| Expected result | Error message shown — account not found |
| Actual result | |
| Status | |

---

## TC-08: Login after 5 consecutive failed attempts

| Field | Details |
|---|---|
| Precondition | User has a registered account |
| Steps | 1. Attempt login with wrong password 5 times in a row 2. Attempt login with correct credentials |
| Expected result | Account locked or CAPTCHA triggered |
| Actual result | |
| Status | |

---

## TC-09: Login with password pasted from clipboard

| Field | Details |
|---|---|
| Precondition | User has a registered account |
| Steps | 1. Copy correct password to clipboard 2. Go to login page 3. Paste password into field 4. Click Login |
| Expected result | Login succeeds — pasting works the same as typing |
| Actual result | |
| Status | |

---

## TC-10: Login with password in wrong case

| Field | Details |
|---|---|
| Precondition | User has a registered account |
| Steps | 1. Go to login page 2. Enter correct email 3. Enter password with caps lock on 4. Click Login |
| Expected result | Login fails — passwords are case sensitive |
| Actual result | |
| Status | |

---

## TC-11: Click Forgot password link

| Field | Details |
|---|---|
| Precondition | None |
| Steps | 1. Go to login page 2. Click Forgot password link |
| Expected result | User is taken to password reset page |
| Actual result | |
| Status | |

---

## TC-12: Login with email containing leading or trailing spaces

| Field | Details |
|---|---|
| Precondition | User has a registered account |
| Steps | 1. Go to login page 2. Enter valid email with a space before or after it 3. Enter correct password 4. Click Login |
| Expected result | System trims spaces and logs in successfully or shows a clear error |
| Actual result | |
| Status | |
