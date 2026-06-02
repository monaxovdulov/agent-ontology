# Negative Findings

This file records what was searched but not strongly confirmed. These findings are useful because they prevent weak claims from becoming page copy.

## 1. No Robust Public Evidence That MCP Has Clearly Stronger Developer Adoption Than A2A

- **Searched for:** comparative adoption studies, public metrics, SDK/download data, integration counts, production deployment counts, and credible ecosystem analyses for MCP vs A2A.
- **Finding:** Public sources show both projects are active, but no apples-to-apples metric was found. Official A2A sources report Linux Foundation governance, v1.0.0, and adoption claims; MCP has strong developer ecosystem visibility and official specs, but comparable public adoption data is weak.
- **Implication:** Future page wording should avoid "MCP won" or "A2A failed" claims. Use date-stamped, scope-specific wording.
- **Evidence status:** weak / contested.

## 2. No Peer-Reviewed Consensus That Anthropic's Five Patterns Are the Canonical Agent Taxonomy

- **Searched for:** papers or formal taxonomies adopting Anthropic's exact five workflow patterns as consensus.
- **Finding:** Anthropic's framing is influential and repeated in implementation guides, but evidence supports "practitioner vocabulary," not "scientific consensus."
- **Implication:** The page should attribute the framing to Anthropic and separate it from broader MAS and LLM-agent literature.
- **Evidence status:** influential but not consensus.

## 3. No Universal Agent-Memory Taxonomy

- **Searched for:** standardized agent-memory typologies matching working/episodic/semantic/procedural memory.
- **Finding:** The four terms are useful and grounded in cognitive vocabulary plus agent architectures, but LLM-agent papers and products use memory terms inconsistently. Some mean RAG, some mean conversation history, some mean reflection logs, and some mean long-term structured stores.
- **Implication:** Present the four-part memory split as this page's practical typology, not a field-wide ontology.
- **Evidence status:** useful but non-standardized.

## 4. Limited Evidence That Multi-Agent Architectures Generally Outperform Single-Agent or Workflow Systems

- **Searched for:** broad, independent studies showing multi-agent superiority across tasks.
- **Finding:** Strong evidence is task-conditional. Anthropic reports gains for broad research tasks; AutoGen/Magentic-One show architectural possibilities; benchmarks show many agent systems still struggle. No general "multi-agent is better" conclusion was found.
- **Implication:** The page should keep its rule: multi-agent only when evals show improvement under cost, latency, and risk constraints.
- **Evidence status:** conditional.

## 5. No Stable Public Map of Agent Protocol Scope and Adoption

- **Searched for:** authoritative comparison across MCP, A2A, LangChain Agent Protocol, AGNTCY, and related protocols.
- **Finding:** Official specs define each project, but secondary comparisons often collapse different scopes: tool/context access, agent-to-agent messages, runtime execution APIs, identity/discovery, and observability.
- **Implication:** The page should compare protocols by standardization target, not by a single maturity ladder.
- **Evidence status:** scope clear in specs; comparative adoption weak.

## 6. Product Architecture Claims Are Mostly Inference

- **Searched for:** official architecture details for Cursor, Devin, Manus, Claude Code, Codex, OpenAI deep research, AutoGPT, and related systems.
- **Finding:** Official docs support visible features and workflow surfaces, but full internal architecture is usually not public. The exception is occasional engineering write-ups such as Anthropic's multi-agent research system.
- **Implication:** Plot product examples as public-facing control surfaces and documented behavior, not definitive internal topology.
- **Evidence status:** product docs are primary for features, weak for internals.

## 7. HITL Is Not Proven as a Sufficient Safety Control

- **Searched for:** agent safety guidance treating human approval as sufficient mitigation.
- **Finding:** Stronger sources frame HITL as one control among permissions, sandboxing, monitoring, policy enforcement, audit, and trusted UI. Prompt injection and context poisoning can also affect what the human sees.
- **Implication:** Future page language should say HITL gates reduce risk only when paired with trusted context, action scoping, and auditability.
- **Evidence status:** HITL useful but insufficient alone.

## 8. Benchmark Leaderboards Are Too Volatile for Durable Page Claims

- **Searched for:** current best scores on AgentBench, WebArena, SWE-bench, GAIA, OSWorld, PaperBench, BrowseComp, and tau-bench.
- **Finding:** Scores change too quickly and depend on harness choices. Benchmark papers are still useful for task design and evaluation dimensions.
- **Implication:** Cite benchmark designs, not current top scores, unless the page adds an explicitly dated benchmark snapshot.
- **Evidence status:** benchmark design durable; scores time-sensitive.

## 9. "Emergence" Is Not a Useful Primary Engineering Explanation

- **Searched for:** sources that make strong emergence claims actionable for LLM multi-agent system design.
- **Finding:** This refresh found stronger engineering explanations through topology, coordination, shared memory, tool boundaries, and traces. "Emergence" remains a possible descriptive term but does not replace observability.
- **Implication:** Keep emergence language cautious and mechanism-first.
- **Evidence status:** contested / low direct utility for taxonomy.

## 10. Agent Protocol Security Is Still Fragmented

- **Searched for:** unified security model across MCP, A2A, Agent Protocol, and AGNTCY.
- **Finding:** Protocol specs and security guidance discuss authentication, authorization, identity, and trust boundaries, but there is no single mature cross-protocol security framework in the reviewed sources.
- **Implication:** Treat protocol security as an area needing ongoing review, especially around delegated actions, agent identity, tool authority, and untrusted content.
- **Evidence status:** incomplete / evolving.
