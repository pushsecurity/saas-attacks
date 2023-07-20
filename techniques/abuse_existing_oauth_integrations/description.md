# Abuse existing OAuth integrations

## Tactics
* Privilege Escalation
* Lateral Movement

## Summary
Some SaaS apps allow OAuth integrations to other apps, which allow the app to gain access to certain data and additional functionality. If an adversary compromises an SaaS account  integrated with other apps, they can escalate privileges and move laterally to other apps.

To abuse apps with existing integrations, that app must expose some usable functionality though the integration back to the user. As an example, an integration with email access scopes, but which does not actually display emails to the user (of the integration) is not very useful to the adversary.

The challenge then is to identify apps that an employee is using that are both likely to have existing integrations, and expose offensively useful functionality through those integrations. Typical apps that fit this bill are workflow automation apps (see [Shadow automations]) which provide highly flexible integrations. Many sales and marketing apps that integrate with email would grant an adversary effective “webmail” access to integrated mailboxes.


## Examples
* [Zapier](examples/zapier.md)

## References