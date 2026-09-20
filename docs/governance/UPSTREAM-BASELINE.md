# Atlas Upstream Baseline

**Record ID:** `UPSTREAM-ATLAS-001`
**Purpose:** Reproducible audit baseline only
**Import status:** NOT IMPORTED

## Upstream repository

- Repository: `AtlasCloudAI/atlas-marketing-studio`
- URL: `https://github.com/AtlasCloudAI/atlas-marketing-studio`
- Selected branch: `main`
- Selected audit commit: `18ec178052f6f97612813997613d88ce34b02fc5`
- Commit message: `fix: reconcile completed marketing studio tasks`
- Commit date: `2026-07-23T14:21:38Z`

This commit is locked as the reproducible starting point for `RADAS-V3-01 / AUDIT-00A`. It is not yet approved as the RADAS application baseline.

## Acquisition strategy

- RADAS V3 remains an independent repository.
- Atlas is treated as an upstream reference and audit subject.
- No Atlas source code is copied during RADAS-V3-00.
- The audit may use a separate local workspace or audit-only branch.
- Any later import must preserve provenance and follow the licence decision.

## Known upstream branches requiring comparison

- `fix/llm-max-tokens` at `96a5a542abafc52299e9ac5ae5526fd6b77a4bc5`
- `fix/poll-gateway-unstable` at `40fc38614a79ec5ddb378ca79deec90f6a9fdf7c`
- `codex/atlas-marketing-studio-readme` at `197382fea45953342176c32717d25333dd9e134d`

These branches are not included automatically. Their changes must be inspected during the repository audit.

## Licence state

Status: `UNRESOLVED`

At Phase 0 review:

- GitHub repository metadata reported no detected licence.
- No standard root `LICENSE` file was present.
- README claims alone are not sufficient for commercial clearance.

Prototype analysis may continue, but commercial reuse remains blocked until the licence is confirmed or affected Atlas code is replaced.

## Integrity rule

Future audit reports must cite the exact commit above. If a newer upstream commit is considered, record it as a new baseline decision instead of silently moving this reference.