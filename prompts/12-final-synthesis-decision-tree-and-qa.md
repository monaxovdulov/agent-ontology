# 12 - Decision Guide, Final Synthesis And QA

## Objective

Finish the reader-facing rewrite: decision guide, conclusion, source/annotation QA and final page sanity check.

## Read first

- All prior prompt completion notes in `prompts/progress.md`
- `audit/priority-fixes.md`
- `audit/reader-facing-problems.md`
- `audit/claim-ledger.md`
- `audit/rewrite-blueprint.md` sections 11-12
- `audit/annotation-ui-spec.md`

## Work

1. Rewrite the decision tree as final synthesis:
   - prompt baseline;
   - workflow;
   - augmented LLM;
   - single-agent loop;
   - multi-agent only when independent branches/specialists/tools/context windows justify it;
   - memory only with policy/provenance;
   - HITL only with permissions/trusted context/audit.
2. Replace changelog-style conclusion with public taxonomy conclusion:
   - how to use the map;
   - what claims are strong;
   - what remains uncertain;
   - how to update the map.
3. Do a claim-audit pass:
   - no unsupported "canonical", "standard", "de-facto", "all major", "80%", "MCP won", "A2A failed";
   - no main-flow "in the original document" language;
   - contested claims marked contested;
   - product claims dated and caveated;
   - safety claims sourced.
4. Do a UI/readability pass:
   - annotations are hidden by default but accessible;
   - no square-bracket citation clutter;
   - no overlapping text in diagrams/tables;
   - page remains a coherent reader-facing artifact.
5. Verification:
   - run lightweight HTML/static checks available in the repo environment;
   - if Browser plugin is available, open the local page and inspect visually;
   - check `git diff` and summarize.

## Acceptance criteria

- The page is no longer an internal repair report.
- Evidence annotation model is used consistently for high-risk claims.
- The final read supports `evidence -> reasoning -> taxonomy decision`.
- `audit/priority-fixes.md` P0 items are addressed or explicitly left as residual risk.
- `prompts/progress.md` is updated.
