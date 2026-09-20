# RADAS V3 Audit Workspace

This directory stores evidence-backed audits required by the official roadmap.

## Rules

- Every finding must cite a repository path, commit, command result or provider evidence.
- Separate confirmed facts from inference.
- Record the exact upstream commit used.
- Do not place secrets, credentials, generated private media or signed URLs here.
- Do not silently convert an audit recommendation into implementation.

## Planned audit packages

```text
docs/audits/
|-- atlas-baseline/
|-- licence/
|-- dependencies/
|-- functional-baseline/
|-- architecture-security/
`-- cost-benchmark/
```

Directories will be created only when their approved phase begins.

## First planned audit

`RADAS-V3-01 / AUDIT-00A - Atlas Repository, Licence and Dependency Audit`