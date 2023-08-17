# Link sharing
ID: SAT1022

## Tactics
* Persistence
* Defense Evasion

## Summary
Many SaaS apps offer the ability to share items with third parties through sharing links. A file storage app may allow a document to be shared with a third party either through explicitly sharing with named accounts in a separate tenant or through creation of an anonymous/public-sharing link.

An adversary can create sharing links to maintain persistent access to data if the password is changed or the compromised account is disabled. Access to resources that have been shared anonymously are usually not logged in the same detail, can’t be attributed to a specific user, and can be used to evade audit controls.

## Examples
* [OneDrive](examples/onedrive.md)
* [Nuclino](examples/nuclino.md)

## References