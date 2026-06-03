# 10 - Real Systems As Dated Map Points

## Objective

Rebuild real-system placements so they are useful examples, not claims about hidden product internals.

## Read first

- `audit/claim-ledger.md` C18-C24
- `audit/evidence-gaps.md` P0 gap 3
- `audit/rewrite-blueprint.md` section 9
- `research/negative-findings.md` section 6
- Existing product source mentions in `index.html` footer

## Work

1. For each system currently listed, separate:
   - documented public surface;
   - taxonomy inference;
   - unknown/internal caveat;
   - review/access date.
2. Systems to cover if still kept:
   - Cursor;
   - Devin;
   - Claude Code;
   - Manus;
   - OpenAI deep research;
   - AutoGPT.
3. Add or update source registry entries for official product docs if they are not in `research/sources.md`.
4. Avoid internal architecture claims unless official docs state them.
5. Keep uncertain placements visibly tentative.
6. If product docs are stale or inaccessible, downgrade the claim or move the example to appendix.

## Acceptance criteria

- Product table no longer presents inference as fact.
- Every product row has dated source evidence or is downgraded/removed.
- "Public behavior, not internal architecture" caveat is structurally visible, not buried.
- `prompts/progress.md` is updated.
