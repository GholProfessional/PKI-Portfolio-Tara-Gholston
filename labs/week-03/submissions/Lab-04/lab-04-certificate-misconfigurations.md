# Lab 04 — Detect Certificate Misconfigurations
at 1817 on 22mar26

## Overview
Briefly describe what this lab was about in your own words.
What PKI concept were you investigating?

My answer: From the Week 3 Lesson videos, there are four components of Digital Certificates within PKI: 1) Identity. 2) Permissions. 3) Lifecycle. 4) Trust. This Week 3 Lab 4 explained about Identity as well as Certificate Extensions aka Permissions, which is what can the Digital Certificate chain's hierarchy can perform or not perform. So, the PKI concept is Integrity as well as Confidentiality and Availability of the CIA Triad including Non-Repudiation and the AAAs' Authentication. Successful Integrity as well as Confidentiality and Availability furthers the trust that the Company/Enterprise ensures for its End Users/customers' data by protecting with more depth of defense techniques while utilizing reasonable resources.

---

## Scenario 1 — Missing Subject Alternative Name

A certificate contains the following: 
Subject: CN=example.com

However, the certificate does not contain a Subject Alternative Name (SAN) extension.

**Would modern browsers trust this certificate?**
The simple, single SAN for the Digital Certificate, which is the website title itself known as the Common Name/CN, would not be acceptable anymore with modern Web browsers because the web service/website has many functions to it like About Page, Contact Us, etc. as well as its behind-the-scenes/back-end functions such as development and testing environments, which all functions can be accessed by the appropriate End Users and personnel. 

**Analysis:**
My answer: These functions are sub-categories of the website aka Common Name/CN and can be searched on the Internet, this is why SANs/Subject Alternative Names exist. SANs allow you to find and access the website from its variety of categories it is comprised of so you do not always have to type in the exact website to access it. 
And when SANs do not exist for the website, an error that an End User would probably see is NET::ERR_CERT_COMMON_NAME_INVALID (I found this on a Internet search). The error explained the website/web service url doesn't match to what the Digital Certificate has in its CN/Common Name and SAN(s)/Subject Alternative Name(s).       

---

## Scenario 2 — Incorrect Extended Key Usage

A certificate contains the following extension:
Extended Key Usage: Client Authentication

The certificate is being used on a web server for HTTPS.

**Would a browser accept this certificate for a web server?**
My answer: The Digital Certificate would not be acceptable with the extension/permission titled Client Authentication for the web server because it must involve TLS/Encryption.  

**Analysis:**
My answer: EKU/Extended Key Usage defined as displaying the permissions/extensions that each Digital Certificate chain can perform with involving TLS/Encryption. The value required for HTTPS is HTTP (web server/website) + TLS/Encryption.   
And the error that End Users would see is an unsecure/unlocked icon for the web server/website and the website will say "This site can't be reached".  

---

## Scenario 3 — Expired Certificate

The certificate validity period shows: 
Not Before: May 1 2022
Not After:  May 1 2023

The current date is after May 1, 2023.

**What happens if this certificate is used today?**
This expired Digital Certificate would not have its secured/encrypted trust anchor in place since it wasn't renewed before its not after/expiration date. 

**Analysis:**
My answer: The Not After/Expiration date fails validation because the Digital Certificate must be renewed prior to this date to remain validated. Digital Certificate Lifecycle Management matters because supervising and maintaining the project of the Digital Certificate will manage its secure trust validation.
And the error that End Users would see an unsecure/unlocked icon (no TLS/Encryption protection anymore) for the web server/website and (with my Internet search) its Digital Certificate would display as 'expired/invalid'. 

---

## Scenario 4 — Missing Intermediate Certificate

A server presents a certificate during a TLS handshake, but the intermediate certificate is not included in the chain.

Question: What error would a browser likely display?

**What error would a browser likely display?**
My answer: The error of not including the Intermediate Certificate during the TLS Handshake session would cause the Digital Certificate to not be trusted for the web server/website.  

**Analysis:**
[Explain how chains establish trust, why servers must include intermediates, and why browser behavior varies]

My answer: Digital Certificate chain(s) establish trust by having a hierarchy that governs the approved validation; the process of validation is to have a Root CA/Certificate that officially approves the Certificate for trust, which the Root CA is known as the grandparent that everyone trusts, whereas the Intermediate CA represents the "face" of supervising the trust validation for the Leaf Certificate that is given to the web server/website. The Intermediate CAs must be on web servers/websites because it manages the Digital Certificate as being trustworthy or revoked for End Users/public to have knowledge about while interacting/communicating with the website. 
And Web browser behavior varies because each have their own services to provide so several need Digital Certificates to secure End Users/customers data and others may not provide services that need to be protected by TLS Digital Certificates. 

---

## Key Takeaway
In 2-3 sentences, explain why certificate misconfiguration is one of the most common causes of PKI outages.

My answer: Certificate Misconfiguration is one of the most common causes of PKI outages because End Users/employees may not have an accurate PKI Management team to maintain the scheduled and timely validation of the Digital Certificates. Another reason could be that End Users/employees do not have the accurate training of how significant PKI and PKI Encryption is for the Company/Enterprise so it is forgotten until it is expired.  
