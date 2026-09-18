<!-- generated: do not edit by hand
schemaVersion: 1
tenantId: e73b65ff-17d7-4c55-adac-cfdac1165870
baseRelease: tenant-runtime-v0.1.0
generatorVersion: 1
contentHash: sha256:9ed07ed86b16de0c8ed19c9ab32fb162dcf7aa99f7b20b2703c50387461396a4
packHash: sha256:6c5ef7fa26ca7ead5699cd9137d80869504289b466a4fe591cc1688146ea32f1
-->

# Feature flags — Example Booking

`instance/features.json` states what this instance asks for.

| Feature | Configured |
| --- | --- |
| `guestBooking` | enabled |
| `onlinePayment` | disabled |
| `requestToBook` | enabled |

Configuration is a request, not a grant. The control plane's runtime
entitlements override this file: a feature enabled here and not entitled stays
off, and discovering that in the browser is expected behaviour, not a bug.
