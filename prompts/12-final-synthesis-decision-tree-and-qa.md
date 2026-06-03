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
   - how to update the map as new research appears.
3. Do a claim-audit pass:
   - no unsupported "canonical", "standard", "de-facto", "all major", "80%", "MCP won", "A2A failed";
   - no main-flow "in the original document" language;
   - contested claims marked contested;
   - product claims dated and caveated;
   - safety claims sourced;
   - living claims have review/access dates and do not present time-sensitive research, specs, product behavior, benchmarks, or safety guidance as permanent facts.
4. Add or verify a compact update policy:
   - new papers/specs/docs go into `research/` before page copy changes;
   - each new source records what claim it supports, limits, contests, or contextualizes;
   - update `page-evidence-registry.json` / claim annotations before strengthening public wording;
   - if evidence changes, note whether the claim strength moved between strong/medium/weak/contested;
   - keep a visible or near-visible "last reviewed" date for the page and for time-sensitive claims.
5. Do a UI/readability pass:
   - annotations are hidden by default but accessible;
   - no square-bracket citation clutter;
   - no overlapping text in diagrams/tables;
   - page remains a coherent reader-facing artifact.
6. Verification:
   - run lightweight HTML/static checks available in the repo environment;
   - if Browser plugin is available, open the local page and inspect visually;
   - check `git diff` and summarize.

## Acceptance criteria

- The page is no longer an internal repair report.
- Evidence annotation model is used consistently for high-risk claims.
- The final read supports `evidence -> reasoning -> taxonomy decision`.
- The page explains how future research/spec/product changes should be incorporated without turning the taxonomy into stale or overconfident claims.
- `audit/priority-fixes.md` P0 items are addressed or explicitly left as residual risk.
- `prompts/progress.md` is updated.
