# Contributing to car-spec

Thank you for considering a contribution. This repository holds the OpenAPI 3.1 specification for the **Categorical Agentic Registry (CAR)** and Trust Engine API. It is intended to be an open contract — scrutiny, counter-proposals, and independent client implementations are welcome.

This repo is a **specification**, not a code package. The source of truth is a single file, `openapi.yaml`. There is no build step and nothing to compile; the spec is the deliverable.

## What we accept

**Specification changes.** File an issue before opening a PR for anything that changes endpoints, schemas, parameters, response shapes, or error codes in `openapi.yaml`. Spec changes require rationale, a backward-compatibility assessment, and a version-bump plan (patch / minor / major). Additive, non-breaking changes are far easier to land than breaking ones.

**Clarifications and corrections.** Fixes to descriptions, examples, mismatched types, missing required fields, or inaccurate documentation are welcome directly as PRs.

**Documentation and typos.** Always welcome.

**New independent clients or generators.** Not accepted in this repository. Generate them from the spec in your own repo (see the README for `openapi-generator` usage), reference this spec, and we will link back from the README when interoperability is demonstrated.

## What we do not accept without discussion

- Breaking changes to existing endpoints or schemas without a corresponding major version bump and documented migration path.
- New endpoints that have no corresponding implementation or design rationale. The spec describes a real API; speculative surface area belongs in an issue first.
- Changes that conflate CAR identity with runtime trust scoring. CAR answers "who is this agent?"; the Trust Engine answers "how much do we trust this agent?" Keep that separation (see the `description` block in `openapi.yaml` and the ADR reference therein).

## The RFC / issue process

For anything beyond a typo or an obvious correction:

1. **Open an issue** using the spec-change template. Describe the current behavior, the proposed change, and why.
2. **Discuss** in the issue. This avoids work on a direction that will not merge.
3. **Open a PR** once there is rough agreement, referencing the issue.

## Before you open a PR

- Read the README and the relevant section of `openapi.yaml`.
- Open an issue to discuss significant or breaking changes.
- Validate the spec locally and confirm it passes:

  ```bash
  npm run validate
  ```

  (This runs `@redocly/cli lint openapi.yaml` — the same check CI runs. No `npm install` is required; the validator is fetched on demand via `npx`.)

- Keep edits to `openapi.yaml` minimal and focused. Preserve the existing formatting and ordering so diffs stay readable.

## Commit style

Conventional commits are encouraged but not mandatory:

- `feat(spec):` new endpoint or schema
- `fix(spec):` correct an endpoint, schema, or example
- `docs:` README or description clarification
- `chore:` repository housekeeping

## Reporting security issues

Do not open a public issue for security vulnerabilities. See [SECURITY.md](./SECURITY.md).

## Code of conduct

This project follows the [Contributor Covenant](./CODE_OF_CONDUCT.md). By participating you agree to uphold this code.

## License

By submitting a Contribution, you agree to license your work under the Apache License, Version 2.0 (the license this project carries). You retain copyright on your Contribution; the license grants us and all users the right to use, modify, and redistribute under the same terms.

## Who decides what merges

Vorion LLC maintains this repository and has final commit authority. Substantive disagreements about specification direction are resolved through the issue tracker with visible rationale. We do not operate a formal voting model; decisions are made by the maintainers with consideration for community input.

## Thanks

Every review, correction, and counter-argument improves the standard. If the spec is wrong somewhere, we want to know.
