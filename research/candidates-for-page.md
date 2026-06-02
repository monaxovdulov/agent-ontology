# Candidates for Future Page Updates

This file lists future edit candidates only. Do not apply them automatically to `index.html`; review the wording and visual impact in a separate page-edit pass.

## High-Confidence Additions

1. **Add classic MAS backfill near the taxonomy framing.**
   - Add Wooldridge & Jennings 1995 for autonomy, reactivity, proactiveness, and social ability.
   - Add Shoham 1993 for agent-oriented programming.
   - Add Smith 1980 Contract Net for task allocation/delegation.
   - Add Rao & Georgeff 1995 for BDI plan/commitment background.
   - Suggested role: a short note that modern LLM agents reuse old agent-system questions but implement them with different substrates: prompts, tools, memory stores, traces, and model calls.

2. **Add current A2A status with date-stamped wording.**
   - Use Google A2A announcement for original scope.
   - Use A2A specification for technical scope.
   - Use Linux Foundation 2026-04-09 v1.0.0 release for current project status.
   - Suggested page claim: "A2A is active and enterprise/interoperability-oriented; comparative adoption versus MCP is not well evidenced by public data."

3. **Add security sources to failure modes and HITL guidance.**
   - Use OWASP LLM Top 10 2025, OWASP Agentic Skills Top 10, AgentDojo, OpenAI Operator System Card, and Five Eyes 2026 guidance.
   - Add a note that HITL is not a universal safety layer; it must be tied to irreversible actions, permissions, audit trail, and trusted UI/context boundaries.

4. **Add benchmark coverage to Evaluation & Observability.**
   - AgentBench: interactive environments.
   - WebArena: realistic web tasks.
   - SWE-bench: software issue resolution.
   - GAIA: general assistant tasks requiring tools and reasoning.
   - tau-bench: tool-agent-user-policy interactions.
   - OSWorld: desktop/computer-use tasks.
   - PaperBench and BrowseComp: long-horizon research implementation and browsing/research tasks.
   - Suggested wording: "Use benchmark design as a source of eval dimensions; do not cite transient leaderboard scores as durable facts."

5. **Add OpenTelemetry GenAI semantic conventions to observability.**
   - This gives the page a vendor-neutral source for tracing terms and attributes.
   - It complements OpenAI Agents SDK tracing and avoids tying observability only to one platform.

6. **Add a tool-design note from Anthropic Writing Tools for Agents.**
   - Suggested location: "Tools != classical software" or failure modes.
   - Key idea: tool names, schemas, descriptions, and outputs are part of the agent's reasoning surface.

## Wording Corrections

1. **Anthropic five-pattern framing**
   - Current risk: "standard vocabulary repeated by all major frameworks" sounds too close to consensus.
   - Safer wording: "Anthropic's framing is an influential practitioner vocabulary that many frameworks echo or implement, but it is not a peer-reviewed consensus taxonomy."

2. **MCP vs A2A adoption**
   - Current risk: "MCP stronger developer adoption; A2A enterprise-niche" may now be too categorical.
   - Safer wording: "MCP and A2A standardize different interfaces. MCP has strong developer mindshare around tool/context integration; A2A has active Linux Foundation governance and enterprise/interoperability support. Public comparative adoption evidence is mixed and should be date-stamped."

3. **"Canonical" augmented LLM**
   - Current risk: "canonical primitive" can read as universal.
   - Safer wording: "Anthropic's useful base primitive for modern agentic systems is the augmented LLM: model plus tools, retrieval, and memory."

4. **Memory typology**
   - Current risk: four memory types may read as a formal ontology.
   - Safer wording: "A practical typology for this page: working, episodic, semantic, and procedural memory. Literature and products do not use one universal memory taxonomy."

5. **Multi-agent cost claims**
   - Current risk: Anthropic's reported token multiplication could be overgeneralized.
   - Safer wording: "In Anthropic's research system, multi-agent orchestration consumed substantially more tokens; treat cost amplification as a design risk, not a universal constant."

6. **Emergence language**
   - Current risk: "strong emergence is rarely provable" is plausible but philosophical and under-cited.
   - Safer wording: "For engineering decisions, prefer observable mechanisms, traces, and evals over attributing behavior to emergence."

## Sources to Replace Older Citations

1. **A2A**
   - Keep: Google Developers Blog 2025-04-09 for launch.
   - Add/replace with: A2A latest specification and Linux Foundation 2026-04-09 v1.0.0 release.
   - Reason: launch-era status is stale for 2026 protocol claims.

2. **MCP**
   - Add/replace with: dated MCP 2025-11-25 specification.
   - Reason: source claims about MCP primitives from the spec, not only the announcement metaphor.

3. **OpenAI agent platform**
   - Add: current Agents SDK docs and tracing docs.
   - Reason: page footer mentions an OpenAI 2026 Agents SDK evolution; living docs are the stronger check for capabilities and terminology.

4. **Evaluation**
   - Add benchmark papers plus OpenTelemetry GenAI conventions.
   - Reason: current page has good evaluation prose but few explicit benchmark/spec anchors.

5. **Safety**
   - Add OWASP, AgentDojo, OpenAI Operator System Card, and Five Eyes 2026 guidance.
   - Reason: current failure modes are useful but need stronger external evidence.

## Items Needing More Evidence Before Adding

1. **"MCP has stronger developer adoption than A2A."**
   - Need public, comparable adoption metrics: active integrations, production deployments, SDK downloads, governance participation, implementation compatibility, or survey data.
   - Current evidence is mixed and mostly proxy-based.

2. **"A2A is enterprise-niche."**
   - Likely directionally plausible, but the phrase should be softened unless backed by public adoption analysis.
   - Linux Foundation's 2026 update should be included if the page keeps any A2A status claim.

3. **"All major frameworks repeat Anthropic's five patterns."**
   - Need a careful source survey across OpenAI, LangGraph/LangChain, Spring AI, Microsoft AutoGen, CrewAI, and others.
   - Better to call it influential rather than universal.

4. **Specific product placements for Cursor, Devin, Manus, AutoGPT, Claude Code, Codex, and OpenAI deep research.**
   - Official docs can support feature existence, but product behavior changes quickly.
   - Use access dates and avoid claims about internal architecture unless official docs say it.

5. **AGNTCY and LangChain Agent Protocol durability.**
   - Both are useful protocol examples, but future page claims should verify project activity and ecosystem adoption at edit time.

6. **Memory subtypes beyond working / episodic / semantic / procedural.**
   - Additional taxonomies exist, but no single agent-memory standard emerged from this refresh.
   - Add more only if it improves decisions or failure-mode reasoning.
