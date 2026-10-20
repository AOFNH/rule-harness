---
iteration: 2026-09-repo-governance-directory
status: current
---

# Decisions

## D1: Name the directory after its repository governance role

Adopt `.repo-governance/`. The existing file declares the repository kind, the
agent operating mode, and core change authority, so it is repository governance
metadata. `.instructions/` is easily read as a directory of instruction
content; `.repo-meta/` lacks a content boundary; `.harness/` is easily confused
with the existing `harness/` tooling directory.

The directory may later be extended with file ownership, upstream
synchronization, and compatibility declarations as real needs arise, but each
new file must separately define its schema, consumers, ownership, and
allowlist entry. Do not pre-create empty files or relax the tracking rule for
the whole directory. Instruction content, test tooling, fixtures, and local
runtime state continue to follow their established storage boundaries.

## D2: Keep role semantics and migrate to a single path

The content of `repository-role.yaml` stays unchanged. The entry rules and the
validation script use only the new path, without an old-path fallback or two
role declarations. When an existing overlay upgrades, it must keep its own
`personal-overlay`, `overlay-maintainer`, and `none` values and review old
paths in references and automation.

The directory rename does not change routing decisions, role permissions, or
data structures, so the catalog, routing fixture expected values,
`schema_version`, and routing `contract_version` are not adjusted. This is a
path migration that still requires downstream repositories to complete an
upstream impact assessment and a semantic compatibility review; this iteration
modifies only core.
