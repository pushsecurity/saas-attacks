# Inbound federation
ID: SAT1041

## Tactics
* Persistence
* Lateral Movement

## Summary
Inbound federation allows users to login to a target identity provider by authenticating with a source identity provider. This is often used in scenarios that involve multiple large divisions that form part of a larger parent, such as with conglomerates or during mergers and acquisitions.

An adversary who has gained administrative control of an application, such as a core identity provider, can use this to both maintain persistent access as well as effectively laterally move to other user accounts by authenticating against an identity provider they control and having those accounts mapped automatically to existing accounts on the target identity provider.

This shares similarities with [ghost logins](/techniques/ghost_logins/description.md), but affects all users of an application instead of being tied specifically to one user account. 

## Examples
* [Okta](examples/okta.md)

## References
* [Okta Cross-Tenant Impersonation](https://sec.okta.com/articles/2023/08/cross-tenant-impersonation-prevention-and-detection)

