# AGENTS/style.md

Tone, language, and formatting rules for this repository, accumulated from direct, repeated user instruction over the guide's development. Treat all of these as binding, not stylistic suggestions.

## Formatting

- No bold Markdown (`**text**`), anywhere, including headings. Use plain text; italics (`*text*`) are fine, used sparingly (e.g. book titles).
- No emoji, anywhere, including headings and checklist markers. A checklist heading reads "Checklist: getting things in writing," not "Checklist: getting things in writing" with a checkmark or any other symbol prefixed.
- Headings use sentence case, not title case ("Get it in writing," not "Get It In Writing").
- Checklists use `- [ ] ` items (unchecked Markdown task list syntax), written as first-person statements: "I know...", "I've asked...", "I will...", "I understand...". Not third-person or imperative ("Know your union rep" is wrong; "I know who my union rep is" is right).

## Terminology

- "Automatic testing" — use this for the practice/discipline in general ("the shift from manual to automatic testing," "the upside of automatic testing"). This is a deliberate, explicit preference over the more common industry phrase "automated testing."
- "Automated test(s)" / "automated test suite" / "automated regression suite" — fine as-is, unchanged. These refer to the artifacts (the tests themselves), not the discipline, and were not the target of the automatic/automated substitution.
- Whenever Playwright and Selenium are named together as a pair or list, also list WebDriver: "Playwright, Selenium, or WebDriver," not "Playwright or Selenium." (WebDriver is the protocol Selenium implements; Playwright doesn't use it, but the user wants it named alongside both regardless — treat this as a fixed style rule, not something to second-guess.)
- POD/HR — the DHCW/NHS Wales People and Organisational Development function, playing the role most organisations call "HR." Always write "POD/HR contact," never "HR" alone and never "your manager." "HR Case Manager" (a specific named POD/HR role used during redeployment) is a distinct, correct term and should stay.
- PADR — Performance Appraisal and Development Review. Always expand on first use in a new section if it hasn't appeared nearby.
- OCP — NHS Wales Organisational Change Policy. Defined in `spec/index.md`.

## Contacts: never "your manager"

This project deliberately routes every escalation, question, and support path through the POD/HR contact and the trade union rep. This was an explicit, repeated correction from the user: an earlier draft referenced "your manager" in several places (as an alternative or additional contact), and every instance was removed. When adding new content that needs a human contact point, use "POD/HR contact" or "union rep" (or both) — do not add "your manager" as an option, even as a soft alternative ("or your manager").

## Framing: growth, not loss

The guide's tone is deliberately weighted towards learning, growth, and encouragement, not job-security anxiety:

- The opening framing is "A growth story," not anything invoking loss, endings, or goodbyes. An earlier draft's heading ("This is a growth story, not a goodbye story") was corrected to drop the negative half entirely.
- Formal job-security protections (the two-thirds test, redeployment, pay protection) are covered, but positioned late in the guide (section 21, "Your safety net, briefly") and explicitly framed as backup information, not the headline.
- Sections on the upside of automatic testing, worldwide/cross-sector context, continuous learning, and self-directed growth (challenge questions, learning toolkit, OKRs) get proportionally more space and come earlier.

## Affirmative phrasing over negative listing

Prefer stating a positive capability directly rather than listing what's absent. This is specifically about rhetorical "no X, no Y" or "isn't just X, it's Y" list-style constructions, not a ban on the word "not" in general (natural, necessary contrasts — e.g. "a variance in tools, not a new job," where the contrast itself is the meaningful legal point — stay as-is).

Example of the pattern to avoid and how it was fixed:

- Before: "no fatigue, no missed step at the end of a long shift"
- After: "staying fresh and completing every step, even at the end of a long shift"

Other examples applied throughout the guide: "Policy sets no fixed number of weeks" became "Policy leaves the number of weeks flexible"; "no fear, no logistics, no assumptions" became "full confidence, open logistics, and a blank slate."

## Adverbs and intensifiers

Keep them light. Avoid stacking words like "genuinely," "truly," "very," "far more," "completely," "absolutely" as filler — they were deliberately trimmed in an earlier simplification pass. Use them only where a specific word is doing real work, not as habitual emphasis.

## Reading level and audience

Write for NHS Wales DHCW manual software testers: assume no prior programming or DevOps background, but real professional competence and intelligence. Explain jargon in plain English the first time it appears (see the "Ways of working" glossary table in README.md section 7 for the model to follow — term, plain-English meaning, why it matters to the reader). Avoid corporate or consultancy-speak.
