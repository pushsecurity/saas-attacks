# SAML enumeration

## Tactics
* Reconnassiance

## Summary

It’s often possible to determine if an organization is using a SaaS app by checking whether a SAML login IdP has been configured for the organization domain.

Where a dedicated SAML IdP endpoint has been configured, a SaaS app usually needs to map certain logins to that endpoint under certain conditions. Commonly, this will be based on the email domain of the user account, or based on a subdomain or path-based tenant separation.

If SAML is used, adversaries can discover whether a target organization is using a SaaS app and what their SAML provider is by making login attempts using their email domain, or by making login attempts via subdomains or path-based tenants based on the organization name.


## Examples
* [Ramp](examples/ramp.md)
* [Expensify](examples/expensify.md)

## References