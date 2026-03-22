# Lab 03 — Verify a Certificate Chain
at 1631 on 22mar26

## Overview
Briefly describe what this lab was about in your own words.
What PKI concept were you investigating?

My answer: My answer: From the Week 3 Lesson videos, there are four components of Digital Certificates within PKI: 1) Identity. 2) Permissions. 3) Lifecycle. 4) Trust. This Week 3 Lab 3 explained about Certificate Extensions aka Permissions, which is what can the Digital Certificate chain's hierarchy can perform or not perform. So, the PKI concept is Confidentiality and Availability of the CIA Triad including Non-Repudiation and the AAAs' Authentication. Successful Confidentiality and Availability furthers the trust that the Company/Enterprise ensures for its End Users/customers' data by protecting with more depth of defense techniques while utilizing reasonable resources.

---

## Environment
- OS:
- Terminal used (Mac Terminal / Git Bash / WSL):
- OpenSSL version (`openssl version`):
- Website used: github.com

I'm using Powershell. 

---

## Chain Verification Result
Paste the output of your `openssl verify` command:
My Powershell result:
PS C:\Users\tghol\labs\Week-03\Submissions> Invoke-WebRequest -Uri "https://curl.se/ca/cacert.pem" -OutFile cacert.pem
PS C:\Users\tghol\labs\Week-03\Submissions> openssl verify -CAfile cacert.pem -untrusted intermediate.pem server.pem
server.pem: OK

---

## Certificate Roles

| Certificate | Subject | Issuer | CA:TRUE/FALSE |
|---|---|---|---|
| server.pem       | Subject| N/A                | CA: FALSE|
| intermediate.pem | N/A    | Issuer CA          | CA: TRUE |
| root.pem         | N/A    | Approval CA        | CA: TRUE |

---

## Observations

1. Which certificate is the root CA?
My answer: The Powershell result of the isaca.org Certificate Chain listed the Root Certificate third, which I saved the begin and end certificate block of information for it as Root.pem.


2. Which is the intermediate CA?
My answer: The Powershell result of the isaca.org Certificate Chain listed the Intermediate Certificate second, which I saved the begin and end certificate block of information for it as Intermediate.pem.


3. Which is the leaf certificate?
My answer: The Powershell result of the isaca.org Certificate Chain listed the Leaf Certificate first, which I saved the begin and end certificate block of information for it as Server.pem.


4. How does the Issuer field connect the chain?
My answer: The Issuer field connects the Digital Certificate chain because it is the approval Root CA/Certificate Authority that gives official authorization to the subject/web service Leaf Certificate, which ensures it is trustworthy as a web service to End Users/public.  


5. Why do intermediate certificates exist?
My answer: Intermediate Certificate(s) exist because it is the Agent representing as the visible CA/Certificate Authority between the approval Root CA and the subject/web service Leaf CA to ensure the maintenance of the Digital Certificate chain's trust anchor. 

