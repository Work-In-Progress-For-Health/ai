# AGENTS/structure.md

How README.md is structured, and the mechanical conventions to preserve when editing it.

## One file, numbered sections

README.md contains the entire guide as 24 numbered `##` sections (at time of writing — the count grows as content is added). This is deliberate and explicit: the guide was originally split into a `guide/` directory of four part-files, and the user reversed that decision, requiring everything readable in the single README.md file. Do not re-split it.

Top-level structure, in order:

1. An unnumbered `# Organisational Change Survival Guide` title and subtitle.
2. An unnumbered `## A growth story` intro (a few paragraphs, no heading number).
3. An unnumbered `## Contents` section: a numbered Markdown list, one line per `##`-level section, each linking to that section's anchor.
4. The 24 numbered `## N. Title` sections themselves, each separated by a `---` horizontal rule.

## Anchors and cross-references

GitHub-flavoured Markdown auto-generates a heading's anchor slug by lowercasing the text, replacing spaces with hyphens, and stripping punctuation (colons, slashes, etc. are dropped; a slash between words like "CPD / personal development plan" becomes a double-hyphen `--` because two words are removed leaving two adjacent hyphens). The Contents list and every in-body `[section N](#n-slug)` link must match this exactly.

When you rename a heading:

1. Compute its new slug.
2. Update the heading itself.
3. Update its entry in the Contents list.
4. `grep -n "#n-old-slug"` across README.md and fix every match — cross-references between sections are frequent and easy to miss.

When you insert a new numbered section:

- Decide whether it's worth renumbering every subsequent section (relabelling `## 12.` through `## 24.` and every cross-reference to them), or whether the content fits better as an unnumbered subsection (`###`) within an existing numbered section. The user has done both at different points; when in doubt, prefer adding as a subsection of an existing section over a full renumber, since renumbering 24 sections' worth of cross-references is expensive and error-prone. Only do a full renumber when the user's request clearly implies a new first-class section in a specific position.

## Checklists

Nearly every numbered section, and many subsections, end with one or more `### Checklist: <name>` blocks. Conventions:

- Heading format: `### Checklist: reflecting on the last 4 years` — sentence case, no emoji, no colon-then-capital.
- Items are `- [ ] ` (unchecked), first-person: "I know...", "I've asked...", "I will...".
- A section can have more than one checklist if it covers more than one sub-topic (e.g. section 20 has both a general reasonable-adjustments checklist and a six-part "building your reasonable adjustments record" checklist broken into "1. What you're requesting" through "6. Team aspects").
- Several sections also carry a "Checklist: check your understanding (part N)" block — a comprehension check distinct from the action-oriented checklists — and section 22 carries a "Checklist: know who to contact" block naming specific contact roles (POD/HR contact, union rep, HR Case Manager, Occupational Health, EAP). Follow this pattern (understanding checks + contact-identification checks) when asked to add "more checklists."

## The glossary-table pattern

Section 7 ("Ways of working you'll meet along the way") uses a three-column table: `| Term | What it means | Why it matters for you |`. This is the model for introducing any new block of jargon — reuse it rather than inventing a new format.

## spec/ traceability

Every factual claim in README.md that comes from an external source (the OCP, the PADR process, DHCW's Welsh Government oversight status) should be traceable to an entry in `spec/*.md`. When adding a new factual section to README.md, add the underlying facts to the relevant `spec/*.md` file in the same change (see [AGENTS/sources.md](sources.md)).
