---
layout: ../layouts/Layout.astro
title: Authorization — idr.to
---

# Authorization

## Source authentication

Sources present a **Signed Host-Identity** and proof of possession at resolve time. See the [API Signed Host-Identity spec](https://github.com/idrto/api/blob/main/docs/SIGNED_HOST_IDENTITY.md).

## Personal plan ACLs

- `public` — any authenticated source may connect (entity-level setting)
- `same-entity` — `source.entityId == target.entityId` with matching subdomain scope

No wildcards, organizational units, or deny rules.

## Enterprise plan ACLs

Evaluation order:

1. Verify Signed Host-Identity + proof of possession
2. Explicit **deny** rules (by priority)
3. Explicit **allow** rules
4. Default **deny**

Supports cross-entity patterns, OU matching, host wildcards, and deny rules via `acl_rules_v2`.

## API

- `PUT /entities/:id/acl-mode` — Personal: set `public` or `same-entity`
- `POST /entities/:id/acls` — create allow/deny rules (Enterprise features gated)

[Pricing](/pricing) · [Billing API](/billing)
