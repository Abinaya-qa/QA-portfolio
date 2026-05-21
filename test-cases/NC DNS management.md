# DNS Settings Management — Test Cases

**Feature:** DNS Settings Management
**URL:** https://www.namecheap.com/myaccount/domains/
**Tested by:** Abinaya
**Test Types:** Positive, Negative, Edge

---

## Format 1 — Detailed (Point-wise)

---

**TC_DNS_001 — Add a Valid A Record**

- **Precondition:** User is logged in and has a domain in their account
- **Steps:**
  1. Go to domain DNS settings
  2. Click Add New Record
  3. Select record type A
  4. Enter a valid hostname e.g. "@"
  5. Enter a valid IP address e.g. "192.168.1.1"
  6. Click Save
- **Expected Result:** A record is saved and appears correctly in the DNS records list
- **Actual Result:** *(to be filled after execution)*
- **Status:** *(Pass / Fail / Blocked)*

---

**TC_DNS_005 — Add a Record with Empty Hostname**

- **Precondition:** User is logged in and has a domain in their account
- **Steps:**
  1. Go to domain DNS settings
  2. Click Add New Record
  3. Select any record type
  4. Leave hostname field empty
  5. Enter a valid value
  6. Click Save
- **Expected Result:** Validation error shown on hostname field — record not saved
- **Actual Result:** *(to be filled after execution)*
- **Status:** *(Pass / Fail / Blocked)*

---

**TC_DNS_010 — Add A Record with Invalid IP Address**

- **Precondition:** User is logged in and has a domain in their account
- **Steps:**
  1. Go to domain DNS settings
  2. Click Add New Record
  3. Select record type A
  4. Enter a valid hostname
  5. Enter invalid IP address e.g. "999.999.999.999"
  6. Click Save
- **Expected Result:** Validation error shown — invalid IP address format, record not saved
- **Actual Result:** *(to be filled after execution)*
- **Status:** *(Pass / Fail / Blocked)*

---

## Format 2 — Tabular (All Test Cases)

---

### Positive Cases

| TC ID | Title | Precondition | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| TC_DNS_001 | Add a valid A record | User logged in with a domain | 1. Go to DNS settings 2. Click Add New Record 3. Select A 4. Enter valid hostname and IP 5. Click Save | A record saved and shown in list | | |
| TC_DNS_002 | Add a valid CNAME record | User logged in with a domain | 1. Go to DNS settings 2. Click Add New Record 3. Select CNAME 4. Enter valid hostname and target 5. Click Save | CNAME record saved and shown in list | | |
| TC_DNS_003 | Add a valid MX record | User logged in with a domain | 1. Go to DNS settings 2. Click Add New Record 3. Select MX 4. Enter valid hostname, mail server and priority 5. Click Save | MX record saved and shown in list | | |
| TC_DNS_004 | Add a valid TXT record | User logged in with a domain | 1. Go to DNS settings 2. Click Add New Record 3. Select TXT 4. Enter @ as hostname 5. Enter valid TXT string 6. Click Save | TXT record saved and shown in list | | |
| TC_DNS_005 | Edit an existing DNS record | User has at least one DNS record | 1. Go to DNS settings 2. Click Edit on existing record 3. Change value to new valid value 4. Click Save | Record updated with new value and shown correctly | | |
| TC_DNS_006 | Delete an existing DNS record | User has at least one DNS record | 1. Go to DNS settings 2. Click Delete on existing record 3. Confirm deletion | Record removed from DNS records list | | |
| TC_DNS_007 | Change to custom nameservers | User has domain using default Namecheap nameservers | 1. Go to DNS settings 2. Select Custom DNS 3. Enter valid nameserver values 4. Click Save | Nameservers updated successfully with confirmation message | | |

---

### Negative Cases

| TC ID | Title | Precondition | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| TC_DNS_008 | Add record with empty hostname | User logged in with a domain | 1. Go to DNS settings 2. Click Add New Record 3. Select any record type 4. Leave hostname empty 5. Enter valid value 6. Click Save | Validation error on hostname field — record not saved | | |
| TC_DNS_009 | Add record with empty value field | User logged in with a domain | 1. Go to DNS settings 2. Click Add New Record 3. Select any record type 4. Enter valid hostname 5. Leave value empty 6. Click Save | Validation error on value field — record not saved | | |
| TC_DNS_010 | Add A record with invalid IP address | User logged in with a domain | 1. Go to DNS settings 2. Click Add New Record 3. Select A 4. Enter valid hostname 5. Enter 999.999.999.999 6. Click Save | Validation error shown — invalid IP address format | | |
| TC_DNS_011 | Change nameservers with invalid value | User logged in with a domain | 1. Go to DNS settings 2. Select Custom DNS 3. Enter "notanameserver" 4. Click Save | Validation error shown — invalid nameserver format | | |

---

### Edge Cases

| TC ID | Title | Precondition | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|
| TC_DNS_012 | Add duplicate DNS record | User already has an A record with hostname @ | 1. Go to DNS settings 2. Click Add New Record 3. Select A 4. Enter same hostname @ and same IP 5. Click Save | Error or warning shown — duplicate record not allowed | | |
| TC_DNS_013 | Add A record with very long hostname | User logged in with a domain | 1. Go to DNS settings 2. Click Add New Record 3. Select A 4. Enter hostname with more than 63 characters 5. Enter valid IP 6. Click Save | Validation error shown — hostname exceeds maximum length | | |
| TC_DNS_014 | Add record with special characters in hostname | User logged in with a domain | 1. Go to DNS settings 2. Click Add New Record 3. Select A 4. Enter hostname with special characters e.g. "host@#$.com" 5. Enter valid IP 6. Click Save | Validation error shown — special characters not allowed in hostname | | |
| TC_DNS_015 | Delete the only remaining DNS record | User has exactly one DNS record | 1. Go to DNS settings 2. Click Delete on the only record 3. Confirm deletion | Record deleted successfully OR warning shown if minimum records required | | |
