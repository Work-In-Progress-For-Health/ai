# AGENTS/sources.md

How to verify and cite factual claims in this repository.

## spec/ is authoritative

`spec/index.md` and `spec/padr.md` are the single source of truth for the OCP and PADR facts used in README.md. If you find README.md asserting something not backed by an entry in `spec/`, either:

- Verify it against a primary source and add it to `spec/` first, then reflect it in README.md; or
- If it can't be verified, soften the claim in README.md (e.g. "typically," "often," "confirm with your POD/HR contact") rather than stating it as settled fact.

## Primary sources used so far

- NHS Wales Organisational Change Policy, December 2025 edition — fetched and read directly (as a PDF) from `https://heiw.nhs.wales/files/key-documents/policies/human-resources-policies/all-wales-organisational-change-policy-docx/`. This is the strongest source in the project: directly quoted, not summarized from search results.
- PADR process facts — based on general, published descriptions from NHS Wales health boards' own PADR and pay-progression-toolkit pages, not one single canonical document. Weaker sourcing than the OCP; phrased with appropriate hedging in `spec/padr.md`.
- DHCW's Welsh Government oversight and escalation status — `gov.wales` blocks direct automated fetches (HTTP 403 on every URL tried, including PDF assets under `gov.wales/sites/default/files/...`). This fact set is built from WebSearch result summaries, not a directly quoted primary source, and is flagged as such in `spec/index.md`. Prefer re-attempting a direct fetch (a future fetch tool or an authenticated route might succeed where WebFetch didn't) before treating this section as fully settled, and keep the "read the current page yourself" hedge in README.md's corresponding checklist.

## When a source blocks automated fetching

Some UK government domains (confirmed so far: `gov.wales`) return HTTP 403 to this project's fetch tooling. When this happens:

1. Fall back to a web search tool and synthesize from indexed result snippets.
2. State explicitly, in `spec/`, that the claim is search-synthesized rather than a direct quotation, and name the domain that blocked the fetch.
3. Carry that hedge through to README.md — don't launder a search-synthesized claim into README.md as if it were a direct quotation. A checklist item telling the reader to read the primary source themselves is a reasonable way to close the gap (see the "Understanding DHCW's oversight status" checklist in README.md section 1 for the pattern).

## Currency of factual claims

Some facts in this project are time-sensitive by nature — DHCW's escalation level, pay bands, specific dates. Where a claim is likely to go stale, say so in `spec/` and prefer relative/hedged language in README.md ("as of [approximate period]," "confirm the current position") over a bare assertion that will silently become wrong later.

## Numbers that must stay exact

A small number of figures are load-bearing and must never be paraphrased loosely:

- The two-thirds (66.6%) match threshold for a post being "substantially unchanged" (OCP §9.2, §9.4–9.5) — not "70-75%," not "roughly two-thirds." The OCP states two-thirds; earlier drafts of this project used an approximated figure from a non-primary source and it was corrected once the primary PDF was read directly.
- The pay protection tables (short-term and long-term, both banded by reckonable service) — reproduce the exact bands from `spec/index.md`, don't round or simplify them.
- The 3-month Redeployment Candidate window and its extension rules under secondment/fixed-term posts.
