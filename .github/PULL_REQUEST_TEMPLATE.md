<!-- Keep it short. car-spec is an OpenAPI spec repo — the only deliverable is openapi.yaml. -->

## What changed

<!-- One or two sentences. What does this PR change in the spec or docs? -->

## Why

<!-- Link the issue this implements, if any: Closes #___ -->

## Type of change

- [ ] Documentation / typo / clarification
- [ ] Additive, non-breaking spec change (new endpoint, optional field, etc.)
- [ ] Breaking spec change (requires a major version bump — describe the migration below)

## Backward compatibility

<!-- If this is a breaking change, describe what breaks and how consumers should migrate. Otherwise write "Non-breaking." -->

## Checklist

- [ ] `npm run validate` passes locally (`@redocly/cli lint openapi.yaml`)
- [ ] An issue was opened first for any significant or breaking change
- [ ] Examples and descriptions are updated to match the change
- [ ] CAR identity and Trust Engine concerns remain separated (no conflation)
