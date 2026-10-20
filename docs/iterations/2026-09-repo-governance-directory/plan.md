---
iteration: 2026-09-repo-governance-directory
status: complete
---

# Repository governance directory naming

## Goal

Rename `.instructions/` to `.repo-governance/` so that the directory name
directly expresses repository identity, maintenance role, and permission
boundaries, and reserves a clear extension scope for future governance
metadata.

## Scope

- Migrate `repository-role.yaml` and update the bootstrap, Git allowlist, and
  validation script accordingly.
- Update the README, live design, and personal overlay upgrade notes.
- State that every new governance file needs its own schema, consumers,
  ownership, and allowlist definition.

This iteration adds no governance files and does not change role fields,
maintenance permissions, or the reference routing strategy.

## Acceptance

- Structural validation reads the core role from the new path, and the
  redaction scan covers the new directory.
- The existing 10 routing regression cases still pass, with expected values
  unchanged.
- The old path appears only in migration notes and this historical record.
- Diff and allowlist review is complete, and the change is saved in one atomic
  commit.
