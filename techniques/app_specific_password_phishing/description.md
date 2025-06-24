# App-specific password phishing
ID: SAT1050

## Tactics
* Initial Access
* Persistence

## Summary

App-Specific password phishing is a social engineering technique where an adversary tricks a user into generating an "app-specific password" for their account and then sharing it with the attacker. These legacy passwords are a feature in some major SaaS providers (like Google and Apple) designed to allow older applications that do not support modern authentication (like OAuth 2.0) to access account data.

The attack flow typically involves a pretext where the attacker, posing as a trusted entity (e.g., tech support, a service provider), directs the user to their account's security settings. The user is then guided through the process of creating a new app-specific password and is instructed to paste this password into a form or chat window controlled by the attacker.

Because app-specific passwords are created by an already-authenticated user, they often bypass standard multi-factor authentication (MFA) prompts upon creation. Once the attacker possesses this password, they can gain persistent, programmatic access to the user's account data (e.g., emails, contacts, files) via APIs, often without triggering the same level of security alerts as a traditional interactive login from an unrecognized device. This makes the access stealthier and more durable than a session token, as these passwords typically remain valid until manually revoked by the user.

This technique is a variant of phishing that targets a specific, often overlooked, credential type. It is similar to [consent phishing](/techniques/consent_phishing/description.md) in that it abuses a legitimate feature, but it targets a direct password credential rather than an OAuth consent grant.

They can also be abused at the persistent phase to maintain access to a compromised account in a similar way to [ghost logins](/techniques/ghost_logins/description.md) and [api keys](/techniques/api_keys/description.md).

## Examples

* [Google](/techniques/app_specific_password_phishing/examples/google.md)

## References
* [Technical blog - Russian Government-Linked Social Engineering Targets App-Specific Passwords](https://citizenlab.ca/2025/06/russian-government-linked-social-engineering-targets-app-specific-passwords/)