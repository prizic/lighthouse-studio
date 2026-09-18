<!-- generated: do not edit by hand
schemaVersion: 1
tenantId: e73b65ff-17d7-4c55-adac-cfdac1165870
baseRelease: tenant-runtime-v0.1.0
generatorVersion: 1
contentHash: sha256:e3d4a028a2ca96301636d9e23c288e01b0bd8432f353a4149e9115e5a3e31524
packHash: sha256:6c5ef7fa26ca7ead5699cd9137d80869504289b466a4fe591cc1688146ea32f1
-->

# Verification checklist — Example Booking

Run all of these before handing off. They are the gates this
repository actually has at release `tenant-runtime-v0.1.0`.

1. `pnpm format:check` — formatting
2. `pnpm lint` — lint and forbidden imports
3. `pnpm typecheck` — types
4. `pnpm test:unit` — unit tests
5. `pnpm build` — both applications build

Then check by hand what a command cannot:

- Both locales render and mean the same thing, in both text directions.
- Keyboard-only navigation reaches every action, with a visible focus ring.
- Error and empty states still say something useful.

Report, in the pull request: what behaviour changed and in which files, the
evidence above, the assumptions you made, the risks you are leaving, and the
white-label, config schema and backend contract versions in this table.

| Version | Value |
| --- | --- |
| whiteLabelVersion | `0.1.0` |
| configSchemaVersion | `3` |
| backendContract | `1–1` |
