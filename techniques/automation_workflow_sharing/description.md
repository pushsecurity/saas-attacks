# Automation workflow sharing

## Tactics
* Execution
* Lateral Movement

## Summary
Some SaaS automation apps allow pre-configured automations to be shared with other users. These can sometimes be shared directly within the app with other app users.

Since automations are incredibly powerful, it is possible for an adversary to create an automation that is designed to appear safe but to backdoor it in a way that performs a malicious action on behalf of the target user. If a user does not inspect the configuration of the automation at all, the automation can be more overtly malicious.

However, by making complicated multi-step automations and making use of built-in logging functionality, it is possible to make automations that can easily pass a cursory examination, while still achieving the adversary’s goals.

This is the SaaS equivalent of convincing a user to open a malicious attachment or run an executable file.

## Examples
* [Microsoft Power Automate](examples/microsoft_power_automate.md)

## References