# Assertables

## What the data shows

Ninety-one releases across about five years. This is a story of at least four distinct eras with very different rhythms. A single average would be meaningless here.

**Era 1 — Initial burst (Mar 2021):** Eleven releases from 1.1.0 to 1.11.0 in a single day, then 2.0.0 the next day. This is almost certainly a backfill — someone retroactively tagging history when a versioning scheme was introduced, or a tool publishing its initial version history in one go. Treating these as "deployments" for DORA purposes would be misleading.

**Era 2 — Sparse and bursty (Apr 2021 – Mar 2023):** Roughly two years with releases clustered in short bursts (three in May 2021, seven in early Feb 2022, another cluster in early 2023). About 18 releases across 24 months, averaging one every 5–6 weeks, but the *pattern* is sprint-then-quiet rather than steady cadence.

**Era 3 — The September 2024 rapid releases:** From Sep 2 to Oct 20, 2024 — a seven-week window — roughly 26 releases, several per week. The version numbers march from 8.0.0 through 8.19.0 into 9.0.0 at a pace that strongly suggests either a major rewrite being rolled out in staged chunks, a semantic-release / automated-release pipeline being turned on, or a CI system that now bumps a version on every merge to main.

**Era 4 — Post-rapid stabilisation (late Oct 2024 – Apr 2026):** The rapid pace returns to clustered releases again — a burst in early November 2024, a big cluster in June 2025 (14 releases in three weeks touching 9.5.x, 9.6.x, 9.7.x *in parallel*), then a slower tail of four releases across late 2025 into 2026.

## The single most important observation

**Multiple minor versions are being maintained in parallel.** Look at early June 2025: 9.5.3, 9.5.4, 9.5.5, 9.5.6 *and* 9.6.0, 9.6.1 *and* 9.7.0 all ship within days of each other. Then 9.5.7, 9.5.8, 9.6.2, 9.6.3, 9.7.1 on the same three days in June. This is the signature of a project that supports several release branches simultaneously — almost certainly a library, framework, SDK, or self-hosted product where users are pinned to different minor versions and each needs backported fixes.

**This is not a DORA deployment-frequency signal at all.** DORA measures how often changes reach *production users of a service*. Here, each release is a published artifact; users pull whichever version they want, whenever they want. The team's "deploy" ends when the package is published — the actual reaching-of-users is on a completely different timeline they don't control.

## Mapping to DORA tiers — with heavy caveats

If you insisted on applying DORA's four tiers anyway: Era 3 (Sep–Oct 2024) would clock as *elite*, Era 4's June 2025 burst as *high*, the quieter stretches as *medium* or *low*. But that ranking is almost certainly meaningless. A library that publishes four patches to three supported branches in one day isn't "elite" — it's responding to a CVE, a regression, or a coordinated release event. DORA wasn't built for this shape of work.

## Questions to ask

- What is this? Library, framework, CLI tool, self-hosted service, SaaS? The answer changes whether DORA applies at all.
- Are the June 2025 parallel releases coordinated patch releases across supported branches (e.g. security fix backported to 9.5, 9.6, 9.7 simultaneously)? That's almost certainly what's happening and it's a meaningful release-engineering event worth naming.
- What happened between September and October 2024 that produced the cascade from 8.0.0 to 9.0.0? A rewrite going GA? Adoption of automated semantic versioning? A migration rolling out in pieces?
- Is version bumping automated (every merge to main produces a release) or manual (a human decides to cut)? The first inflates the metric; the second reflects intent.
- What does "deployment" mean for this team — publishing a package, tagging a release, or something reaching actual users?
- What is the support policy for minor versions? How many branches are kept alive at once?
- Are the other DORA metrics tracked? For a library, change failure rate (releases that get yanked or immediately patched) is far more informative than frequency.

## Recommendations — held lightly

If this is a library or self-hosted product (which the shape of the data strongly suggests), **don't use DORA's deployment-frequency tiers at all**. They were calibrated for internet services where the team controls when code reaches users. The more useful metrics here are time-from-commit-to-published-release, number of supported branches, patch-release rate per branch (a proxy for stability of each minor), and — crucially — how quickly a security fix can be shipped to all supported branches simultaneously. The June 2025 parallel-release event suggests the team is already good at that last one.

## The honest read

The data shape tells me more about the project's release engineering than about team performance. The March 2021 mass-tag, the 2024 cascade through two major versions, and the parallel-branch patch releases in June 2025 are all artifacts of how releases are *produced and labelled*, not measures of how fast value reaches users. Before drawing DORA conclusions, figure out what the releases actually represent — then pick a metric that matches. For most of what this data looks like, deployment frequency isn't it.
