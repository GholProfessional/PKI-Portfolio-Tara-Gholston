# Week 01 Lab — Key Pair Generation
at 2045 on 08mar26
## Screenshot Evidence

If using OpenSSL:
1. Capture a screenshot showing:
  - The command used to generate the private key
  - The command used to extract the public key
2. Save it as:

**assets/screenshots/week-01/keypair-generation.png** 

3. Embed the screenshot below:

**![Key Pair Generation](../../assets/screenshots/week-01/keypair-generation.png)**

If using a browser-based generator, capture the generated key pair screen (redact sensitive portions of the private key before committing).

---

## Key Identification
**Which file is the public key?**
<!-- Example: public.key --> 
My answer is Please see private.key in file titled Week -01 key-pair-generation (used OpenSSL via Windows).

**Which file is the private key?**
<!-- Example: private.key -->
My answer is Please see public.key in file titled Week -01 key-pair-generation (used OpenSSL via Windows).

---

## Key Properties
Briefly describe:
- What makes the public key safe to share?
- - The Public Key is accessible to all Users who need to use it to decrypt a data message. 
  
- What makes the private key sensitive?
- -  The Private Key is sensitive because it is only accessible to the User who needs to use it to encrypt and decrypt a data message. 
   
## Security Scenario
What would happen if someone obtained your private key?
- - When and if someone gains my Private Key, the data message and any other content could be attacked and compromised. 


Explain the risk in terms of:
  - Identity:
  - - The risk is that the identity of the User can have more items stole from them by the attacker as well as the surrounding area that can be accessed because of Access Control Rights.  
    
  - Impersonation:
  - - The risk that the identity of the User can be used to do malicious things by the attacker.
  
  - Trust:
  - - The risk that the User and Company/Enterprise/Org cannot be trusted with employee and customer data because of the attack. 

---

## Observations
Document three observations from this lab.

### Observation 1
<!-- What did you notice about key generation? -->
- - I observed that the Windows OpenSSL commands are different than the Linus and iOS commands that were suggested. 

### Observation 2
<!-- What did you notice about key size or format? -->
- - I observed that the Private Key and Public Key are similar in format except for length. 

### Observation 3
<!-- What did you notice about how the keys differ? -->
- - I observed that Private Key is much longer than the Public Key.
---

## Reflection
In 3–5 sentences, explain:

Why must the private key remain secret in a PKI system? 
- - The Private Key must be secret because the PKI system uses it as identification and authentication for the User to use send as well as receive data and use web services. And this allows the PKI Encryption to protect the User and Web services from attacks. 


Focus on how identity is tied to possession of the private key. 
- - The Private Key is tied to identity/Integrity (CIA Triad) by being only in the access of the User whose identity is authorized by the PKI sytem. 

