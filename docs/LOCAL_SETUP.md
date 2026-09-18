<!-- generated: do not edit by hand
schemaVersion: 1
tenantId: e73b65ff-17d7-4c55-adac-cfdac1165870
baseRelease: tenant-runtime-v0.1.0
generatorVersion: 1
contentHash: sha256:193b0bb377257ffc9fef61d3499d6b85e044195528ee70b335d0cb42cdce41fb
packHash: sha256:6c5ef7fa26ca7ead5699cd9137d80869504289b466a4fe591cc1688146ea32f1
-->

# Local setup — Example Booking

```bash
pnpm install --frozen-lockfile
pnpm build
```

Both applications read two public values and nothing else:

| Name | What it is |
| --- | --- |
| `NEXT_PUBLIC_SUPABASE_URL` | The project URL. Public. |
| `NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY` | An RLS-constrained browser key. Public. |

Point them at a non-production project. There is no third value: a service-role
or secret key in either application would read every tenant's data from a
browser, and no task in this repository needs one.

This repository cannot migrate a database and must not try. Schema belongs to
the platform pipeline. Config schema version here is 3.
