# API keys
ID: SAT1004

## Tactics
* Persistence
* Defense Evasion

## Summary
Many SaaS apps let you configure an API key to enable programmatic access. These keys generally do not expire, are not affected by password resets, are not covered by MFA, and are often not even tied to user accounts. As such, they’re an ideal persistence mechanism as they survive the deletion of a compromised account. API actions are also often logged differently to normal user access, which makes them useful for evading monitoring of sensitive actions.

An adversary that has compromised an account could then read existing API keys from the app settings, if the app allows this, or create a new API key.

## Examples
* [Shortcut](examples/shortcut.md)

## References