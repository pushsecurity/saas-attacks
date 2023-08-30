# OAuth token leakage
ID: SAT1040

## Tactics
* Initial Access

## Summary 

During the OAuth authorization code flow, after a user grants permission to a third-party application, the service provider generates an authorization code and redirects the user's browser back to the third-party application's specified *redirect_uri*. This *redirect_uri* is an endpoint on the third-party application's server where the authorization code will be sent. If the third-party application's server doesn't properly validate the *redirect_uri* when receiving the authorization code callback, an attacker could modify the *redirect_uri* parameter during the authorization request to point to a malicious server they control.

This may allow an adversary to intercept the authorization code and use it to request an access token for the victim's account from the service provider. This access token can then be used to access the victim's resources without their consent.

## Examples

## References

* [OWASP - Testing for OAuth Authorization Server Weaknesses](https://owasp.org/www-project-web-security-testing-guide/latest/4-Web_Application_Security_Testing/05-Authorization_Testing/05.1-Testing_for_OAuth_Authorization_Server_Weaknesses) 