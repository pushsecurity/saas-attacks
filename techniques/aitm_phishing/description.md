# AiTM Phishing
ID: SAT1042

## Tactics
* Initial Access

## Summary
Attacker-in-the-Middle (AITM) phishing is a newer variant of phishing that uses dedicated tooling to act as a web proxy between the victim and a legitimate login portal for an application the victim has access to, principally to make it easier to defeat MFA protection. 

As MFA has become more universal, classic password harvesting focused phishing attacks have reduced in effectiveness. Typically, for a full account compromise an MFA push notification or a one-time-passcode (OTP) needs to be entered at the time of login. 

AITM phishing solves this issue by proxying in real-time to the target login portal, making use of entered OTP codes or accepted MFA push notifications to achieve a full authenticated session. This leaves the adversary with access to both a valid password and valid session cookies they can steal and use to hijack the session. 

Additional benefits are that it is relatively quick and easy to target a new application and, once logged-in, a victim user will see all the real data they would expect to see ordinarily (e.g. their own emails/files etc) as it is a proxy of the real application. This reduces their chances of realizing they have been compromised due to the authentic working nature of the proxied application. 

Typical techniques to implement this involve either transparent web proxy techniques that seek to present the application with no noticeable changes (e.g. Evilginx2), or the use of desktop-control techniques to have the victim unknowingly interact with an attacker’s own browser instance (e.g. noVNC based techniques).

## Examples

## References
* [Evilginx - AITM web proxy](https://github.com/kgretzky/evilginx2)
* [EvilnoVNC - AITM noVNC proxy](https://github.com/JoelGMSec/EvilnoVNC)
* [Modlishka- AITM web proxy](https://github.com/drk1wi/Modlishka)
* [Muraena - AITM web proxy](https://github.com/muraenateam/muraena)
* [NoPhish - AITM noVNC proxy](https://github.com/powerseb/NoPhish)