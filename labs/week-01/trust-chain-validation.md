# Week 01 Mini Lab — Trust Chain Validation

## Screenshot Evidence
at 2244 on 08mar26

Capture a screenshot of the Certification Path (certificate chain) from your browser.

Save it as:

assets/screenshots/week-01/trust-chain-validation.png (please see the screenshot I have)

Embed the screenshot below:

![Trust Chain Validation](../../assets/screenshots/week-01/trust-chain-validation.png)


## Website Information

**Website inspected:**  
<!-- Enter full URL -->
- - isaca.org
    
---

## Certificate Chain Breakdown

**Leaf (Server) Certificate**  
<!-- Enter Common Name or Subject -->
- - isaca.org.

**Intermediate Certificate Authority**
<!-- Enter Intermediate CA name -->
- - WE1. (Organization is Google Trust Services LLC)

**Root Certificate Authority (Trust Anchor)**
<!-- Enter Root CA name -->
- - GTS Root R4.

---

## Trust Anchor Verification

Is the Root CA marked as trusted by your system?

<!-- Yes / No -->
- - Yes. When I click on the lock icon, it states Connection is secure by a trusted authority.

If yes, explain where that trust comes from (OS/browser root store).
- - It comes from Authority Information Access on isaca.org's Certificate Viewer details, it displayed "CA Issuers: URI: http://i.pki.goog/we1.crt".

If no, explain what warning or behavior occurred.
- - 

---

## Observations

Document three observations about the certificate.

### Observation 1
<!-- What did you notice about the chain structure? -->
- - It is located in steps/levels at the top of the isaca.org's Certificate Viewer details.

### Observation 2
<!-- What did you notice about the Root CA? -->
- - It is a popular search engine company Google. 

### Observation 3
<!-- What did you notice about how the browser determines trust? -->
- - The Root CA web browser also has a lock icon and HTTPS 

---

## Reflection

In 3–5 sentences, explain:
- Why the Root certificate is called a trust anchor?
- - The Root certificate is known as the Trust Anchor because it has the authority to approve or revoke the web service or entity's certificate.
  
- How validation walks the certificate chain? 
- - Validation is represented by the Certificate Chain by the Subject/Web service is validated by the Intermediate CA who gets approval from the Root CA.  

- What would happen if the Root CA were not trusted?
- - When the Root CA is not trusted then the Trust Anchor is broken and loses its authority and responsibility, which another entity will become the Root CA. 
    

Use your own words.
