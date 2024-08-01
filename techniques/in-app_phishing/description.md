# In-app phishing
ID: SAT1020

## Tactics
* Initial Access
* Lateral Movement

## Summary
It’s possible to conduct phishing and other social engineering attacks, using native features of SaaS apps. This will often result in activity directly within an app the target already uses and/or may result in email notifications being delivered directly to the target but from legitimate email domains associated with the SaaS app. This is a broad area but commonly can be through shared content or collaborations features, such as document sharing and commenting functionality.

Users will often treat activity within legitimate apps or email notifications from confirmed legitimate SaaS app domains with a much higher level of trust than they would traditional phishing emails and therefore they are more likely to fall victim.

This can be used as both an initial access method, using SaaS apps that allow communication with external users, or as a lateral movement method once a foothold has been established on a legitimate tenant for the target organization. 

For example, a malicious document could be shared with a target using a document sharing app in an attempt to gain a foothold elsewhere. A different example involving lateral movement might be a ticketing system where comments and ticket creation functionality could be abused to spread malicious links aimed at harvesting further user credentials. 

## Examples

* [GitHub](examples/github.md)
* [Monday.com](https://www.bleepingcomputer.com/news/security/mondaycom-removes-share-update-feature-abused-for-phishing-attacks/)

## References
* [Jade sleet compromise using GitHub repository collaboration](https://github.blog/2023-07-18-security-alert-social-engineering-campaign-targets-technology-industry-employees/)
* [Evilginx - MITM framework for phishing login credentials](https://github.com/kgretzky/evilginx2)
* [MITRE ATT&CK - Phishing: Spearphishing via Service](https://attack.mitre.org/techniques/T1566/003/)

