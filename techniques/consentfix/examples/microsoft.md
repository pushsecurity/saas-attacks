# ConsentFix - Microsoft

## Overview

ConsentFix targets Microsoft accounts by abusing the Azure CLI OAuth application, a first-party Microsoft app that enjoys implicit tenant trust and does not require a user-facing consent prompt.

## Attack flow

1. The target encounters a malicious or compromised site (often surfaced via Google Search) displaying a fake Cloudflare Turnstile verification screen.
2. The page asks for a business email address to filter targets.
3. The target clicks a "Sign In" button that opens a legitimate Microsoft login URL, pre-configured to use Azure CLI as the OAuth application.
4. After signing in (or selecting an existing account), Microsoft redirects the browser to `localhost` — the registered redirect URI for Azure CLI. This redirect generates a URL in the address bar containing an OAuth authorization code.
5. The phishing page instructs the target to copy this URL and paste it back into the page as the final "verification" step.
6. The attacker extracts the authorization code from the pasted URL and exchanges it with Microsoft's token endpoint for an access token.

## Impact

The attacker gains OAuth access to the victim's Microsoft account without ever seeing their password or MFA factors. Because the authentication flow is entirely legitimate, this technique works even against organizations enforcing phishing-resistant authentication (e.g. passkeys, FIDO2 hardware keys).

## References
* [ConsentFix - Push Security blog](https://pushsecurity.com/blog/consentfix/)
