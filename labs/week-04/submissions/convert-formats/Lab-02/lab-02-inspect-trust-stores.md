# Lab 02 — Inspect Your Trust Store

at 1922 on 29mar26

## Overview
Briefly describe what this lab was about in your own words. What PKI concept or system behavior were you investigating?

at 2115 on 29mar26: The Digital Certificate's Root CA of the website isaca.org I have chosen is listed along with other Root CA websites that are trusted by my local computer/laptop. 

My answer: 


## Environment
- Operating System:
- Terminal Used:
- OpenSSL Version (openssl version):

I'm using Powershell, now GitBash.

## Steps Performed

1. Used Powershell and received an error result of "Verify Return Code: 20 (unable to get no local issuer certificate)". 

2. After troubleshooting with Instructor Tonia W. on this error, she had me install GitBash and the accurate result "Verify Return Code: 0" worked.  

3.

4.

## Results
- How many trusted root CAs did you find on your system?

at 1933 on 29mar26: There are 49 certificates on my Certificate Manager's local computer (Windows). I am using Powershell but now only using GitBash for Windows after troubleshooting help with Instructor Tonia W.  

- Name at least one specific root CA you inspected. Include its Subject and expiration date.

at 0758 on 29mar26: GTS Root 4, Google Trust Services; and Saturday June 21, 2036. 

- What did the verify return code output tell you?

at 2020 on 29mar26: Used Powershell and received an error result of "Verify Return Code: 20 (unable to get no local issuer certificate)". After troubleshooting with Instructor Tonia W. on this error, she had me install GitBash and the accurate result "Verify Return Code: 0" worked.


If you include screenshots, store them in the assets folder and reference them here:

![Description](../../assets/screenshots/week-04/Screenshot (186)_Week04Lab02_certslist.png)
![Description](../../assets/screenshots/week-04/Screenshot (191)_ISACA.Subj&ExpirDate.png)
![Description](../../assets/screenshots/week-04/Screenshot (197)_PowershelleVerify20error.png)
![Description](../../assets/screenshots/week-04/Screenshot (285)_Wk04Lab02.verifycode0.png)


## Key Findings

## Explanation
- Why does your browser trust a certificate from a website you have never visited before?

at 2110 on 29mar26: There are trusted websites established as Root CAs so the browser's Certificate Manager will acknowledge it. 

- What would happen if an enterprise's internal root CA was NOT in the trust store?

at 2111 on 29mar26: When the Enterprise's internal Root CA is not in the Trust Store, the Digital Certificate will not be recognized.

- What surprised you about how many roots are pre-installed on your system?

at 2113 on 29mar26: I was surprised to see 49 Root CAs pre-installed on my local computer because I thought since I was only using several websites frequently that there would be less amount. 


## Challenges / Troubleshooting

A troubleshoot was needed for Powershell result "Verify Return Code: 20 (not local )". And Instructor Tonia W. helped me by asking me to install GitBash. Using GitBash, I now received the accurate result "Verify Return Code: 0".

## Artifacts
- root_cas.pem (macOS) or equivalent, screenshots stored in assets/screenshots/week-04/
