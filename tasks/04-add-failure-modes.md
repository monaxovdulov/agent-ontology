# 04 - Add Failure Modes

## Status

Done.

## Priority

Wave 2: close content gaps.

## Problem

The current map is too sterile because it does not cover how agent systems fail.

## Task

Add a Failure Modes section with a compact taxonomy.

## Suggested Failure Modes

- Cascading errors.
- Context poisoning.
- Hallucination amplification between agents.
- Infinite loops.
- Agreement bias between agents.

## Acceptance Criteria

- [x] The section explains each failure mode in practical terms.
- [x] The taxonomy connects failures to architectural choices where possible.
- [x] At least one visual or table summarizes the failure modes.

## Notes

- Added a compact Failure Modes section to `agent-ontology.html` after the technology/protocol layer and before the remaining gaps/conclusion.
- Covered cascading errors, context poisoning, hallucination amplification between agents, infinite loops, and agreement bias.
- Used the existing `stack` table style to map each mode to symptoms, architectural amplifiers, and containment tactics.
