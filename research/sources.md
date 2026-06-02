# Sources Catalog

Selected sources are grouped here as a working catalog for future page edits. `use` means the source is strong enough to support page wording; `maybe` means useful context but should not carry a strong claim alone.

## 1. Anthropic: Building Effective Agents

- **Authors / org:** Erik Schluntz and Barry Zhang, Anthropic
- **Year / date:** 2024-12-19
- **URL:** https://www.anthropic.com/engineering/building-effective-agents
- **Type:** official engineering blog / architecture guide
- **Evidence tier:** Tier 2
- **Reliability:** primary
- **Categories:** agent architecture patterns; workflow vs agent autonomy; tool use and tool design; evaluation and observability
- **Why it matters:** This is the strongest primary source for the current page's distinction between workflows and agents, plus the augmented LLM and five workflow patterns. It strengthens the taxonomy by giving a practitioner vocabulary for when control flow is encoded in code versus dynamically selected by the model.
- **Gap closed:** Prevents the page from treating all multi-step LLM systems as "agents."
- **Why this source:** It is more primary than framework retellings of the same pattern set.
- **Page sections:** "Категориальный дребезг"; "Пять канонических паттернов"; "Decision tree"; "Evaluation & Observability"
- **Note:** use

## 2. Anthropic: Writing Tools for Agents

- **Authors / org:** Anthropic
- **Year / date:** 2025-09-11
- **URL:** https://www.anthropic.com/engineering/writing-tools-for-agents
- **Type:** official engineering blog / tool design case study
- **Evidence tier:** Tier 2
- **Reliability:** primary
- **Categories:** tool use and tool design; safety / HITL / security / prompt injection; production agent systems
- **Why it matters:** The article gives concrete guidance on tool interface design, context efficiency, error handling, and agent-facing affordances. It supports the page's claim that tools are not just classical APIs: their names, descriptions, schemas, and outputs become part of the agent's reasoning environment.
- **Gap closed:** Adds evidence for why tool design is an agent architecture concern, not a minor implementation detail.
- **Why this source:** It is a primary production lesson from a frontier lab, more useful than generic "tools for agents" explainers.
- **Page sections:** "Tools != classical software"; "Failure modes"; "Decision tree"
- **Note:** use

## 3. Anthropic: How We Built Our Multi-Agent Research System

- **Authors / org:** Anthropic
- **Year / date:** 2025-06-13
- **URL:** https://www.anthropic.com/engineering/built-multi-agent-research-system
- **Type:** official engineering blog / production case study
- **Evidence tier:** Tier 2
- **Reliability:** primary
- **Categories:** multi-agent coordination; production agent systems; evaluation and observability; safety / HITL
- **Why it matters:** This is a rare detailed production write-up on when multi-agent coordination helped, what topology was used, and what costs followed. It is useful for claims about broad research tasks, parallel subagents, traces, and the fact that multi-agent systems can dramatically increase token usage.
- **Gap closed:** Replaces vague "multi-agent is better" language with a narrower condition: broad, parallelizable research with clear supervisor-worker orchestration.
- **Why this source:** It gives concrete system design and measured trade-offs rather than a conceptual overview.
- **Page sections:** "Реальные системы"; "Топология x координация"; "Evaluation & Observability"; "Anti-patterns"
- **Note:** use

## 4. OpenAI: A Practical Guide to Building Agents

- **Authors / org:** OpenAI
- **Year / date:** 2025; exact publication date not captured in source
- **URL:** https://cdn.openai.com/business-guides-and-resources/a-practical-guide-to-building-agents.pdf
- **Type:** official guide / technical report
- **Evidence tier:** Tier 1
- **Reliability:** primary
- **Categories:** agent architecture patterns; workflow vs agent autonomy; tool use and tool design; safety / HITL; evaluation and observability
- **Why it matters:** The guide is a primary OpenAI source for practical agent design: tool selection, guardrails, orchestration, and incremental deployment. It is useful as a second independent source for the "start simple, add autonomy only when justified" rule.
- **Gap closed:** Reduces dependence on Anthropic as the single source for workflow-vs-agent framing.
- **Why this source:** It is official and implementation-oriented, stronger than sales pages about agent platforms.
- **Page sections:** "Decision tree"; "Evaluation & Observability"; "Failure modes"
- **Note:** use

## 5. OpenAI Agents SDK Documentation

- **Authors / org:** OpenAI
- **Year / date:** living docs; accessed 2026-06-03
- **URL:** https://platform.openai.com/docs/guides/agents
- **Type:** official docs
- **Evidence tier:** Tier 1
- **Reliability:** primary
- **Categories:** production agent systems; tool use and tool design; evaluation and observability; workflow vs agent autonomy
- **Why it matters:** The docs give current OpenAI vocabulary for hosted tools, handoffs, guardrails, and agent execution. They are useful for checking whether the page's "OpenAI Responses API / Agents SDK" positioning is current.
- **Gap closed:** Keeps product-system placement tied to living docs rather than older launch posts.
- **Why this source:** Official docs are better than third-party tutorials for API capabilities and naming.
- **Page sections:** "Реальные системы"; "Стек"; "Evaluation & Observability"
- **Note:** use

## 6. OpenAI Agents SDK Tracing Documentation

- **Authors / org:** OpenAI
- **Year / date:** living docs; accessed 2026-06-03
- **URL:** https://openai.github.io/openai-agents-python/tracing/
- **Type:** official docs
- **Evidence tier:** Tier 1
- **Reliability:** primary
- **Categories:** evaluation and observability; production agent systems
- **Why it matters:** The tracing docs support the page's claim that production agent systems need observable model calls, tool calls, handoffs, and spans. They give a concrete example of tracing as a built-in SDK concern.
- **Gap closed:** Moves observability from a generic "logs" concept to explicit agent execution traces.
- **Why this source:** It is a primary SDK reference and more concrete than broad observability blogs.
- **Page sections:** "Evaluation & Observability"; "Decision tree"
- **Note:** use

## 7. OpenAI: Computer Use Tool Documentation

- **Authors / org:** OpenAI
- **Year / date:** living docs; accessed 2026-06-03
- **URL:** https://platform.openai.com/docs/guides/tools-computer-use
- **Type:** official docs
- **Evidence tier:** Tier 1
- **Reliability:** primary
- **Categories:** production agent systems; tool use and tool design; safety / HITL; evaluation
- **Why it matters:** The current docs are a primary source for computer-use tool loops, screenshots, actions, and interaction with external interfaces. They support the page's distinction between ordinary API tools and agents that act through browser or GUI surfaces.
- **Gap closed:** Grounds "computer use" in official current docs rather than product hype.
- **Why this source:** Official docs are more durable for current capability shape than media coverage of Operator/CUA.
- **Page sections:** "Timeline 2022-2026"; "Реальные системы"; "Failure modes"
- **Note:** use

## 8. OpenAI: Operator System Card

- **Authors / org:** OpenAI
- **Year / date:** 2025-01-23
- **URL:** https://cdn.openai.com/operator_system_card.pdf
- **Type:** official system card / safety report
- **Evidence tier:** Tier 1
- **Reliability:** primary
- **Categories:** safety / HITL / security / prompt injection; production agent systems; tool use
- **Why it matters:** The system card gives concrete safety framing for browser-acting agents: confirmations, restricted actions, monitoring, and adversarial risks. It strengthens the taxonomy's HITL and irreversible-action gates.
- **Gap closed:** Provides a primary source for why human approval and action boundaries are required in computer-use agents.
- **Why this source:** It is system-specific and safety-focused, not a generic AI safety checklist.
- **Page sections:** "Failure modes"; "Decision tree"; "Timeline 2022-2026"
- **Note:** use

## 9. OpenAI: PaperBench

- **Authors / org:** OpenAI
- **Year / date:** 2025-04-02
- **URL:** https://cdn.openai.com/papers/22265bac-3191-44e5-b057-7aaacd8e90cd/paperbench.pdf
- **Type:** benchmark / technical report
- **Evidence tier:** Tier 1
- **Reliability:** primary
- **Categories:** evaluation and observability; production agent systems
- **Why it matters:** PaperBench evaluates long-horizon scientific implementation tasks, which are closer to agent workflows than simple QA. It helps the taxonomy avoid overfitting evaluation language to short tool-use tasks.
- **Gap closed:** Adds evidence that agent evaluation must cover long-horizon artifacts, not only single-turn answer correctness.
- **Why this source:** It is an official benchmark from a lab building agentic systems and includes task design detail.
- **Page sections:** "Evaluation & Observability"; "Decision tree"
- **Note:** use

## 10. OpenAI: BrowseComp

- **Authors / org:** OpenAI
- **Year / date:** 2025-04-16
- **URL:** https://arxiv.org/abs/2504.12516
- **Type:** benchmark / technical report
- **Evidence tier:** Tier 2
- **Reliability:** primary
- **Categories:** evaluation and observability; tool use and retrieval; production agent systems
- **Why it matters:** BrowseComp targets hard web-browsing questions where search, source selection, and multi-step synthesis matter. It is useful for the taxonomy's deep research and web-agent evaluation claims.
- **Gap closed:** Separates retrieval/browser competence from generic model intelligence.
- **Why this source:** It is a purpose-built benchmark from the system developer, better than anecdotal browser-agent demos.
- **Page sections:** "Evaluation & Observability"; "Реальные системы"; "Timeline 2022-2026"
- **Note:** maybe

## 11. Google Developers Blog: Announcing the Agent2Agent Protocol

- **Authors / org:** Google
- **Year / date:** 2025-04-09
- **URL:** https://developers.googleblog.com/en/a2a-a-new-era-of-agent-interoperability/
- **Type:** official announcement / protocol rationale
- **Evidence tier:** Tier 2
- **Reliability:** primary
- **Categories:** agent protocols; multi-agent coordination; production agent systems
- **Why it matters:** This is the primary launch source for A2A's intended niche: agent-to-agent interoperability across vendors and enterprise systems. It supports the page's claim that A2A is complementary to MCP rather than a replacement.
- **Gap closed:** Corrects protocol-layer compression by distinguishing model/tool context protocols from agent-to-agent protocols.
- **Why this source:** It is the launch source and defines the protocol's stated scope.
- **Page sections:** "Протокольный слой"; "Стек"; "Timeline 2022-2026"
- **Note:** use

## 12. A2A Protocol Specification

- **Authors / org:** A2A Project, Linux Foundation
- **Year / date:** latest spec accessed 2026-06-03; v1.0.0 released 2026-04-09
- **URL:** https://a2a-protocol.org/latest/specification/
- **Type:** official protocol specification
- **Evidence tier:** Tier 1
- **Reliability:** primary
- **Categories:** agent protocols; multi-agent coordination; production agent systems
- **Why it matters:** The specification is the durable primary source for A2A's concepts: agent cards, tasks, messages, artifacts, streaming, push notifications, and security. It is stronger than launch blogs for any claim about what A2A actually standardizes.
- **Gap closed:** Prevents outdated A2A wording from relying only on the April 2025 announcement.
- **Why this source:** Official specs beat summaries and vendor adoption posts.
- **Page sections:** "Протокольный слой"; "Стек"; "Content risks"
- **Note:** use

## 13. Linux Foundation: A2A Protocol Surpasses 150 Organizations

- **Authors / org:** Linux Foundation
- **Year / date:** 2026-04-09
- **URL:** https://www.linuxfoundation.org/press/a2a-protocol-surpasses-150-organizations-lands-in-major-cloud-platforms-and-sees-enterprise-production-use-in-first-year
- **Type:** official press release / governance and adoption update
- **Evidence tier:** Tier 2
- **Reliability:** primary for project status; weak for comparative adoption
- **Categories:** agent protocols; production agent systems
- **Why it matters:** The release is important because the current page says A2A is alive but enterprise-niche. By 2026, A2A has a stable v1.0.0 spec and Linux Foundation adoption claims, so future wording should be more date-stamped and less categorical.
- **Gap closed:** Updates the status of A2A from launch-era framing to 2026 project status.
- **Why this source:** It is the project's official governance/adoption update.
- **Page sections:** "Протокольный слой"; "Timeline 2022-2026"; "Content risks"
- **Note:** use with caution

## 14. Model Context Protocol Specification

- **Authors / org:** Model Context Protocol project
- **Year / date:** latest dated specification 2025-11-25; accessed 2026-06-03
- **URL:** https://modelcontextprotocol.io/specification/2025-11-25
- **Type:** official protocol specification
- **Evidence tier:** Tier 1
- **Reliability:** primary
- **Categories:** agent protocols; tool use and tool design; memory and retrieval; production agent systems
- **Why it matters:** MCP is the primary source for standardizing context, tools, prompts, resources, elicitation, sampling, and transport between AI applications and external capabilities. It supports the taxonomy's claim that protocols are a separate layer from frameworks and infrastructure.
- **Gap closed:** Replaces vague "MCP is a protocol" language with exact primitives and scope.
- **Why this source:** The official spec is stronger than launch announcements or third-party MCP lists.
- **Page sections:** "Протокольный слой"; "Стек"; "Tools"; "Memory"
- **Note:** use

## 15. LangChain Agent Protocol

- **Authors / org:** LangChain
- **Year / date:** living repository; accessed 2026-06-03
- **URL:** https://github.com/langchain-ai/agent-protocol
- **Type:** official protocol repository
- **Evidence tier:** Tier 1
- **Reliability:** primary
- **Categories:** agent protocols; workflow vs agent autonomy; production agent systems
- **Why it matters:** Agent Protocol is useful because it standardizes client/server interactions for running agents, not agent-to-agent messaging or tool context. It helps keep the page's protocol layer multi-dimensional instead of MCP-vs-A2A only.
- **Gap closed:** Clarifies that "agent protocol" can mean runtime control APIs, not only interoperability between agents.
- **Why this source:** Official repository beats framework summaries.
- **Page sections:** "Протокольный слой"; "Стек"
- **Note:** maybe

## 16. AGNTCY Documentation

- **Authors / org:** AGNTCY / Linux Foundation project ecosystem
- **Year / date:** living docs; accessed 2026-06-03
- **URL:** https://docs.agntcy.org/
- **Type:** official docs / protocol ecosystem
- **Evidence tier:** Tier 1
- **Reliability:** primary for project scope
- **Categories:** agent protocols; multi-agent coordination; production agent systems
- **Why it matters:** AGNTCY frames a broader "Internet of Agents" ecosystem: identity, directories, interoperability, and agent discovery. It is useful as a contrast to A2A and MCP because it addresses network and registry concerns beyond one transport contract.
- **Gap closed:** Prevents the protocol section from collapsing all protocol work into two names.
- **Why this source:** Official docs are more reliable than vendor press coverage for scope and components.
- **Page sections:** "Протокольный слой"; "Стек"; "Timeline 2022-2026"
- **Note:** maybe

## 17. OpenTelemetry GenAI Semantic Conventions

- **Authors / org:** OpenTelemetry
- **Year / date:** living spec; accessed 2026-06-03
- **URL:** https://opentelemetry.io/docs/specs/semconv/gen-ai/
- **Type:** official observability specification
- **Evidence tier:** Tier 1
- **Reliability:** primary
- **Categories:** evaluation and observability; production agent systems; tool use
- **Why it matters:** The spec gives a vendor-neutral vocabulary for tracing LLM and agent-related operations. It strengthens the page's observability section by connecting traces to an ecosystem standard rather than vendor-specific dashboards.
- **Gap closed:** Adds a standards-backed source for model/tool spans and telemetry fields.
- **Why this source:** It is a standards project, more durable than observability product docs.
- **Page sections:** "Evaluation & Observability"; "Decision tree"
- **Note:** use

## 18. ReAct: Synergizing Reasoning and Acting in Language Models

- **Authors / org:** Shunyu Yao et al.
- **Year / date:** ICLR 2023; arXiv 2022-10
- **URL:** https://openreview.net/forum?id=WE_vluYUL-X
- **Type:** peer-reviewed paper
- **Evidence tier:** Tier 1
- **Reliability:** primary
- **Categories:** agent architecture patterns; tool use and tool design; workflow vs agent autonomy
- **Why it matters:** ReAct is a foundational source for interleaving reasoning traces with external actions. It supports the page's loop-level view of agents and explains why tool calls are part of the reasoning process, not just post-processing.
- **Gap closed:** Grounds modern tool-using LLM agents in a cited research pattern.
- **Why this source:** Peer-reviewed primary source, stronger than later tutorials using the term.
- **Page sections:** footer sources; "Пять канонических паттернов"; "Tools"
- **Note:** use

## 19. Reflexion: Language Agents with Verbal Reinforcement Learning

- **Authors / org:** Noah Shinn et al.
- **Year / date:** 2023
- **URL:** https://arxiv.org/abs/2303.11366
- **Type:** paper / preprint
- **Evidence tier:** Tier 2
- **Reliability:** primary
- **Categories:** agent architecture patterns; memory and retrieval; evaluation and observability
- **Why it matters:** Reflexion is useful for evaluator-optimizer and self-reflection loops, but it also shows why "memory" can mean stored feedback and lessons rather than only RAG. It supports cyclic architectures with explicit feedback and retry budgets.
- **Gap closed:** Adds a research basis for critic/evaluator loops and episodic feedback.
- **Why this source:** It is the primary paper for the named pattern, better than benchmark summaries.
- **Page sections:** "Пять канонических паттернов"; "Memory typology"; "Failure modes"
- **Note:** maybe

## 20. Generative Agents: Interactive Simulacra of Human Behavior

- **Authors / org:** Joon Sung Park et al.
- **Year / date:** UIST 2023
- **URL:** https://arxiv.org/abs/2304.03442
- **Type:** peer-reviewed paper
- **Evidence tier:** Tier 1
- **Reliability:** primary
- **Categories:** memory and retrieval; multi-agent coordination; historical / classic MAS literature
- **Why it matters:** The paper provides a concrete memory stream, reflection, and planning architecture for simulated agents interacting over time. It is useful for separating episodic memory, reflection, and social simulation from generic RAG.
- **Gap closed:** Supports the page's memory typology and warns that multi-agent social behavior depends on architecture, not magic emergence.
- **Why this source:** Peer-reviewed and system-specific; stronger than popular summaries of "AI villages."
- **Page sections:** "Memory typology"; "Топология x координация"; "Emergence"
- **Note:** use

## 21. MemGPT: Towards LLMs as Operating Systems

- **Authors / org:** Charles Packer et al.
- **Year / date:** 2023-10-12
- **URL:** https://arxiv.org/abs/2310.08560
- **Type:** paper / preprint
- **Evidence tier:** Tier 2
- **Reliability:** primary
- **Categories:** memory and retrieval; agent architecture patterns
- **Why it matters:** MemGPT frames memory as a managed hierarchy with explicit movement between context and external storage. It is valuable for the page's distinction between context window, logs, retrieval, and durable agent memory.
- **Gap closed:** Prevents "memory" from being reduced to a bigger prompt or vector search.
- **Why this source:** It is a primary architecture paper with concrete memory management mechanisms.
- **Page sections:** "Memory typology"; "Decision tree"
- **Note:** use

## 22. AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation

- **Authors / org:** Qingyun Wu et al., Microsoft Research
- **Year / date:** 2023-08-16
- **URL:** https://arxiv.org/abs/2308.08155
- **Type:** paper / preprint; official Microsoft project source
- **Evidence tier:** Tier 2
- **Reliability:** primary
- **Categories:** multi-agent coordination; agent architecture patterns; production agent systems
- **Why it matters:** AutoGen is a major early framework source for conversation-based multi-agent orchestration. It helps map group chat, coordinator, assistant, user proxy, and tool-executing roles onto the taxonomy's topology and coordination axes.
- **Gap closed:** Adds a framework-level multi-agent reference beyond Anthropic's supervisor-worker case.
- **Why this source:** It is the primary Microsoft paper for the framework.
- **Page sections:** "Топология x координация"; "Roles"; "Real systems"
- **Note:** maybe

## 23. Magentic-One: A Generalist Multi-Agent System

- **Authors / org:** Microsoft Research / AutoGen team
- **Year / date:** 2024-11-06
- **URL:** https://arxiv.org/abs/2411.04468
- **Type:** paper / preprint; production-style research system
- **Evidence tier:** Tier 2
- **Reliability:** primary
- **Categories:** multi-agent coordination; production agent systems; evaluation and observability
- **Why it matters:** Magentic-One gives a concrete multi-agent architecture with an orchestrator and specialized agents for browsing, coding, file handling, and terminal work. It is useful evidence for role specialization and orchestration beyond a single product vendor.
- **Gap closed:** Supports "roles in a coordination graph" with an independent Microsoft system.
- **Why this source:** More technical and architectural than product demos.
- **Page sections:** "Рекурсия через вызовы"; "Топология x координация"; "Реальные системы"
- **Note:** maybe

## 24. AgentBench: Evaluating LLMs as Agents

- **Authors / org:** Xiao Liu et al.
- **Year / date:** ICLR 2024
- **URL:** https://arxiv.org/abs/2308.03688
- **Type:** benchmark paper
- **Evidence tier:** Tier 1
- **Reliability:** primary
- **Categories:** evaluation and observability; tool use; production agent systems
- **Why it matters:** AgentBench evaluates LLMs across interactive environments, which fits agentic capability better than static QA. It supports the page's idea that agent systems need task-success metrics, not only language-model scores.
- **Gap closed:** Adds benchmark evidence for evaluating action loops.
- **Why this source:** Peer-reviewed benchmark paper; stronger than leaderboard blog posts.
- **Page sections:** "Evaluation & Observability"; "Decision tree"
- **Note:** use

## 25. WebArena: A Realistic Web Environment for Building Autonomous Agents

- **Authors / org:** Shuyan Zhou et al.
- **Year / date:** ICLR 2024
- **URL:** https://arxiv.org/abs/2307.13854
- **Type:** benchmark paper
- **Evidence tier:** Tier 1
- **Reliability:** primary
- **Categories:** evaluation and observability; tool use and tool design; production agent systems
- **Why it matters:** WebArena is a key source for web-agent evaluation in realistic sites with actions, state, and success criteria. It helps define what "browser operator" evaluation should include.
- **Gap closed:** Moves web-agent claims away from demos and toward reproducible tasks.
- **Why this source:** Peer-reviewed benchmark with concrete environment design.
- **Page sections:** "Evaluation & Observability"; "Computer use"; "Failure modes"
- **Note:** use

## 26. SWE-bench: Can Language Models Resolve Real-World GitHub Issues?

- **Authors / org:** Carlos E. Jimenez et al.
- **Year / date:** ICLR 2024
- **URL:** https://arxiv.org/abs/2310.06770
- **Type:** benchmark paper
- **Evidence tier:** Tier 1
- **Reliability:** primary
- **Categories:** evaluation and observability; production agent systems; tool use
- **Why it matters:** SWE-bench is a foundational benchmark for coding agents because it evaluates real GitHub issue resolution against tests. It supports the taxonomy's coding-agent examples and the need for regression suites.
- **Gap closed:** Provides a stronger evaluation source than product claims about coding autonomy.
- **Why this source:** Peer-reviewed and widely used; task design is more durable than leaderboard numbers.
- **Page sections:** "Реальные системы"; "Evaluation & Observability"; "Decision tree"
- **Note:** use

## 27. GAIA: A Benchmark for General AI Assistants

- **Authors / org:** Grégoire Mialon et al.
- **Year / date:** ICLR 2024
- **URL:** https://arxiv.org/abs/2311.12983
- **Type:** benchmark paper
- **Evidence tier:** Tier 1
- **Reliability:** primary
- **Categories:** evaluation and observability; tool use and retrieval
- **Why it matters:** GAIA focuses on questions that require reasoning, multimodality, web browsing, and tool use. It is useful for differentiating general assistant benchmarks from isolated retrieval or coding benchmarks.
- **Gap closed:** Supports evaluation across mixed skills and multi-step assistant tasks.
- **Why this source:** Peer-reviewed benchmark paper; stronger than generic "agent benchmark" lists.
- **Page sections:** "Evaluation & Observability"; "Deep research"
- **Note:** use

## 28. tau-bench: Tool-Agent-User Interaction Benchmark

- **Authors / org:** Karthik Narasimhan / collaborators
- **Year / date:** 2024-06-17
- **URL:** https://arxiv.org/abs/2406.12045
- **Type:** benchmark paper / preprint
- **Evidence tier:** Tier 2
- **Reliability:** primary
- **Categories:** evaluation and observability; tool use and tool design; production agent systems
- **Why it matters:** tau-bench is valuable because it evaluates agents in tool-use tasks with simulated user interactions, policies, and state. It fits production workflows where the agent must obey business rules rather than simply answer.
- **Gap closed:** Adds a benchmark for tool-user-policy interaction, not only web or coding tasks.
- **Why this source:** More relevant to operational agents than generic task suites.
- **Page sections:** "Evaluation & Observability"; "HITL"; "Failure modes"
- **Note:** use

## 29. OSWorld: Benchmarking Multimodal Agents for Open-Ended Tasks in Real Computer Environments

- **Authors / org:** Tianbao Xie et al.
- **Year / date:** 2024
- **URL:** https://arxiv.org/abs/2404.07972
- **Type:** benchmark paper
- **Evidence tier:** Tier 1
- **Reliability:** primary
- **Categories:** evaluation and observability; tool use; production agent systems
- **Why it matters:** OSWorld evaluates agents in real desktop environments, which is essential for computer-use claims. It helps keep "browser/computer operator" systems separate from normal API tools.
- **Gap closed:** Provides a benchmark reference for GUI-level action, state, and failure.
- **Why this source:** Stronger than vendor demos for computer-use capability claims.
- **Page sections:** "Timeline 2022-2026"; "Evaluation & Observability"; "Failure modes"
- **Note:** use

## 30. AgentDojo: A Dynamic Environment to Evaluate Attacks and Defenses for LLM Agents

- **Authors / org:** Edoardo Debenedetti et al.
- **Year / date:** NeurIPS 2024
- **URL:** https://arxiv.org/abs/2406.13352
- **Type:** benchmark paper
- **Evidence tier:** Tier 1
- **Reliability:** primary
- **Categories:** safety / HITL / security / prompt injection; evaluation and observability; tool use
- **Why it matters:** AgentDojo is a central source for prompt-injection and tool-use attacks in agentic settings. It supports the page's warning that tool outputs and retrieved content must be treated as untrusted.
- **Gap closed:** Adds benchmark evidence for indirect prompt injection and agent security failure modes.
- **Why this source:** Peer-reviewed benchmark; more rigorous than red-team anecdotes.
- **Page sections:** "Failure modes"; "Tools"; "HITL"
- **Note:** use

## 31. Agent-SafetyBench

- **Authors / org:** Zhejiang University / collaborators
- **Year / date:** 2024-12
- **URL:** https://arxiv.org/abs/2412.14470
- **Type:** benchmark paper / preprint
- **Evidence tier:** Tier 2
- **Reliability:** primary
- **Categories:** safety / HITL / security / prompt injection; evaluation and observability
- **Why it matters:** The benchmark is useful as a broader safety-evaluation source for agent systems, especially where agents interact with tools and environments. It should not carry product-safety claims by itself, but it helps expand the failure-mode evidence base.
- **Gap closed:** Adds a safety benchmark beyond prompt-injection-specific work.
- **Why this source:** More structured than safety blog posts, but still should be paired with OWASP or system cards.
- **Page sections:** "Failure modes"; "Evaluation & Observability"
- **Note:** maybe

## 32. OWASP Top 10 for LLM Applications 2025

- **Authors / org:** OWASP GenAI Security Project
- **Year / date:** 2024-11-17 for v2025 release; accessed 2026-06-03
- **URL:** https://genai.owasp.org/llm-top-10/
- **Type:** official security guidance
- **Evidence tier:** Tier 1
- **Reliability:** primary security framework
- **Categories:** safety / HITL / security / prompt injection; tool use; production agent systems
- **Why it matters:** OWASP's LLM Top 10 provides a widely recognized security vocabulary for prompt injection, excessive agency, data leakage, and supply-chain risks. It strengthens the taxonomy's failure-mode section with a security framework rather than only engineering intuition.
- **Gap closed:** Adds formal security categories to agent failures.
- **Why this source:** It is a primary security-community artifact, more durable than vendor checklists.
- **Page sections:** "Failure modes"; "Decision tree"; "Tools"
- **Note:** use

## 33. OWASP Agentic Skills Top 10

- **Authors / org:** OWASP GenAI Security Project
- **Year / date:** updated March 2026; accessed 2026-06-03
- **URL:** https://owasp.org/www-project-agentic-skills-top-10/
- **Type:** official security guidance
- **Evidence tier:** Tier 1
- **Reliability:** primary security framework
- **Categories:** safety / HITL / security / prompt injection; agent protocols; tool use; production agent systems
- **Why it matters:** This OWASP project targets the execution layer of agentic skills across platforms such as Claude Code, Cursor/Codex-style manifests, and VS Code extensions. It is especially relevant to procedural memory, tool authority, skill supply-chain risk, audit logging, and autonomous workflow behavior.
- **Gap closed:** Provides agent-specific security framing for skills/tools that the current page only sketches.
- **Why this source:** Agentic-skill guidance is more relevant than general prompt-injection explainers for coding-agent and tool-execution systems.
- **Page sections:** "Failure modes"; "HITL"; "Decision tree"
- **Note:** use

## 34. Five Eyes: Careful Adoption of Agentic AI Services

- **Authors / org:** Five Eyes cybersecurity agencies, published by New Zealand NCSC
- **Year / date:** 2026-05-01
- **URL:** https://www.ncsc.govt.nz/protect-your-organisation/careful-adoption-of-agentic-ai-services/
- **Type:** public-sector security guidance
- **Evidence tier:** Tier 1
- **Reliability:** primary official guidance
- **Categories:** safety / HITL / security / prompt injection; production agent systems; tool use
- **Why it matters:** This is a fresh 2026 official source on agentic AI adoption risks, governance, permissions, monitoring, and controls. It can update the page's safety guidance without relying only on vendor sources.
- **Gap closed:** Adds independent government guidance for high-risk deployment and procurement decisions.
- **Why this source:** It is current, official, and cross-agency, stronger than informal risk lists.
- **Page sections:** "Failure modes"; "Decision tree"; "Content risks"
- **Note:** use

## 35. Intelligent Agents: Theory and Practice

- **Authors / org:** Michael Wooldridge and Nicholas R. Jennings
- **Year / date:** 1995
- **URL:** https://doi.org/10.1017/S0269888900008122
- **Type:** peer-reviewed paper
- **Evidence tier:** Tier 1
- **Reliability:** primary
- **Categories:** historical / classic MAS literature; agent architecture patterns
- **Why it matters:** This is a classic source for pre-LLM agent definitions, autonomy, social ability, reactivity, and proactiveness. It helps the page distinguish practical LLM-agent vocabulary from the older agent research tradition.
- **Gap closed:** Prevents the taxonomy from implying that "agent" was invented by LLM tooling.
- **Why this source:** Canonical, peer-reviewed, and conceptual without being tied to current vendor products.
- **Page sections:** "Ontology vs taxonomy"; "Historical MAS"; "Autonomy"
- **Note:** use

## 36. Agent-Oriented Programming

- **Authors / org:** Yoav Shoham
- **Year / date:** 1993
- **URL:** https://doi.org/10.1016/0004-3702(93)90034-9
- **Type:** peer-reviewed paper
- **Evidence tier:** Tier 1
- **Reliability:** primary
- **Categories:** historical / classic MAS literature; agent architecture patterns; multi-agent coordination
- **Why it matters:** Shoham's paper is a core source for treating agents as systems with mental-state-like programming abstractions. It is useful as background for why "roles," "commitments," and "intentions" appear in agent taxonomies.
- **Gap closed:** Adds historical depth for agent abstractions without importing all BDI formalism into the page.
- **Why this source:** Primary and foundational; stronger than modern blog histories.
- **Page sections:** "Roles"; "Autonomy"; "Historical MAS"
- **Note:** use

## 37. The Contract Net Protocol

- **Authors / org:** Reid G. Smith
- **Year / date:** 1980
- **URL:** https://doi.org/10.1109/TC.1980.1675516
- **Type:** peer-reviewed paper
- **Evidence tier:** Tier 1
- **Reliability:** primary
- **Categories:** historical / classic MAS literature; multi-agent coordination; agent protocols
- **Why it matters:** Contract Net is a classic coordination protocol for task announcement, bidding, and award. It maps cleanly onto modern orchestrator-worker and delegation patterns, while reminding the page that many "agentic" coordination ideas predate LLMs.
- **Gap closed:** Provides a historical protocol foundation for delegation and market-style task allocation.
- **Why this source:** It is the original source, better than secondary MAS textbook summaries.
- **Page sections:** "Топология x координация"; "Рекурсия через вызовы"; "Historical MAS"
- **Note:** use

## 38. BDI Agents: From Theory to Practice

- **Authors / org:** Anand S. Rao and Michael P. Georgeff
- **Year / date:** 1995
- **URL:** https://cdn.aaai.org/ICMAS/1995/ICMAS95-042.pdf
- **Type:** conference paper
- **Evidence tier:** Tier 1
- **Reliability:** primary
- **Categories:** historical / classic MAS literature; agent architecture patterns; workflow vs agent autonomy
- **Why it matters:** BDI gives a formal lens for beliefs, desires, intentions, commitments, and plan selection. It is useful for distinguishing modern LLM "plans" and tool loops from older symbolic agent architectures.
- **Gap closed:** Adds foundation for autonomy and intentional-state language while avoiding ungrounded anthropomorphism.
- **Why this source:** It is a primary classic BDI reference from the MAS literature.
- **Page sections:** "Autonomy"; "Roles"; "Historical MAS"
- **Note:** use
