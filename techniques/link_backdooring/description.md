# Link backdooring
ID: SAT1021

## Tactics
* Privilege Escalation
* Lateral Movement

## Summary
Users have long been trained to be wary of clicking links from external sources such as email. However, they don’t usually exercise the same caution when clicking links within trusted apps.

Many SaaS apps have functionality to include links to other systems. For example, SaaS-based Office documents may have links in them, tickets in ticket tracking systems and wikis can be especially link-heavy. Often these systems don’t exercise the same link security you would expect in external email, so malicious links can be more easily obfuscated to appear legitimate, even if a user checks.

An adversary who has gained a foothold into a trusted SaaS app where links are common could automate backdooring links in the app to direct to a phishing site they control. Since users are used to their sessions or SSO logins expiring, they’ve grown accustomed to clicking a (seemingly legitimate) link within a trusted system. This makes sending users to a phishing site within a trusted app that much easier because it looks like the standard SSO login page.

Wiki-style apps are a particularly interesting target for this type of attack as links are commonplace and individual users can often edit fairly large amounts of content (and links included therein). Adversaries can even use APIs to automate updating these links.


## Examples
* [Nuclino](examples/nuclino.md)

## References
* [Evilginx - MITM framework for phishing login credentials](https://github.com/kgretzky/evilginx2)
