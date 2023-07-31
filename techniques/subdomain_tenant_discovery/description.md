# Subdomain tenant discovery

## Tactics
* Reconnassiance

## Summary
SaaS vendors make use of different strategies to separate different tenants from one another. One of these methods is the use of a unique subdomain, which is often picked during the creation of a new tenant.

Consequently, DNS enumeration techniques to discover valid subdomains can give an insight into who uses a given SaaS app. For example, adversaries can use DNS brute forcing or passive DNS enumeration to discover this information.

It’s common for the organization name itself to be used, making it easy to discover these tenant names or subdomains.

## Examples
* [BambooHR](examples/bamboohr.md)

## References
* [MITRE ATT&CK - Wordlist Scanning](https://attack.mitre.org/techniques/T1595/003/)
