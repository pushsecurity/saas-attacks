# SAMLjacking

## Tactics
* Initial Access

## Summary

When configuring SAML integrations for a SaaS app, you must provide a URL to an IdP service so the app can hand-off authentication during the SAML flow. Users expect to be redirected to common SSO login pages (e.g. Google or Microsoft login), and are unlikely to check that the login URL they are redirected to matches the official domain.

An adversary could configure an app tenant with SAML and configure the URL to point to a credential phishing page that looks like or proxies a legitimate authentication service (e.g. Google or Microsoft).

The adversary could target users by sending seemingly legitimate links to the app login page to the tenant. This attack can be made more effective by naming the tenant something familiar for the target (few apps restrict the names of tenants) and using in-app invite mechanisms to lure victims to the tenant.

## Examples
* [Nuclino](examples/nuclino.md)

## References
[Evilginx - MITM framework for phishing login credentials](https://github.com/kgretzky/evilginx2)
