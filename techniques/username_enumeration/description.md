# Username enumeration
ID: SAT1038

## Tactics
* Reconnassiance

## Summary
When attempting to authenticate to a SaaS app, the login mechanism itself may disclose whether the username/email address is a known/valid account, even if the provided password is incorrect.
Since email addresses are commonly used during the authentication process and the domain associated will often give away the organization, checking known valid email address combinations for the target organization will often reveal whether the target organization is using the SaaS app, and could lead to the discovery of valid user accounts.

## Examples
* [Ramp](examples/ramp.md)
* [Expensify](examples/expensify.md)

## References
* [MITRE ATT&CK - Account Discovery](https://attack.mitre.org/techniques/T1087/)
* [Holehe - OSINT tool for finding registered accounts](https://github.com/megadose/holehe)