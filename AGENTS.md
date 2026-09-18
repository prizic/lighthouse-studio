<!-- generated: do not edit by hand
schemaVersion: 1
tenantId: e73b65ff-17d7-4c55-adac-cfdac1165870
baseRelease: tenant-runtime-v0.1.0
generatorVersion: 1
contentHash: sha256:0af087ab61adb47df3ec3f812bb549aab92dd8e299835b0c395b9c329a6afe06
packHash: sha256:6c5ef7fa26ca7ead5699cd9137d80869504289b466a4fe591cc1688146ea32f1
-->

# Agent contract — Example Booking

Customize Client and Dashboard for the tenant described in
`docs/WHITE_LABEL_AGENT_BRIEF.md` while keeping this instance compatible with
the platform it is distributed from.

## Read before changing code

Completely, in this order, before your first edit:

1. [`docs/WHITE_LABEL_AGENT_BRIEF.md`](docs/WHITE_LABEL_AGENT_BRIEF.md)
2. [`docs/ARCHITECTURE.md`](docs/ARCHITECTURE.md)
3. [`docs/CUSTOMIZATION_BOUNDARIES.md`](docs/CUSTOMIZATION_BOUNDARIES.md)
4. [`docs/DESIGN_SYSTEM.md`](docs/DESIGN_SYSTEM.md)
5. [`docs/FEATURE_FLAGS.md`](docs/FEATURE_FLAGS.md)
6. [`docs/LOCAL_SETUP.md`](docs/LOCAL_SETUP.md)
7. [`docs/VERIFICATION_CHECKLIST.md`](docs/VERIFICATION_CHECKLIST.md)
8. [`docs/UPSTREAM_UPDATE_GUIDE.md`](docs/UPSTREAM_UPDATE_GUIDE.md)

## Safe change order

Stop at the lowest rung that genuinely works, and say in the pull request why
you had to go higher.

1. `instance/` — configuration, content, features, assets, approved theme tokens.
2. A documented extension slot under `instance/extensions/`.
3. Distributed core, only with explicit platform-owner approval and a written
   reason why 1 and 2 do not work.

## Never do these

- Never add Platform Admin code or infer its private implementation.
- Never add or run a Supabase production migration from this repository.
- Never use a Supabase service-role or secret key in either application, in any file, for any reason.
- Never trust a hostname, URL parameter, form value, JWT user metadata, or hidden UI control as authorization.
- Never bypass RLS, booking RPCs, price calculation, idempotency, webhook signature verification, or payment state reconciliation.
- Never put a secret, real customer data, a provider token, or a production dump in Git, a test, a screenshot, a log, or an AI prompt.
- Never remove RTL, keyboard, focus, contrast, mobile, or error-state behaviour.
- Never install a dependency without checking its licence, maintenance, security, bundle impact, and whether a package already here solves the need.

## Invariants

- Only Client and Dashboard ship in this repository.
- Tenant identity comes from verified deployment configuration and is revalidated by server and database authorization.
- Every booking and capacity change goes through a versioned atomic backend contract.
- Runtime entitlements from the control plane override local feature configuration.
- An existing booking keeps its policy, price, duration, and intake snapshots; a later edit never rewrites it.
- English and Arabic are functionally equivalent.

## Before handing off

1. `pnpm format:check`
2. `pnpm lint`
3. `pnpm typecheck`
4. `pnpm test:unit`
5. `pnpm build`

Then report changed behaviour and files, the evidence, your assumptions, the
remaining risks, and the versions in `docs/VERIFICATION_CHECKLIST.md`.
