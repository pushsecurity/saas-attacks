# ConsentFix
ID: SAT1051

## Tactics
* Initial Access
* Defense Evasion

## Summary

ConsentFix is a social engineering technique that combines ClickFix-style deception with OAuth authorization code theft. An adversary presents a fake verification screen — often impersonating a Cloudflare Turnstile or similar challenge — that prompts the target to sign in via a legitimate OAuth flow. The attack abuses a trusted first-party OAuth application (such as Azure CLI) to avoid consent prompts, making the login page appear entirely legitimate.

After the target authenticates, their browser is redirected to a localhost URI, which generates a URL in the browser's address bar that contains an OAuth authorization code. The phishing page instructs the target to paste this URL back as part of the "verification" process. The attacker extracts the authorization code from the pasted URL and exchanges it for an access token, gaining full access to the target's account.

Because the target authenticates through a legitimate identity provider and no credentials or MFA tokens are ever exposed to the attacker, this technique bypasses MFA including phishing-resistant methods such as passkeys.

A demo video explaining how ConsentFix works is given below:

[![demo video](https://img.youtube.com/vi/AAiiIY-Soak/0.jpg)](https://www.youtube.com/watch?v=AAiiIY-Soak)

## Examples
* [Microsoft](examples/microsoft.md)

## References
* [ConsentFix - Push Security blog](https://pushsecurity.com/blog/consentfix/)
* [MITRE ATT&CK - Phishing: Spearphishing Link](https://attack.mitre.org/techniques/T1566/002/)
