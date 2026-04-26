# 11 - Add Decision Tree

## Priority

Wave 3: make the framing honest.

## Status

Done.

## Problem

The map does not yet answer the practical question: "I have task X, what should I build?"

## Task

Add a decision tree for choosing between workflow, single-agent, multi-agent, tool-use, memory, and HITL designs.

## Acceptance Criteria

- [x] The decision tree starts from user/task constraints.
- [x] It includes complexity, risk, cost, eval readiness, and HITL requirements.
- [x] It recommends the simplest architecture that fits the task.
- [x] The output is usable as a design aid.

## Notes

- Added `§ 13 — decision tree` to `agent-ontology.html` after anti-patterns and before the remaining source gaps.
- Built a compact SVG and decision table that start from task constraints and escalate through prompt, workflow, augmented LLM, single-agent, multi-agent, memory, and HITL gates.
- Connected the design aid back to A1-A7, eval/observability, cost/risk controls, failure modes, memory policy, and anti-patterns.
- Renumbered the remaining source-gap and summary sections to `§14` and `§15`.
