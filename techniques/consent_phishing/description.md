# Consent phishing
ID: SAT1010

## Tactics
* Initial Access

## Summary

OAuth allows users to grant third-party apps permissions to access their data. Adversaries can abuse this functionality by tricking users into authorizing access for malicious OAuth apps.

In a consent phishing attack, an adversary sends a phishing link to a target that requests permissions to access sensitive data or permissions to perform dangerous actions. If the target grants consent for the permissions, the adversary gains that level of access over the target’s account. This level of access will bypass MFA and persist through password changes.

Consent phishing is most commonly associated with attacks aimed at getting access to Microsoft Azure or Google Workspace tenants. However, it has become more common for SaaS apps to implement their own OAuth-authenticated APIs and app stores that can be targeted in the same way.


## Examples
* [Microsoft](examples/microsoft.md)
* [GitHub](https://www.bleepingcomputer.com/news/security/gitloker-attacks-abuse-github-notifications-to-push-malicious-oauth-apps/)

## References

* [Decoding consent phishing - technical blog post](https://www.mwrcybersec.com/decoding-consent-phishing)
* [O365 attack toolkit - perform consent phishing attacks against O365](https://github.com/mdsecactivebreach/o365-attack-toolkit)
* [MITRE ATT&CK - Phishing: Speakphishing Link](https://attack.mitre.org/techniques/T1566/002/)
* [Compromised Microsoft Partner Network accounts used for consent phishing](https://www.bleepingcomputer.com/news/security/microsoft-disables-verified-partner-accounts-used-for-oauth-phishing/)
