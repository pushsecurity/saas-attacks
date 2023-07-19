# Evil twin integrations

## Tactics
* Persistence
* Defense Evasion

## Summary
OAuth apps provide a mechanism for maintaining long-term persistent access to compromised accounts that resist normal recovery actions, such as password resets. However, an in-depth investigation may lead to the discovery of OAuth integrations created by the adversary. Once these malicious integrations are deleted, the adversary would lose their persistence mechanism as soon as the access token expires (within hours or minutes).

Instead, the attacker could enumerate existing OAuth integrations the user has already granted/installed, find one that exposes useful scopes and functionality, and create a second instance or twin of that integration. These twin integrations look identical to the original integration as SaaS apps don’t display the details of the account on the other side of the integration, and are therefore unlikely to be discovered and deleted.

This attack relies on the victim having already installed or created an OAuth integration that would be useful to the attacker. Existing integrations with workflow automation / no-code automation platforms are typically the most useful, but other apps that access (and expose) sensitive data like email are common in marketing, sales and customer support tools.


## Examples
* [Hubspot](examples/hubspot.md)

## References

https://pushsecurity.com/blog/maintaining-persistent-access-in-a-saas-first-world