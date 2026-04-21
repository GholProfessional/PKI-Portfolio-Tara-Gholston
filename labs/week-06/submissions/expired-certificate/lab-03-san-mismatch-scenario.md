# Lab 03 — Diagnose a Hostname and SAN Mismatch Scenario

at 2017 on 20apr26

**File path in your repo:** `labs/week-06/submissions/san-mismatch/lab-03-san-mismatch-scenario.md`

---

## Overview
> What PKI failure type were you diagnosing?

My answer - Each Subject's web services are not listed in the SAN so it is causing a failure.


---

## Diagnostic Walkthrough

**Step 1 — Retrieve**




**Step 2 — Parse and Read**




**Step 3 — Validate the Chain**




**Step 4 — Revocation and Trust**




---

## Question 1 — Step-by-Step Walkthrough
> Walk through each step. What did each find? Pass or failure? What did each rule out?

My answer - SAN titled appointments.metrogeneral.hospital is not matching to the subject/hostname titled schedule.metrogeneral.hospital. 

---

## Question 2 — Understanding the SAN Mismatch
> Cert and server are legitimate — why does it fail? Why does a browser show an "attacker" warning when there's no attacker? Why does a valid, unrevoked cert fail on a hostname mismatch?

My answer - the requested web service/server "appointments.metrogeneral.hospital" is not given in the Subject's SAN list so a failure occurs. 


---

## Question 3 — The Web Team's Mistake
> What did they get right and miss? Explain in plain language (non-technical) why DNS update isn't enough. When should the PKI team be involved in a rebrand?

My answer - I don't understand this question.


---

## Question 4 — Can This Be Fixed Without a New Certificate?
> Can you modify a cert's SAN after issuance? What is the only correct remediation? After the new cert, what happens to the old one?

My answer - No, and a new certificate would have to be created to match to the accurate SAN list for the certificate's Subject. And the previous certificate is documented on revocation list and replaced by the new certificate. 


---

## Incident Summary

```
INCIDENT SUMMARY

System Affected:
Date/Time Detected:
Date/Time Change Was Made That Caused Failure:

Failure Type:

What Failed: SAN list doesn't have all of the accurate Subject's web services given.

Why It Failed (Root Cause — the decision that caused it):

Diagnostic Steps:
    Step 1 — Retrieve:
    Step 2 — Parse:
    Step 3 — Chain:
    Step 4 — Revocation/Trust:

Remediation:

Prevention Going Forward:
```

---

## Key Findings

- 
- 
- 

---

## Questions or Confusion Points




---
---
