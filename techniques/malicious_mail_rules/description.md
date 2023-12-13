# Malicious mail rules
ID: SAT1023

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
* [Malicious Outlook Rules - Technical blog post](https://www.netspi.com/blog/technical/adversary-simulation/malicious-outlook-rules/)
* [Ruler - A tool to abuse Exchange services](https://github.com/sensepost/ruler)
* [XRulez - A command line tool for creating malicious outlook rules](https://github.com/FSecureLABS/XRulez)
* [MITRE ATT&CK - Email Forwarding Rule](https://attack.mitre.org/techniques/T1114/003/)
* [Multi-account Office365 compromise using mail rules](https://darktrace.com/blog/breakdown-of-a-multi-account-compromise-within-office-365)
* [Microsoft blog - Mail rules used to hide attacks](https://www.microsoft.com/en-us/security/blog/2023/12/12/threat-actors-misuse-oauth-applications-to-automate-financially-driven-attacks/)
