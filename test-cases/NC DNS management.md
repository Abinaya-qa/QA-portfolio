# Test Cases — Namecheap DNS Settings Management

## Page details
- **URL:** https://www.namecheap.com/myaccount/domains/
- **Prepared by:** Abinaya
  
---

## TC-01: Add a valid A record

| Field | Details |
|---|---|
| Precondition | User is logged in and has a domain in their account |
| Steps | 1. Go to domain DNS settings 2. Click Add New Record 3. Select record type A 4. Enter a valid hostname 5. Enter a valid IP address 6. Click Save |
| Expected result | A record is saved and appears in the DNS records list |
| Actual result | |
| Status | |

---

## TC-02: Add a valid CNAME record

| Field | Details |
|---|---|
| Precondition | User is logged in and has a domain in their account |
| Steps | 1. Go to domain DNS settings 2. Click Add New Record 3. Select record type CNAME 4. Enter a valid hostname 5. Enter a valid target domain 6. Click Save |
| Expected result | CNAME record is saved and appears in the DNS records list |
| Actual result | |
| Status | |

---

## TC-03: Add a valid MX record

| Field | Details |
|---|---|
| Precondition | User is logged in and has a domain in their account |
| Steps | 1. Go to domain DNS settings 2. Click Add New Record 3. Select record type MX 4. Enter a valid hostname 5. Enter a valid mail server address 6. Enter priority value 7. Click Save |
| Expected result | MX record is saved and appears in the DNS records list |
| Actual result | |
| Status | |

---

## TC-04: Add a record with empty hostname field

| Field | Details |
|---|---|
| Precondition | User is logged in and has a domain in their account |
| Steps | 1. Go to domain DNS settings 2. Click Add New Record 3. Select any record type 4. Leave hostname field empty 5. Enter a valid value 6. Click Save |
| Expected result | Validation error shown on hostname field — record not saved |
| Actual result | |
| Status | |

---

## TC-05: Add a record with empty value field

| Field | Details |
|---|---|
| Precondition | User is logged in and has a domain in their account |
| Steps | 1. Go to domain DNS settings 2. Click Add New Record 3. Select any record type 4. Enter a valid hostname 5. Leave value field empty 6. Click Save |
| Expected result | Validation error shown on value field — record not saved |
| Actual result | |
| Status | |

---

## TC-06: Add a duplicate DNS record

| Field | Details |
|---|---|
| Precondition | User already has an A record with hostname @ pointing to an IP address |
| Steps | 1. Go to domain DNS settings 2. Click Add New Record 3. Select record type A 4. Enter the same hostname @ 5. Enter the same IP address 6. Click Save |
| Expected result | Error message shown — duplicate record not allowed or warning displayed |
| Actual result | |
| Status | |

---

## TC-07: Edit an existing DNS record

| Field | Details |
|---|---|
| Precondition | User has at least one DNS record in their account |
| Steps | 1. Go to domain DNS settings 2. Click Edit on an existing record 3. Change the IP address or value to a new valid value 4. Click Save |
| Expected result | Record is updated with the new value and shown correctly in the list |
| Actual result | |
| Status | |

---

## TC-08: Delete an existing DNS record

| Field | Details |
|---|---|
| Precondition | User has at least one DNS record in their account |
| Steps | 1. Go to domain DNS settings 2. Click Delete on an existing record 3. Confirm the deletion |
| Expected result | Record is removed from the DNS records list |
| Actual result | |
| Status | |

---

## TC-09: Add a TXT record for domain verification

| Field | Details |
|---|---|
| Precondition | User is logged in and has a domain in their account |
| Steps | 1. Go to domain DNS settings 2. Click Add New Record 3. Select record type TXT 4. Enter @ as hostname 5. Enter a valid TXT string 6. Click Save |
| Expected result | TXT record is saved and appears in the DNS records list |
| Actual result | |
| Status | |

---

## TC-10: Add an A record with an invalid IP address

| Field | Details |
|---|---|
| Precondition | User is logged in and has a domain in their account |
| Steps | 1. Go to domain DNS settings 2. Click Add New Record 3. Select record type A 4. Enter a valid hostname 5. Enter an invalid IP address like 999.999.999.999 6. Click Save |
| Expected result | Validation error shown — invalid IP address format |
| Actual result | |
| Status | |

---

## TC-11: Change nameservers to custom nameservers

| Field | Details |
|---|---|
| Precondition | User is logged in and has a domain using Namecheap default nameservers |
| Steps | 1. Go to domain DNS settings 2. Select Custom DNS option 3. Enter valid custom nameserver values 4. Click Save |
| Expected result | Nameservers updated successfully — confirmation message shown |
| Actual result | |
| Status | |

---

## TC-12: Change nameservers with invalid nameserver value

| Field | Details |
|---|---|
| Precondition | User is logged in and has a domain in their account |
| Steps | 1. Go to domain DNS settings 2. Select Custom DNS option 3. Enter an invalid nameserver value like "notanameserver" 4. Click Save |
| Expected result | Validation error shown — invalid nameserver format |
| Actual result | |
| Status | |
