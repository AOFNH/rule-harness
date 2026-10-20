---
iteration: 2026-09-ruleharness-name
status: current
---

# Decisions

## D1: Adopt RuleHarness

Rename `Codex Agent Instructions Harness — Core` / `codex-agent-instructions-harness-core`
to `RuleHarness` / `rule-harness`. The positioning statement, originally
written in Chinese, translates to "a cross-agent framework for instruction
management, context routing, and validation".

The name follows the approach of Ruler, Rulesync, and OpenSpec: name the
project after its core concept and state the client support scope in its
description. Keeping Rule and Harness emphasizes the rule system and its
validation; client names move to the adapter notes, and core/overlay is
expressed through the README and the repository role declaration.

## D2: Distinguish the extension direction from implemented support

The current bootstrap and client-specific guidance still target Codex first.
Another client may be declared supported only after it has an explicit adapter
and validation; the rename does not mean those adaptations are complete.

Keep the existing boundary of a single canonical instruction source plus
client adapters. Keep Codex-specific guidance such as `CODEX_HOME`,
`AGENTS.override.md`, and profiles, and do not generalize client-specific
mechanisms into generic ones through text substitution.

## D3: The rename does not change the runtime contract

This round does not change rule applicability, evidence priority, role
permissions, or data structures. The catalog, fixture expected values,
`contract_version`, `schema_version`, and existing release tag naming stay
unchanged; historical iteration records keep their original context.

The hosted repository name and this checkout's origin are updated together.
Other checkouts and personal overlays verify their remote URLs during later
maintenance and complete the normal upstream impact assessment; this round does
not modify those repositories.
