# Security Policy

RADAS V3 is not yet approved for production use.

## Current phase

The repository is in governance and audit preparation. No production runtime, user data, payment flow or AI provider credentials should exist in the repository.

## Sensitive information

Never commit:

- API keys or provider credentials
- authentication secrets
- payment secrets or webhook signing keys
- database credentials
- private customer or user data
- generated private media
- signed media URLs

Use local environment files that are excluded by `.gitignore`. Example files must contain placeholders only.

## Reporting a security issue

Do not publish exploitable details in a public issue. Report the issue privately to the repository owner and include:

- affected component
- reproduction steps
- possible impact
- suggested mitigation, if known

## Security gates

Production use remains blocked until the roadmap's production-hardening gate is approved, including authentication, ownership, upload, SSRF, webhook, rate-limit, retry, credit and provider-budget controls.