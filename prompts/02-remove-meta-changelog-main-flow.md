# 02 - Remove Meta/Changelog Main Flow

## Objective

Make the page stop reading like an internal repair log. Move old-document diagnostics and task-history language out of the main reader-facing narrative.

## Read first

- `audit/reader-facing-problems.md`
- `audit/priority-fixes.md`
- `audit/claim-ledger.md` rows C02, C25, C47, C54, C55
- `prompts/01-source-registry-and-annotation-scaffold.md` output, if present

## Work

1. Edit `index.html`.
2. Move or rewrite the main-flow content that says:
   - "в исходнике";
   - "пропущен/пропущена";
   - "добавлена/добавлены";
   - "теперь";
   - "что осталось от исходника";
   - "research backfill" as task history.
3. Preserve useful substance:
   - category mistakes;
   - topology vs coordination;
   - workflow vs agent;
   - augmented LLM caveat;
   - protocol layer caveat;
   - classic MAS transfer.
4. Put internal history into an appendix/collapsed notes section or remove it from the public flow.
5. Do not solve every content claim in this task; focus on reader-facing narrative hygiene.

## Acceptance criteria

- The page no longer opens with `Категориальный дребезг` as an old-document critique.
- The final section no longer ends as a changelog.
- Main text speaks to the reader, not to a previous task list.
- Old diagnostic material is either moved to appendix/hidden notes or converted into standalone taxonomy reasoning.
- `prompts/progress.md` is updated.
