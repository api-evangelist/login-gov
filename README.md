# Login.gov (login-gov)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
