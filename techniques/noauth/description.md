# nOAuth
ID: SAT1025

## Tactics
* Initial Access

## Summary

SaaS apps that make use of OAuth integrations require an identifier to match accounts between the application and identity provider. The OAuth specification states that a user should be identified by the subject claim. The subject claim is an immutable identifier and not an attribute that a user can alter. However, apps can be configured to identify users via other claims (in other words account metadata/attributes), which can lead to unintended consequences.

nOAuth is a common misconfiguration where apps use the 'email' claim to identify users instead of the subject claim.

An adversary could create their own tenant and set the 'email' attribute on their account to match their target's email address. This would allow them to authenticate to any vulnerable SaaS app where the target has an account.

## Examples
* [AzureAD](examples/azuread.md)

## References

* [nOAuth: How Microsoft OAuth Misconfiguration Can Lead to Full Account Takeover](https://www.descope.com/blog/post/noauth)