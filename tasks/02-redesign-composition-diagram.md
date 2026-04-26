# 02 - Redesign Composition Diagram

## Priority

Wave 1: fix false claims.

## Status

Done.

## Problem

Figure 3 uses nested rectangles, which implies physical containment. In real systems, a meta-orchestrator usually calls domain agents as tools or peers rather than containing them.

## Task

Redesign the composition diagram to show sibling agents and tool calls across levels instead of nested containment.

## Acceptance Criteria

- [x] The diagram avoids visual nesting that implies container ownership.
- [x] Meta-orchestrator, domain agents, tools, and peers are shown as separate nodes.
- [x] Edges distinguish orchestration, tool invocation, and peer delegation where useful.
- [x] The caption explicitly clarifies "calls/coordinates" rather than "contains".

## Notes

- Replaced fig.3 nested rectangles in `agent-ontology.html` with sibling nodes for the meta-orchestrator, domain agents, tool nodes, and peer agent.
- Added directed edges and legend entries for orchestration, tool invocation, and peer delegation.
- Updated the composition section text and fig.3 caption to describe calls/coordination rather than containment.
