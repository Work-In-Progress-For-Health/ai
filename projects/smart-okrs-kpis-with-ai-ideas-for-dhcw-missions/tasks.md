# Tasks: SMART OKRs & KPIs with AI Ideas for DHCW Missions

Companion to `plan.md`. Steps are grouped by phase, then by mission, then by cross-cutting concern. Each task has: owner placeholder, expected output, definition of done (DoD), and suggested due window.

Legend: **O** = output · **DoD** = definition of done · **Due** = suggested timeframe.

---

## Phase 0 — Foundations (weeks 1-4)

### 0.1 Set up the OKR/KPI working group

- Identify executive sponsor (CEO/CDIO), mission leads (5), KPI owner, IG lead, finance lead, communications lead.
- **O**: RACI matrix and Terms of Reference.
- **DoD**: Signed off by exec team; first meeting scheduled.
- **Due**: Week 1.

### 0.2 Confirm canonical sources of truth

- For each candidate metric, identify the data source and steward (NDR, CMDB, EHR, HRIS, app analytics, BI tool).
- **O**: Source-of-truth register (one row per metric).
- **DoD**: Each entry has owner, system, refresh cadence, access route.
- **Due**: Week 2.

### 0.3 Publish definitions and methodology

- Pin definitions for "in-scope service", "active user", "go-live", "live AI use case", "priority role", "core EHR module".
- **O**: Definitions document v1.0.
- **DoD**: Reviewed by IG, clinical, finance, partners; merged.
- **Due**: Week 3.

### 0.4 Stand up the measurement platform

- Choose tooling (BI, observability, model registry, survey).
- **O**: Architecture decision record (ADR) per choice.
- **DoD**: Tools provisioned in a non-prod environment.
- **Due**: Week 4.

### 0.5 Equity-and-inclusion guardrail design

- Decide disaggregation dimensions (deprivation decile, age, language, condition).
- **O**: Equity reporting spec.
- **DoD**: Pilot dashboard with disaggregation for one KPI.
- **Due**: Week 4.

---

## Phase 1 — Baseline each mission (weeks 4-12)

### 1.1 Mission 1 — Platform baselines

- Inventory services and classify cloud-readiness; measure data-centre RU footprint.
- Score technical debt across the application estate.
- Capture cyber posture baseline.
- **O**: Mission-1 baseline pack (services × cloud-readiness × debt × posture).
- **DoD**: Published to mission lead and exec; numbers reconciled against CMDB.
- **Due**: Week 8.

### 1.2 Mission 2 — Products baselines

- Map current EHR modules per health board.
- Measure e-prescribing share, closed-loop med admin rate, prescribing-error rate.
- Run a HIMSS-EMRAM-equivalent assessment (or document gap to do so).
- **O**: Mission-2 baseline pack.
- **DoD**: Health-board CIOs co-sign.
- **Due**: Week 10.

### 1.3 Mission 3 — Records baselines

- Measure current NHS Wales App MAU, retention curve, CSAT.
- Measure record coverage and domain completeness.
- Measure data staleness per domain.
- **O**: Mission-3 baseline pack including equity stratification.
- **DoD**: App analytics + NDR queries reproducible from a runbook.
- **Due**: Week 10.

### 1.4 Mission 4 — Innovation baselines

- Inventory existing AI/automation pilots and live use cases.
- Document SDE current capability and existing project throughput.
- Define £-per-FTE-hour assumption for benefits maths.
- **O**: Mission-4 baseline pack incl. benefits methodology.
- **DoD**: Finance signs off the £ rate; clinical signs off assurance bar.
- **Due**: Week 12.

### 1.5 Mission 5 — Organisation baselines

- Pull engagement, turnover, internal-fill rate, programme RAG.
- Compute 2024 carbon baseline (Scopes 1, 2, in-scope 3).
- **O**: Mission-5 baseline pack.
- **DoD**: Sustainability and HR leads co-sign.
- **Due**: Week 12.

---

## Phase 2 — Draft OKRs and KPIs per mission (weeks 8-16)

For each mission, in parallel:

### 2.M — Per-mission drafting tasks

- Convert strategic objectives into 2-4 Objectives with 3-5 Key Results each.
- For each KR, fill the KPI template (Title, Scope, Owner, Formula, Units, Source, Frequency, Comments).
- Sense-check against the SMART criteria (one mark per letter).
- **O**: Per-mission OKR/KPI sheet.
- **DoD**: Mission lead, finance, and IG initial.
- **Due**: Week 12-14 (staggered).

### 2.X — Stress-test and red-team

- Hold a "metric pre-mortem": how could each KPI be gamed or misread?
- Add guardrail metrics (e.g., complaints rate alongside MAU; safety events alongside automation).
- **O**: Risk-and-guardrail addendum per mission.
- **DoD**: Independent reviewer (not in mission team) signs off.
- **Due**: Week 14.

### 2.Y — Compare with adjacent organisations

- Map each KPI to the nearest NHSE/Scotland/PHW equivalent; record gaps.
- **O**: Comparator matrix.
- **DoD**: Published with at least one peer-org contact per row.
- **Due**: Week 16.

---

## Phase 3 — Validate, prioritise, commit (weeks 14-20)

### 3.1 Internal review

- Walk-through with each directorate; capture amendments.
- **O**: Revised OKR/KPI book v0.9.
- **Due**: Week 16.

### 3.2 Stakeholder review

- Workshops with the 7 health boards, Welsh Government, social care reps, and patient panel.
- **O**: Stakeholder consultation log + amendments.
- **DoD**: ≥80% of consulted stakeholders respond; objections logged and answered.
- **Due**: Week 18.

### 3.3 Prioritise

- Apply a value-vs-feasibility scoring to KRs; lock the Top 20 strategic objectives mapped from the 5 missions.
- **O**: Final scored portfolio.
- **Due**: Week 19.

### 3.4 Approve and publish v1.0

- Exec approval; publish public summary, internal full version, data dictionary.
- **O**: Published OKR/KPI book v1.0.
- **Due**: Week 20.

---

## Phase 4 — Operate the OKR/KPI system (ongoing from week 16)

### 4.1 Reporting cadence

- Weekly: product SLO/error-budget reviews.
- Monthly: KPI scoreboard to board; programme RAG; equity gap alert review.
- Quarterly: KR check-ins; portfolio rebalancing; FinOps + carbon review.
- Annual: outcome review; public report; refresh.
- **DoD**: Calendar invites in place; dashboards published.

### 4.2 Operating dashboards

- Build one dashboard per mission with KR burn-up + KPI trend + equity stratification.
- Build a single "DHCW Strategy on a page" rollup.
- **DoD**: Dashboards reviewed by exec; access permissions verified.

### 4.3 Data quality monitoring

- Automated checks for staleness, completeness, schema drift on every KPI feed.
- **DoD**: Alerts route to a named data steward; SLO of <2% stale rate.

### 4.4 Decision logging

- Every quarterly review records: target adjustments, retired KPIs, new KPIs, rationale.
- **DoD**: Decisions visible in a public-by-default log.

---

## Phase 5 — Per-mission delivery tasks (concurrent with Phase 4)

### Mission 1 — Platform

- M1.1 Establish cloud landing zones; publish "cloud-by-default" policy.
- M1.2 Build the NDR onboarding pipeline; reduce median time-to-onboard.
- M1.3 Decommission first wave of legacy data-centre kit.
- M1.4 Run quarterly architecture-drift detection; remediate top findings.
- M1.5 Pilot AI-assisted migration on 3 services; measure suggestion acceptance + defect rate.

### Mission 2 — Products

- M2.1 Roll out e-prescribing to remaining GP practices in waves; report monthly.
- M2.2 Sequence all-Wales EHR module go-lives across 7 health boards.
- M2.3 Stand up closed-loop med-admin in inpatient pilot sites; scale.
- M2.4 Procure and run annual HIMSS EMRAM-equivalent assessment.
- M2.5 Pilot ambient voice (AVT) in one specialty; benefit-case and assurance audit.

### Mission 3 — Records

- M3.1 Marketing/onboarding campaigns aligned to MAU trajectory; equity guardrail per campaign.
- M3.2 Ship record-domain modules per published roadmap; cut staleness with each release.
- M3.3 Wearables ingestion pilot with one condition cohort.
- M3.4 Welsh-language coverage and assistive features ship in parallel with each release.
- M3.5 LLM record-summary feature behind feature flag; measure comprehension uplift vs. control.

### Mission 4 — Innovation

- M4.1 Open SDE to first 5 research projects; capture cycle-time.
- M4.2 Build the AI model registry and assurance pipeline.
- M4.3 Ship 10 productionised AI/automation use cases with benefit cases.
- M4.4 Publish a public AI-transparency register (model cards).
- M4.5 Quarterly model-monitoring report (accuracy, drift, fairness).

### Mission 5 — Organisation

- M5.1 Launch academy programmes (data, software, cyber, AI).
- M5.2 Publish carbon baseline and net-zero route map.
- M5.3 Quarterly engagement pulse + annual NHS staff survey alignment.
- M5.4 Stand up an internal LLM knowledge assistant; KPI on questions answered.
- M5.5 Programme-health AI predictor pilot for Tier-1 portfolio.

---

## Phase 6 — AI assurance and ethics (cross-cutting)

- A.1 Adopt or extend an existing assurance framework (e.g., NHS AI Lab, MHRA software-as-medical-device).
- A.2 Maintain a public AI register with risk class, owner, evaluation history.
- A.3 Red-team every clinical-impact model pre-go-live; repeat annually.
- A.4 Bias audits with disaggregated performance reporting.
- A.5 Human-in-the-loop checkpoints for clinical-facing AI.
- A.6 Incident response playbook for AI failures (hallucination, drift, prompt injection).

---

## Phase 7 — Communications and engagement

- C.1 "Strategy on a page" + simple-language summary in English and Welsh.
- C.2 Public dashboard with selected KPIs (transparency).
- C.3 Quarterly stakeholder bulletin; annual public report.
- C.4 Internal storytelling: feature one team per month delivering against an OKR.
- C.5 Patient-public-involvement panel reviews record/app changes.

---

## Acceptance checklist (the final gate before "live")

- [ ] Every mission has 2-4 Objectives, each with 3-5 Key Results.
- [ ] Every KR has at least one KPI with all template fields populated.
- [ ] Every KPI has a baseline measured before a target is committed.
- [ ] Each KPI has an equity disaggregation plan or a documented reason it is exempt.
- [ ] Each KPI has a named owner, source, and refresh cadence.
- [ ] Each Objective has a guardrail metric to detect gaming or harm.
- [ ] Each AI use case has a benefit case, an assurance class, and a monitoring plan.
- [ ] Carbon, equity, and patient-safety guardrails are reviewed each quarter.
- [ ] Methodology and definitions are publicly published.
- [ ] An external/independent reviewer has stress-tested the OKR/KPI book.

---

## Open questions to resolve before publishing v1.0

1. Final 2024 baselines for cloud-services-in-scope, technical-debt index, carbon.
2. Sequence of NDR onboarding by domain × health board.
3. Canonical engagement survey and CSAT methodology.
4. £-per-FTE-hour value used for productivity benefits.
5. Assurance bar for clinical-facing AI (named framework + named approver).
6. Identity-assurance level required for sensitive app features.
7. Scope of the all-Wales EHR "core modules" and the rollout order.
8. Welsh-language and accessibility baselines for every public-facing product.
