# 06 - Protocol Stack, MCP And A2A

## Objective

Fix the protocol layer and MCP/A2A adoption/status claims. This is a P0 content-risk task.

## Read first

- `audit/claim-ledger.md` C11, C32-C35, C53
- `audit/evidence-gaps.md` P0 gap 1
- `audit/priority-fixes.md` P0 item 2
- `research/sources.md` entries for MCP spec, A2A Google announcement, A2A spec, Linux Foundation A2A 2026 release, LangChain Agent Protocol, AGNTCY, OpenTelemetry GenAI
- `research/content-risks.md` sections 2, 3 and 11
- `research/negative-findings.md` sections 1 and 5

## Work

1. Rewrite the protocol row/table so protocols are grouped by standardization target:
   - tool/context access: MCP;
   - agent-to-agent tasks/messages/artifacts: A2A;
   - runtime/client-server execution APIs: LangChain Agent Protocol;
   - identity/discovery/interoperability ecosystem: AGNTCY;
   - observability semantics: OpenTelemetry GenAI, if included.
2. Remove or heavily qualify:
   - "MCP de-facto standard";
   - "MCP stronger developer adoption";
   - "A2A enterprise-niche";
   - any "MCP won / A2A failed" implication.
3. Add date-stamped wording for A2A:
   - Google launched A2A in April 2025;
   - the A2A project/spec is active;
   - Linux Foundation v1.0.0 / 2026 status should be included if supported by research.
4. Replace adoption comparison with:
   - different scopes;
   - public comparative adoption evidence is mixed/weak;
   - MCP is prominent in developer tool/context integrations;
   - A2A is active and enterprise/interoperability-oriented.
5. Update fig.5 caption/text so the diagram does not hard-code contested adoption claims.

## Acceptance criteria

- All MCP/A2A claims are scope-specific and date-stamped.
- Contested adoption comparison is explicitly marked contested or removed.
- The protocol layer no longer collapses all protocols into one maturity ladder.
- `prompts/progress.md` is updated.
