# Account recovery

## Tactics
* Lateral Movement

## Summary
Most SaaS apps allow accounts to be recovered via email. This can be through the use of forgotten password functionality via the directly registered email address or via a secondary recovery email address.

This presents an opportunity for an adversary to laterally move to other SaaS apps if they have gained access to a user’s mailbox and then triggering an account recovery process.

While this may alert the user through the appearance of password reset emails, a variety of other techniques, such as mail rules or automations, can be used to capture the emails. The adversary can then delete emails automatically before the user sees them.

## Examples
* [IFTTT](examples/ifttt.md)

## References