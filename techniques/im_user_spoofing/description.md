# IM user spoofing

## Tactics
* Initial Access
* Lateral Movement

## Summary
Some instant messaging apps do not strongly control the way a user presents themselves in terms of display names, full names, user handles, photos, and so on.

Given that instant messaging systems are often focused on internal communications, users usually trust them. An adversary could take advantage of this to use a compromised account, or an external account where the instant messaging app permits cross-tenant communication (e.g. Slack connect or MS Teams), to spoof their identity to increase the success of phishing attacks and other social engineering attempts.

For example, a compromised user account could be renamed and have the photo changed to match the CEO and attempt CEO fraud by directly messaging members of the finance team. These profile details make CEO impersonation much more credible.

## Examples
* [Slack](examples/slack.md)

## References