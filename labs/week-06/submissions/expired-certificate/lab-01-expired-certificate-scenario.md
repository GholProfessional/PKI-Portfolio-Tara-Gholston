# Lab 01 — Diagnose an Expired Certificate

at 0537 on 20apr26

**File path in your repo:** `labs/week-06/submissions/expired-certificate/lab-01-expired-certificate-scenario.md`

---

## Overview
> What PKI failure type were you diagnosing?

My answer - expired certificate. 

---

## Diagnostic Walkthrough

**Step 1 — Retrieve**
> What was found when the certificate was retrieved?

My answer - expired certificate.


**Step 2 — Parse and Read**
> What did parsing reveal? What specifically failed?

My answer - expired certificate.


**Step 3 — Validate the Chain**
> What did chain validation show? Pass or failure?

My answer - expired certificate. However, the Certificate validation called Online Certificate Status Protocol (OSCP) displayed "good". 


**Step 4 — Revocation and Trust**
> What did revocation and hostname checks show?

My answer - Revocation is none. And Hostname is a match to the SAN which is billing.metrogeneral.hospital.


---

## Question 1 — Step-by-Step Walkthrough
> For each step: what did it reveal, pass or failure, what did it rule out?

My answer - all pass except for the certificate expired.


---

## Question 2 — Root Cause Identification
> What is the single root cause? Why does "OCSP good" NOT contradict the expired cert error? Why do passing chain and hostname checks not resolve the incident?

My answer - expired certificate. 
However, the Certificate validation called Online Certificate Status Protocol (OSCP) displayed "good" since it doesn't provided any information on expired certificates.
Passing Chain and Hostname checks do not resolve because the chain is listing what information exist for the certificate and the hostname explains if it and the SAN(s) match or not. 

---

## Question 3 — Remediation Path
> Specific first action to restore service. Renewal or replacement — justify. What else would you want to know before issuing the replacement?

My answer - since it is an expired certificate it would need to be a renewal. When the expired certificate doesn't have any revoked information then I feel like it would just need to be renewed.
Prior to deciding to perform a certificate replacement, you would need information on the reason for this action such as what is the root cause for needing it replaced like a vulnerability or threat to the certificate.   


---

## Incident Summary

```
INCIDENT SUMMARY

System Affected: Security leaf certificate expired for Metro General Hospital's billing portal server.
Date/Time Detected: Apr 08 23:59:59 2026 GMT.
Date/Time of Actual Failure (cert expiry): expired 6 days prior so Apr 02 2026 23:59:59 GMT.

Failure Type: expired security certificate.

What Failed:

Why It Failed (Root Cause): the personnel did not renew the leaf certificate prior to the expiration date. 

Diagnostic Steps:
    Step 1 — Retrieve:
    Step 2 — Parse:
    Step 3 — Chain:
    Step 4 — Revocation/Trust:

Remediation:

Prevention Going Forward:
```

My answer - have the billing portal's certificate renewal date as a notification. 

---

## Key Findings

- 
- 
- 

---

## Questions or Confusion Points




---
---
