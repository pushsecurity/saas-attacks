# MFA downgrade
ID: SAT1045

## Tactics
* Initial Access

## Summary
Phishing-resistant MFA factors, such as passkeys or vendor-specific implementations like Okta Fastpass, have been introduced to deal with the problem of [AiTM phishing attacks](/techniques/aitm_phishing/description.md) and credential theft. An MFA downgrade attack can be used to prevent the use of a passkey in order to force the use of a vulnerable factor, such that an AiTM phishing attack is still successful.

Traditional authentication factors, like passwords, push notifications and time-based one-time-passwords (TOTPs) are all vulnerable to phishing attacks as they can be either captured and replayed by an attacker or work without even needing to be replayed, as is the case with push notifications. Additionally, [MFA fatigue](/techniques/mfa_fatigue/description.md) attacks are often effective against push notification factors too, when an attacker has already compromised a password factor.

Using a phishing-resistant factor, such as a passkey, prevents these attacks because they are cryptographically tied to the domain being accessed. Therefore, if a user accesses a AiTM phishing website on a malicious domain, it’s not possible for them to send a successful challenge/response to authenticate.

However, just because a user has a phishing-resistant factor setup and may use them by default, it does not mean they are necessarily enforced. Often services support the use of multiple authentication options, particularly for second factors. In particular, passkeys are device-bound and so enforcing their use prevents logins from other devices and can cause recovery issues in a lost/broken device scenario. Therefore, it is common for the default case to be that passkey authentication is optional, rather than required.

Attackers can exploit this by using an AiTM phishing attack to modify requests/responses so as to prevent the ability of passkeys to be selected as a login option and prompting the user to use vulnerable factors, such as passwords, TOTPs and push notifications instead. Since the server-side will support these authentication options in this case, if the user continues to enter other authentication factors then their authenticated session will be compromised despite the fact they usually use passkeys or similar.


## Examples
* [Microsoft - Windows Hello for Business MFA downgrade attack](https://medium.com/@yudasm/bypassing-windows-hello-for-business-for-phishing-181f2271dc02#c32b)

## References
* [FIDO Alliance - Passkeys 101](https://fidoalliance.org/passkeys/)
* [X33fcon - Unraveling and Countering Adversary-in-the-Middle Phishing Attacks - MFA downgrade section](https://youtu.be/-W-LxcbUxI4?t=1541)