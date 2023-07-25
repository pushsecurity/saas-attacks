# MFA fatigue

## Tactics
* Initial Access

## Summary
One of the most common implementations of MFA is using push notifications to a mobile device that allow the user to approve or deny the login request. This is generally the most user friendly approach as a user can authenticate with the push of a button from their phone lock screen, without needing to read a code from another app and type it in anywhere.

An adversary can exploit this process by continually making login requests with compromised credentials at inconvenient times (e.g. the middle of the night) or generally with an annoying frequency. Even if the user initially rejects the push notifications initially it can quickly become infuriating to receive ongoing push notifications and lead to an assumption that perhaps something legitimate is continually failing to authenticate and just needs to be approved to make the problem go away.

Eventually, the user only needs to click to approve the login once, whether through mistake or frustration, and the adversary will gain access to their account. 

## Examples


## References
* [Uber breach by Lapsus$](https://www.darkreading.com/attacks-breaches/uber-breach-external-contractor-mfa-bombing-attack)
