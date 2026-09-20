# Contributing to RADAS V3

## Governing source

Read `RADAS-V3-OFFICIAL-ROADMAP.md` before proposing or implementing work.

## Branch convention

Use one scoped branch per approved work package:

- `phase/radas-v3-00`
- `audit/radas-v3-01`
- `fix/<short-description>`
- `docs/<short-description>`

Do not commit directly to `main`.

## Commit convention

Use concise Conventional Commit style messages:

- `docs(governance): establish phase 0 scaffold`
- `chore(audit): record atlas baseline`
- `fix(credits): prevent duplicate settlement`

One commit should represent one coherent, reviewable change.

## Safe Git procedure

1. Confirm the repository, branch and expected baseline commit.
2. Confirm the working tree is clean before applying a patch.
3. Stage exact files only; do not use `git add .`.
4. Run `git diff --cached --check`.
5. Review `git diff --cached --stat` and `git diff --cached`.
6. Commit only after the staged diff matches the approved scope.
7. Push the scoped branch and open a pull request.

## Scope control

- Do not modify RADAS V1 or RADAS V2.
- Do not add product features during governance or audit phases.
- Do not import Atlas code before the relevant gate allows it.
- Do not expose provider/model controls to users without a roadmap change.
- Do not lock pricing before `RADAS-COST-00` is complete.

## Secrets and generated assets

- Never commit API keys, access tokens, credentials or payment secrets.
- Commit only example environment files containing names and safe descriptions.
- Do not commit generated images, videos, database files or local logs.

## Pull request evidence

Each pull request must state:

- phase/work-package ID
- starting commit
- files changed
- tests or document checks performed
- risks and deferred work
- whether the roadmap or an ADR changed