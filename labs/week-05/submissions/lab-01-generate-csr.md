# Lab — Generate a CSR and Simulate the Issuance Workflow

at 0638 on 05apr26

## Overview
Briefly describe the purpose of this lab in your own words.
What PKI concept or system behavior were you investigating?

????

---

## Steps Performed
Summarize the key steps you performed to complete the lab.

Do **not copy the lab instructions**.
Describe what you actually did.

1. Lab-01 step 2 - What is the key type and size shown in the output? My answer: the private key is hexadecimal type and its size is 2048 bit, 2 primes.

2. Lab-01 step 3 - cannot generate a CSR file. Please see Challenges/Troubleshoot section below.

3. Lab-01 step 4 - not able to inspect the CSR file and provide my answers to what the Certificate Subject's fields of Common Name, Organization, etc. since I cannot generate a CSR file.
   
4. Lab-01 step 5 - cannot self sign the Certificate. Please see Challenges/Troubleshoot section below.

5. Lab-01 step 6 - not able to inspect the Self Sign Certificate file and provide my answers to what is the Certificate's Subject, Issuer, Validity: Not Before and Not After, and Public Key Algorithm as well as RSA Public Key.
   
6. Lab-01 step 7 (Compare CSR to Signed Certificate) - not able to extract the Public Key from the Certificate as well as cannot complete the following two steps of Public Key extracted from Private Key and compare them. Please see Challenges/Troubleshoot section below.


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

My Option B two screenshots on test_csr errors: 
<img width="1366" height="768" alt="Week5Lab1_step3test_csr error" src="https://github.com/user-attachments/assets/7639fab7-885c-4dc7-963c-9d9468a59362" />

<img width="1366" height="768" alt="Week5Lab1_step3test_csr error1" src="https://github.com/user-attachments/assets/a749736a-8a98-4a03-8633-c3cecc4a2587" />



---

## Key Findings
Document the most important observations from the lab.

Examples:

- What you discovered about the certificate, key, or protocol
- How a specific field or extension affected the outcome
- What a validation result indicated
- Any unexpected behavior or results


My answers: See the Challenges and Troubleshooting section below because I cannot figure out to accurately troubleshoot this Week 5 Lab 01 steps from my Windows OS computer and using GitBash. 

---

## Explanation
Explain **why the results matter**.

Examples:

- Why a specific field or extension is required
- Why a validation succeeded or failed
- What the result means in a real-world PKI context
- How this connects to the week's learning outcomes

My answers: ????

---

## Challenges / Troubleshooting
Document any issues encountered during the lab and how you resolved them.

Examples:

- Command errors
- Missing files or dependencies
- Verification failures and how you diagnosed them

## Challenges - 
1) Lab-01 step 3 Generate a CSR/Certificate Signing Request: when I use the step 3 command on GitBash, I cannot generate a CSR file so see the result/output I received is:

Can't open "C:\Program Files\OpenSSL-Win64\bin\openssl.cfg" for reading, No such
 file or directory
004F0000:error:80000002:system library:BIO_new_file:No such file or directory:..
/openssl-3.5.5/crypto/bio/bss_file.c:67:calling fopen(C:\Program Files\OpenSSL-W
in64\bin\openssl.cfg, r)
004F0000:error:10000080:BIO routines:BIO_new_file:no such file:../openssl-3.5.5/
crypto/bio/bss_file.c:75: 


2) Lab-01 step 5 Self sign Certificate: when I use the step 5 command on GitBash, I cannot self sign so see the result/output I received is:

Can't open "labs/week-05/submissions/generate-csr/test_csr.pem" for reading, No
such file or directory
10490000:error:80000002:system library:BIO_new_file:No such file or directory:..
/openssl-3.5.5/crypto/bio/bss_file.c:67:calling fopen(labs/week-05/submissions/g
enerate-csr/test_csr.pem, rb)
10490000:error:10000080:BIO routines:BIO_new_file:no such file:../openssl-3.5.5/
crypto/bio/bss_file.c:75:
error: unable to load certificate request input from file 'labs/week-05/submissi
ons/generate-csr/test_csr.pem'


3) Lab-01 step 7 Compare CSR to Signed Certificate: when I use the step 7's first command out of three commands on GitBash, I cannot extract the Public Key from the Certificate so see the result/output I received is:

Could not open file or uri for loading certificate from labs/week-05/submissions
/generate-csr/test_cert.pem: No such file or directory


## Troubleshooting - 
1) I have searched and found this Internet result (https://stackoverflow.com/questions/70365875/error-during-creation-self-signed-ssl-with-openssl) to troubleshoot but I still receive the same challenge result/output.
   
2) I have found this troubleshooting in my Internet search of "creating Windows Certificate using GitBash" so I will try it now: https://www.bing.com/search?q=create%20Windows%20Certificate%20using%20gitbash%20&qs=n&form=QBRE&sp=-1&lq=0&pq=create%20windows%20certificate%20using%20gitbash%20&sc=12-41&sk=&cvid=DD305DBB49B4431CB5E19D7B1018FBD2 (the article these steps are from: https://www.linkedin.com/pulse/easy-ways-generate-self-signed-ssl-certs-charles-crampton-t4lwe).
   
3) 
---

## Artifacts
List the files generated or submitted during this lab.

Examples:

- Any `.pem`, `.crt`, or `.key` files produced
- Your completed lab write-up `.md` file
- Screenshots stored in `assets/screenshots/`

---

*CVI PKI Career Pathway — Foundations Phase*
