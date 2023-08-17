# Passwordless logins
ID: SAT1029

## Tactics
* Lateral Movement

## Summary
Some SaaS apps allow passwordless email-based authentication, where an OTP is sent via email when a login is requested, rather than a user having a standard password.

An adversary with email access could laterally move to other SaaS apps that support this login type. This technique has the added benefit of avoiding detection due to a user noticing that their credentials have been altered.

## Examples
* [Canva](examples/canva.md)
* [Slack](examples/slack.md)
* [Expensify](examples/expensify.md)
## References