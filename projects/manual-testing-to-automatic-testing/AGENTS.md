# AGENTS.md

Instructions for AI coding agents working in this repository (any tool — Claude Code, Codex, Copilot, Cursor, etc.). If you are specifically Claude Code, also read [CLAUDE.md](CLAUDE.md).

## What this repository is

A single, comprehensive guide for NHS Wales / Digital Health and Care Wales (DHCW) manual software testers whose teams are moving towards test automation. It is documentation, not software: no build step, no tests to run, no dependencies to install.

## The two hard rules

1. `spec/*.md` is the single source of truth. Facts used in `README.md` — NHS Wales Organisational Change Policy (OCP) provisions, the PADR process, DHCW's Welsh Government oversight status — are specified in `spec/` first. If `README.md` and `spec/` disagree, `spec/` is correct; fix `README.md` to match it.
2. `README.md` contains the entire guide and must not be split into multiple files. This was tried (a `guide/` directory with one file per part) and explicitly reversed by the user, who required the whole guide — every section, every checklist — to be readable in the single `README.md` file. `README.md` is exempt from the 40KB file-size guideline below; every other file in this repo should stay under it.

## File layout

| Path | Purpose | Size target |
|---|---|---|
| `README.md` | The entire guide: all numbered sections and checklists | No limit (explicit exception) |
| `index.md` | A short pointer to `README.md` and `spec/` | A few KB |
| `spec/index.md` | OCP policy facts: source of truth | Under 40KB |
| `spec/padr.md` | PADR process facts: source of truth | Under 40KB |
| `CLAUDE.md` | Claude Code-specific instructions | Under 40KB |
| `AGENTS.md` | This file | Under 40KB |
| `AGENTS/style.md` | Tone, language, and formatting rules | Under 40KB |
| `AGENTS/structure.md` | Section numbering, anchors, checklist conventions | Under 40KB |
| `AGENTS/sources.md` | How to verify and cite factual claims | Under 40KB |

Read [AGENTS/style.md](AGENTS/style.md), [AGENTS/structure.md](AGENTS/structure.md), and [AGENTS/sources.md](AGENTS/sources.md) before making a non-trivial content edit — each covers one concern in more depth than fits here.

## Workflow for a content change

1. Fact change (policy, process, DHCW status)? Update the relevant `spec/*.md` file first.
2. Update `README.md` to match. Search (`grep -n`) for every place the changed fact, term, or cross-reference appears — key facts repeat across many sections by design, and a partial edit leaves the guide self-contradictory.
3. Changed a heading's text? Its anchor slug changes too. Find and fix every internal `[text](#n-old-slug)` link that pointed at it, including the numbered Contents list.
4. Re-check file sizes: `README.md` is expected to be large; everything else should stay under 40KB.

## Quick-reference constraints (see AGENTS/style.md for full detail)

- No bold Markdown (`**text**`). No emoji.
- "Automatic testing" for the practice/discipline; "automated test(s)" is fine for the artifacts.
- Playwright and Selenium mentioned together always also list WebDriver.
- Support contacts are POD/HR and the trade union rep — never "your manager."
- Prefer affirmative phrasing over "no X, no Y" listing constructions.
- Most sections and subsections end with a `Checklist: ...` block of `- [ ] ` first-person items.

## Don't

- Split `README.md` into multiple files.
- Add facts to `README.md` with no corresponding entry in `spec/`.
- Reintroduce bold markup, emoji, or "your manager" as a contact.
