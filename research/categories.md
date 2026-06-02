# Sources by Category

Each category lists sources that can support future page edits. Sources marked `maybe` should be used only as supporting context or paired with stronger evidence.

## Agent Architecture Patterns

- **Anthropic: Building Effective Agents** (`use`): strongest primary practitioner source for augmented LLM, prompt chaining, routing, parallelization, orchestrator-workers, evaluator-optimizer, and the workflow-vs-agent boundary.
- **OpenAI: A Practical Guide to Building Agents** (`use`): independent OpenAI guidance for incremental agent construction, guardrails, tool design, and orchestration.
- **ReAct** (`use`): research basis for interleaving reasoning and acting.
- **Reflexion** (`maybe`): useful for cyclic evaluator/self-feedback patterns and memory-like feedback stores.
- **MemGPT** (`use`): architecture source for explicit memory management.
- **Wooldridge & Jennings 1995** (`use`): classic autonomy/reactivity/proactiveness/social ability vocabulary.
- **Shoham 1993** (`use`): classic agent-oriented abstraction source.
- **Rao & Georgeff 1995** (`use`): classic BDI source for plan/commitment language.

## Workflow vs Agent Autonomy

- **Anthropic: Building Effective Agents** (`use`): primary wording for workflow as predefined code paths and agent as model-directed control flow.
- **OpenAI: A Practical Guide to Building Agents** (`use`): second source for escalating from simple systems to agentic loops only when task conditions justify it.
- **OpenAI Agents SDK Documentation** (`use`): current product vocabulary for agents, handoffs, tools, and guardrails.
- **ReAct** (`use`): action loop pattern that sits near the agentic side of the autonomy axis.
- **BDI Agents** (`use`): older formal framing for autonomy and intention; transfer carefully, because LLM agents do not literally have BDI mental states.

## Multi-Agent Coordination

- **Anthropic: How We Built Our Multi-Agent Research System** (`use`): production supervisor-worker case with concrete trade-offs.
- **AutoGen** (`maybe`): framework and paper for conversation-based multi-agent orchestration.
- **Magentic-One** (`maybe`): orchestrator plus specialized agents for multi-domain tasks.
- **Generative Agents** (`use`): social simulation, memory, reflection, planning, and interactions.
- **Contract Net Protocol** (`use`): classic task allocation through announcement/bid/award coordination.
- **A2A Protocol Specification** (`use`): current agent-to-agent interoperability protocol.
- **AGNTCY Documentation** (`maybe`): broader network/discovery/identity view of agent interoperability.

## Tool Use and Tool Design

- **Anthropic: Writing Tools for Agents** (`use`): strongest practical source for agent-facing tool design.
- **ReAct** (`use`): foundational reasoning/action interleaving.
- **OpenAI Computer Use docs** (`use`): current computer-use action loop and specialized tool/environment interface.
- **OpenAI Operator System Card** (`use`): action restrictions, approvals, and safety around browser actions.
- **MCP Specification** (`use`): protocol source for tools, resources, prompts, and context exchange.
- **tau-bench** (`use`): benchmark for tool-agent-user interactions under policies.
- **AgentDojo** (`use`): tool outputs and indirect instructions as adversarial channels.

## Agent Protocols

- **MCP Specification** (`use`): model/application-to-context/tool/data protocol; use exact spec concepts rather than only "USB-C" metaphor.
- **Google A2A Announcement** (`use`): launch rationale for agent-to-agent interoperability.
- **A2A Protocol Specification** (`use`): primary source for agent cards, tasks, messages, artifacts, streaming, security, and transport.
- **Linux Foundation A2A v1.0 Release** (`use with caution`): current project/adoption status; do not use alone for comparative adoption claims.
- **LangChain Agent Protocol** (`maybe`): runtime API for running agents; useful to show that protocol scope is not only MCP/A2A.
- **AGNTCY Documentation** (`maybe`): broader identity/discovery/interoperability ecosystem.
- **Contract Net Protocol** (`use`): historical protocol precedent for delegation and coordination.

## Memory and Retrieval

- **MemGPT** (`use`): memory hierarchy and explicit movement between context and long-term storage.
- **Generative Agents** (`use`): memory stream, reflection, retrieval scoring, planning.
- **Reflexion** (`maybe`): verbal feedback memory for retry loops.
- **MCP Specification** (`use`): resources and context access, but do not conflate MCP resources with durable agent memory.
- **BrowseComp** (`maybe`): search and browsing evaluation for research agents.
- **GAIA** (`use`): multi-skill assistant benchmark that often requires retrieval/tool use.

## Evaluation and Observability

- **OpenAI Agents SDK Tracing Documentation** (`use`): SDK-level trace primitives.
- **OpenTelemetry GenAI Semantic Conventions** (`use`): standards-backed telemetry vocabulary.
- **AgentBench** (`use`): interactive agent benchmark.
- **WebArena** (`use`): realistic web-agent environment.
- **SWE-bench** (`use`): real software issue resolution benchmark.
- **GAIA** (`use`): general AI assistant benchmark.
- **tau-bench** (`use`): tool-agent-user interaction benchmark.
- **OSWorld** (`use`): desktop/computer-use agent benchmark.
- **PaperBench** (`use`): long-horizon research replication/implementation benchmark.
- **BrowseComp** (`maybe`): hard web-browsing benchmark; good for deep research, but avoid leaderboard-specific claims.

## Safety / HITL / Security / Prompt Injection

- **OWASP Top 10 for LLM Applications 2025** (`use`): broad LLM app risk vocabulary.
- **OWASP Agentic Skills Top 10** (`use`): agent-specific execution-layer risks around skills, tool authority, manifests, audit logging, and autonomous workflow behavior.
- **Five Eyes: Careful Adoption of Agentic AI Services** (`use`): fresh 2026 public-sector guidance on permissions, monitoring, procurement, and controls.
- **AgentDojo** (`use`): benchmark evidence for indirect prompt injection and tool misuse.
- **OpenAI Operator System Card** (`use`): primary source for action confirmations and browser-agent safety controls.
- **OpenAI Computer Use docs** (`use`): computer-use action surface and tool interface.
- **Anthropic: Writing Tools for Agents** (`use`): tool design as risk control.

## Production Agent Systems

- **Anthropic multi-agent research system** (`use`): production research-agent architecture and cost/quality trade-offs.
- **OpenAI Agents SDK Documentation** (`use`): current OpenAI agent platform vocabulary.
- **OpenAI Computer Use docs / Operator System Card** (`use`): computer-use product and safety framing.
- **Magentic-One** (`maybe`): research system that resembles production orchestration.
- **AutoGen** (`maybe`): framework-level architecture reference.
- **A2A / MCP / AGNTCY / Agent Protocol** (`use/maybe by scope`): production interoperability surfaces; track current versions before page edits.

## Historical / Classic MAS Literature

- **Wooldridge & Jennings 1995** (`use`): classic definition and properties of agents.
- **Shoham 1993** (`use`): agent-oriented programming and mental-state abstractions.
- **Contract Net Protocol 1980** (`use`): task allocation and delegation protocol.
- **BDI Agents 1995** (`use`): belief-desire-intention plan/commitment framing.
- **Generative Agents 2023** (`use`): LLM-era bridge back to simulation and social behavior; useful but not a substitute for older MAS theory.

## Category Gaps

- Comparative protocol adoption remains weakly evidenced. Official A2A and MCP sources describe project status and scope, but do not give apples-to-apples adoption metrics.
- Memory terminology is not standardized across LLM agent literature. The current page's four-part typology is practical, not a universal ontology.
- There is no peer-reviewed consensus that Anthropic's five workflow patterns are "canonical"; they are influential practitioner patterns and should be described that way.
