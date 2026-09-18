<!-- generated: do not edit by hand
schemaVersion: 1
tenantId: e73b65ff-17d7-4c55-adac-cfdac1165870
baseRelease: tenant-runtime-v0.1.0
generatorVersion: 1
contentHash: sha256:be2aa667b1c6aab999e723ba4e5715d14a67b5cba496c75f0841a2d333c627a0
packHash: sha256:6c5ef7fa26ca7ead5699cd9137d80869504289b466a4fe591cc1688146ea32f1
-->

# Architecture — Example Booking

This repository holds two applications and the packages they import.

- `apps/client` — the public booking surface.
- `apps/dashboard` — the tenant's own operations surface.
- `packages/*` — the shared closure both import. Distributed, not tenant-owned.
- `instance/` — this tenant's configuration, content, tokens and assets.
- `.platform/` — ownership metadata. Read it; never edit it.

Data flows one way. A browser talks to an application, the application talks to
`api_v1` in Postgres with a publishable, RLS-constrained key, and Postgres
decides what the caller may see. Booking, capacity, price and eligibility
correctness lives in atomic database functions, never in this repository.

The backend this release speaks to is contract range 1–1.
Anything outside it is an upgrade, not a configuration change — see
`docs/UPSTREAM_UPDATE_GUIDE.md`.
