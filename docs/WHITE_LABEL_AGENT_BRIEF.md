<!-- generated: do not edit by hand
schemaVersion: 1
tenantId: e73b65ff-17d7-4c55-adac-cfdac1165870
baseRelease: tenant-runtime-v0.1.0
generatorVersion: 1
contentHash: sha256:0e43c1d284cc02f4c432ebe7790e9d121d8450a34e00ffac3ce137240ed97df6
packHash: sha256:6c5ef7fa26ca7ead5699cd9137d80869504289b466a4fe591cc1688146ea32f1
-->

# White label agent brief — Example Booking

The tenant is `lighthouse-studio`. Its instance answers on `lighthouse-studio-client.vercel.app` (client) and `lighthouse-studio-dashboard.vercel.app` (dashboard).

| Fact | Value |
| --- | --- |
| Tenant | `e73b65ff-17d7-4c55-adac-cfdac1165870` |
| Instance | `1f032e82-ec87-4a17-ba56-6fdab802acbe` |
| Default locale | `en` |
| Supported locales | `ar`, `en` |
| Enabled features | `guestBooking`, `requestToBook` |

Tenant, brand and instance are three different things and this pack never uses
them interchangeably: the tenant is the business, the brand is its visual and
written identity, and the instance is this deployed pair of applications.

Customization is configuration. The brand direction lives in
`instance/brand.json`, the words in `instance/content/`, the pages in
`instance/navigation.json`, and the entitlements in `instance/features.json`.
