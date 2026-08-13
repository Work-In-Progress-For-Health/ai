# CLAUDE.md

Instructions for Claude Code working in this repository. Read this before editing anything. See also [AGENTS.md](AGENTS.md) for guidance that applies to any AI coding agent, not just Claude Code.

## What this repository is

A single, comprehensive guide for NHS Wales / Digital Health and Care Wales (DHCW) manual software testers whose teams are moving towards test automation. It is a documentation project, not a software project — there is no code to build, test, or run.

## File layout and the two hard rules

- `README.md` — the entire guide. Every section (1 through 24 at time of writing), every checklist. This file is explicitly exempt from the repo's normal 40KB-per-file guideline (see below) because the user has twice explicitly instructed: the whole guide must be readable in this one file, and it must not be split into multiple files again. Do not re-split it into a `guide/` directory or similar, even to satisfy the size guideline, unless a future instruction explicitly reverses this.
- `index.md` — a short pointer to `README.md` and `spec/`. Keep it under a few KB. It exists so a reader or agent has a one-line entry point, not as a second copy of the guide.
- `spec/*.md` — the single source of truth for factual claims used in `README.md`. Currently `spec/index.md` (NHS Wales Organisational Change Policy facts) and `spec/padr.md` (PADR process facts).
- `AGENTS.md`, `AGENTS/*.md` — agent-facing conventions, in the general `agents.md` format so they're useful to any AI tool, not just Claude Code.

The two hard rules for this repo:

1. `spec/` is authoritative. If a fact in `README.md` and a fact in `spec/` disagree, `spec/` is right. Fix `README.md` to match, or update `spec/` first if the fact itself has changed, then bring `README.md` into agreement.
2. `README.md` is not split. Every other file listed above should stay under 40,000 bytes; `README.md` is the sole, deliberate exception.

## Workflow for a content change

1. If the change is a fact about the OCP, PADR, or DHCW's oversight status, update the relevant `spec/*.md` file first.
2. Update `README.md` to match. Use `grep -n` to find every place a changed fact, term, or cross-reference appears — this guide repeats key facts (POD/HR contact, the two-thirds test, PADR) across many sections, and a partial edit leaves it self-contradictory.
3. If a section's heading text changes, its anchor slug changes too (GitHub-flavoured Markdown: lowercase, spaces to hyphens, punctuation stripped). Find and update every internal `[text](#n-old-slug)` link that pointed at it, including the numbered Contents list near the top.
4. Re-check file size (`wc -c README.md`) is expected to be large; check every other file is still under 40KB.

## Style rules (accumulated from direct user instruction — treat as binding, not optional)

- No bold Markdown (`**text**`) anywhere. Plain text, headings, and italics (`*text*`, used sparingly, e.g. book titles) only.
- No emoji anywhere, including in headings and checklist markers. Checklist headings read "Checklist: ..." not "✅ Checklist: ...".
- Say "automatic testing," not "automated testing," when referring to the practice/discipline generally (e.g. "the shift from manual to automatic testing"). "Automated test(s)" / "automated test suite" as a noun phrase for the artifacts themselves is fine and unchanged.
- Whenever Playwright and Selenium are mentioned together as a pair, list WebDriver alongside them too (e.g. "Playwright, Selenium, or WebDriver").
- The support contacts are always POD/HR and the trade union rep. Do not introduce "your manager" as a contact or escalation route — this project deliberately routes everything through POD/HR and the union rep, reflecting DHCW's actual structure. ("HR Case Manager" is a distinct named POD/HR role and is fine to keep.)
- Favour plain, affirmative sentences over negation-heavy or listy-negative constructions. "No fatigue, no missed step" reads as a list of absences; prefer stating the positive capability directly ("can run continuously, completing every step"). This isn't a ban on the word "not" — natural, necessary contrasts stay — it's specifically about rhetorical "no X, no Y" / "isn't just X, it's Y" patterns.
- Keep adverbs and intensifiers light: avoid stacking words like "genuinely," "truly," "very," "far more," "completely" as filler.
- Tone throughout: friendly, supportive, encouraging, plain English, for an audience that may have no software background. Checklists are the default way to make advice actionable — most sections end with one.
- Every numbered section and most subsections end (or nearly end) with a "Checklist: ..." block using `- [ ] ` items, written as first-person statements ("I know...", "I've asked...", "I will...").

## Verifying claims

Several sections make claims about UK/NHS Wales policy, law, or DHCW's current status (the OCP two-thirds test, PADR/pay progression, the Welsh Government oversight and escalation framework). These were researched via WebFetch/WebSearch against primary sources where possible; `gov.wales` blocks direct automated fetches (returns HTTP 403), so any gov.wales-sourced fact in this project is flagged in `spec/` as coming from search-indexed summaries rather than a directly quoted primary source. When adding or changing a factual claim, prefer fetching and quoting a primary source; when that's blocked, say so explicitly in `spec/` and hedge the claim in `README.md` (e.g. "confirm the current position directly").

## What not to do

- Don't add a `guide/` directory, split `README.md` by section, or otherwise fragment the guide across files — this was tried and explicitly reversed by the user.
- Don't remove the `spec/` → `README.md` traceability by hard-coding new facts straight into `README.md` without a corresponding `spec/` entry.
- Don't reintroduce bold markup, emoji, or "your manager" as a contact when editing — these were explicit, repeated removals.
