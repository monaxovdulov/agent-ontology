# Evidence Gaps

## P0 gaps: must fix before public rewrite

### 1. MCP vs A2A comparative adoption

Current wording says MCP is stronger in developer adoption and A2A is enterprise-niche. Research explicitly says comparative public adoption evidence is weak/contested.

Available support:

- MCP specification: supports MCP scope and primitives.
- Google A2A announcement: supports launch intent.
- A2A specification: supports technical scope.
- Linux Foundation 2026-04-09 update: supports active project/v1.0.0/governance/adoption claims, but is not neutral comparative adoption data.
- `research/negative-findings.md`: says no robust public apples-to-apples adoption metric was found.

Needed rewrite:

"MCP and A2A standardize different surfaces. MCP is prominent in developer tool/context integrations; A2A is active under Linux Foundation governance and oriented toward agent-to-agent interoperability. Public comparative adoption evidence is mixed and date-sensitive."

### 2. "80% production systems today"

No source in `research/` supports this quantitative claim.

Action: delete unless a robust survey or dataset is added. A vague replacement like "many production systems" still needs evidence or should be framed as "common practitioner pattern in reviewed sources."

### 3. Product/system placements

The page maps Cursor, Devin, Claude Code, Manus, deep research and AutoGPT onto A2/A3/A4. Product docs can support visible features, but not hidden internal topology.

Available support:

- footer mentions product docs, but these are not included in `research/sources.md`;
- `research/negative-findings.md` warns product architecture claims are mostly inference.

Needed:

- add product docs to research catalog or annotate them as page-local sources;
- add access dates;
- separate documented feature from taxonomy inference;
- keep Manus and similar systems explicitly tentative.

### 4. Safety/failure-mode taxonomy

Failure modes are useful but currently under-sourced.

Available support:

- AgentDojo: indirect prompt injection and tool-use attacks.
- OWASP LLM Top 10 2025: prompt injection, excessive agency, data leakage, supply-chain risks.
- OWASP Agentic Skills Top 10: agent skill/tool execution risks.
- Five Eyes 2026: governance, permissions, monitoring and controls.
- OpenAI Operator System Card: browser-acting agents, confirmations, restricted actions, adversarial risks.
- Anthropic Writing Tools for Agents: tool outputs and schemas as reasoning surface.

Needed:

- local citations near context poisoning, tool-output trust, excessive agency, HITL, audit and permissions claims;
- caveat that HITL is not sufficient alone.

### 5. Evaluation & observability

The page has strong advice but lacks claim-level evidence.

Available support:

- OpenAI Agents SDK tracing docs;
- OpenTelemetry GenAI semantic conventions;
- AgentBench, WebArena, SWE-bench, GAIA, tau-bench, OSWorld, PaperBench, BrowseComp.

Needed:

- distinguish public benchmark design from local production evals;
- cite benchmark papers for eval dimensions, not leaderboard scores;
- cite tracing specs/docs for trace event vocabulary.

## P1 gaps: should fix during rewrite

### 6. Anthropic five patterns as vocabulary

Research supports "influential practitioner vocabulary", not "canonical consensus".

Available support:

- Anthropic Building Effective Agents;
- OpenAI Practical Guide;
- AutoGen and Magentic-One as alternative architectures;
- LangChain Agent Protocol / LangGraph-style framing;
- `research/negative-findings.md` on no peer-reviewed consensus.

Needed:

- keep Anthropic patterns, but explicitly scope them to workflow/control-flow patterns;
- avoid "all major frameworks", "standard vocabulary", "complete theory".

### 7. Augmented LLM as primitive

Research supports it as a useful Anthropic base primitive, not a universal atom.

Available support:

- Anthropic Building Effective Agents;
- OpenAI Practical Guide;
- ReAct;
- MCP specification.

Needed:

- say "for this practical map" and attribute to Anthropic;
- avoid "канонический" and "атом всех современных агентных систем".

### 8. Memory typology

The four-part split is useful, but not universal.

Available support:

- MemGPT;
- Generative Agents;
- Reflexion;
- MCP specification;
- `research/negative-findings.md` on no universal agent-memory taxonomy.

Needed:

- present as practical typology;
- add caveat that products and papers use memory terms inconsistently;
- source claims about working/episodic/semantic/procedural separately.

### 9. Timeline 2022-2026

Timeline claims are plausible but need milestone-level evidence.

Available support:

- ReAct for 2022;
- OpenAI function calling for 2023;
- Anthropic Building Effective Agents for 2024 workflow/agent framing;
- OpenAI CUA docs / Operator System Card and Anthropic multi-agent research system for 2025;
- OpenAI Agents SDK docs, A2A spec/LF release, Five Eyes 2026 for 2026.

Needed:

- update from "April snapshot" to an explicit "reviewed through 2026-06-03";
- cite each milestone locally;
- explain why each changed control loop, contracts, topology or execution substrate.

### 10. Classic MAS transfer

Research catalog has Wooldridge & Jennings, Shoham, Contract Net and BDI. Current footer also cites Hearsay-II, Nii, FIPA and Minsky, which are not in `research/sources.md`.

Needed:

- either add those sources to `research/` before using them as evidence;
- or limit page claims to sources already in the research catalog;
- keep Society of Mind as metaphor/annotation, not core taxonomy evidence.

## P2 gaps: useful cleanup

### 11. Stack layer examples

Examples like Vertex AI, Bedrock, Langfuse, Helicone, Pydantic AI and Spring AI are not locally sourced. They are probably fine as examples, but should not carry strong claims.

Action: keep as non-evidentiary examples or annotate only if used for argument.

### 12. "Tools != classical software"

Anthropic Writing Tools supports the direction, but the current wording makes a broad deterministic/non-deterministic contrast. It should be softened and attached to source.

Action: keep, but frame as tool-interface design principle rather than formal theorem.

### 13. Emergence

The page's skepticism is useful for engineering, but "strong emergence rarely provable" is philosophically loaded.

Action: move to annotation or rewrite as "prefer traceable mechanisms before using emergence as explanation."
