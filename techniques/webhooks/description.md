# Webhooks

## Tactics
* Defense Evasion
* Exfiltration

## Summary
Some SaaS apps allow webhooks to be configured so callbacks are made when certain events are triggered. For example, a webmail platform may allow a webhook callback when a new email is received.         

This is useful to an adversary looking to extract new data as it is created from that API. This could be new emails, new files, a real-time view into channels in instant messaging apps, etc.

Adversaries using this technique may also evade detection controls as these are not requests made to the SaaS app (showing in logs) but rather requests to an attacker app made from the app.

## Examples
* [Microsoft 365](examples/microsoft_365.md)

## References
* [MITRE ATT&CK - Exfiltration Over Web Service](https://attack.mitre.org/techniques/T1567/)
