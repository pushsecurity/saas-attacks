# Guest User Access
ID: SAT1044

## Tactics
* Privilege Escalation
* Initial Access

## Summary

In SaaS platforms like Salesforce, ServiceNow, and Zendesk, misconfigurations related to guest user permissions can lead to unauthorized data access or escalation of privileges. These platforms often allow guest/unauthenticated users limited access for specific purposes. However, if the guest access is not correctly configured, it may grant broader permissions than intended.

An attacker can exploit such misconfigurations by accessing a guest account and leveraging the excessive permissions to access or manipulate sensitive data, potentially leading to a full account takeover or data breach.

## Examples
* [Salesforce guest user misconfiguration allowing data access](https://arstechnica.com/information-technology/2023/04/misconfigured-servers-running-salesforce-software-are-leaking-sensitive-data/).
* [ServiceNow instance where guest users could access PII Data](https://www.csoonline.com/article/572239/nearly-70-of-servicenow-instances-leaking-data.html).

## References

* [Give Secure Access to Unauthenticated Users with the Guest User Profile](https://help.salesforce.com/s/articleView?id=sf.networks_public_access.htm&type=5).
* [General Information | Potential Public List Widget Misconfiguration](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1553688).
