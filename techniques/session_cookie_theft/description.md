# Session cookie theft
ID: SAT1044

## Tactics
* Lateral Movement
* Defense Evasion

## Summary

Due to increasing use of SaaS apps, core identity providers acting as SSO gateways to them, and the widespread adoption of MFA, hybrid attacks involving the theft of valid browser session cookies from compromised endpoints using infostealing malware are becoming more common. These session cookies are then used to pivot from an endpoint compromise and laterally move to downstream SaaS applications. They are typically imported into an adversary's own browser and then used to resume access to the authenticated session without re-authenticating. 

Prevoiously, endpoint compromises would have often involved credential dumping and been focused on lateral movement to other endpoints or internal servers. Now there is an increasing drive to move to SaaS applications instead. Widespread MFA use makes captured passwords less useful alone and so stealing authenticated session cookies is a valid method to circumvent MFA. This can even potentially circumvent modern phishing-resistant MFA factors such as passkeys as it can circumvent the requirement to re-authenticate entirely. 

Session cookies for any SaaS application are useful but when valid sessions for core IdPs are compromised then adversaries will typically be able to laterally move to a large number of downstream SaaS applications by abusing SSO mechanisms like SAML and OIDC. Vendor-specific technologies like Okta SWA will also allow direct credential compromise for other downstream SaaS applications.

While adversaries may steal cookies directly using compromised endpoints, stolen cookies have also become available for sale in the criminal world from infostealing malware, therefore it may be possible to directly purchase cookies for use. More information of the criminal ecosystem can be found in this [blog post](https://blog.sekoia.io/traffers-a-deep-dive-into-the-information-stealer-ecosystem/) and more information on a variety of stealer malware families can be found in this [threat report](https://news.sophos.com/en-us/2024/03/12/2024-sophos-threat-report/).

This technique is related to, but distinct from, [AitM Phishing](/techniques/aitm_phishing/description.md), which seeks to compromise sessions to circumvent MFA as an initial access vector.

## References

* [MITRE ATT&CK - Browser Session Hijacking](https://attack.mitre.org/techniques/T1185/)
* [2024 Sophos Threat Report](https://news.sophos.com/en-us/2024/03/12/2024-sophos-threat-report/)
* [Traffers - a deep dive into the information stealer ecosystem](https://blog.sekoia.io/traffers-a-deep-dive-into-the-information-stealer-ecosystem/)
