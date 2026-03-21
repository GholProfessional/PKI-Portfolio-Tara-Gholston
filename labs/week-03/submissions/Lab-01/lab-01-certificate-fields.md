# Lab 01 — Inspect X.509 Certificate Fields
at 1034 on 21mar26

## Overview
Briefly describe what this lab was about in your own words.
What PKI concept were you investigating?

My answer: From the Week 3 Lesson videos, there are four components of Digital Certificates within PKI: 1) Identity. 2) Permissions. 3) Lifecycle. 4) Trust. This Week 3 Lab 1 explained about identity so the PKI concept is Integrity of the CIA Triad including Non-Repudiation and the AAAs' Authentication. Successful Integrity furthers the trust that the Company/Enterprise ensures for its End Users/customers' data. 

---

## Environment
- OS:
- Terminal used (Mac Terminal / Git Bash / WSL):
- OpenSSL version (`openssl version`):

I'm using Powershell. 

---

## Certificate Fields

Used again the website isaca.org.

| Field                | Value from your output |
|----------------------|------------------------|
| Version              |       3 (0x2)          |
| Serial Number        |    MAC Address         |
| Signature Algorithm  |    ecdsa-with-SHA256   |
| Issuer               |  Google Trust Services |
| Subject              |       isaca.org        |
| Not Before           |Mar 18 01:41:10 2026 GMT|
| Not After            |Jun 16 02:41:01 2026 GMT|
| Public Key Algorithm |     id-ecPublicKey     |

---

## Observations

1. Who issued the certificate?
My answer: Google Trust Services.

2. What domain or organization does it represent?
My answer: Google.

3. When does it expire?
My answer: June 16, 2026 at 0200/2am.   

4. What public key algorithm is used?
My answer: I believe "..ec.." represents ECC/Elliptic Curve Cryptography.

5. Why does the Issuer field matter in a PKI system?
My answer: The Issuer field is important in a PKI system because it explains the trust chain hierarchy. The Company/Enterprise, which is the Subject, will need to be granted approval by the Issuer (I believe this is the CA/(Root) Certificate Authority or Intermediate CA) to have access and permissions to use other web services securely via Digital Certificates.
