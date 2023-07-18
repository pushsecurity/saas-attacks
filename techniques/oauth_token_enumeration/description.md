# OAuth token enumeration

## Tactics
* Discovery

## Summary
SaaS app users may have authenticated using OIDC (social logins) or have created other OAuth integrations to share data and make better use of the app. If an adversary has compromised a user’s account, they can list out existing OAuth integrations to identify other SaaS apps in use.

This may allow an adversary to target those apps for lateral movement or better target those apps for attack.

## Examples
* [Google](examples/google.md)
* [Microsoft](examples/microsoft.md)

## References