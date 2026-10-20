---
iteration: 2026-09-ruleharness-name
status: complete
---

# Acceptance record

## Baseline

- Structural validation passed; the role is core / core-maintainer.
- 10 abstract routing regression cases passed.
- The working tree was clean before starting; the directory naming change had
  been completed in an earlier commit.

## After the change

- [x] The display name and repository name are unified across current
      documents, with the cross-client positioning and the current support
      boundary added.
- [x] Codex-specific mechanisms, core/overlay roles, and historical iteration
      records keep their original semantics.
- [x] Structural validation passes and the 10 routing regression cases pass;
      expected values were not modified.
- [x] The hosted repository has been renamed to `rule-harness`; this
      checkout's origin has been updated and Git access verified.
- [x] The old display name and repository name remain only in this round's
      decisions, to explain the migration.
- [x] The complete diff, allowlist, staged file list, and `git diff --check`
      review is complete; the documentation is saved in one atomic commit.
