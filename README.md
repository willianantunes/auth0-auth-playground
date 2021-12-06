# Auth0 Auth Playground

Just playing a bit around with Auth0.

I'm exploring, so do not consider this project as a real one (if you look at the code, you're going to laugh, haha).
This is far to be considered a production-ready one.

## Notes

### Configuring it to run locally

Instead of using `localhost`, please configure your `hosts` adding `app.local` to answer for your loopback address. If you configure your Application on Auth0 using `localhost`, the user will have to consent all scopes you're asking for.

### OpenID Configuration Request

You can get your [OpenID Configuration Request](https://openid.net/specs/openid-connect-discovery-1_0.html#ProviderConfigurationRequest)
through the following URL:

    https://{domain}/.well-known/openid-configuration

Giving how this project is configured:

    https://antunes.us.auth0.com/.well-known/openid-configuration

Sample output:

```json
{
  "issuer": "https://antunes.us.auth0.com/",
  "authorization_endpoint": "https://antunes.us.auth0.com/authorize",
  "token_endpoint": "https://antunes.us.auth0.com/oauth/token",
  "device_authorization_endpoint": "https://antunes.us.auth0.com/oauth/device/code",
  "userinfo_endpoint": "https://antunes.us.auth0.com/userinfo",
  "mfa_challenge_endpoint": "https://antunes.us.auth0.com/mfa/challenge",
  "jwks_uri": "https://antunes.us.auth0.com/.well-known/jwks.json",
  "registration_endpoint": "https://antunes.us.auth0.com/oidc/register",
  "revocation_endpoint": "https://antunes.us.auth0.com/oauth/revoke",
  "scopes_supported": [
    "openid",
    "profile",
    "offline_access",
    "name",
    "given_name",
    "family_name",
    "nickname",
    "email",
    "email_verified",
    "picture",
    "created_at",
    "identities",
    "phone",
    "address"
  ],
  "response_types_supported": [
    "code",
    "token",
    "id_token",
    "code token",
    "code id_token",
    "token id_token",
    "code token id_token"
  ],
  "code_challenge_methods_supported": [
    "S256",
    "plain"
  ],
  "response_modes_supported": [
    "query",
    "fragment",
    "form_post"
  ],
  "subject_types_supported": [
    "public"
  ],
  "id_token_signing_alg_values_supported": [
    "HS256",
    "RS256"
  ],
  "token_endpoint_auth_methods_supported": [
    "client_secret_basic",
    "client_secret_post"
  ],
  "claims_supported": [
    "aud",
    "auth_time",
    "created_at",
    "email",
    "email_verified",
    "exp",
    "family_name",
    "given_name",
    "iat",
    "identities",
    "iss",
    "name",
    "nickname",
    "phone_number",
    "picture",
    "sub"
  ],
  "request_uri_parameter_supported": false
}
```

## Links

Architecture/Project:

- [Project Planning Guide](https://auth0.com/docs/architecture-scenarios/b2c/architecture#project-planning-guide)
- [Implementation Planning Checklists](https://auth0.com/docs/architecture-scenarios/checklists)

Projects:

- [auth0-samples/auth0-django-web-app](https://github.com/auth0-samples/auth0-django-web-app/tree/master/01-Login)

Articles:

- [Python API: Authorization](https://auth0.com/docs/quickstart/backend/python/01-authorization)
- [Use HashiCorp Terraform to Manage Your Auth0 Configuration](https://auth0.com/blog/use-terraform-to-manage-your-auth0-configuration/)

Forums:

- [Prompt user for information during signup](https://community.auth0.com/t/prompt-user-for-information-during-signup/6767)
- [How do I skip the consent page for my API Authorization flow?](https://community.auth0.com/t/how-do-i-skip-the-consent-page-for-my-api-authorization-flow/6035)
- [How to allow the end-user to update their own profile information?](https://community.auth0.com/t/how-to-allow-the-end-user-to-update-their-own-profile-information/6228)
- [How to set name as required field for user?](https://community.auth0.com/t/how-to-set-name-as-required-field-for-user/54780/3)
- [Can you use Universal Login page for both passwordless AND “standard” login?](https://community.auth0.com/t/can-you-use-universal-login-page-for-both-passwordless-and-standard-login/24830)
- [Structure of @@config@@](https://community.auth0.com/t/structure-of-config/9155)

APIs:

- [Authentication API](https://auth0.com/docs/api/authentication)
- [Auth0 Management API](https://auth0.com/docs/api/management/v2/)
