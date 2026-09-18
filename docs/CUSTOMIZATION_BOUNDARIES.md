<!-- generated: do not edit by hand
schemaVersion: 1
tenantId: e73b65ff-17d7-4c55-adac-cfdac1165870
baseRelease: tenant-runtime-v0.1.0
generatorVersion: 1
contentHash: sha256:4666b635930c7b9dcd2883cb69ad42a278a83b0d2336db70b05d760dcb7b86c7
packHash: sha256:6c5ef7fa26ca7ead5699cd9137d80869504289b466a4fe591cc1688146ea32f1
-->

# Customization boundaries — Example Booking

This instance is tier `config-only`.

**Change these freely.**

- instance/assets/**
- instance/brand.json
- instance/content/**
- instance/features.json
- instance/navigation.json
- instance/theme.css

**Change these only through a documented extension slot**, under
`instance/extensions/`, and say in the pull request why configuration could not
do it.

**Never change these.** They are enforced, not advised: the branch ruleset and
export CI both refuse them.

- .platform/**
- apps/platform-admin/**
- control-plane/**
- packages/email/**
- packages/integrations/**
- packages/supabase-admin/**
- supabase/**

The safe change order is the order of this list. Configuration first, an
approved extension slot second, distributed core only with recorded
platform-owner approval and a written reason the first two do not work.
