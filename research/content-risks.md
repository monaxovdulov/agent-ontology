# Content Risks

These are current page claims or themes that should be handled carefully in a future edit. This pass does not edit `index.html`.

## 1. Anthropic Patterns as "Standard Vocabulary"

- **Current formulation / topic:** The page says Anthropic introduced a standard vocabulary now repeated by all major frameworks.
- **Why risky:** Anthropic's framework is influential and useful, but this refresh did not find peer-reviewed consensus that the five workflow patterns are a universal taxonomy. Some frameworks echo the patterns; others use graph, actor, crew, conversation, or runtime-control vocabularies.
- **Sources:** Anthropic Building Effective Agents; OpenAI Practical Guide; LangChain Agent Protocol; AutoGen; Magentic-One.
- **Safer formulation:** "Anthropic's five-pattern framing is an influential practitioner vocabulary for LLM workflows. It is useful for this taxonomy, but should not be treated as the full consensus of agent architecture research."

## 2. MCP Stronger Than A2A in Developer Adoption

- **Current formulation / topic:** "2026: MCP stronger with developers; A2A alive but enterprise-niche."
- **Why risky:** Public evidence for comparative adoption is weak and proxy-based. A2A has a Linux Foundation project, a stable v1.0.0 specification released on 2026-04-09, and official adoption claims. MCP also has strong developer mindshare and ecosystem usage, but no apples-to-apples public metric was found.
- **Sources:** MCP 2025-11-25 specification; A2A latest specification; Google A2A announcement; Linux Foundation A2A v1.0 release.
- **Safer formulation:** "MCP and A2A standardize different surfaces. MCP is prominent in developer tool/context integrations; A2A is active and enterprise/interoperability-oriented under Linux Foundation governance. Comparative public adoption evidence is mixed and should be date-stamped."

## 3. A2A Status Based Only on Launch-Era Sources

- **Current formulation / topic:** A2A described from 2025 launch and transfer context.
- **Why risky:** A2A's status changed after launch: latest specs and the 2026 v1.0.0 release should be included for any current claim.
- **Sources:** A2A specification; Linux Foundation 2026-04-09 release; Google Developers Blog 2025-04-09.
- **Safer formulation:** "Google launched A2A in April 2025; the Linux Foundation A2A project later published v1.0.0 in April 2026. Treat claims about adoption and niche as time-sensitive."

## 4. "Augmented LLM" as Canonical Primitive

- **Current formulation / topic:** Augmented LLM is described as the canonical primitive: model + tools + retrieval + memory.
- **Why risky:** This is a strong Anthropic practitioner abstraction, not a universal formal primitive. It remains useful, but should be attributed.
- **Sources:** Anthropic Building Effective Agents; OpenAI Practical Guide; ReAct; MCP specification.
- **Safer formulation:** "For this practical map, Anthropic's augmented LLM is a useful base primitive: model plus tools, retrieval, and memory."

## 5. Memory as Four Fixed Types

- **Current formulation / topic:** Working, episodic, semantic, and procedural memory are presented as the memory typology.
- **Why risky:** This is a practical taxonomy, not a standardized agent-memory ontology. Literature uses overlapping terms, and products often conflate memory, retrieval, context, and logs.
- **Sources:** MemGPT; Generative Agents; Reflexion; MCP specification.
- **Safer formulation:** "A practical memory split for this page is working, episodic, semantic, and procedural memory; the important engineering requirement is explicit read/write policy, provenance, TTL, and separation from logs/context."

## 6. Multi-Agent Cost Amplification

- **Current formulation / topic:** Multi-agent systems can dramatically increase token usage and observability burden.
- **Why risky:** Anthropic's multi-agent research case is strong but domain-specific. The exact multiplier should not be generalized to all multi-agent systems.
- **Sources:** Anthropic multi-agent research system; Magentic-One; AutoGen.
- **Safer formulation:** "Production multi-agent systems can substantially increase cost and trace volume; Anthropic reports this in a broad research setting, so cost amplification should be measured per task domain."

## 7. HITL as a Safety Gate

- **Current formulation / topic:** HITL gates are recommended for irreversible or high-risk actions.
- **Why risky:** Human approval is necessary in some settings but not sufficient. Approval prompts can be poorly contextualized, agent summaries can hide malicious tool output, and users can rubber-stamp repeated requests.
- **Sources:** OpenAI Operator System Card; OWASP Agentic Skills Top 10; OWASP LLM Top 10; Five Eyes 2026 guidance; AgentDojo.
- **Safer formulation:** "Use HITL for irreversible or high-risk actions, but pair it with trusted UI, scoped permissions, audit trails, policy checks, and untrusted-content boundaries."

## 8. Prompt Injection and Context Poisoning

- **Current formulation / topic:** Tool outputs, retrieved content, and shared memory can poison context.
- **Why risky:** The page's framing is good, but it should cite security work and specify that prompt injection is not only a prompt problem; it is a boundary and authority problem.
- **Sources:** AgentDojo; OWASP LLM Top 10; OWASP Agentic Top 10; Anthropic Writing Tools for Agents.
- **Safer formulation:** "Treat retrieved content, peer output, and tool responses as untrusted data unless explicitly promoted through policy; never let untrusted text acquire instruction authority."

## 9. Evaluation Chooses Architecture

- **Current formulation / topic:** Architecture should be selected by evals and traces.
- **Why risky:** The claim is directionally strong, but the page should avoid implying that public benchmarks alone decide production architecture. Local task evals, trace analysis, regression suites, and risk controls are all needed.
- **Sources:** AgentBench; WebArena; SWE-bench; GAIA; tau-bench; OSWorld; PaperBench; OpenAI tracing docs; OpenTelemetry GenAI semantic conventions.
- **Safer formulation:** "Public benchmarks suggest eval dimensions; production architecture should be selected by local task evals, traces, cost/latency, intervention rate, and regression risk."

## 10. Product Architecture Placement

- **Current formulation / topic:** Real systems are plotted as points on the map: Codex, Claude Code, Cursor, Devin, OpenAI deep research, AutoGPT, etc.
- **Why risky:** Product docs change rapidly and rarely expose full internal architecture. Public docs can support visible features and UX/control surfaces, not hidden topology.
- **Sources:** OpenAI Agents SDK docs; OpenAI Computer Use docs; product docs in current footer; Anthropic multi-agent research system for one unusually detailed case.
- **Safer formulation:** "These placements are based on public product docs and observed control surfaces as of a dated review; internal architecture may differ."

## 11. Protocol Layer as a Single Axis

- **Current formulation / topic:** MCP, A2A, Agent Protocol, and AGNTCY are listed together as protocols.
- **Why risky:** They solve different problems: tool/context exchange, agent-to-agent messaging, runtime execution APIs, identity/discovery/interoperability ecosystems. Grouping is fine, but comparison should be by scope.
- **Sources:** MCP specification; A2A specification; LangChain Agent Protocol; AGNTCY docs.
- **Safer formulation:** "The protocol layer contains different standardization targets: tool/context access, agent-to-agent messages, runtime-control APIs, identity/discovery, and observability."

## 12. "Emergence" in Engineering Systems

- **Current formulation / topic:** Strong emergence is treated skeptically and framed as often hiding missing observability.
- **Why risky:** The engineering point is useful, but "strong emergence" is a philosophical/scientific claim and should not be over-asserted without sources.
- **Sources:** Classic MAS sources; Generative Agents; evaluation and observability sources.
- **Safer formulation:** "For architecture work, explain multi-agent behavior through topology, memory, tools, coordination, and traces before attributing it to emergence."
