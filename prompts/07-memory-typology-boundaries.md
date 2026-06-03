# 07 - Memory Typology And Boundaries

## Objective

Rewrite memory as a practical, caveated typology with source-backed boundaries.

## Read first

- `audit/claim-ledger.md` C42-C44
- `audit/evidence-gaps.md` P1 gap 8
- `audit/rewrite-blueprint.md` section 5
- `research/sources.md` entries for MemGPT, Generative Agents, Reflexion, MCP specification, Anthropic Writing Tools for Agents
- `research/content-risks.md` memory section
- `research/negative-findings.md` section 3

## Work

1. Keep the four-part split only as "this page's practical typology":
   - working memory;
   - episodic memory;
   - semantic memory;
   - procedural memory.
2. Add the caveat that no universal agent-memory taxonomy was found.
3. Preserve the important boundaries:
   - context window is a runtime buffer, not durable memory;
   - retrieval is a selection mechanism, not a memory policy;
   - logs become memory only after curation/summarization/provenance.
4. Tie memory to safety:
   - write policy;
   - TTL;
   - provenance;
   - freshness;
   - delete/forget rules;
   - authority boundaries for retrieved/tool text.
5. Add hidden/visible annotations near the main memory definition and boundary table.

## Acceptance criteria

- Memory section no longer reads as a universal ontology.
- Each memory type has a practical architecture mapping and caveat.
- RAG/retrieval/context/logs are clearly separated from memory.
- `prompts/progress.md` is updated.
