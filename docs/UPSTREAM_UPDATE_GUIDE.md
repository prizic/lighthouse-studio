<!-- generated: do not edit by hand
schemaVersion: 1
tenantId: e73b65ff-17d7-4c55-adac-cfdac1165870
baseRelease: tenant-runtime-v0.1.0
generatorVersion: 1
contentHash: sha256:c3b7cd6dffbd70457b4966c0b8040b09758854dffe6698b16277e960931b1aff
packHash: sha256:6c5ef7fa26ca7ead5699cd9137d80869504289b466a4fe591cc1688146ea32f1
-->

# Upstream update guide — Example Booking

This instance is at `tenant-runtime-v0.1.0`.

| Version | Value |
| --- | --- |
| whiteLabelVersion | `0.1.0` |
| configSchemaVersion | `3` |
| backendContract | `1–1` |

An upstream update arrives as a pull request that replaces the distributed tree
and re-renders this pack at the new release. Your configuration under
`instance/` is yours and is never rewritten by an update.

A conflict in `instance/` is yours to resolve. A conflict anywhere else means
the instance changed distributed core, which is the case the safe change order
exists to prevent — resolve it by moving the change into configuration or an
extension slot, or by recording platform-owner approval for it.

If the new release's backend contract range excludes the deployed backend, the
update does not land: Client and Dashboard are promoted and rolled back as one
pair under an N/N-1 contract, and half a pair is never promoted.
