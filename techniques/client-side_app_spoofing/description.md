# Client-side app spoofing

## Tactics
* Execution
* Persistence
* Defense Evasion

## Summary
Some OAuth integrations intended for use by desktop or mobile clients (rather than typical SaaS-to-SaaS integrations) can be controlled by adversaries. These client integrations tend to either make use of the [public client type](https://oauth.net/2/client-types/) for OAuth (the correct intended flow for this scenario), or the client secret for the OAuth app is directly embedded in the code, which is not considered good security practice and can be extracted by an adversary.

While an adversary will generally not be able to control the reply/callback URLs to utilize these legitimate integrations in a consent phishing attack, they can perform localhost callbacks to manually consent to permissions themselves for accounts they have already compromised. This is sufficient to conduct a persistence attack to maintain long-term control of the user account, leaving the adversary with tokens they can use to maintain access.

The adversary can customize the level of access they would like to maintain by requesting more permissions than would be usually used for the integration.

This technique has the added benefit of appearing more legitimate as the OAuth integration itself will be one known to be associated with a legitimate client of some kind. If the target user already uses the client in question, it will be even more stealthy as the OAuth integration already exists - effectively an [evil twin integration](../evil_twin_integrations/description.md).

## Examples
* [Thunderbird](examples/thunderbird.md)

## References

* [Maintaining persistent access in a SaaS-first world](https://pushsecurity.com/blog/maintaining-persistent-access-in-a-saas-first-world)