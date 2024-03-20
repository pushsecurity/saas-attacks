# Device Enrollment
ID: SAT1043

## Tactics
* Initial Access
* Persistence

## Summary
Some attack techniques result in temporary access to an account being obtained, possibly including knowledge of the account password, such as through AiTM phishing that proxies MFA codes or similar. In these situations, the ability to enroll a new device for an account can allow an adversary to maintain long-term access to the account. 

Most commonly, this would be the enrollment of a new MFA device in order to allow the adversary to complete MFA challenges for future authentication. However, it could also involve enrolling adversary-controlled devices into device management software to bypass other controls. 

This persistence form of device enrollment has been observed as a technique used by both [APT29](https://www.ncsc.gov.uk/news/svr-cyber-actors-adapt-tactics-for-initial-cloud-access) and [Scattered Spider](https://www.reliaquest.com/blog/scattered-spider-attack-analysis-account-compromise/)

In some cases, this can even form part of the initial access phase. For example, if compromising a dormant account using a credential stuffing attack, this may have been previously configured without MFA and newer security settings may prompt for MFA enrollment during the authentication process. In this case, the adversary will need to perform MFA device enrollment in order to successfully complete the attack and gain access to the account. This has been observed in [attacks by APT29 against Azure](https://www.mandiant.com/resources/blog/apt29-continues-targeting-microsoft) in the past.

## Examples

## References
* [NCSC advisory on cloud attacks by APT29](https://www.ncsc.gov.uk/news/svr-cyber-actors-adapt-tactics-for-initial-cloud-access)
* [Scattered Spider Attack Analysis - Technical Blog](https://www.reliaquest.com/blog/scattered-spider-attack-analysis-account-compromise/)
* [APT29 Attack Analysis - Technical Blog](https://www.mandiant.com/resources/blog/apt29-continues-targeting-microsoft)
* [MITRE - Account Manipulation: Device Registration](https://attack.mitre.org/techniques/T1098/005/)
