<div align="center">

[![badge](https://img.shields.io/badge/Push%20Security-Sponsored%20Project-blue.svg?logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0nMzExJyBoZWlnaHQ9JzE1Mycgdmlld0JveD0nMCAwIDMxMSAxNTMnIGZpbGw9J25vbmUnIHhtbG5zPSdodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2Zyc+PHBhdGggZD0nTTIzNS4wMjIgMTUyLjEwN0MyNzYuODU2IDE1Mi4xMDcgMzEwLjkwMSAxMTguMDk2IDMxMC45MDEgNzYuMzA0OUMzMTAuOTAxIDM0LjUxMzQgMjc2Ljg3MSAwLjUwMjkzIDIzNS4wMjIgMC41MDI5M0MxOTMuMTc0IDAuNTAyOTMgMTU5LjE0NCAzNC41MTM0IDE1OS4xNDQgNzYuMzA0OUMxNTkuMTQ0IDExOC4wOTYgMTkzLjE4OCAxNTIuMTA3IDIzNS4wMjIgMTUyLjEwN1pNMjAyLjc1IDQ0LjA2NDlDMjExLjM3MyAzNS40NTA3IDIyMi44MjUgMzAuNzA0NyAyMzUuMDIyIDMwLjcwNDdDMjQ3LjIxOSAzMC43MDQ3IDI1OC42NzIgMzUuNDUwNyAyNjcuMjk1IDQ0LjA2NDlDMjc1LjkxOCA1Mi42NzkxIDI4MC42NjkgNjQuMTM0OSAyODAuNjY5IDc2LjMwNDlDMjgwLjY2OSA4OC40NzQ4IDI3NS45MTggOTkuOTMwNyAyNjcuMjk1IDEwOC41NDVDMjU4LjY3MiAxMTcuMTU5IDI0Ny4yMTkgMTIxLjkwNSAyMzUuMDIyIDEyMS45MDVDMjIyLjgyNSAxMjEuOTA1IDIxMS4zNzMgMTE3LjE1OSAyMDIuNzUgMTA4LjU0NUMxOTQuMTI3IDk5LjkzMDcgMTg5LjM5MSA4OC40NzQ4IDE4OS4zOTEgNzYuMzA0OUMxODkuMzkxIDY0LjEzNDkgMTk0LjE0MiA1Mi42NzkxIDIwMi43NSA0NC4wNjQ5WicgZmlsbD0nI0ZENzQ1MicvPjxwYXRoIGQ9J00xNDIuMjg3IDAuNTAyOTNMNTQuNjU3NyAxNTIuMTA3SDg5LjU4MTNMMTc3LjE5NiAwLjUwMjkzSDE0Mi4yODdaJyBmaWxsPScjRkQ3NDUyJy8+PHBhdGggZD0nTTg3LjYyOTEgMC41MDI5M0wwIDE1Mi4xMDdIMzQuOTIzNkwxMjIuNTUzIDAuNTAyOTNIODcuNjI5MVonIGZpbGw9JyNGRDc0NTInLz48L3N2Zz4=)](https://pushsecurity.com)
 [![badge](https://img.shields.io/badge/BlueHat_--_The_new_SaaS_cyber_kill_chain-white?logo=youtube&logoColor=FF0000&style=s)](https://www.youtube.com/watch?v=pdDzUTFVIZc)
[![badge](https://img.shields.io/twitter/follow/jukelennings?style=social)](https://twitter.com/jukelennings)
[![badge](https://img.shields.io/twitter/follow/jacques_sec?style=social)](https://twitter.com/jacques_sec)
[![badge](https://img.shields.io/twitter/follow/pushsecurity?style=social)](https://twitter.com/pushsecurity)

<a href="https://pushsecurity.com">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/pushsecurity/saas-attacks/assets/95348608/7b32b771-5774-4b58-bd2b-1b8cd82c8857">
  <img src="https://github.com/pushsecurity/saas-attacks/assets/95348608/f732944a-9066-4e5d-a0a3-8e1b77ee0526">
</picture>
</a>

</div>

# SaaS attack techniques

This repository is a collection of SaaS-specific attack techniques. It is intended to be a resource for security researchers, red/blue teams, and penetration testers to learn about and share SaaS attack techniques.

> Quick note: we wanted to start sharing as early as possible, so this is very much a work in progress. Hopefully there is enough to see the shape of things to come, but no doubt there are gaps - we'll be filling them in over the coming weeks and months. If you can help fill in some references, add examples, or point us to missing techniques - please open an issue (or even a PR)! We'll be very sure to credit you.

For more information on the background to this project, check the following [blog post](https://pushsecurity.com/blog/saas-attack-techniques/)

The Microsoft BlueHat 2023 "The new SaaS cyber kill chain" presentation that covers a lot of this research can be found below: 

[BlueHat - The new SaaS cyber kill chain](https://www.youtube.com/watch?v=pdDzUTFVIZc)

For a podcast covering this topic, checkout the DCP Podcast by SpectreOps below:

[DCP Podcast - Episode 35](https://www.youtube.com/watch?v=NAOE875gAOg)

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
||[IM user spoofing](techniques/im_user_spoofing/description.md)||[Inbound federation](techniques/inbound_federation/description.md)||[Device code phishing](techniques/device_code_phishing/description.md)|||[SAMLjacking](techniques/samljacking/description.md)||
||[nOAuth](techniques/noauth/description.md)||[Device enrollment](techniques/device_enrollment/description.md)||[Session cookie theft](techniques/session_cookie_theft/description.md)|||[Inbound federation](techniques/inbound_federation/description.md)||
||[MFA fatigue](techniques/mfa_fatigue/description.md)|||||||[Session cookie theft](techniques/session_cookie_theft/description.md)||
||[Device code phishing](techniques/device_code_phishing/description.md)|||||||||
||[Hijack OAuth flows](techniques/hijack_oauth_flows/description.md)|||||||||
||[AiTM Phishing](techniques/aitm_phishing/description.md)|||||||||
||[Device enrollment](techniques/device_enrollment/description.md)|||||||||


Another divergence from the ATT&CK framework is that these techniques are not solely based on observation. Instead, we’re allowing more exploratory techniques that haven't been seen in the wild. We think this is important because SaaS is a relatively new attack surface, and we want to encourage security researchers to think creatively about how SaaS can be abused to better anticipate future attacks.

We’ve also removed a few columns that are common in these MITRE-style frameworks, some (like Impact) are so similar they aren't worth duplicating. Others (perhaps most notably the Command & Control phase) because they no longer apply. Since SaaS is delivered directly on the internet, you can’t force an attacker to access it through your web gateway. You can try forcing your own employees through a gateway, but attackers can access it directly like everyone else (there are edge cases here, but they are rare). This means there is generally no need for C2 techniques.

Finally, some need a slightly broader definition. For example, the Execution phase includes techniques that are not strictly code execution on an endpoint, but achieve an equivalent outcome in the SaaS context.

## Scope

When we started this research project, the first task was to choose an initial scope. Like every good red-teamer, we wanted to start with low-cost techniques, so that means we were looking for techniques that:
* Avoid highly effective controls that are expensive to bypass, especially endpoint controls like EDR - so endpoint malware-based techniques are out
* Look for features that can be abused long-term, rather than bugs that will be patched quickly - so no zero-days
* Go beyond the dozen or so core SaaS apps like O365 and Google Workspace - look to the hundreds of other apps that have primitive security controls and store or have access to highly sensitive data

While we left out techniques that are endpoint-based attacks that lead to a SaaS compromise (MITRE does a good job of these techniques) we think that it makes sense to add techniques to go from SaaS to the endpoint might make sense to add here. We're still thinking about this, but we'd love to hear your thoughts.
