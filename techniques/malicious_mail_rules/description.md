# Malicious mail rules

## Tactics
* Persistence
* Privilege Escalation
* Defense Evasion

## Summary
Common SaaS mail providers like Office365 and Gmail provide mail rule functionality that allows users to automate certain tasks on their mailboxes. This includes forwarding, moving emails, marking them as read and deleting them.

This can be used maliciously for multiple purposes. Mail rules persist after account changes, such as password resets. So one obvious tactic is to use them to persist access to a compromised mailbox by setting up auto-forwarding rules for all emails (or ones with interesting keywords, like “password reset” or “invoice”) to an external address - this is typical in BEC-style attacks.

By intercepting password or MFA reset emails through forwarding and auto-delete rules, mail rules can be used to move laterally to compromise accounts for other SaaS apps, while also avoiding alerting the user to the malicious activity.

## Examples
* [Office 365](examples/office_365.md)

## References