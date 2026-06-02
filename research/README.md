# Research Backlog

This folder is a research backlog for the AI agents taxonomy page. It is intentionally separate from `index.html`: the goal is to collect evidence, risks, and future edit candidates without changing the published design or page copy in this pass.

## Scope

The refresh covers AI agents, multi-agent systems, agent protocols, tool use, memory, workflow-vs-agent autonomy, evaluation, observability, safety, and production agent systems.

The target is quality over volume: about 25-40 sources that add distinct evidence. A source is included only if it strengthens a concrete part of the taxonomy, closes a known ambiguity, or provides a primary reference for a protocol, benchmark, product pattern, or safety claim.

## Evidence Tiers

- **Tier 1**: peer-reviewed papers, official technical reports, official documentation, official specifications, protocol repositories, standards, or public-sector guidance.
- **Tier 2**: arXiv/preprints from credible research groups, production case studies from labs/companies, and official engineering blogs with implementation detail.
- **Tier 3**: secondary surveys or explainers used only for navigation, not as the basis for claims.
- **Reject**: SEO roundups, marketing pages without technical claims, Medium-style retellings, pages without verifiable links, and secondary summaries where a stronger primary source exists.

## Inclusion Rules

For every source, record:

- title;
- authors or organization;
- year and exact date when available;
- URL;
- source type;
- evidence tier;
- primary or secondary reliability;
- topic categories;
- why it matters for the taxonomy;
- which gap, mistake, or ambiguity it closes;
- why this source is better than alternatives;
- current page sections it could strengthen;
- `use`, `maybe`, or `skip` recommendation.

Do not include a source only because it is famous or recent. When two sources make the same point, prefer the more primary, technical, dated, or durable source.

## Freshness Rules

- For 2025-2026 protocols and product docs, treat the source as time-sensitive and record the access date or release date.
- For benchmark papers, cite benchmark design and task coverage, not transient leaderboard scores.
- For production products, cite official docs only for feature existence and system shape; do not infer adoption or effectiveness unless the source gives evidence.
- For disputed claims, either require two independent sources or mark the evidence as weak, mixed, or contested.

## Files

- `sources.md`: selected catalog with evidence notes.
- `categories.md`: category-based index.
- `candidates-for-page.md`: future page additions, wording corrections, replacement sources, and items needing more evidence.
- `content-risks.md`: current claims that need caution or stronger evidence.
- `rejected.md`: sources not used and why.
- `negative-findings.md`: searches that did not produce strong confirmation.
- `bibliography.json`: machine-readable source catalog.

## Current Page Constraints

This refresh must not edit `index.html`, `assets/styles.css`, or `agent-ontology.html`. Future page edits should be a separate commit after reviewing this backlog.
