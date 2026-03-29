# Lab 01 — Convert Certificate Formats


## Overview
Briefly describe what this lab was about in your own words. What PKI concept or system behavior were you investigating?

at 1027 on 23mar26 - my answer: Digital Certificate is the actual document, and the Certificate format(s) are the various mechanisms used to view and read this document. 


## Environment
- Operating System:
- Terminal Used:
- OpenSSL Version (openssl version):

I'm using Powershell.

## Steps Performed
Summarize the key steps you performed. Do not copy the lab instructions — describe what you actually did.

1. at 0803 on 24mar26 (at work before I get busy): On Powershell, I viewed the isaca.org leaf certificate and I saved it to Week 04 convert-formats folder. I observed that I can easily read the BEGIN and END lines of the Certificate's signature in human lanaguage, which it tells me that its encoding/format can be saved as a PEM file.  

2. at 0034 on 25mar26: I observed that the leaf_cert.der command on Powershell didn't display any results on it. However, in the converts-format folder on my laptop I do see a Digital Certificate titled leaf_cert and when I opened it I observed its details including the Certificate Chain.    

3. at 0049 on 25mar26: I observed that there is no difference in output with the original leaf_cert PEM file and the leaf_cert_restored PEM file after converting from the .der file format. And the diff command result/output on Powershell confirms that the two files cancel each out, there are two arrows: one pointing left and other pointing right in the Side Indicator area.  

4. at 1602 on 29mar26: I observed that the test_key.pem file was created. However, the test_key.pem and the test_cert.pem would not collaborate on my laptop to create the signed certificate with the private key. I had to ask for troubleshooting help with the Instructor Tonia W. which I kept my OpenSSL and installed GitBash. While using GitBash, we learned that my laptop was picking up both files and wouldn't allow the test_cert.pem to be created. After multiple troubleshooting steps in two hours, specifically five or six steps (I have screenshots), helped me created the accurate result for Week 04 Lab 01 step 6 second command.    
And last part of bundle the PFX file command, which ask for a password, doesn't work for me on GitBash. I continued to receive this result "Could not open file or uri for loading private key from -inkey file from labs/week-04/submissions/convert-formats/test_key.pem: No such file or directory". 

6. at 1615 on 29mar26: I cannot complete step 7 to verify PFX file either because of the last piece of step 6 above.   


## Results
- What did the PEM file look like compared to the DER file?

at 1727 on 29mar26 - my answer: PEM file was a plaintext/human readable file whereas the DER file is the actual certificate. 

- What happened when you opened the .der file in a text editor?

at 1734 on 29mar26 - my answer: the opened DER file  in the text editor appears as ciphertext/non-human readable text. 

- What did the diff output show after converting PEM → DER → PEM?

at 1735 on 29mar26 - my answer: the restored PEM file displayed the same plaintext/human readable text as the original PEM file. 

- What information was displayed when you verified the PFX?

at 1738 on 29mar26 - my answer: I couldn't achieve this result because I need to continue troubleshooting the step 6 and step 7 since I cannot access the password that I need to type in. So, no test_bundle.pfx file exist for me. 

## Key Findings

## Explanation
- Why does a PFX require a password?

at 1617 on 29mar26 - My answer: The password represents protecting the sensitive data which is the private key so only the individual with the access rights can see it.   
  
- In what real-world scenario would you choose PEM vs DER vs PFX?

at 1617 on 29mar26 - My answer:
- PEM would be used by Linux web servers and OpenSSL for plaintext/human readable files needed.
- DER would be used by Java and older Enterprise systems for ciphertext/non-human readable files needed.
- PFX would be used by Windows certificate(s) and key transfers between systems for certificates to be associated with private key. 
  
- Why is it important never to commit private key files to GitHub?

at 1629 on 29mar26 - My answer: Never commit the private key to GitHub because only the individual with the access rights can see it will be able to read the certificate or sensitive data. 


## Challenges / Troubleshooting

at 1635 on 29mar26: Please see number 5 and number 6 above for challenges and troubleshooting I experienced for Week 04 Lab 01 step 6 and step 7.
## Artifacts
- leaf_cert.pem, leaf_cert.der, leaf_cert_restored.pem, test_cert.pem, test_bundle.pfx
