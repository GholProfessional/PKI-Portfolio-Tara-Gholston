# Lab 01 — [Enterprise Certificate Analysis]

at 1943 on 19apr26

## Overview
Briefly describe the purpose of this lab in your own words.
What PKI concept or system behavior were you investigating?

My answer - Investigate a known Enterprise's Digital Certificate life cycle and how is it managed in the Enterprise's infrastructure.

---

## Steps Performed
Summarize the key steps you performed to complete the lab.

Do **not copy the lab instructions**.
Describe what you actually did.

1. Performed Step 1 on GitBash, tried to retrieve the certificate however still not able to see it even though I do observe that the enterprise_cert.pem as well as the full_chain_output appeared in my personal/local folder (Windows). When I opened both with Notepad, I observed a blank page. 

2. 
   
3. 

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

My answer - I am still not able to complete this Week 07 Lab 01 because I still cannot retrieve and view the cert.pem file using GitBash (on Windows device). As an IT Auditor (my current employment), I am able to understand the reason for performing this process for Week 07 Lab 01.  

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

My answer - Performed Step 1 on GitBash, tried to retrieve the certificate however still receive an error message, see below. However, I do observe that the enterprise_cert.pem as well as the full_chain_output file appeared in my personal/local C:/ folder (Windows). When I opened both with Notepad, I observed a blank page. 

GitBash error below: 
"$ openssl x509 -in enterprise_cert.pem -text -noout
Could not find certificate from enterprise_cert.pem"


---

## Artifacts
List the files generated or submitted during this lab.

Examples:

- Any `.pem`, `.crt`, or `.key` files produced
- Your completed lab write-up `.md` file
- Screenshots stored in `assets/screenshots/`

My answer - enterprise_cert.pem, and full_chain_output file.

---

*CVI PKI Career Pathway — Foundations Phase*
