---
iteration: 2026-09-ruleharness-name
status: complete
---

# RuleHarness project naming

## Goal

Adopt the display name `RuleHarness` and the repository name `rule-harness`: a
short, client-neutral name that expresses instruction management, context
routing, and validation, and leaves room for adapting other agents later.

## Scope

- Update the README, bootstrap title, live design, and maintenance document
  titles.
- State that the project currently targets Codex first, and that other clients
  may be declared supported only after their adaptation and validation are
  complete.
- Express core/overlay as a repository role while keeping the existing routing
  protocol and permission boundaries.
- Synchronize the hosted repository name and this checkout's origin URL.

This round does not implement new client adapters and does not change routing
expected values, the role schema, or historical iteration records.

## Acceptance

- Current documents use the new name; the old name appears only in the naming
  change record.
- Structural validation and the existing 10 routing regression cases pass.
- Diff and allowlist review is complete, and the documentation change is saved
  in one atomic commit.
- The new hosted repository name and the origin URL are verified; if this
  cannot be completed, the external blocker is recorded explicitly.
