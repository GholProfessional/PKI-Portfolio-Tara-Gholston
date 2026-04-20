# Lab 02 — Diagnose a Broken Certificate Chain Scenario

at 1847 on 20apr26

**File path in your repo:** `labs/week-06/submissions/broken-chain/lab-02-broken-chain-scenario.md`

---

## Overview
> What PKI failure type were you diagnosing?

My answer - lack of certificate chain trust.


---

## Diagnostic Walkthrough

**Step 1 — Retrieve**




**Step 2 — Parse and Read**




**Step 3 — Validate the Chain**




**Step 4 — Revocation and Trust**




---

## Question 1 — Step-by-Step Walkthrough
> Walk through each step. What did each reveal? Pass or failure? What did each step rule out?

My answer - Intermediate CA isn't recognized in the TLS handshake. 

---

## Question 2 — Understanding the Chain Failure
> Leaf is valid, root is trusted — why does it still fail? Why is trusted root not enough without the intermediate? Why don't clients just fetch the intermediate from the CA Issuers URI automatically?

My answer - Intermediate CA is missing in the certificate chain so this is the failure. The Intermediate certificate is the approver of the Leaf certificate. And the Intermediate certificate would need to be approved by the Root CA to a part of the trust in the certificate chain.  


---

## Question 3 — Why This Happens
> What specific installation mistake caused this? Why might it appear for some clients but not others? Is it immediate or gradual?

My answer - The server configuration including the certificate chain is where the mistake exist. This mistake may be viewed immediately by certain Operating Systems like Linux and Macintosh/MAC but Windows wouldn't display. 


---

## Question 4 — Remediation
> What must be added to the server config (describe the correct bundle)? Renewal or replacement? What would you verify after the fix?

My answer - I don't understand what is meant by correct bundle because I have been having issues with each Week labs and trying to troubleshoot so I am missing this knowledge. I would say to replace the certificate since the Intermediate CA is not working. And I don't understand about what to verify after the fix. 


---

## Incident Summary

```
INCIDENT SUMMARY

System Affected: Certificate chain.
Date/Time Detected:
Date/Time of Failure (approximate install date):

Failure Type: Certificate chain broken.

What Failed:Intermediate CA.

Why It Failed (Root Cause): 

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


