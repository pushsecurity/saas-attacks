# Password scraping
ID: SAT1028

## Tactics
* Credential Access

## Summary

While it may not be security good practice, many teams stored passwords in cleartext, especially shared or system credentials. This could be passwords stored in files that are hosted in SaaS file stores, passwords noted in wikis or ticketing systems or passwords sent in emails during registration processes or as a result of forgotten password functionality.

One more modern example is that some SaaS apps allow passwordless email-based authentication, where a OTP is sent via email when a login is requested, rather than a user having a standard password.

An adversary could search for passwords via compromised apps in order to discover passwords that may allow them to move laterally to other apps and potentially as different user accounts too.

Additionally, cloud password managers are ripe targets for password scraping as compromising a cloud identity that allows direct access to a cloud password manager can enable large-scale password scraping.


## Examples
* [Okta](examples/okta.md)
* [Canva](examples/canva.md)


## References
* [MITRE ATT&CK - Unsecured Credentials](https://attack.mitre.org/techniques/T1552/)
* [Abusing Okta SWA - Technical blog post](https://pushsecurity.com/blog/okta-swa/)
* [Can my admins steal my cloud password manager secrets? - Technical blog post](https://pushsecurity.com/blog/can-my-admins-steal-my-cloud-password-manager-secrets/)
