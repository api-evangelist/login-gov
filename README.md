# Login.gov (login-gov)

Login.gov is the U.S. federal government's secure single sign-on and identity verification service for the public, operated by the General Services Administration's Technology Transformation Services (GSA TTS). Relying parties — federal, and in some cases state and local — federate user authentication to Login.gov via OpenID Connect (iGov profile) or SAML 2.0, with support for IAL1 (auth-only) and IAL2 (identity-verified) assurance and AAL2 multi-factor authentication including phishing-resistant and PIV/CAC authenticators.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/login-gov/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=government-api-evangelist&utm_content=login-gov)

## Tags

Government, Federal, GSA, Identity, Authentication, SSO, OIDC, SAML, IAL2, AAL2

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Environments

| Environment | OIDC issuer | SAML base | Use |
|---|---|---|---|
| Sandbox | `https://idp.int.identitysandbox.gov` | `https://idp.int.identitysandbox.gov` | Free; test users only; sign up at [portal.int.identitysandbox.gov](https://portal.int.identitysandbox.gov) |
| Production | `https://secure.login.gov` | `https://secure.login.gov` | Requires signed Interagency Agreement (IAA) |

## Assurance Levels

| Level | Meaning | Login.gov `acr_values` |
|---|---|---|
| IAL1 | Authentication only | `urn:acr.login.gov:auth-only` |
| IAL2 | Identity-verified | `urn:acr.login.gov:verified` |
| IAL2 + Facial Match (required) | Identity-verified, facial match mandatory | `urn:acr.login.gov:verified-facial-match-required` |
| IAL2 + Facial Match (preferred) | Identity-verified, facial match optional | `urn:acr.login.gov:verified-facial-match-preferred` |
| AAL2 | Multi-factor | `http://idmanagement.gov/ns/assurance/aal/2` |
| AAL2 phishing-resistant | Security keys, PIV/CAC, platform passkeys | `http://idmanagement.gov/ns/assurance/aal/2?phishing_resistant=true` |
| AAL2 HSPD-12 | PIV/CAC only | `http://idmanagement.gov/ns/assurance/aal/2?hspd12=true` |

## APIs

### Login.gov OpenID Connect API

iGov-profile OpenID Connect surface for relying parties. Authorization code flow with `private_key_jwt` (web apps) or PKCE (native apps). Implicit flow is **not** supported.

**Human URL:** [https://developers.login.gov/oidc/](https://developers.login.gov/oidc/)

- [Documentation — OIDC overview](https://developers.login.gov/oidc/)
- [Documentation — Getting started](https://developers.login.gov/oidc/getting-started/)
- [Documentation — Authorization](https://developers.login.gov/oidc/authorization/)
- [Documentation — Token](https://developers.login.gov/oidc/token/)
- [Documentation — UserInfo](https://developers.login.gov/oidc/user-info/)
- [Documentation — Logout](https://developers.login.gov/oidc/logout/)
- [Documentation — Certificates / JWKS](https://developers.login.gov/oidc/certificates/)
- [OpenAPI](openapi/login-gov-oidc-openapi.yml)
- [JSON Schema — UserInfo](json-schema/login-gov-userinfo-schema.json)
- [JSON Schema — ID Token](json-schema/login-gov-id-token-schema.json)
- [JSON-LD context](json-ld/login-gov-context.jsonld)
- [Naftiko Capability — OIDC Authentication](capabilities/oidc-authentication.yaml)
- [Spectral Ruleset](rules/login-gov-rules.yml)

### Login.gov SAML 2.0 API

SAML 2.0 federation for relying parties that prefer SAML. HTTP-Redirect SSO, HTTP-POST SLO, persistent UUID v4 NameID, year-versioned endpoints (`2026` certificates valid through April 1, 2027).

**Human URL:** [https://developers.login.gov/saml/](https://developers.login.gov/saml/)

- [Documentation — SAML overview](https://developers.login.gov/saml/)
- [Documentation — Getting started](https://developers.login.gov/saml/getting-started/)
- [OpenAPI](openapi/login-gov-saml-openapi.yml)
- [Naftiko Capability — SAML Authentication](capabilities/saml-authentication.yaml)

## Scopes & Attributes

| Scope | Attribute(s) | IAL2 required |
|---|---|---|
| `openid` | `sub` | No |
| `email` | `email`, `email_verified` | No |
| `all_emails` | `all_emails` | No |
| `locale` | `locale` | No |
| `profile:name` | `given_name`, `family_name` | Yes |
| `profile:birthdate` | `birthdate` | Yes |
| `profile:verified_at` | `verified_at` | Yes |
| `profile` | name + birthdate + verified_at | Yes |
| `address` | `address` | Yes |
| `phone` | `phone`, `phone_verified` | Yes |
| `social_security_number` | `social_security_number` | Yes |
| `x509` / `x509:subject` / `x509:issuer` / `x509:presented` | x509 claims | No (PIV/CAC) |

## Examples

- [UserInfo — IAL1 response](examples/login-gov-userinfo-ial1-example.json)
- [UserInfo — IAL2 response](examples/login-gov-userinfo-ial2-example.json)
- [Token exchange](examples/login-gov-token-exchange-example.json)

## Pricing & Limits

- [Plans (cost-recoverable IAA model)](plans/login-gov-plans-pricing.yml)
- [Rate limits](rate-limits/login-gov-rate-limits.yml)

## Open Source

Login.gov is built in the open under the GSA / 18F GitHub organization.

- [identity-idp](https://github.com/18F/identity-idp) — the Login.gov IdP (Ruby on Rails)
- [identity-oidc-sinatra](https://github.com/18F/identity-oidc-sinatra) — sample OIDC relying party
- [identity-saml-sinatra](https://github.com/18F/identity-saml-sinatra) — sample SAML relying party

## Other Resources

- [Login.gov public site](https://www.login.gov)
- [Become a partner](https://www.login.gov/partners/get-started/)
- [Business inquiries](https://www.login.gov/partners/business-inquiries/)
- [Status](https://status.login.gov)
- [Privacy policy](https://www.login.gov/policy/)
- [Accessibility](https://www.login.gov/accessibility/)
- [Vocabulary](vocabulary/login-gov-vocabulary.yml)

## Maintainers

- Kin Lane — info@apievangelist.com — [apievangelist.com](https://apievangelist.com)
