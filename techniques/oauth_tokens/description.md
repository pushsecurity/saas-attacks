# OAuth tokens

## Tactics
* Execution
* Persistence


## Summary
An adversary can use a malicious OAuth app or API development tool to create an OAuth token, using arbitrary permissions to maintain long-term programmatic access to a compromised user account.

SaaS apps typically use OAuth tokens to grant access to app APIs, normally in the context of the user creating the token. Long term access is maintained through refresh tokens, which typically never expire. Refresh tokens can be used to generate short-lived access tokens, which are used to query the API. These tokens generally continue working after password changes and do not require MFA, resulting in a very effective way to maintain control over a compromised user account.

To get access to a raw refresh token after compromising a SaaS account, an adversary could create an integration with a malicious app they control. Most SaaS apps that support OAuth integrations provide SDKs and examples for creating these apps, and many don’t require verification or any security checks before publishing OAuth apps. An alternative method of creating and accessing OAuth tokens is through the use of in-browser API test utilities.

Because the app is controlled by the adversary, the requested scopes or permissions attached to the created token are chosen by the adversary, and are typically limited only by the scopes the app developer has made available.

## Examples
* [Microsoft Graph Explorer](examples/graph_explorer.md)
* [Slack API tester](examples/slack_api_tester.md)

## References