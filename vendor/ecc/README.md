# Vendored ECC skills

Frozen snapshot of upstream ECC skills that the workflow depends on.
Vendoring removes the install-time requirement to point
`install-profile.py` at a local ECC repo.

## Contents

- `skills/` — 15 ECC native skills referenced by Hermes workflows

This collection is **skill-only**. Rules and MCP configs were removed
to keep the repo positioned as a portable skill collection rather than
a host-specific profile.

## Refreshing from upstream

Run `scripts/refresh-ecc-vendor.sh <path-to-ecc-repo>` from the repo root.
The script overwrites the snapshot in place. Commit the diff to lock the
new version.

## Upstream

ECC repo: <https://github.com/everything-claude-code/everything-claude-code>
(or the local checkout used during refresh).

## Notes

- `production-audit` was removed from upstream and is therefore not
  vendored. If a workflow ever references it, replace with a current
  ECC skill or drop the reference.
