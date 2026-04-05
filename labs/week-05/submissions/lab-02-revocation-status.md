# Lab — Check Certificate Revocation Status with OCSP

at 0950 on 05apr26

## Overview
Briefly describe the purpose of this lab in your own words.
What PKI concept or system behavior were you investigating?

My answer: ????

---

## Steps Performed
Summarize the key steps you performed to complete the lab.

Do **not copy the lab instructions**.
Describe what you actually did.

1. Week 5 Lab 02 step 2 - Retrieve the Certificate Chain: What is the Subject (issued to) and what is the Issuer (signed by)?

My answer: Subject issued to GitHub.com, and Issuer signed by Sectigo Limited.   


3. Week 5 Lab 02 step 3 - What does it mean that the Subject and Issuer of issuer_cert.pem are different from the leaf cert?

My answer: The Issuer_cert.pem file is different from the leaf_cert.pem file because it comes from the Certificate fullchain and is the           Intermediate CA whereas the leaf_cert.pem is the Subject's Certificate. 


4. Week 5 Lab 02 step 4 - What is the OCSP responder URL in this certificate?

My answer: http://ocsp.sectigo.com


5. Week 5 Lab 02 step 5 - What is the CRL Distribution Point URL?

My answer: http://crt.sectigo.com/SectigoPublicServerAuthenticationCADVE36.crt


6. Week 5 Lab 02 step 8 - three questions to answer about the OSCP Responder result/output:

My answers: 
- What is the status of the certificate you queried?

The status stated "good".


- What do This Update and Next Update tell you about OCSP response caching?

The current update caching titled This Update is April 2, 2026. And the future update caching titled Next Update is April 9, 2026.


- Why does the query require the issuer certificate in addition to the leaf certificate?

The Issuer Certificate is needed along with the Leaf Certificate in the command for Week 5 Lab 2 step 8 because the result/output will provide any revoked information on the Subject/Leaf Certificate that had been documented by the Issuer/CA. 

7. 

---

## Results
Include the important outputs or findings from the lab.

Examples may include:

- Command outputs
- Certificate fields or values
- Verification results
- Screenshots (if applicable)

If you include screenshots, store them in `assets/screenshots/` at the root of your repo and reference them here.

**How to embed an image:**

**Option A — Terminal / Local Editor**

Save your screenshot to `assets/screenshots/` in your repo, then reference it using a relative path from your submission file:

```markdown
![Description of your screenshot](../../../assets/screenshots/your-filename.png)
```

> The `../../../` moves up three levels: `submissions/` → `week-03/` → `labs/` → repo root, then into `assets/screenshots/`.

**Option B — GitHub Web (Easiest)**

Open your `.md` file on GitHub, click the pencil icon to edit, then **drag and drop your image directly into the text editor**. GitHub will upload it automatically and insert the correct link for you.

Example of what an embedded image looks like:

```markdown
![Certificate output showing SAN field](../../../assets/screenshots/san-field.png)
```

---

## Key Findings
Document the most important observations from the lab.

Examples:

- What you discovered about the certificate, key, or protocol
- How a specific field or extension affected the outcome
- What a validation result indicated
- Any unexpected behavior or results

-
-
-

---

## Explanation
Explain **why the results matter**.

Examples:

- Why a specific field or extension is required
- Why a validation succeeded or failed
- What the result means in a real-world PKI context
- How this connects to the week's learning outcomes

---

## Challenges / Troubleshooting
Document any issues encountered during the lab and how you resolved them.

Examples:

- Command errors
- Missing files or dependencies
- Verification failures and how you diagnosed them

---

## Artifacts
List the files generated or submitted during this lab.

Examples:

- Any `.pem`, `.crt`, or `.key` files produced
- Your completed lab write-up `.md` file
- Screenshots stored in `assets/screenshots/`

---

*CVI PKI Career Pathway — Foundations Phase*
