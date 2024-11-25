# Cross-IdP Impersonation
ID: SAT1047

## Tactics
* Initial Access
* Persistence

## Summary

Cross-IdP impersonation is when an adversary uses an account with the correct target email address but registered with an identity provider that is not in use by the target organization to authenticate to a target SaaS application. This can allow strong SSO authentication measures to be circumvented.

For example, if a target organization has user@example.com email addresses and uses Microsoft Entra as their identity provider, but an attacker is able to create a user@example.com account with Google somehow, then they can potentially circumvent SSO logins to downstream SaaS applications by using "Login with Google" social logins instead of "Login with Microsoft" or a SAML-based SSO login. This is also affected by the configuration of the downstream SaaS application. 

## References
* [Technical blog post - Verification phishing and cross-idp impersonation](https://pushsecurity.com/blog/a-new-class-of-phishing-verification-phishing-and-cross-idp-impersonation/)
* [Zendesk vulnerability allows Slack compromise](https://cyberinsider.com/zendesk-vulnerability-allows-slack-takeovers-through-apple-oauth-exploit/)