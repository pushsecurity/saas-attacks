# Okta SWA password scraping

Okta supports true SSO mechanisms like SAML and OIDC but also has an authentication method called SWA that operates more like a password manager. Administrators can restrict users from seeing their underlying passwords by disabling the "password reveal" feature if they like. However, it's possible to bypass this even if it is configured.

Consequently, an adversary compromising an Okta account can extract passwords to access all apps that have been configured using Okta SWA in order to maintain longer-term persistent access and potentially uncover passwords that are also shared with other accounts.

Full details can be found in the following blog post:

https://pushsecurity.com/blog/okta-swa/
