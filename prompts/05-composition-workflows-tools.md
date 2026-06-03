# 05 - Composition, Workflows And Tools

## Objective

Rewrite composition, Anthropic workflow patterns and tool-design claims so they are evidence-backed and not overcanonical.

## Read first

- `audit/claim-ledger.md` C10, C25-C31, C49-C50
- `audit/rewrite-blueprint.md` sections 4-5
- `research/sources.md` entries for Anthropic Building Effective Agents, Anthropic Writing Tools for Agents, ReAct, MCP spec, OpenAI Practical Guide, AutoGen, Magentic-One
- `research/content-risks.md` sections on Anthropic patterns and augmented LLM
- `research/negative-findings.md` on five-pattern consensus

## Work

1. Rewrite composition as "recursive calls/contracts" without old-document critique.
2. Change "canonical primitive" / "atom of all systems" to a sourced practical primitive:
   - "Anthropic's useful base primitive for this map is the augmented LLM: model plus tools, retrieval and memory."
3. Scope Anthropic's five patterns:
   - influential practitioner vocabulary;
   - workflow/control-flow patterns;
   - not complete consensus taxonomy.
4. Fix the autonomous agent definition:
   - avoid "no predetermined graph" as an absolute;
   - emphasize model-selected next actions inside budgets/policies.
5. Move or integrate "tools != classical software" near composition/tools:
   - tool names, schemas, descriptions and outputs are part of the agent's reasoning surface;
   - source it to Anthropic Writing Tools for Agents and optionally MCP.

## Acceptance criteria

- No "canonical", "atom", "all major frameworks" or "consensus ontology" overclaim remains.
- The workflow/agent distinction is clear and attributed.
- Tool-design advice has a local evidence anchor.
- `prompts/progress.md` is updated.
