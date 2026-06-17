# Security Policy

## Reporting a vulnerability

Please report security issues privately — not through public GitHub issues or discussions.

**Preferred:** Use GitHub's private vulnerability reporting for this repository. Go to the **Security** tab → **Report a vulnerability** (or open <https://github.com/vorionsys/car-spec/security/advisories/new>). This keeps the report private, lets us collaborate on a fix in a private advisory, and tracks disclosure in one place.

**Secondary:** If you cannot use GitHub's reporting flow, email **security@vorion.org**.

> Reviewer note: the `security@vorion.org` inbox has not yet been confirmed as a monitored mailbox with a response SLA. Confirm the inbox is monitored and assign an owner before relying on it as a primary channel. Until then, GitHub private vulnerability reporting is the dependable path.

Please include:

- The affected part of the spec (endpoint, schema, parameter, or section of `openapi.yaml`)
- A clear description of the issue and why it is a security concern
- Reproduction steps, an example payload, or a minimal demonstration where applicable
- Your assessment of severity and impact
- Whether you intend to disclose publicly, and on what timeline

## Scope

This repository is an OpenAPI **specification** — a machine-readable contract — not a running service or shipped code. What is in scope here:

In-scope:

- Specification ambiguities or errors that would lead implementers to build an insecure API (for example, an auth scheme described incorrectly, a missing required field that enables an unsafe default, or an error code that leaks sensitive detail)
- Schema or example payloads in `openapi.yaml` that disclose secrets, internal endpoints, or other sensitive information
- Descriptions that misrepresent the security model of the CAR / Trust Engine API in ways that would weaken an operator's posture

Out-of-scope (report to the relevant project, not here):

- Vulnerabilities in the live Vorion CAR / Trust Engine service itself (this repo only describes its contract)
- Vulnerabilities in code generated from this spec, or in third-party clients and generators
- Issues in dependencies of the validation tooling (report those upstream)
- Issues in consumers of this spec (SDKs, CLIs, products) — report those to the respective project

## Supported versions

Until v1.0.0 of the API contract reaches a stable cadence, only the latest published spec version receives corrections. No long-term-support commitment at this stage; consumers on older spec versions should expect to upgrade.

## Disclosure

We prefer coordinated disclosure. After we acknowledge a report and have a fix in progress, we will agree on a public disclosure date. Attribution to the reporter is included unless you request anonymity.

If a reported issue is already being exploited in the wild, we may publish immediately without waiting for a coordinated date.
