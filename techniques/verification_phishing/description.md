# Verification phishing
ID: SAT1048

## Tactics
* Initial access

## Summary
Email verification is sometimes used as a control, such as when registering new accounts. This is typically implemented by emailing the target user with either a clickable link for them to verify or a verification code that that they need to enter. 

Verification phishing is when an adversary uses phishing, or some other type of social engineering, to convince a user to click a verification link or pass them the verification code in order to defeat this control. This is most relevant when combined with [cross-idp impersonation](/techniques/cross-idp_impersonation/description.md) in order to circumvent strong SSO authentication to gain direct control of downstream SaaS applications. 

## References
* [Technical blog post - Verification phishing and cross-idp impersonation](https://pushsecurity.com/blog/a-new-class-of-phishing-verification-phishing-and-cross-idp-impersonation/)