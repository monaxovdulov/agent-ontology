# Reader-Facing Problems

## 1. The page opens as a repair report

The first major section is `§ 01 — диагностика / Категориальный дребезг`, and the first sentence says there are "девять мест" where previous content mixed categories. This makes the reader ask: "What previous document? Why am I reading the debugging notes?" The page should begin with the taxonomy problem and evidence-backed frame, not with defects of an older artifact.

Affected areas:

- `§01` entire diagnostic list.
- `§05` "В исходнике пять уровней..."
- `§07` "В исходнике они были перемешаны."
- `§14` "Что добавляет research backfill."
- `§15` "Что осталось от исходника."

Fix direction: move old-document commentary into appendix, hidden notes, or audit trail. Main text should speak directly to the reader.

## 2. Claims often skip the reasoning bridge

The page repeatedly jumps from a source-flavored observation to a taxonomy decision:

- Anthropic distinguishes workflows and agents -> therefore A2 is the central autonomy axis.
- MCP/A2A exist -> therefore protocol layer is a separate A6 slice.
- Memory is not just RAG -> therefore four memory types form the map.
- Multi-agent systems can cost much more -> therefore minimal sufficient architecture is the rule.

These conclusions are mostly plausible, but the current page rarely shows the bridge:

`source evidence -> why it matters -> what taxonomy decision follows -> limitation`

Without that bridge, readers see confident synthesis but cannot audit it.

## 3. Footer-only sourcing weakens trust

The page has a bibliography-like footer, but claims appear hundreds of lines earlier without local citation. This is especially damaging for:

- product placements;
- protocol status claims;
- 2026 timeline claims;
- safety/failure-mode claims;
- benchmark/evaluation claims;
- "standard", "canonical", "de-facto", and adoption language.

The result is not a scholarly page; it is worse: it looks sourced in aggregate but unsourced at the claim level.

## 4. The text sounds like a task history

Phrases like "пропущен", "добавлена", "теперь", "оставшаяся слабость", "что добавляет research backfill" and "что осталось от исходника" expose the implementation history. That makes the page feel generated from task tickets rather than authored as a final artifact.

This is not only tone. It breaks taxonomy clarity because the reader must separate:

- what is a claim about AI agents;
- what is a claim about the old page;
- what is a claim about the rewrite process.

## 5. Strong labels outrun the evidence

The page uses labels that imply consensus or settled market status:

- "канонический примитив"
- "атом всех современных агентных систем"
- "центральная ось консенсуса"
- "де-факто стандарт"
- "MCP сильнее у разработчиков"
- "A2A enterprise-нишевый"
- "80% production-систем"
- "иерархическая команда повсеместно"
- "сильная эмерджентность редко доказуема"

Some are directionally reasonable, but research explicitly warns that public evidence is weaker or contested. The reader-facing version should prefer:

- "useful practitioner primitive";
- "prominent in developer tooling";
- "active enterprise/interoperability-oriented project";
- "public comparative adoption evidence is mixed";
- "in Anthropic's reported research system";
- "for engineering decisions, prefer traceable mechanisms over emergence language."

## 6. Product placements are inference-heavy

`§04` is useful, but the table mixes documented public behavior with inferred architecture. The caveat "based on public behavior, not internal architecture" is good, yet every row still needs local dated evidence and a visible uncertainty state.

Reader risk: a product user may treat coordinates as facts about internals rather than a public-surface interpretation.

Fix direction: label each placement as:

- **documented surface:** official docs say this exists;
- **taxonomy inference:** the page maps it to A2/A3/A4;
- **unknown:** internal orchestration may differ.

## 7. Tables compress too many claim types

Several tables combine definitions, examples, recommendations and status claims in one row. Example: the tech stack row for protocols defines protocols, claims MCP is de-facto standard, claims A2A is enterprise-niche, and lists LangChain Agent Protocol/AGNTCY as peers. That is too much for one row.

Fix direction: separate tables by claim type:

- definitions;
- examples;
- evidence status;
- taxonomy decision;
- caveat.

## 8. Timeline mixes durable shifts and product snapshots without enough anchors

The timeline tries to separate conceptual shifts from hype, which is good. But each year still needs a local citation and a reason why that event changes architecture. The 2026 wording is also stale relative to the current audit date: it says "snapshot on April" while research includes May/June 2026 material.

Fix direction: timeline should be "dated evidence points", not "year = label".

## 9. Safety and HITL are under-specified

The page recommends trust boundaries and HITL gates, but it does not yet show the stronger safety model from research:

- human approval is not sufficient by itself;
- prompts/tool outputs/retrieved content are authority-boundary problems;
- permissions, audit trails, trusted UI, policy checks, sandboxing and monitoring matter.

Reader risk: a builder may add an approval dialog and think the safety problem is solved.

## 10. The final section closes with changelog, not synthesis

The page should end by giving readers a stable mental model: how to use the taxonomy, what claims are strong, what is deliberately uncertain, and how to update the map. Current `§15` ends with a list of what was fixed from the old source, so the final impression is "this page was improved" rather than "this taxonomy is justified."
