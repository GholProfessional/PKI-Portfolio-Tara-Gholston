# Week 2 Lesson Notes — Cryptography Fundamentals
at 0509 on 20mar26

## 1. Core Concept

Explain the difference between confidentiality, integrity, and authenticity.

(my first Community post from two weeks ago, I copied and pasted below)

My shared thoughts on Week 1 Lessons on what is PKI...CIA Triad.

Hello, Community/Cohorts,

I have taken off work today, not feeling well.

As I listen to the Week 1 video lessons, I would like to briefly mention about the CIA Triad which includes two additional components. This is how I understand PKI so I would like to share.

Please share your thoughts and understanding to this since I'm still learning and clarifying.

I have learned that PKI and PKI Encryption are two separate things (literally yesterday through other certificate and certification study I am doing). Originally, through my ISACA CISA studying, I thought PKI Encryption represented all of the process. But I had clarification notes from another study which explained the separation.

This leads into my mention of the CIA Triad plus two additional components.

C - Confidentiality.

I - Integrity.

A - Availability.

N - Non-Repudiation.

A - Authentication.

My understanding of PKI (Infrastructure) and PKI Encryption involve:

1) Integrity (the identity part that Tonia W. explained in the Week 1 videos).

-- I understand this as ensuring the authentic identity of the requested information from the End User/Company to the RA/Registration Authority which will be used to get a Digital Signature or Digital Certificate created.

2) Confidentiality (the encryption/protection part that Tonia W. explained).

3) Authentication.

-- I feel like this also fits the identity part because as the PKI's Trust Anchor is successfully approved by the CA/Certification Authority, this is represented as the approved, created Digital Signature or Digital Certificate to the End User/Company. Going forward the End User/Company has Authentication and can gain access (Authorization) with the trusted Digital Signature or Digital Certificate.

---

## 2. Week 2 Labs 1 - 3 workings

1) Encrypt and decrypt data using symmetric encryption. 
2) Generate and compare cryptographic hashes.
3) Digitally sign and verify files.

Please see my three Week 2 Lab folders with the Powershell work I have completed. I forgot to screenshot my Lab 1 work on Powershell, and do have a screenshot of both Lab 2 and Lab 3. I do have documents with screenshots of Powershell work uploaded but I believe the files are too big. 


---
4) Identify why private key protection is critical in PKI systems

Private Key security is crucial in PKI systems because verifies Integrity and builds trust in that data is only accessed and read by authorized End Users.  


## 3. Observations

Lab 1 
1) Why the encrypted file is unreadable.
2) What would happen if the wrong password were used.
3) What security property symmetric encryption provides.
4) Why TLS uses symmetric encryption for data transfer.


Lab 2 
1) Why the hash changed after a small modification
2) Why hashing does NOT provide confidentiality
3) What security property hashing provides
4) Where hashing is used in PKI systems
Examples to consider:
Certificate signatures.
File integrity validation.
Code signing. 


Lab 3 
1) Why verification succeeds before tampering.
2) Why verification fails after modification.
3) Why digital signatures require both hashing and asymmetric cryptography.
4) How this relates to certificate signing in PKI.


---

## 4. Common Misconceptions
