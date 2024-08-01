# Ghost logins
ID: SAT1017

## Tactics
* Initial access
* Persistence
* Defense Evasion

## Summary
A common SaaS app feature allows logins to the same account using multiple methods simultaneously – for example, a standard password-based authentication (local to the SaaS app) and an SSO mechanism, such as an OIDC social login or SAML login. This can be relevant for both initial access and persistence phases.

For initial access, it's possible users will have configured much weaker authentication mechanisms at some point. For example, a weak single-factor password before SSO was configured or a secondary/recovery address using a personal webmail account. They later migrate to strong SSO but the original methods remain active and attackers can find these weaknesses in future. This was a discussion point during the 2024 Snowflake credential breaches as local passwords were not disabled if migrating Snowflake to SAML SSO authentication.

For persistence, if an adversary gains access to a SaaS account temporarily, they can configure an alternative authentication method to maintain access to the account, alongside the legitimate user. If the user uses a social login to access the account, an adversary may be able to configure a separate username/password login to access the account or even (though much less commonly) connect a second social account that the adversary controls. This allows the adversary to maintain persistent access to the user account even in the event of password changes or MFA changes.

This attack will go unnoticed if the victim organization relies on SSO logs for auditing access to SaaS applications. The attack bypasses SSO as the login remains local to the SaaS app or, in the case of an OIDC SSO login, the adversary’s own social account.


## Examples
* [Snowflake](https://www.youtube.com/watch?v=5yeOAM4YCAI)
* [Shortcut](examples/shortcut.md)
* [Expensify](examples/expensify.md)

## References
* [MITRE ATT&CK - Use Alternate Authentication Material](https://attack.mitre.org/techniques/T1550/)
* [X thread explaining ghost logins with reference to Snowflake](https://x.com/jukelennings/status/1801985628034281703)
* [Google email verification flaw abused to compromise 3rd party SaaS services](https://krebsonsecurity.com/2024/07/crooks-bypassed-googles-email-verification-to-create-workspace-accounts-access-3rd-party-services/)
