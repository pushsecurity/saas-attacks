# API secret theft
ID: SAT1005

## Tactics
* Credential Access
* Lateral Movement

## Summary
Apps that support integrations through API keys (rather than the more common OAuth integrations) will sometimes allow those keys to be read after being set. Adversaries who gain access to apps where these integrations have been created can extract these secrets and use them to laterally move to different apps or contexts.

In apps that don’t explicitly make these secrets readable to the user, it might be possible to leak them out of the application. This is a typical scenario for build automation or CI/CD apps where build and deployment secrets are often exposed in clear-text inside the build environment.


## Examples
* [Postman](examples/postman.md)

## References
* [MITRE ATT&CK - Steal Application Access Token](https://attack.mitre.org/techniques/T1528/)
