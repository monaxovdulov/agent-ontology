# 09 - Evaluation, Observability And Benchmarks

## Objective

Ground eval and observability in tracing docs/specs and benchmark design, while avoiding overclaims that public benchmarks alone choose production architecture.

## Read first

- `audit/claim-ledger.md` C39-C40
- `audit/evidence-gaps.md` P0 gap 5
- `audit/rewrite-blueprint.md` section 8
- `research/sources.md` entries for OpenAI tracing docs, OpenTelemetry GenAI conventions, AgentBench, WebArena, SWE-bench, GAIA, tau-bench, OSWorld, PaperBench, BrowseComp, OpenAI Practical Guide, Anthropic Building Effective Agents
- `research/content-risks.md` evaluation section
- `research/negative-findings.md` section 8

## Work

1. Rewrite "evaluation выбирает архитектуру" to a safer claim:
   - local evals and traces justify architecture changes;
   - public benchmarks provide task/eval dimensions, not durable production answers.
2. Keep the baseline -> inspect traces -> change architecture -> rerun regression loop.
3. Add source-backed trace event vocabulary:
   - model calls;
   - tool calls;
   - retrieval;
   - state changes;
   - handoffs;
   - spans/events where OpenTelemetry/OpenAI docs apply.
4. Add benchmark dimension map:
   - AgentBench: interactive environments;
   - WebArena: realistic web tasks;
   - SWE-bench: coding issue resolution;
   - GAIA: mixed tool/reasoning assistant tasks;
   - tau-bench: tool-user-policy interactions;
   - OSWorld: desktop/computer-use;
   - PaperBench/BrowseComp: long-horizon research/browsing.
5. Do not cite leaderboard scores unless explicitly dated and necessary.

## Acceptance criteria

- Eval section distinguishes benchmark design from local production evals.
- Trace vocabulary is tied to OpenAI/OTel sources.
- Architecture escalation remains metric-driven but not overclaimed.
- `prompts/progress.md` is updated.
