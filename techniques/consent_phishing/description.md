# Consent phishing

## Tactics
* Initial Access

## Summary

OAuth allows users to grant third-party apps permissions to access their data. Adversaries can abuse this functionality by tricking users into authorizing access for malicious OAuth apps.

In a consent phishing attack, an adversary sends a phishing link to a target that requests permissions to access sensitive data or permissions to perform dangerous actions. If the target grants consent for the permissions, the adversary gains that level of access over the target’s account. This level of access will bypass MFA and persist through password changes.

Consent phishing is most commonly associated with attacks aimed at getting access to Microsoft Azure or Google Workspace tenants. However, it has become more common for SaaS apps to implement their own OAuth-authenticated APIs and app stores that can be targeted in the same way.


## Examples
* [Microsoft](examples/microsoft.md)

## References

* https://www.mwrcybersec.com/decoding-consent-phishing
