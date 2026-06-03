# 01 - Source Registry And Annotation Scaffold

## Objective

Create the evidence foundation that later rewrite tasks will use for local hidden annotations. Do not rewrite the whole page in this task.

## Read first

- `audit/annotation-ui-spec.md`
- `audit/claim-ledger.md`
- `audit/evidence-gaps.md`
- `research/README.md`
- `research/sources.md`
- `research/content-risks.md`
- `research/negative-findings.md`

## Work

1. Create a source/claim registry for page evidence. Prefer `research/page-evidence-registry.json` if it is practical; otherwise use `research/page-evidence-registry.md`.
2. Include stable source IDs for the research sources most needed by P0/P1 claims:
   - Anthropic Building Effective Agents
   - Anthropic Writing Tools for Agents
   - Anthropic multi-agent research system
   - OpenAI Practical Guide to Building Agents
   - OpenAI Agents SDK docs and tracing docs
   - OpenAI Computer Use docs and Operator System Card
   - MCP specification
   - A2A specification
   - Linux Foundation A2A 2026 update
   - OpenTelemetry GenAI conventions
   - AgentBench, WebArena, SWE-bench, GAIA, tau-bench, OSWorld, PaperBench, BrowseComp
   - AgentDojo, OWASP LLM Top 10, OWASP Agentic Skills, Five Eyes 2026
   - MemGPT, Generative Agents, Reflexion
   - Wooldridge & Jennings, Shoham, Contract Net, BDI
3. Define 20-30 priority claim IDs from `audit/claim-ledger.md`, especially C09-C16, C18-C24, C32-C46 and C52-C55.
4. For each priority claim ID, include:
   - claim type;
   - evidence strength;
   - one-sentence reasoning bridge;
   - source IDs;
   - caveat;
   - reviewed date when source is time-sensitive.
5. If editing `index.html`, only add minimal non-invasive annotation scaffolding. Do not visually redesign the page.

## Acceptance criteria

- There is a durable registry future prompts can reference.
- Registry distinguishes "source exists" from "source supports this claim".
- Contested claims are marked contested, not silently upgraded.
- `prompts/progress.md` is updated after completion.
