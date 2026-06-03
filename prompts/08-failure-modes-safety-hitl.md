# 08 - Failure Modes, Safety And HITL

## Objective

Ground failure modes and HITL guidance in safety/security sources. Fix any implication that HITL alone is a sufficient safety control.

## Read first

- `audit/claim-ledger.md` C36-C38, C46
- `audit/evidence-gaps.md` P0 gap 4
- `audit/rewrite-blueprint.md` section 7
- `research/sources.md` entries for AgentDojo, OWASP LLM Top 10, OWASP Agentic Skills Top 10, Five Eyes 2026, OpenAI Operator System Card, Anthropic Writing Tools for Agents
- `research/content-risks.md` safety, HITL and context poisoning sections
- `research/negative-findings.md` sections 7 and 10

## Work

1. Rewrite the failure modes intro:
   - failure modes derive from autonomy, topology, coordination, tools, memory, permissions and protocol boundaries, not only A2/A3/A4.
2. Keep the table if useful, but attach evidence/caveats:
   - cascading errors;
   - context poisoning;
   - hallucination amplification;
   - infinite loops;
   - agreement bias if framed as page-defined heuristic.
3. Add a stronger safety boundary model:
   - untrusted retrieved content/tool output/peer output must not gain instruction authority;
   - permissions and scoped capabilities;
   - sandboxing;
   - audit trails;
   - trusted UI/context for approvals;
   - monitoring and policy checks.
4. Rewrite HITL:
   - use for irreversible/high-risk actions;
   - not sufficient alone;
   - must pair with context, policy, permissions and audit.
5. Add local annotations for safety claims.

## Acceptance criteria

- HITL is never presented as a standalone safety solution.
- Prompt injection/context poisoning is framed as an authority-boundary problem.
- Safety claims have local evidence from OWASP/AgentDojo/Five Eyes/OpenAI system card.
- `prompts/progress.md` is updated.
