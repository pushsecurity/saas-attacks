# System integrations
ID: SAT1036

## Tactics
* Persistence
* Defense Evasion

## Summary
Some SaaS apps allow OAuth integrations that are not tied to a user account, but to the app tenant, or a machine account instead. Since the integration is not tied to a specific user, persistence can be maintained after a user account has been disabled or deleted.

It can also frustrate forensics by obfuscating which user account is responsible for actions taken by the integration, particularly when that relates to a user account that has since been deleted. This is somewhat equivalent to migrating to a system process in an endpoint attack.

In some cases, app-level integrations require administrative permissions but in others a standard user can do this, resulting in a more significant threat.

## Examples
* [Slack](examples/slack.md)

## References
* [Slack Attack: A phisher's guide to persistence and lateral movement](https://pushsecurity.com/blog/phishing-slack-persistence/)