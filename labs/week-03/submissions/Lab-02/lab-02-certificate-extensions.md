# Lab 02 — Investigate Certificate Extensions
at 1244 on 21mar26

## Overview
Briefly describe what this lab was about in your own words.
What PKI concept were you investigating?

My answer: From the Week 3 Lesson videos, there are four components of Digital Certificates within PKI: 1) Identity. 2) Permissions. 3) Lifecycle. 4) Trust. This Week 3 Lab 2 explained Certificate Extensions aka Permissions, which is what can the Digital Certificate perform or not perform. So, the PKI concept is Confidentiality and Availability of the CIA Triad including Non-Repudiation and the AAAs' Authentication. Successful Confidentiality and Availability furthers the trust that the Company/Enterprise ensures for its End Users/customers' data by protecting with more depth of defense techniques while utilizing reasonable resources. 

---

## Environment
- OS:
- Terminal used (Mac Terminal / Git Bash / WSL):
- OpenSSL version (`openssl version`):

I'm using Powershell.

---

## Extensions Found

### Subject Alternative Name (SAN)
Paste the value from your output:
My Powershell output:
DNS:isaca.org, DNS:*.brqa.isaca.org, DNS:*.dev.isaca.org, DNS:*.develop.nexus.isaca.org, DNS:*.isaca.org, DNS:*.nexus.isaca.org, DNS:*.prod.isaca.org, DNS:*.qa.isaca.org, DNS:*.sit.isaca.org, DNS:*.stage.isaca.org, DNS:*.stage.nexus.isaca.org, DNS:*.test.isaca.org, DNS:*.uat.isaca.org

### Key Usage
Paste the value from your output:
My Powershell output:
critical
Digital Signature

### Extended Key Usage (EKU)
Paste the value from your output:
My Powershell output:
TLS Web Server Authentication

### Basic Constraints
Paste the value from your output:
My Powershell output:
critical
CA:FALSE

---

## Observations

1. What domains appear in the SAN field?
My answer: There is the website itself (isaca.org) as well as the project management of the website and its NEXUS content management system including development and testing environments.  

2. What operations are permitted by Key Usage?
My answer: The Digital Certificate of isaca.org can provide critical Digital Signature(s). 

3. What applications are authorized by EKU?
My answer: The Digital Certificate of isaca.org can provide TLS (Encryption) of Web Server/website Authentication. 

4. Can this certificate issue other certificates? How do you know?
My answer: No, the Digital Certificate of isaca.org cannot issue other certificates, because the Digital Certificate's extension/permission titled Basic Constraints gave a result that the CA/Certificate Authority is false.  

5. Why are these extensions important for TLS validation?
My answer: The extensions/permissions are important for TLS (Encryption) validation because it verifies what can the Digital Certificate actually perform or not.  
