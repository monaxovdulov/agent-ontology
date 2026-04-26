# 05 - Add Evaluation And Observability

## Priority

Wave 2: close content gaps.

## Status

Done.

## Problem

Evaluation and observability are central to production agents, but the current document only mentions them briefly.

## Task

Add a section explaining eval-driven development and observability for agent systems.

## Key Points

- Start simple, optimize through evals.
- Trace tool calls, model calls, retrieval, state changes, and handoffs.
- Measure task success, cost, latency, intervention rate, and regression risk.
- Treat evals as the working loop, not a postscript.

## Acceptance Criteria

- [x] The document has a dedicated Evaluation & Observability section.
- [x] It includes tracing and eval-driven development.
- [x] It gives concrete metrics for agent systems.
- [x] It connects evaluation to architecture selection.

## Notes

- Added a dedicated `Evaluation & Observability` section to `agent-ontology.html` after the protocol/failure-modes content.
- Framed evals as the working loop: baseline, trace inspection, architecture change, regression rerun.
- Added trace coverage for model calls, tool calls, retrieval, state changes, and handoffs.
- Added concrete metrics: task success, cost, latency, intervention rate, and regression risk.
