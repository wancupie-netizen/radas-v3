# RADAS V3

RADAS V3 is an AI Creative Studio that transforms products and ideas into ready-to-use visual content, especially short-form videos.

> Turn products and ideas into videos.

## Current project state

- Active phase: `RADAS-V3-02 / AUDIT-00B - Clean Functional Baseline`
- Product implementation: not started
- Atlas source import: not started
- Commercial licence clearance: unresolved
- Production deployment: not approved

## Single source of truth

All product scope, phase order, gates and locked decisions are governed by:

- [RADAS-V3-OFFICIAL-ROADMAP.md](RADAS-V3-OFFICIAL-ROADMAP.md)

If another document conflicts with the roadmap, the roadmap takes precedence until it is formally updated.

## MVP boundary

The approved MVP contains:

1. Product Video
2. Story
3. Image
4. My Products
5. My Creations
6. Credits
7. Settings

Features outside this boundary require an approved roadmap change.

## Repository rules

- RADAS V1 and RADAS V2 must not be modified by V3 work.
- Do not commit secrets, API keys, generated media or local environment files.
- Do not import Atlas code until the audit phase authorises it.
- Do not commit directly to `main`.
- Use phase-scoped branches and review the exact staged diff before commit.

## Governance documents

- [Project boundaries](docs/governance/PROJECT-BOUNDARIES.md)
- [Upstream baseline](docs/governance/UPSTREAM-BASELINE.md)
- [Phase status](docs/governance/PHASE-STATUS.md)
- [Architecture decisions](docs/decisions/README.md)
- [Audit workspace](docs/audits/README.md)
- [Contributing rules](CONTRIBUTING.md)
- [Security policy](SECURITY.md)

## Development status

This repository currently contains governance and audit preparation only. No application runtime, database, AI provider, payment integration or deployment configuration is approved yet.
