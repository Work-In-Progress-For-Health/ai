# Tasks: SMART OKRs & KPIs + AI Ideas for DHCW Priorities

Sequenced, comprehensive task list for turning the plan into a delivered KPI/OKR system. Tasks are grouped into phases. Each task has: **Why**, **Steps**, **Outputs**, **Owner**, **Done when**.

## Phase 0 — Foundations (Weeks 1-4)

### T0.1 — Confirm priority inventory
- Why: The publication-scheme page lists frameworks but not concrete priority statements; the IMTP and 2024-2030 strategy supply the missing detail. We need one canonical list.
- Steps:
  1. Pull the latest IMTP (2025-2028) "20 strategic objectives" list.
  2. Cross-reference against the 5 missions and 3 core programmes.
  3. Resolve duplicates and naming inconsistencies.
- Outputs: `priorities-inventory.csv` with columns: id, title, mission, programme, IMTP-objective-ref, owner.
- Owner: Strategy & Performance.
- Done when: Inventory signed off by Director of Strategy.

### T0.2 — Confirm escalation context & success criteria
- Why: DHCW is at WG escalation level 3 (Feb-2025); every OKR must visibly contribute to de-escalation.
- Steps:
  1. Read WG oversight & escalation framework (May 2025).
  2. Note the specific findings that triggered level 3.
  3. Map each finding to one or more missions / KRs in `plan.md`.
- Outputs: `escalation-mapping.md`.
- Owner: Director of Strategy + Director of Operations.
- Done when: Each escalation finding has at least one OKR owner.

### T0.3 — Adopt SMART/OKR/KPI templates
- Why: Consistency makes the scorecard machine-readable.
- Steps:
  1. Approve the templates from `AGENTS.md`.
  2. Publish as a one-page reference in DHCW intranet.
- Outputs: Template page; YAML schema for KPI records.
- Owner: PMO.
- Done when: All OKR drafts use the template.

### T0.4 — Stand up a KPI registry
- Why: Need a single durable store for KPI definitions independent of dashboards.
- Steps:
  1. Decide tooling (Confluence + Git-backed YAML preferred).
  2. Define `kpi.schema.yaml` with: title, OKR ref, scope, owner, formula, units, source, frequency, comments, equity-breakdown.
  3. Seed with KPIs from `plan.md` §5.
- Outputs: `kpi-registry/` directory.
- Owner: Head of Performance.
- Done when: All §5 KPIs are in the registry and link to dashboards.

## Phase 1 — Instrument the missing data (Weeks 3-12, in parallel)

### T1.1 — NHS Wales App analytics pipeline
- Why: M3 MAU and feature-adoption KPIs depend on event analytics.
- Steps:
  1. Spec event schema (login, feature view, transaction success/fail) with privacy review.
  2. Implement on Android, iOS, web.
  3. Sink events to NDR with daily-refresh MAU view.
- Outputs: Snowplow/Mixpanel pipeline; `app_events` table; `mau` view.
- Owner: DSPP lead engineer.
- Done when: MAU dashboard live and reconciled to authentication logs ±2%.

### T1.2 — Service availability & MTTR instrumentation
- Why: M2.O1 requires four-nines proof for top-10 services.
- Steps:
  1. List top-10 services (T0.1 input).
  2. Add synthetic monitors per service.
  3. Stand up incident-timeline tooling so MTTR is computable from ITSM.
- Outputs: Grafana board "Top-10 reliability"; ITSM incident-timeline plugin.
- Owner: SRE / Platform Lead.
- Done when: Availability + Sev-1 + MTTR all published monthly.

### T1.3 — Architecture conformance tracking
- Why: M1 KPI2 needs evidence per design review.
- Steps:
  1. Add "Target architecture references" mandatory field to TDA template.
  2. Tag historic submissions retrospectively.
- Outputs: TDA dashboard with conformance %.
- Owner: Chief Architect.
- Done when: Conformance % is reported monthly.

### T1.4 — AI use-case register
- Why: M4 KPI1 needs an audited record.
- Steps:
  1. Define register schema (clinical safety class, IG, bias review, energy, benefit hypothesis, hours-released).
  2. Bootstrap with current pilots.
  3. Publish quarterly to Board.
- Outputs: `ai-use-case-register/`.
- Owner: Director of Innovation.
- Done when: ≥10 entries, each with full schema completion.

### T1.5 — IMTP milestone tracker
- Why: M5.O1.KR2 needs a defensible delivery-rate %.
- Steps:
  1. Import IMTP milestones into a single tracker.
  2. Tag each by mission + programme + quarter.
  3. Build monthly rollup view.
- Outputs: Balanced-scorecard milestone dashboard.
- Owner: PMO.
- Done when: Monthly Exec pack draws from it automatically.

### T1.6 — Equity guardrail data
- Why: Prevent adoption KPIs from hiding inequity.
- Steps:
  1. Join NHS Wales App users to WIMD quintiles via LSOA.
  2. Add Welsh-language-preference breakdown.
  3. Surface guardrail panels next to every adoption KPI.
- Outputs: Equity panels in Power BI / Tableau.
- Owner: Head of Data Insight.
- Done when: No headline adoption metric ships without an equity breakdown.

## Phase 2 — Author the OKRs per mission (Weeks 4-10)

For each mission, produce a workshop output following the `plan.md` §5 template.

### T2.1 — Mission 1 OKRs (Platform for digital transformation)
- Steps: workshop with Architecture + WG digital lead; agree priority data domains (target = 8); set M1.O1 baselines; ratify KPIs M1.O1.KPI1, KPI2.
- Output: `okrs/m1.md`.

### T2.2 — Mission 2 OKRs (High-quality digital products & services)
- Steps: workshop with Operations + SRE; confirm top-10 services; set Sev-1 baseline Q1 FY26/27; ratify KPIs M2.O1.KPI1-3.
- Output: `okrs/m2.md`.

### T2.3 — Mission 3 OKRs (Digital health and care record)
- Steps: workshop with DSPP + Records programme; agree MAU baseline + interim targets; confirm 3-of-7 care settings for Phase 1 record; ratify KPIs M3.O1.KPI1-3, M3.O2.KPIs.
- Output: `okrs/m3.md`.

### T2.4 — Mission 4 OKRs (Innovation, AI, NDR SDE)
- Steps: workshop with Innovation + NDR + Clinical Safety; agree productivity definition (hours released vs. throughput per FTE); ratify KPIs M4.O1.KPI1-3.
- Output: `okrs/m4.md`.

### T2.5 — Mission 5 OKRs (Trusted partner / org health)
- Steps: workshop with COO + HR + Sustainability; ratify escalation, milestone, engagement, carbon KPIs.
- Output: `okrs/m5.md`.

### T2.6 — Programme-level OKRs (cross-cutting)
- NDR programme OKR (KPIs: domains onboarded, query latency, SDE active projects).
- DSPP programme OKR (KPIs: MAU, feature breadth, SUS, equity).
- Digital Medicines programme OKR (KPIs: % prescriptions digitally enabled, reconciliation accuracy, shortage-alert lead time).
- Output: `okrs/programmes.md`.

## Phase 3 — Comparative benchmarking (Weeks 6-12)

### T3.1 — NHS England benchmarking
- Steps: pull NHSE 2025/26 planning guidance numeric targets (FDP 85% by Mar-2026, RTT 65%, A&E 78%, 4% productivity, 1% cost reduction). Map each to the DHCW analogue if any; flag gaps.
- Output: `benchmarks/nhs-england.md`.

### T3.2 — NHS Scotland benchmarking
- Steps: read Care in the Digital Age delivery plan 2025-2026 and NSS Strategic Framework 2024-2026. Compare Digital Front Door MVP pattern to NHS Wales App rollout; compare NDP to NDR.
- Output: `benchmarks/nhs-scotland.md`.

### T3.3 — NHS Wales system benchmarking
- Steps: align DHCW KPIs to the NHS Wales Performance Framework 2025-26 (5 strategic priorities + Quadruple Aim). Every DHCW KPI gets a "contributes to NHS Wales SP#X / QA dimension" tag.
- Output: `benchmarks/nhs-wales.md`.

### T3.4 — Synthesise lessons
- Steps: 1-page "what we adopt, what we adapt, what we reject".
- Output: `benchmarks/synthesis.md`.

## Phase 4 — Telemetry & observability stack (Weeks 8-16)

### T4.1 — Three-layer observability model
- Steps: stand up service-layer (Grafana/Prometheus), product-layer (Snowplow/Mixpanel into NDR), outcome-layer (Power BI/Tableau).
- Output: architecture diagram + access list.
- Owner: Head of Platform + Head of Data Insight.

### T4.2 — Cadence + publication
- Steps: define what is published weekly / monthly / quarterly / annually; align to publication-scheme requirements.
- Output: `cadence.md`; calendar invites for review meetings.

### T4.3 — AI observability
- Steps: add model-drift, fairness, hallucination, override-rate panels per M4 use-case.
- Output: standard AI-use-case dashboard template.

### T4.4 — Public KPI pack
- Steps: agree which KPIs are externally publishable; format quarterly KPI pack for publication-scheme page.
- Output: first published pack on the publication-scheme page.

## Phase 5 — AI use-cases (Weeks 10-26+, rolling)

### T5.1 — Triage candidate AI use-cases
- Steps: score 20+ candidate use-cases on (clinical safety risk, IG complexity, expected hours released, equity impact, energy footprint). Pick top 10 to progress.
- Output: scored register.

### T5.2 — Prioritised pilots
- For each of:
  - NHS Wales App symptom triage (bilingual EN/CY).
  - Ambient-listening clinical scribe pilot.
  - LLM natural-language query over NDR SDE.
  - Prescribing anomaly detection.
  - Radiology / dermatology AI-assisted triage.
  - IT service-desk first-line AI assistant.
  - LLM-assisted Board report drafting.
  Steps: clinical safety case (DCB0129/0160 equivalent), bias review, IG approval, success criteria, evaluation plan, post-deployment audit.
- Output: per-use-case dossier in the AI register.

### T5.3 — Productivity baseline & uplift measurement
- Steps: time-and-motion baseline per use-case; post-deploy measurement; sign-off by Finance for the M4.O1.KR2 hours-released total.
- Output: audited benefit cases linked to M4 KPIs.

## Phase 6 — Governance, sign-off, and operating rhythm (Weeks 12-20)

### T6.1 — Balanced-scorecard refresh
- Steps: replace current scorecard with the OKR-aligned version; ensure every cell has owner, KPI ref, threshold, RAG rule.
- Output: refreshed scorecard.

### T6.2 — Board approval
- Steps: paper to DHCW Board summarising new OKR/KPI set; vote.
- Output: minuted approval.

### T6.3 — Welsh Government alignment
- Steps: share OKR set with WG digital lead; confirm it answers the escalation-level-3 findings.
- Output: WG written acknowledgement.

### T6.4 — Audit Wales engagement
- Steps: brief Audit Wales for 2026 structured assessment on the OKR/KPI changes.
- Output: meeting note.

### T6.5 — Operating rhythm
- Steps: lock weekly programme stand-ups, monthly mission scorecard review, quarterly Board pack, annual cycle (Business Plan → IMTP → Annual Report).
- Output: published rhythm calendar.

## Phase 7 — Continuous improvement

### T7.1 — Quarterly KPI review
- Steps: each quarter, review every KPI for: is it still load-bearing? is data still trustworthy? did it drive a decision? Retire ones that didn't.
- Output: KPI registry diff per quarter.

### T7.2 — Annual missions retrospective
- Steps: at end of each FY, retrospective on what missions actually moved; rebase targets.
- Output: Annual Report contribution; updated `plan.md`.

### T7.3 — External re-benchmarking
- Steps: re-run Phase 3 benchmarking annually.
- Output: refreshed `benchmarks/*.md`.

## Dependencies (summary)

- T0.1 blocks T1.* and T2.*.
- T1.1 blocks M3 KPIs.
- T1.2 blocks M2 KPIs.
- T1.4 blocks M4 KPIs.
- T1.5 blocks M5 KPIs.
- Phase 2 blocks Phase 4.4 (public pack).
- Phase 5 outputs feed M4 KRs.
- Phase 6.3 (WG alignment) is the de-escalation gate.

## Acceptance criteria for the whole exercise

- Every one of the 5 missions has at least one Objective with 3+ Key Results and 2+ KPIs in the registry.
- Every KPI has named owner, formula, source, frequency.
- Every adoption KPI has an equity guardrail.
- Every AI use-case has clinical safety + bias + IG review on file.
- The balanced scorecard rolls up from KPIs to KRs to Objectives to missions with no manual re-keying.
- A quarterly public KPI pack is published on the publication-scheme page.
- DHCW exits WG escalation level 3 by 31-Mar-2027 (the headline outcome).
