# Account ambushing

## Tactics
* Initial Access

## Summary
Many SaaS apps have features that can be used to effectively backdoor an account, such as the ability to configure multiple login methods or create API keys to access the account programmatically. This makes it possible for an adversary to backdoor user accounts before they are first used by the legitimate user.

As some apps do not perform email verification during registration, it is often possible for an adversary to sign up for accounts using the potential target user’s email address.

When the real user attempts to sign up for the app, it will usually produce an error saying the account is already registered and prompt them to recover the account.

In such cases, the only way for the user to gain access to the app is to perform a password reset. If they do not discover the backdoor methods used by the adversary then the adversary will maintain access to their account and any sensitive data added to the app going forward.

## Examples
* [IFTTT](examples/ifttt.md)

## References