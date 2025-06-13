# Device code phishing
ID: SAT1012

## Tactics
* Initial Access
* Defense Evasion

## Summary

OAuth supports multiple different authentication flows that can be used to grant access to an app. One of these is the device authorization grant, which is intended for use with input-constrained devices, such as smart TVs and printers.

This flow operates by supplying a user with a unique code and instructing them to visit a webpage in a browser on a different device to enter the code in order to authorize the device. 

This can be used by an adversary to conduct a phishing attack against a target by convincing them to visit their authentication provider website and enter a code supplied by the adversary, thereby granting access to their account.

This shares similar advantages to a consent phishing attack in that it allows access to a target's account without requiring their password or MFA tokens.

It also has other advantages in that the link the target needs to visit is a legitimate URL and there is no prompt to consent to explicit permissions beyond entering the device code and signing in. Additionally, verified apps can be impersonated in some cases. 

## Examples
* [Microsoft](examples/microsoft.md)
* [GitHub](https://www.praetorian.com/blog/introducing-github-device-code-phishing/)

## References
* [Introducing a new phishing technique for compromising Office 365 accounts](https://aadinternals.com/post/phishing/)
* [How to Detect Malicious OAuth Device Code Phishing](https://www.inversecos.com/2022/12/how-to-detect-malicious-oauth-device.html)
* [PhishInSuits - a tool for device code phishing vs SMS](https://github.com/secureworks/PhishInSuits)
* [Microsoft device code documentation](https://learn.microsoft.com/en-us/azure/active-directory/develop/v2-oauth2-device-code)
* [MITRE ATT&CK - Phishing: Speakphishing Link](https://attack.mitre.org/techniques/T1566/002/)
