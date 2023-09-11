# Shadow workflows
ID: SAT1033

## Tactics
* Execution
* Exfiltration

## Summary

The SaaS world is, by design, largely abstracted away from operating systems and application binaries. There isn’t always a generic equivalent of gaining code execution as you might during an endpoint compromise.

The closest approximation to this in the SaaS world may be low- or no-code automation apps. These are SaaS apps that are focused on integrating with a variety of other SaaS apps and allow the user to automate common tasks. In no-code apps this is done using easy-to-learn UI components that abstract code, where low-code flavors provide scaffolding to minimize code. The user created functions are often called automations, workflows or playbooks.

An adversary with access to a target SaaS account can configure a workflow automation to execute a wide range of malicious actions against the breached account. This could be a daily export of files from shared cloud drives, automatic forwarding and deleting of emails, cloning instant messages, exporting user directories. Basically anything that is possible using the target app’s API.

While the graphical interface is useful for non-technical users, many of these automation platforms allow advanced users to craft direct API calls (often called low-code), which unlocks enormous flexibility for adversaries.

Akin to traditional endpoint “Living Off The Land” (LOTL) techniques such as PowerShell, an adversary may use these legitimate, well-known SaaS automation apps rather than custom OAuth integrations to avoid detection.

A demo video of an attack chain combining a shadow workflow with an [evil twin integration](/techniques/evil_twin_integrations/description.md) is given below:
 
[![demo video](https://img.youtube.com/vi/g2EITjjJH1s/0.jpg)](https://www.youtube.com/watch?v=g2EITjjJH1s)

## Examples
* [Zapier](examples/zapier.md)
* Microsoft Power Automate

## References

* [Living off the Cloud. Cloudy with a Chance of Exfiltration](https://www.pentestpartners.com/security-blog/living-off-the-cloud-cloudy-with-a-chance-of-exfiltration/)
* [MITRE ATT&CK - Automated Exfiltration](https://attack.mitre.org/techniques/T1020/)
* [The shadow workflow's evil twin - Technical blog post](https://pushsecurity.com/blog/nearly-invisible-attack-chain/)
