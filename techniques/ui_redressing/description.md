# UI redressing
ID: SAT1049

## Tactics
* Initial access

## Summary
UI redressing attacks can be used to trick a user into performing an action on a legitimate application that is different to what they perceived. The classic example is Clickjacking, that operates by overlaying an invisible iframe over a malicious website. The user thinks they are clicking buttons or other elements on the visible malicious site but are actually clicking buttons in the invislbe iframe that perform actions on the target website.

While Clickjacking is generally blocked by default due to modern browser controls, the discovery of [DoubleClickjacking](https://www.paulosyibelo.com/2024/12/doubleclickjacking-what.html) has increased the risk of this class of attack again. DoubleClickjacking is not protected against by default and has additionally been shown to be highly effective for performaning malicious OAuth consent grants, similar to a [consent phishing attack](/techniques/consent_phishing/description.md). 

## Examples
* [Salesforce](https://youtu.be/4rGvRRMrD18)
* [Slack](https://youtu.be/r7qpY74jtTw)
* [Shopify](https://youtu.be/DTdyvzfVPcI)

## References

* [OWASP - Clickjacking](https://owasp.org/www-community/attacks/Clickjacking)
* [Technical blog - DoubleClickjacking: A New Era of UI Redressing](https://www.paulosyibelo.com/2024/12/doubleclickjacking-what.html)
