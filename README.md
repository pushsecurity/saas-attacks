# SaaS attack techniques

This repository is a collection of SaaS-specific attack techniques. It is intended to be a resource for security researchers, red/blue teams, and penetration testers to learn about and share SaaS attack techniques.

> Quick note: we wanted to start sharing as early as possible, so this is very much a work in progress. Hopefully there is enough to see the shape of things to come, but no doubt there are gaps - we'll be filling them in over the coming weeks and months. If you can help fill in some references, add examples, or point us to missing techniques - please open an issue (or even a PR)! We'll be very sure to credit you.

For more information on the background to this project, check the following [blog post](https://pushsecurity.com/blog/saas-attack-techniques/)

## The SaaS attacks matrix

We’ve taken inspiration from the MITRE ATT&CK framework (certainly intended as the sincerest form of flattery), but wanted to make a conscious break away from the endpoint-focused ATT&CK techniques and instead focus on techniques that are SaaS-first. In fact, none of these techniques touch endpoints or customer networks - so we’re calling them networkless attacks.

| Reconnaissance | Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Exfiltration |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|[SAML enumeration](techniques/saml_enumeration/description.md)|[Consent phishing](techniques/consent_phishing/description.md)|[Shadow workflows](techniques/shadow_workflows/description.md)|[API keys](techniques/api_keys/description.md)|[Link backdooring](techniques/link_backdooring/description.md)|[API keys](techniques/api_keys/description.md)|[Password scraping](techniques/password_scraping/description.md)|[Email discovery](techniques/email_discovery/description.md)|[Link backdooring](techniques/link_backdooring/description.md)|[Takeout services](techniques/takeout_services/description.md)|
|[Subdomain tenant discovery](techniques/subdomain_tenant_discovery/description.md)|[Poisoned tenants](techniques/poisoned_tenants/description.md)|[OAuth tokens](techniques/oauth_tokens/description.md)|[OAuth tokens](techniques/oauth_tokens/description.md)|[Abuse existing OAuth integrations](techniques/abuse_existing_oauth_integrations/description.md)|[OAuth tokens](techniques/oauth_tokens/description.md)|[API secret theft](techniques/api_secret_theft/description.md)|[App directory lookup](techniques/app_directory_lookup/description.md)|[Abuse existing OAuth integrations](techniques/abuse_existing_oauth_integrations/description.md)|[Webhooks](techniques/webhooks/description.md)|
|[Slug tenant enumeration](techniques/slug_tenant_enumeration/description.md)|[SAMLjacking](techniques/samljacking/description.md)|[Client-side app spoofing](techniques/client-side_app_spoofing/description.md)|[Evil twin integrations](techniques/evil_twin_integrations/description.md)|[Malicious mail rules](techniques/malicious_mail_rules/description.md)|[Evil twin integrations](techniques/evil_twin_integrations/description.md)||[OAuth token enumeration](techniques/oauth_token_enumeration/description.md)|[API secret theft](techniques/api_secret_theft/description.md)|[Shadow workflows](techniques/shadow_workflows/description.md)|
|[DNS reconnaissance](techniques/dns_reconnaissance/description.md)|[Account ambushing](techniques/account_ambushing/description.md)||[Malicious mail rules](techniques/malicious_mail_rules/description.md)||[Malicious mail rules](techniques/malicious_mail_rules/description.md)|||[Passwordless logins](techniques/passwordless_logins/description.md)|
|[Username enumeration](techniques/username_enumeration/description.md)|[Credential stuffing](techniques/credential_stuffing/description.md)||[Link sharing](techniques/link_sharing/description.md)||[Link sharing](techniques/link_sharing/description.md)|||[Account recovery](techniques/account_recovery/description.md)||
||[App spraying](techniques/app_spraying/description.md)||[System integrations](techniques/system_integrations/description.md)||[System integrations](techniques/system_integrations/description.md)|||[In-app phishing](techniques/in-app_phishing/description.md)||
||[Email phishing](techniques/email_phishing/description.md)||[Ghost logins](techniques/ghost_logins/description.md)||[Ghost logins](techniques/ghost_logins/description.md)|||[IM user spoofing](techniques/im_user_spoofing/description.md)||
||[IM phishing](techniques/im_phishing/description.md)||[Client-side app spoofing](techniques/client-side_app_spoofing/description.md)||[Client-side app spoofing](techniques/client-side_app_spoofing/description.md)|||[Automation workflow sharing](techniques/automation_workflow_sharing/description.md)||
||[IM user spoofing](techniques/im_user_spoofing/description.md)||||[Device code phishing](techniques/device_code_phishing/description.md)|||[SAMLjacking](techniques/samljacking/description.md)||
||[nOAuth](techniques/noauth/description.md)|||||||||
||[MFA fatigue](techniques/mfa_fatigue/description.md)|||||||||
||[Device code phishing](techniques/device_code_phishing/description.md)|||||||||
||[Hijack OAuth flows](techniques/hijack_oauth_flows/description.md)|||||||||

Another divergence from the ATT&CK framework is that these techniques are not solely based on observation. Instead, we’re allowing more exploratory techniques that haven't been seen in the wild. We think this is important because SaaS is a relatively new attack surface, and we want to encourage security researchers to think creatively about how SaaS can be abused to better anticipate future attacks.

We’ve also removed a few columns that are common in these MITRE-style frameworks, some (like Impact) are so similar they aren't worth duplicating. Others (perhaps most notably the Command & Control phase) because they no longer apply. Since SaaS is delivered directly on the internet, you can’t force an attacker to access it through your web gateway. You can try forcing your own employees through a gateway, but attackers can access it directly like everyone else (there are edge cases here, but they are rare). This means there is generally no need for C2 techniques.

Finally, some need a slightly broader definition. For example, the Execution phase includes techniques that are not strictly code execution on an endpoint, but achieve an equivalent outcome in the SaaS context.

## Scope

When we started this research project, the first task was to choose an initial scope. Like every good red-teamer, we wanted to start with low-cost techniques, so that means we were looking for techniques that:
* Avoid highly effective controls that are expensive to bypass, especially endpoint controls like EDR - so endpoint malware-based techniques are out
* Look for features that can be abused long-term, rather than bugs that will be patched quickly - so no zero-days
* Go beyond the dozen or so core SaaS apps like O365 and Google Workspace - look to the hundreds of other apps that have primitive security controls and store or have access to highly sensitive data

While we left out techniques that are endpoint-based attacks that lead to a SaaS compromise (MITRE does a good job of these techniques) we think that it makes sense to add techniques to go from SaaS to the endpoint might make sense to add here. We're still thinking about this, but we'd love to hear your thoughts.
