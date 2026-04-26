# 10 - Add Anti-Patterns

## Priority

Wave 3: make the framing honest.

## Status

Done.

## Problem

The current map describes structures but not common mistakes.

## Task

Add an Anti-Patterns section.

## Candidate Anti-Patterns

- Over-engineering.
- Using multi-agent architecture for single-agent tasks.
- Shipping without evals.
- Treating workflow vs agent as a rigid binary.
- Adding memory without a retrieval or update strategy.

## Acceptance Criteria

- [x] Each anti-pattern has a symptom, cause, and practical correction.
- [x] The section is operational, not just cautionary.
- [x] Anti-patterns connect back to the taxonomy dimensions.

## Notes

- Added `§ 12 — anti-patterns` to `agent-ontology.html` after memory typology and before the remaining source gaps.
- Covered over-engineering, multi-agent for single-agent tasks, shipping without evals, rigid workflow-vs-agent framing, and memory without write/retrieval strategy.
- Connected each anti-pattern to taxonomy dimensions such as A1/A2/A3/A4/A6, eval metrics, and memory policy.
- Renumbered the remaining source-gap and summary sections to `§13` and `§14`.
