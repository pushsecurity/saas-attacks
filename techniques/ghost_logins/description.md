# Ghost logins

## Tactics
* Persistence
* Defense Evasion

## Summary
A common SaaS app feature allows logins to the same account using multiple methods simultaneously – for example, a standard password-based authentication (local to the SaaS app) and an SSO mechanism, such as an OIDC social login or SAML login.

If an adversary gains access to a SaaS account temporarily, they can configure an alternative authentication method to maintain access to the account, alongside the legitimate user. If the user uses a social login to access the account, an adversary may be able to configure a separate username/password login to access the account or even (though much less commonly) connect a second social account that the adversary controls.

This allows the adversary to maintain persistent access to the user account even in the event of password changes or MFA changes.

This attack will go unnoticed if the victim organization relies on SSO logs for auditing access to SaaS applications. The attack bypasses SSO as the login remains local to the SaaS app or, in the case of an OIDC SSO login, the adversary’s own social account.


## Examples
* [Shortcut](examples/shortcut.md)

## References