# Evidence Annotation UI Spec

Goal: make claims auditable without turning the page into an academic paper full of bracket citations.

## Design principle

Normal reading should feel like continuous prose. Evidence appears as a small affordance on claims where trust matters: hover on desktop, tap/click on mobile, source drawer for deeper inspection.

## Claim markup model

Use claim-level spans or blocks with stable IDs.

```html
<span
  class="claim"
  data-claim-id="protocol-mcp-a2a-scope"
  data-claim-type="protocol-status"
  data-evidence-strength="contested"
>
  MCP and A2A standardize different surfaces.
  <button class="evidence-marker" aria-label="Evidence for protocol scope"></button>
</span>
```

For table rows, annotate the row or the specific cell:

```html
<tr
  class="claim-row"
  data-claim-id="memory-four-part-typology"
  data-claim-type="definition"
  data-evidence-strength="medium"
>
  ...
</tr>
```

## Source registry

Keep a single source registry near the end of the page or in a separate committed JSON file. The page can embed a small static JSON blob.

```html
<script type="application/json" id="evidence-registry">
{
  "claims": {
    "memory-four-part-typology": {
      "type": "definition",
      "strength": "medium",
      "status": "practical-typology-not-standard",
      "reasoning": "MemGPT, Generative Agents and Reflexion support separate memory mechanisms, but research found no universal agent-memory taxonomy.",
      "sources": ["memgpt-2023", "generative-agents-2023", "reflexion-2023", "negative-memory-taxonomy"],
      "caveat": "Use as this page's engineering split, not as a field-wide ontology."
    }
  },
  "sources": {
    "memgpt-2023": {
      "title": "MemGPT: Towards LLMs as Operating Systems",
      "year": "2023",
      "url": "https://arxiv.org/abs/2310.08560",
      "tier": "Tier 2",
      "accessed": "2026-06-03"
    }
  }
}
</script>
```

## Evidence marker

Preferred visual:

- tiny outlined dot, superscript lozenge, or subtle underline chip;
- no bracket numbers like `[12]`;
- marker appears only for claims that need evidence;
- marker can become more visible on hover/focus.

Suggested states:

- **strong:** solid marker;
- **medium:** outlined marker;
- **weak:** dotted marker;
- **contested:** outlined marker with split fill;
- **missing:** red/amber marker only in author/audit mode, not public mode.

## Hover tooltip

Desktop hover/focus tooltip should include:

- claim type;
- evidence strength;
- one-sentence reasoning;
- 1-3 source labels;
- caveat if any.

Example:

```text
Protocol status · contested
MCP and A2A have different technical scopes, but public comparative adoption data is weak.
Sources: MCP spec; A2A spec; LF A2A 2026; negative finding.
```

Tooltip rules:

- maximum 3 source labels;
- no long excerpts;
- source labels open drawer on click;
- keyboard focus must show same content.

## Click popover

Clicking marker opens a popover beside the claim.

Popover fields:

- claim title;
- current claim text;
- claim type;
- evidence strength;
- reasoning bridge;
- source list with links;
- caveats / contested status;
- last reviewed date;
- "open source drawer" action.

For table rows, popover should anchor to row marker, not cover the row text.

## Source drawer

The drawer is for deeper inspection. It should slide from the side on desktop and from bottom on mobile.

Drawer sections:

- selected claim;
- evidence summary;
- sources with title, org/authors, date, tier, reliability, URL;
- "supports" notes: what the source actually supports;
- "does not support" notes if a source is often overused;
- related negative findings.

This matters because "source exists" is not the same as "source supports this exact claim."

## Mobile fallback

No hover on mobile. The evidence marker is a normal button:

- tap opens bottom sheet;
- bottom sheet has same fields as popover;
- source links open in new tab;
- close button and swipe-down dismissal;
- accessible focus trap.

Tables:

- row-level evidence markers should be placed in the first cell or as a small icon in the row header;
- tapping row marker opens bottom sheet.

## Accessibility

- `button.evidence-marker` must have `aria-label`.
- Popovers should use `role="dialog"` or accessible disclosure pattern.
- Tooltip text must also be reachable through keyboard focus.
- Evidence strength should not be conveyed by color alone.

## Claim type values

Use the same vocabulary as the audit:

- `definition`
- `taxonomy-claim`
- `historical-claim`
- `protocol-status-claim`
- `product-system-claim`
- `architectural-recommendation`
- `causal-claim`
- `safety-claim`
- `evaluation-claim`
- `meta-commentary`

## Evidence strength values

- `strong`
- `medium`
- `weak`
- `contested`
- `missing`

Public page should normally show `strong`, `medium`, `weak`, `contested`. `missing` should be author-only and should not ship as a public claim.

## Annotation placement rules

Use visible markers for:

- protocol adoption/status;
- product placements;
- safety recommendations;
- timeline milestones;
- benchmark/evaluation claims;
- strong terms like "standard", "canonical", "de-facto";
- taxonomy decisions that depend on multiple sources.

Use hidden annotations without visible marker for:

- simple glossary definitions;
- implementation notes;
- design rationale that is not contested.

Move to appendix rather than annotate when:

- the claim is about the old document;
- the claim is process history;
- the source only supports why the page was changed, not why the taxonomy is true.

## Authoring workflow

Every public claim with marker should have:

1. stable claim ID;
2. claim type;
3. evidence strength;
4. one-sentence reasoning;
5. at least one source;
6. caveat or limitation if evidence is not strong;
7. reviewed date for living docs/product/protocol claims.
