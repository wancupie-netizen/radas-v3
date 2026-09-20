# ADR-0001: RADAS V3 Repository Isolation

**Status:** ACCEPTED
**Date:** 2026-09-20
**Roadmap decision:** `DEC-001`, `DEC-002`, `DEC-003`, `DEC-006`

## Context

RADAS V1 and V2 serve different product directions and must remain preserved. Atlas Marketing Studio is a useful reference candidate, but its architecture, product scope and licence state require audit before reuse.

## Decision

RADAS V3 will:

- use the independent repository `wancupie-netizen/radas-v3`
- preserve V1 and V2 without modification
- maintain an independent Git history
- treat Atlas as an upstream reference and audit subject
- avoid copying Atlas source during Phase 0
- record any later source import with exact provenance and licence treatment

## Consequences

Positive:

- V1/V2 production risk is isolated.
- V3 product and UI can evolve independently.
- Atlas provenance and licence decisions remain auditable.
- A failed V3 experiment does not damage earlier products.

Trade-offs:

- Useful code must be selected and imported deliberately.
- Shared branding or frameworks require explicit decisions.
- Audit work occurs before feature implementation.

## Alternatives considered

### Upgrade RADAS V2 directly

Rejected because V3 has a different product identity, architecture and operating model.

### Fork Atlas directly on GitHub

Rejected for Phase 0 because it would couple RADAS history and identity to an unresolved upstream licence and an unaudited codebase.

### Copy Atlas immediately into `main`

Rejected because it would bypass the mandatory repository, licence, dependency and cost audits.