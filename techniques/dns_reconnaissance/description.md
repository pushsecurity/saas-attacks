# DNS reconnaissance

## Tactics
* Reconnassiance

## Summary
Some SaaS apps require ownership verification for a domain as part of the setup process. A common way to verify ownership is to publish a specific string as a DNS TXT record that the SaaS vendor can verify as proof.
Querying DNS TXT records can reveal which SaaS apps the target organization might be using. MX and SPF records are also useful in discovering SaaS apps used to send and receive mail for the organization.

## Examples
* [TXT records](examples/txt_hsbc.md)

## References