# Slug tenant enumeration

## Tactics
* Reconnassiance

## Summary
SaaS vendors make use of different strategies to separate tenants from one another. Often, this is based on the creation of a “slug” chosen by the user during tenant creation. This is used as either a path separator, query parameter, or subdomain to separate tenants.

There are often methods within a SaaS app that allow existing slugs to be enumerated, for example, when attempting to create a new tenant the app may error stating that a tenant with that slug already exists.

It is common for the organization name itself to be used, or something very close to it, so querying a number of variations of the organization name is often a method for discovering if a SaaS app is in use and what the tenant name is.


## Examples
* [BambooHR](examples/bamboohr.md)

## References
* [MITRE ATT&CK - Wordlist Scanning](https://attack.mitre.org/techniques/T1595/003/)
