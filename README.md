# Login.gov (login-gov)

Login.gov is the U.S. federal government's secure single sign-on and identity verification service for the public, operated by the General Services Administration's Technology Transformation Services (GSA TTS). Relying parties — federal, and in some cases state and local — federate user authentication to Login.gov via OpenID Connect (iGov profile) or SAML 2.0, with support for IAL1 (auth-only) and IAL2 (identity-verified) assurance and AAL2 multi-factor authentication including phishing-resistant and PIV/CAC authenticators.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/login-gov/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/login-gov/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- Government
- Federal
- GSA
- Identity
- Authentication
- SSO
- OIDC
- SAML
- IAL2
- AAL2

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Login.gov OpenID Connect API

The Login.gov OIDC integration surface used by relying parties. Conforms to the
iGov OpenID Connect Profile. Supports authorization code flow with
private_key_jwt (web apps) or PKCE (native apps); implicit flow is not supported.
Exposes discovery, JWKS, authorize, token, userinfo, and RP-initiated logout
endpoints in both sandbox (idp.int.identitysandbox.gov) and production
(secure.login.gov).

- **Human URL:** [https://developers.login.gov/oidc/](https://developers.login.gov/oidc/)
- **Base URL:** `https://secure.login.gov`

#### Tags

- OIDC
- OpenID Connect
- Authentication
- SSO
- Federal

#### Properties

- [Documentation](https://developers.login.gov/oidc/)
- [Documentation](https://developers.login.gov/oidc/getting-started/)
- [Documentation](https://developers.login.gov/oidc/authorization/)
- [Documentation](https://developers.login.gov/oidc/token/)
- [Documentation](https://developers.login.gov/oidc/user-info/)
- [Documentation](https://developers.login.gov/oidc/logout/)
- [Documentation](https://developers.login.gov/oidc/certificates/)
- [Sign Up](https://portal.int.identitysandbox.gov)
- [OpenAPI](openapi/login-gov-oidc-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/login-gov-oidc.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/login-gov-oidc.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/login-gov-userinfo-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/login-gov-id-token-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/login-gov-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Spectral Ruleset](rules/login-gov-rules.yml)

### Login.gov SAML 2.0 API

SAML 2.0 federation surface for relying parties that prefer SAML over OIDC. Uses
HTTP-Redirect SSO and HTTP-POST SLO with the persistent NameID format (UUID v4).
Endpoints are year-versioned (2026 = certificates valid through April 1, 2027).
Metadata is published; clients should consume it dynamically to handle annual
certificate rotations.

- **Human URL:** [https://developers.login.gov/saml/](https://developers.login.gov/saml/)
- **Base URL:** `https://secure.login.gov`

#### Tags

- SAML
- Authentication
- SSO
- Federal

#### Properties

- [Documentation](https://developers.login.gov/saml/)
- [Documentation](https://developers.login.gov/saml/getting-started/)
- [OpenAPI](openapi/login-gov-saml-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/login-gov-saml.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/login-gov-saml.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://www.login.gov)
- [Portal](https://www.login.gov/partners)
- [Documentation](https://developers.login.gov)
- [Sign Up](https://www.login.gov/partners/get-started/)
- [Getting Started](https://developers.login.gov/oidc/getting-started/)
- [Sandbox](https://portal.int.identitysandbox.gov)
- [GitHub Organization](https://github.com/18F)
- [GitHub Repository](https://github.com/18F/identity-idp)
- [GitHub Repository](https://github.com/18F/identity-oidc-sinatra)
- [GitHub Repository](https://github.com/18F/identity-saml-sinatra)
- [Status Page](https://status.login.gov)
- [Blog](https://www.login.gov/about/news/)
- [Contact](https://www.login.gov/contact/)
- [Business Inquiries](https://www.login.gov/partners/business-inquiries/)
- [Privacy](https://www.login.gov/policy/)
- [Accessibility](https://www.login.gov/accessibility/)
- [Plans](plans/login-gov-plans-pricing.yml)
- [Rate Limits](rate-limits/login-gov-rate-limits.yml)
- [Vocabulary](vocabulary/login-gov-vocabulary.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
