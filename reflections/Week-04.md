# Week 04 Reflection

at 2123 on 29mar26

Submit this in your portfolio repository:

`reflections/week-XX.md` (e.g. `reflections/week-04.md`)

---

## Prompts

1. What did you learn this week?

My answer: I learned how to view Digital Certificates in the formats of: PEM file, DER file, and PFX file. Also, I have learned how to find the Root CAs/Certificate Authorities on my local computer as a Windows User which this helped me understand what my previous error troubleshooting in Week 03 Lab 03 was about.  


2. What concept was most challenging?

****first error in Week 04 Lab 01 step 6****

(I have a Community post about this) I observed that the test_key.pem file was created. However, the test_key.pem and the test_cert.pem would not collaborate on my laptop to create the signed certificate with the private key. I had to ask for troubleshooting help with the Instructor Tonia W. which I kept my OpenSSL and installed GitBash. While using GitBash, we learned that my laptop was picking up both files and wouldn't allow the test_cert.pem to be created. After multiple troubleshooting steps in two hours, specifically five or six steps (I have screenshots), helped me created the accurate result for Week 04 Lab 01 step 6 second command.


****second error in Week 04 Lab01 last piece of step 6 and step 7****

And last part of bundle the PFX file command, which ask for a password, doesn't work for me on GitBash. I continued to receive this result "Could not open file or uri for loading private key from -inkey file from labs/week-04/submissions/convert-formats/test_key.pem: No such file or directory". (I have a comment on the Community post about this update error)


****error in Week 04 Lab 02****

(I also have a Community post about this)

A troubleshoot was needed for my Powershell result "Verify Return Code: 20 (not local )". And Instructor Tonia W. helped me by asking me to install GitBash. Using GitBash, I now received the accurate result "Verify Return Code: 0".


3. Where does this concept appear in real-world systems?


My answer: I have learned that: 

1) format PEM file(s) are plaintext/human readable files and used by Linux and OpenSSL. 

2) format DER file(s) are acutal certificate files and would be used by Java and older Enterprise systems for ciphertext/non-human readable files. 

3) format PFX file(s) are used by Windows certificate(s) and key transfers between systems for certificates to be associated/signed with a private key.


4. How would you explain this topic to a non-technical audience?

My answer: Digital Certificates have variety of formats to open and view it in such as PEM file, DER file, and PFX file. 


5. What questions remain?

My answer: I still need help troubleshooting Week 04 Lab 01 step 6 (password result not appearing for me in GitBash) and step 7.

---

## Professional Growth Check

- [ ] I documented my work clearly and in my own words
- [ ] I used structured formatting in my submission files
- [ ] My commit message was meaningful and descriptive

---

*CVI PKI Career Pathway — Foundations Phase*
