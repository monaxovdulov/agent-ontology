# Rewrite Blueprint

This is an information architecture blueprint only. It is not a new `index.html`.

## Core rewrite principle

The page should read as a standalone taxonomy:

1. Define scope.
2. Show why the dimensions exist.
3. Attach evidence to claims.
4. Use examples only after the map is justified.
5. Keep uncertainty visible but not noisy.

Internal changelog, source critique and task history should move out of the main narrative.

## Proposed page order

### 0. Hero / thesis

Keep:

- Practical taxonomy, not formal ontology.
- Minimal sufficient autonomy as the operating principle.

Rewrite:

- Remove "checking old document" framing.
- Add one-sentence promise: "This map separates autonomy, topology, coordination, composition, protocols, memory and evaluation so builders can choose the simplest architecture that passes their evals."

Visible citations:

- none required in hero, unless there is a small "evidence-backed map" marker opening the source drawer.

Hidden annotations:

- taxonomy scope;
- why not formal ontology.

### 1. Scope and evidence rules

New section.

Purpose:

- Define "AI agent" operationally for the page.
- Explain that claims are evidence-tagged and some are taxonomy decisions.
- Distinguish old MAS literature, LLM-agent practitioner sources, specs/docs, benchmarks and product examples.

Visible citations:

- Wooldridge & Jennings / Shoham for historical agent concept.
- Anthropic / OpenAI for modern workflow-agent framing.

Hidden annotations:

- "taxonomy, not formal ontology";
- evidence-strength legend.

### 2. The main design question: who controls the loop?

Keep/rename:

- Current A2 autonomy material.
- Anthropic workflow-vs-agent distinction.

Rewrite:

- Rename from diagnostic language to "Autonomy is a gradient."
- Attribute Anthropic as an influential practitioner frame, not consensus.
- Connect to OpenAI Practical Guide as second practical source.

Visible citations:

- Anthropic Building Effective Agents;
- OpenAI Practical Guide.

Hidden annotations:

- caveat: no peer-reviewed consensus that this is the full taxonomy.

### 3. Core map: autonomy x topology x coordination

Keep:

- A2/A3/A4 as the core.
- Topology x coordination grid.

Rewrite:

- Replace "most independent" with "most useful independent decisions in this page's map."
- Replace "any cell is real architecture" with "the grid is a design space; some cells are common, some rare, some mostly theoretical."
- Delete unsupported "80% production" claim.

Visible citations:

- Contract Net for auction/delegation;
- AutoGen/Magentic-One or Anthropic multi-agent system for multi-agent coordination;
- LangGraph/official docs only if kept as product/framework examples.

Hidden annotations:

- each grid example gets type: paper, framework doc, product example, metaphor.

### 4. Composition: model, augmented LLM, harness, subagents

Keep:

- The recursion/call graph idea.
- The "calls/contracts, not physical containment" distinction.

Rewrite:

- Remove "in the source there were five levels."
- Say: "Composition is recursive because a harness can call tools, agents or peers through contracts."
- Change "canonical primitive" to "useful base primitive in Anthropic's framing."

Visible citations:

- Anthropic Building Effective Agents for augmented LLM;
- ReAct for reasoning/action loop;
- A2A spec or Contract Net for delegation/contracts if used.

Hidden annotations:

- limitation: not every product exposes subagent internals.

### 5. Tools and memory as agent-facing surfaces

Combine:

- Current `Memory typology`.
- Current "Tools != classical software" from research backfill.

Rewrite:

- Explain that tools, retrieval, memory and context are not minor implementation details; they define what the agent can perceive, do and remember.
- Present working/episodic/semantic/procedural as **practical typology**, not field-wide standard.
- Keep boundary table: context window, retrieval, logs are not memory by default.

Visible citations:

- Anthropic Writing Tools for Agents;
- MemGPT;
- Generative Agents;
- Reflexion;
- MCP specification.

Hidden annotations:

- source-specific examples of memory architecture;
- caveat from negative findings on no universal memory taxonomy.

### 6. Protocol and stack layer

Keep:

- Model/protocol/pattern/framework/platform/infrastructure distinction.

Rewrite:

- Split "protocols" by standardization target:
  - tool/context access: MCP;
  - agent-to-agent task/message/artifact exchange: A2A;
  - runtime/client-server execution API: LangChain Agent Protocol;
  - identity/discovery/interoperability ecosystem: AGNTCY;
  - observability semantics: OpenTelemetry GenAI.
- Remove "MCP de-facto standard" unless heavily qualified.
- Rewrite A2A as active, date-stamped and scope-specific.

Visible citations:

- MCP spec;
- A2A spec;
- Linux Foundation A2A 2026 release;
- LangChain Agent Protocol repo;
- AGNTCY docs;
- OpenTelemetry GenAI conventions.

Hidden annotations:

- comparative adoption evidence is mixed;
- exact access/review date.

### 7. Failure modes and safety boundaries

Keep:

- Cascading errors;
- context poisoning;
- hallucination amplification;
- infinite loops;
- agreement bias, if caveated;
- trust-boundary rule.

Rewrite:

- Tie each failure to architecture, tool authority, memory, protocol handoff and human approval.
- Add explicit statement: HITL is useful but insufficient alone.

Visible citations:

- OWASP LLM Top 10;
- OWASP Agentic Skills Top 10;
- AgentDojo;
- OpenAI Operator System Card;
- Five Eyes 2026 guidance.

Hidden annotations:

- per-row evidence source;
- failure label status: standard / page-defined / heuristic.

### 8. Evaluation and observability

Keep:

- Baseline -> inspect traces -> change architecture -> rerun regression.
- Trace events and metrics table.

Rewrite:

- Replace "evaluation chooses architecture" with "local evals and traces decide whether extra architecture is justified."
- Clarify that public benchmarks provide eval dimensions, not universal production scores.

Visible citations:

- OpenAI tracing docs;
- OpenTelemetry GenAI conventions;
- AgentBench/WebArena/SWE-bench/GAIA/tau-bench/OSWorld/PaperBench as benchmark-design sources.

Hidden annotations:

- benchmark scope tags: web, coding, GUI, tool-user-policy, long-horizon research.

### 9. Real systems as dated map points

Move later than current placement. The reader should first understand the axes.

Keep:

- Cursor, Devin, Claude Code, Manus, deep research, AutoGPT as examples if sourced.

Rewrite:

- For each system show:
  - documented surface;
  - taxonomy inference;
  - unknown/internal caveat;
  - review date.
- Do not imply internal topology unless official docs say it.

Visible citations:

- official docs per product, with access date.

Hidden annotations:

- product source links;
- evidence strength per coordinate.

### 10. Timeline: how the map became necessary

Move after core concepts and systems.

Keep:

- 2022 ReAct;
- 2023 tool/function calling;
- 2024 workflow-agent framing;
- 2025 multi-agent/computer-use execution surfaces;
- 2026 harness hardening/protocol maturation.

Rewrite:

- Use exact evidence dates.
- Make timeline explain why architecture changed, not just what launched.
- Change "April snapshot" to "reviewed through 2026-06-03."

Visible citations:

- one marker per milestone.

Hidden annotations:

- why milestone affects control loop, tool contract, topology or execution substrate.

### 11. Decision guide

Keep:

- "simplest architecture that fits."
- Prompt -> workflow -> augmented LLM -> single-agent -> multi-agent.
- Memory/eval/HITL gates.

Rewrite:

- Put as synthesis after evidence sections.
- Add safety caveat: HITL gate requires permissions, trusted context, audit and rollback.

Visible citations:

- Anthropic and OpenAI practical guides;
- OWASP/Five Eyes/OpenAI Operator for HITL/risk controls.

Hidden annotations:

- each recommendation links to section evidence.

### 12. Appendix / hidden notes

Move here:

- current `§01` diagnostic;
- current `§14` research backfill;
- current `§15` "what remained from original";
- rejected/negative findings summary;
- source methodology;
- maybe a compact "change history" if the author wants it preserved.

Reader default:

- appendix collapsed.
- no internal task language in main flow.

## Sections to delete from main narrative

- `§01 — диагностика` as public opening.
- `§14 — research backfill` as main section.
- `§15 — что осталось от исходника`.
- Unsupported exact quantitative claims like "80% production."
- Causal adoption lesson about developer experience vs corporate architecture unless backed by research.

## Sections to rename

- `§02 — структура` -> `The Map: Dimensions of Agent Systems`
- `§03 — главное наблюдение` -> `Core Design Space: Topology x Coordination`
- `§05 — композиция` -> `Composition Is Recursive`
- `§06 — пропуск исходника` -> `Workflow Patterns and the Autonomy Gradient`
- `§07 — тех. слой` -> `Stack and Protocol Targets`
- `§09 — проверка` -> `Evaluation and Observability`
- `§11 — память` -> `Memory, Context and Retrieval`
- `§13 — decision tree` -> `Choosing the Smallest Architecture That Works`

## Citation strategy

Visible citations should appear only where they carry trust:

- contested claims;
- protocol/product status;
- safety recommendations;
- timeline milestones;
- benchmark/eval claims;
- definitions borrowed from named sources.

Hidden annotations should handle:

- detailed source notes;
- evidence strength;
- caveats;
- reasoning bridge;
- rejected/negative findings.
