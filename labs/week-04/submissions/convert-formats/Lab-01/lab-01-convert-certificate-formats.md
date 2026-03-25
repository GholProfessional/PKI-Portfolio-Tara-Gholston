# Lab 01 — Convert Certificate Formats


## Overview
Briefly describe what this lab was about in your own words. What PKI concept or system behavior were you investigating?

## Environment
- Operating System:
- Terminal Used:
- OpenSSL Version (openssl version):

I'm using Powershell.

## Steps Performed
Summarize the key steps you performed. Do not copy the lab instructions — describe what you actually did.

1. at 0803 on 24mar26 (at work before I get busy): On Powershell, I viewed the isaca.org leaf certificate and I saved it to Week 04 convert-formats folder. I observed that I can easily read the BEGIN and END lines of the Certificate's signature in human lanaguage, which it tells me that its encoding/format can be saved as a PEM file.  

2. at 0034 on 25mar26: I observed that the leaf_cert.der command on Powershell didn't display any results on it. However, in the converts-format folder on my laptop I do see a Digital Certificate titled leaf_cert and its details including the Certificate Chain.    

3. 

4.

5.


## Results
- What did the PEM file look like compared to the DER file?
- What happened when you opened the .der file in a text editor?
- What did the diff output show after converting PEM → DER → PEM?
- What information was displayed when you verified the PFX?

## Key Findings

## Explanation
- Why does a PFX require a password?
- In what real-world scenario would you choose PEM vs DER vs PFX?
- Why is it important never to commit private key files to GitHub?

## Challenges / Troubleshooting

## Artifacts
- leaf_cert.pem, leaf_cert.der, leaf_cert_restored.pem, test_cert.pem, test_bundle.pfx
