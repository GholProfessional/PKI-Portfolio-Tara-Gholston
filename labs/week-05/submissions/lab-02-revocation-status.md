# Lab 02 — Check Certificate Revocation Status with OCSP

at 0950 on 05apr26

## Overview
Briefly describe what this lab was about in your own words.
What PKI concept or system behavior were you investigating?

My answer: referencing the four components of Digital Certificates within PKI (from Week 3 Lesson videos): 1) Identity. 2) Permissions. 3) Lifecycle. 4) Trust. This Week 5 Lab 1 and Lab 2 explained about Identity and Trust with creating, maintaining, and validating or revoking the Digital Certificate(s). 

---

## Environment
- Operating System:
- Terminal Used:
- OpenSSL Version (`openssl version`):
- Target site used:

I'm using GitBash.

---

## Steps Performed
Summarize the key steps you performed to complete the lab.
Do not copy the lab instructions — describe what you actually did.

1. Used the command to get the Subject/Leaf Certificate private key. 
2. Used the commands to receive the Certificate's fullchain information to see all three Certificates that make up the Trust Anchor. 
3. Used the commands to get the OSCP/Online Certificate Status Protocol validation information on the Subject's Certificate. 
4. Lastly, compared how the two Certificate validation techniques: OSCP and the CRL/Certificate Revocation List perform. 
5.

---

## Results
Include the important outputs or findings from the lab.

1) What was the Subject and Issuer of the leaf certificate?
2) What OCSP URL did you find in the Authority Information Access extension?
3) What CRL Distribution Point URL did you find?
4) What was the OCSP response status for the certificate?
5) What do "This Update" and "Next Update" tell you?

1) Week 5 Lab 02 step 2 - My answer: Subject issued to GitHub.com, and Issuer signed by Sectigo Limited.
 
 Week 5 Lab 02 step 3 - My answer: The Issuer_cert.pem file is different from the leaf_cert.pem file because it comes from the Certificate fullchain and is the Intermediate CA whereas the leaf_cert.pem is the Subject's Certificate.

2) Week 5 Lab 02 step 4 - My answer: http://ocsp.sectigo.com

3) Week 5 Lab 02 step 5 - My answer: http://crt.sectigo.com/SectigoPublicServerAuthenticationCADVE36.crt

4) Week 5 Lab 02 step 8 - My answer: The status stated "good".

5) The current update caching titled This Update is April 2, 2026. And the future update caching titled Next Update is April 9, 2026.


If you include screenshots, store them in the assets folder and reference them here:
![Description](../../assets/screenshots/week-05/your-screenshot.png)

My Option B screenshot (drag and drop):
[ocsp_response.txt](https://github.com/user-attachments/files/26489980/ocsp_response.txt)OCSP Response Data:
    OCSP Response Status: successful (0x0)
    Response Type: Basic OCSP Response
    Version: 1 (0x0)
    Responder Id: 1799A804C16FE42D70A80A103D03D3E91AB82663
    Produced At: Apr  2 10:10:14 2026 GMT
    Responses:
    Certificate ID:
      Hash Algorithm: sha1
      Issuer Name Hash: B70E1256A2619B389154FE9CB9F0168E07A68C0B
      Issuer Key Hash: 1799A804C16FE42D70A80A103D03D3E91AB82663
      Serial Number: 1DC289C1EADAFB04E9D1CF53D5D72253
    Cert Status: good
    This Update: Apr  2 10:10:14 2026 GMT
    Next Update: Apr  9 10:10:13 2026 GMT

    Signature Algorithm: ecdsa-with-SHA256
    Signature Value:
        30:44:02:20:1f:18:b9:19:c7:ac:67:30:23:d6:6c:b0:dd:24:
        9a:8e:68:b6:30:48:be:ff:83:1a:9f:55:90:fa:47:df:e4:99:
        02:20:38:17:aa:86:0c:5c:88:22:8d:79:7b:49:08:c1:aa:47:
        2e:38:17:d2:e7:18:32:66:c4:35:87:b5:71:2b:31:73
labs/week-05/submissions/revocation-status/leaf_cert.pem: good
	This Update: Apr  2 10:10:14 2026 GMT
	Next Update: Apr  9 10:10:13 2026 GMT


---

## Key Findings
Document the most important observations from the lab.

• I observed that OSCP result/output is readable and concise to understand about the validation of the Certificate.  
•
•

---

## Explanation
Explain why the results matter.

1) Why does an OCSP query require both the leaf certificate and the issuer certificate?
2) What is the difference between OCSP and CRL in practice?
3) What would happen if a system trusted a revoked certificate because OCSP was unavailable?

1) The Issuer Certificate is needed along with the Leaf Certificate in the command for Week 5 Lab 2 step 8 because the result/output will provide any revoked information on the Subject/Leaf Certificate that had been documented by the Issuer/CA.
   
2) The difference between OCSP and CRL in the real world/in-practice is that OSCP performs more efficiently/with speed in validating or revoking a Certificate then the CRL/Certificate Revocation List. 
   
3) If OSCP was not available and a system trusted a revoked certificate then the trust is completely broken and possible high likelihood as well as impact of vulnerabilities and threats can occur to the Company/Enterprise.    

---

## Challenges / Troubleshooting
Document any issues encountered and how you resolved them.

My answer: None this time.

---

## Artifacts
List the files generated during this lab. (see Week-05 in the Screenshots folder)

- leaf_cert.pem
- issuer_cert.pem
- ocsp_response.txt
