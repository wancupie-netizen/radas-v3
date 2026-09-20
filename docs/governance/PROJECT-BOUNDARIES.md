# RADAS V3 Project Boundaries

**Decision state:** LOCKED
**Authority:** `RADAS-V3-OFFICIAL-ROADMAP.md`

## Repository isolation

RADAS V3 is developed only in:

- Repository: `wancupie-netizen/radas-v3`
- Default branch: `main`
- Initial baseline: `a8cc8f8cb8fce80d4f83a72520c98895808af5b4`

RADAS V3 is not a fork and has an independent root commit.

## Preserved systems

- RADAS V1 is preserved.
- RADAS V2 is preserved.
- Their repositories, deployments, databases and production configuration are outside the scope of RADAS V3.

No V3 task authorises changes to V1 or V2 unless the founder explicitly changes this boundary in the official roadmap.

## Allowed during RADAS-V3-00

- governance documents
- repository conventions
- upstream baseline records
- audit workspace preparation
- environment-variable inventory with placeholders only

## Prohibited during RADAS-V3-00

- application feature development
- UI implementation
- production deployment
- database provisioning
- payment integration
- AI provider integration
- copying Atlas source into RADAS V3
- real credentials or secrets

## Atlas relationship

Atlas Marketing Studio is an upstream audit/reference candidate. RADAS V3 is not a GitHub fork of Atlas. Atlas source may not be imported until the audit confirms the technical and legal treatment.

## Repository visibility

The repository is public at the start of Phase 0. No secrets or proprietary runtime configuration may be introduced while it remains public. Repository visibility must be reconsidered before source import or commercial implementation.