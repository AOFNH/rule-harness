---
iteration: 2026-09-repo-governance-directory
status: complete
---

# Acceptance record

## Baseline

- `python3 harness/scripts/validate.py --root .`: passed; the role is
  core / core-maintainer.
- `python3 harness/scripts/route_regression.py --root .`: 10 abstract routing
  cases passed.
- The working tree was clean before starting.

## After the change

- [x] The role declaration was migrated unchanged; the bootstrap, allowlist,
      validation entry point, and redaction scan use the new path.
- [x] Documentation describes the directory's responsibility, its extension
      boundary, and the requirement that overlays keep their own role.
- [x] Structural validation passes and recognizes core / core-maintainer at
      the new path.
- [x] The 10 routing regression cases pass; expected values were not modified.
- [x] The Git blob hash of the role file is identical before and after the
      migration; its content is unchanged.
- [x] The allowlist admits only the new role file; other files in the new
      directory remain ignored by default.
- [x] The old path appears only in migration notes and this historical record.
- [x] The complete diff, staged file list, and `git diff --check` review
      passed; this iteration is saved in one atomic commit.
