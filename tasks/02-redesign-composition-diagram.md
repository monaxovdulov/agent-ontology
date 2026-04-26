# 02 - Redesign Composition Diagram

## Priority

Wave 1: fix false claims.

## Problem

Figure 3 uses nested rectangles, which implies physical containment. In real systems, a meta-orchestrator usually calls domain agents as tools or peers rather than containing them.

## Task

Redesign the composition diagram to show sibling agents and tool calls across levels instead of nested containment.

## Acceptance Criteria

- The diagram avoids visual nesting that implies container ownership.
- Meta-orchestrator, domain agents, tools, and peers are shown as separate nodes.
- Edges distinguish orchestration, tool invocation, and peer delegation where useful.
- The caption explicitly clarifies "calls/coordinates" rather than "contains".

