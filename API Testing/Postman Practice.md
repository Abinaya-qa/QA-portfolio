# API Testing Notes — Postman Practice

**Tool:** Postman
**Tested by:** Abinaya


---

## What is an API

An API is a way for two systems to talk to each other.
When a customer searches for a domain on Namecheap, the
website sends a request to the server through an API and
gets back the results.

As a QA engineer I test the API directly using Postman
without going through the website. This helps me find
whether a bug is in the frontend or the backend.

---

## HTTP Methods

| Method | What it does | Namecheap example |
|---|---|---|
| GET | Fetch existing data | Get list of domains in an account |
| POST | Create something new | Register a new domain |
| PUT | Update existing data | Change nameserver settings |
| DELETE | Remove something | Delete a host record |

---

## Status Codes I Experienced

| Code | Meaning | How I saw it |
|---|---|---|
| 201 Created | Something was created successfully | POST request to create a user worked |
| 400 Bad Request | Data sent was wrong or malformed | Sent POST without comma between JSON properties |
| 401 Unauthorized | No valid API key provided | Sent GET request without API key in header |
| 404 Not Found | Resource does not exist | Sent GET request to a wrong URL |

---

## Requests I Practiced

---

**Request 1 — GET request**

- **Method:** GET
- **URL:** https://reqres.in/api/users/2
- **Status received:** 401 Unauthorized
- **Why:** API key was missing in the request header
- **What I learned:** GET requests fetch data from the
  server. A 401 means authentication is missing — this
  is the same error customers get in Namecheap when
  their API key is wrong or missing.

---

**Request 2 — POST request**

- **Method:** POST
- **URL:** https://reqres.in/api/users
- **Body sent:**
```json
{
  "name": "Abinaya",
  "job": "QA Testing"
}
```
- **Status received:** 201 Created
- **What I learned:** POST requests send data to create
  something new. The body contains the data in JSON
  format. Status 201 means it was created successfully.
  JSON requires a comma after every property except
  the last one.

---

**Request 3 — Wrong URL**

- **Method:** GET
- **URL:** https://reqres.in/api/users/999
- **Status received:** 404 Not Found
- **What I learned:** 404 means the resource does not
  exist on the server. Useful in QA to verify that
  invalid endpoints are handled correctly.

---

**Request 4 — Invalid JSON — 400 error**

- **Method:** POST
- **URL:** https://reqres.in/api/users
- **Status received:** 400 Bad Request
- **What happened:** Sent POST request without a comma
  after the first JSON property. Server could not
  parse the JSON body.
- **How I fixed it:** Added the missing comma after
  "name": "Abinaya" and sent again — got 201 Created.
- **What I learned:** JSON requires a comma after every
  property except the last one. Missing commas cause
  400 errors. Reading the error message carefully
  revealed the root cause — the same investigative
  approach I use every day in customer support.

---

## My Collection in Postman

All requests were saved in My Collection in Postman
with clear names:

- GET - Fetch User by ID
- GET - 401 Unauthorized Example
- GET - 404 Not Found Example
- POST - Create New User
- POST - 400 Bad Request Example

---

