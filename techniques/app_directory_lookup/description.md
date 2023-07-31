# App directory lookup

## Tactics
* Discovery

## Summary
SaaS apps will generally have a user directory and often this is visible to any user of the app. It may be a direct list of all users of the app or a result of visible group memberships or similar.

An adversary who has gained a foothold via a SaaS app could download the list of users accessible to them in order to better target attacks against other users. Commonly, usernames or emails for users will be identical on other SaaS apps, potentially helping target users of those apps.

## Examples
* [Shortcut](examples/shortcut.md)

## References
* [MITRE ATT&CK - Account Discovery](https://attack.mitre.org/techniques/T1087/)
