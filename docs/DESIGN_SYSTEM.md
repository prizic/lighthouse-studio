<!-- generated: do not edit by hand
schemaVersion: 1
tenantId: e73b65ff-17d7-4c55-adac-cfdac1165870
baseRelease: tenant-runtime-v0.1.0
generatorVersion: 1
contentHash: sha256:c4f7e756e2621d21c689aeea089b92fb16c46ca8108743cb279ef9e919f5ef05
packHash: sha256:6c5ef7fa26ca7ead5699cd9137d80869504289b466a4fe591cc1688146ea32f1
-->

# Design system — Example Booking

Brand tokens live in `instance/brand.json` at config schema version
3, and `instance/theme.css` maps them to CSS custom
properties. Components read the properties; they never hard-code a colour.

- Every colour pair in the token set must keep its contrast ratio. Changing a
  background without its `on*` partner is what breaks it.
- RTL is a semantic layout foundation, not a late skin. This instance ships Arabic, so every layout change must be checked in both directions.
- Keyboard focus, visible focus rings, touch targets and error states are part
  of the component contract. Removing one is a regression, not a style choice.

Brand assets are raster PNGs under `instance/assets/`, referenced by
`instance/brand.json`. A reference without a file fails the build.
