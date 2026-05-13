# Tasks: SMART OKRs & KPIs with AI Ideas for the Digital Service Standard for Wales

Companion to `plan.md`. Steps are grouped by phase, then by Standard, then by cross-cutting concern. Each task has: owner placeholder, expected output, definition of done (DoD), and suggested due window.

Legend: **O** = output · **DoD** = definition of done · **Due** = suggested timeframe.

---

## Phase 0 — Foundations (weeks 1-4)

### 0.1 Set up the OKR/KPI working group

- Identify executive sponsor (Welsh Govt Director of Digital Public Services), Standard leads (10), KPI owner, IG/DPO, finance lead, Welsh Language Commissioner liaison, accessibility lead, comms lead.
- **O**: RACI matrix and Terms of Reference.
- **DoD**: Signed off by exec; first meeting scheduled.
- **Due**: Week 1.

### 0.2 Confirm canonical sources of truth

- For each candidate metric, identify the data source and steward (service register, CMS, analytics, BI, scanners, surveys).
- **O**: Source-of-truth register (one row per metric).
- **DoD**: Each entry has owner, system, refresh cadence, access route.
- **Due**: Week 2.

### 0.3 Publish definitions and methodology

- Pin definitions: "in-scope service", "public-facing", "active user", "service owner empowered", "MVT (minimum viable team)", "critical service", "live AI use case", "open-source", "weeknote", "well-being statement".
- **O**: Definitions document v1.0 (bilingual EN/CY).
- **DoD**: Reviewed by IG, accessibility, Welsh Language Commissioner; merged.
- **Due**: Week 3.

### 0.4 Stand up the measurement platform

- Choose tooling: service register (e.g., Backstage), BI, observability (OpenTelemetry/Grafana), accessibility scanner, AI model registry, survey platform.
- **O**: Architecture decision records (ADRs).
- **DoD**: Tools provisioned in a non-prod environment.
- **Due**: Week 4.

### 0.5 Equity-and-inclusion guardrail design

- Decide disaggregation dimensions: language (cy/en/other), deprivation decile, age band, accessibility-needs flag.
- **O**: Equity reporting spec.
- **DoD**: Pilot dashboard with disaggregation for one KPI.
- **Due**: Week 4.

### 0.6 Adopt or extend the Digital Service Standard Review process

- Confirm CDPS review cadence; align internal stage gates (alpha/beta/live) to it.
- **O**: Stage-gate playbook.
- **DoD**: Pilot review scheduled with a real service.
- **Due**: Week 4.

---

## Phase 1 — Baseline each Standard (weeks 4-12)

### 1.1 Standard 1 — Well-being baselines

- Inventory public-facing services and count those with a published well-being statement.
- Measure baseline carbon-per-transaction for top-10 services.
- **O**: Standard-1 baseline pack.
- **DoD**: Future Generations Commissioner's office sighted.
- **Due**: Week 8.

### 1.2 Standard 2 — Welsh language baselines

- Audit Welsh-language coverage per service; collect session-share data; collect Welsh CSAT where available.
- **O**: Standard-2 baseline pack.
- **DoD**: Welsh Language Commissioner liaison co-signs.
- **Due**: Week 8.

### 1.3 Standard 3 — User needs baselines

- For each service: top-task list, user-needs artefact freshness, WCAG status, AT-user-test recency.
- **O**: Standard-3 baseline pack.
- **DoD**: Head of User Research + Accessibility Lead co-sign.
- **Due**: Week 10.

### 1.4 Standard 4 — Iteration baselines

- DORA metrics (deployment frequency, lead time, CFR, MTTR) per service.
- Idea-to-production cycle-time baseline.
- **O**: Standard-4 baseline pack.
- **DoD**: Engineering leads co-sign; data is reproducible from CI logs.
- **Due**: Week 10.

### 1.5 Standard 5 — Data-and-research baselines

- Inventory service scorecards (where they exist), automation rate, research repository state.
- Sample decision-evidence rate from recent tickets.
- **O**: Standard-5 baseline pack.
- **DoD**: PMO + UR Lead co-sign.
- **Due**: Week 10.

### 1.6 Standard 6 — Ethics/privacy/security baselines

- DPIA, threat model, ethics review freshness per service.
- Open Critical/High vuln count; NCSC CAF posture for top services.
- AI register state.
- **O**: Standard-6 baseline pack.
- **DoD**: DPO + CISO + Ethics Lead co-sign.
- **Due**: Week 12.

### 1.7 Standard 7 — Service ownership baselines

- Service register reconciliation: who owns what.
- Empowerment survey to current owners; tenure data.
- **O**: Standard-7 baseline pack.
- **DoD**: People Lead + CDPS Standards Lead co-sign.
- **Due**: Week 12.

### 1.8 Standard 8 — Team composition baselines

- MVT compliance review per service; perm/contract mix; discipline coverage.
- Diversity-of-hire baseline.
- **O**: Standard-8 baseline pack.
- **DoD**: Workforce Lead + DEI Lead co-sign.
- **Due**: Week 12.

### 1.9 Standard 9 — Technology baselines

- Stack records per service; tech-radar v0 produced; supplier concentration baseline.
- API catalogue audit; exit-strategy readiness review.
- **O**: Standard-9 baseline pack.
- **DoD**: CTO + Procurement Lead co-sign.
- **Due**: Week 12.

### 1.10 Standard 10 — Open-working baselines

- Weeknote audit; public-roadmap audit; OSS repo audit; reuse audit.
- **O**: Standard-10 baseline pack.
- **DoD**: Communications Lead + Engineering Lead co-sign.
- **Due**: Week 12.

---

## Phase 2 — Draft OKRs and KPIs per Standard (weeks 8-16)

For each Standard, in parallel:

### 2.S — Per-Standard drafting tasks

- Convert each Standard into 2-3 Objectives with 3-5 Key Results each.
- For each KR, fill the KPI template (Title, OKR, Scope, Owner, Formula, Units, Source, Frequency, Comments).
- Sense-check against SMART criteria (one mark per letter).
- **O**: Per-Standard OKR/KPI sheet.
- **DoD**: Standard lead, finance, IG, accessibility, Welsh Language liaison initial.
- **Due**: Week 12-14 (staggered).

### 2.X — Stress-test and red-team

- Hold a "metric pre-mortem": how could each KPI be gamed or misread?
- Add guardrail metrics: e.g., complaints rate alongside MAU; Welsh-language CSAT gap alongside session share; CFR alongside deploy frequency.
- **O**: Risk-and-guardrail addendum per Standard.
- **DoD**: Independent reviewer (not in Standard team) signs off.
- **Due**: Week 14.

### 2.Y — Compare with adjacent organisations

- Map each KPI to the nearest equivalent in GOV.UK, NHS England, NHS Scotland, and within NHS Wales partners.
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

- Workshops with the 7 health boards, local authorities, social-care reps, patient panel, Future Generations Commissioner, Welsh Language Commissioner, accessibility groups.
- **O**: Stakeholder consultation log + amendments.
- **DoD**: ≥80% of consulted stakeholders respond; objections logged and answered.
- **Due**: Week 18.

### 3.3 Prioritise

- Apply value-vs-feasibility scoring to KRs; lock the top portfolio aligned to the 10 Standards.
- **O**: Final scored portfolio.
- **Due**: Week 19.

### 3.4 Approve and publish v1.0

- Exec approval; publish public summary, internal full version, data dictionary, in English and Welsh.
- **O**: Published OKR/KPI book v1.0.
- **Due**: Week 20.

---

## Phase 4 — Operate the OKR/KPI system (ongoing from week 16)

### 4.1 Reporting cadence

- Weekly: product SLO/error-budget reviews; DORA pulses; weeknotes.
- Monthly: scorecard to leadership; programme RAG; equity-gap alert review.
- Quarterly: KR check-ins; portfolio rebalance; tech-radar movement; FinOps + carbon review.
- Annual: outcome review; public report; refresh.
- **DoD**: Calendar invites in place; dashboards published.

### 4.2 Operating dashboards

- One dashboard per Standard: KR burn-up + KPI trend + equity stratification.
- One "Wales Service Standard on a page" rollup.
- **DoD**: Dashboards reviewed by exec; access permissions verified; bilingual labels.

### 4.3 Data quality monitoring

- Automated checks for staleness, completeness, schema drift on every KPI feed.
- **DoD**: Alerts route to named data stewards; <2% stale rate SLO.

### 4.4 Decision logging

- Every quarterly review records: target adjustments, retired KPIs, new KPIs, rationale.
- **DoD**: Decisions visible in a public-by-default log (aligns with Standard 10).

---

## Phase 5 — Per-Standard delivery tasks (concurrent with Phase 4)

### Standard 1 — Welsh well-being

- S1.1 Roll out well-being statement template + LLM-assisted drafting tool.
- S1.2 Publish per-service carbon dashboards (Scope 2 from cloud bills, Scope 3 from suppliers).
- S1.3 Establish outcome-metric review board (rotates quarterly).
- S1.4 Run a "future generations" stress-test on top-5 services per year.

### Standard 2 — Welsh language

- S2.1 Build/adopt a bilingual CMS with parity-quality enforcement.
- S2.2 Stand up LLM translation pipeline with human-in-the-loop QA; publish error-rate weekly.
- S2.3 Welsh-language usability research panel established (recruit + pay).
- S2.4 Welsh-language analytics with active-switch prompts deployed across services.

### Standard 3 — User needs and accessibility

- S3.1 Service-by-service top-task analysis; published top-10 lists.
- S3.2 Accessibility audit programme — automated + manual + AT-user testing partner contracts.
- S3.3 Cross-channel journey mapping pilots (online + phone + in-person).
- S3.4 Plain-language scoring integrated into content authoring.

### Standard 4 — Iteration

- S4.1 DORA-metrics pipeline live for all services.
- S4.2 Engineering enablement programme (CI/CD, test automation, trunk-based development).
- S4.3 Experiment platform stood up; experiment ledger public-by-default.
- S4.4 Release-risk classifier piloted on 3 services.

### Standard 5 — Data and research

- S5.1 Service scorecard template + automation framework.
- S5.2 Research repository programme; insight-of-the-week feed.
- S5.3 PR/ticket template enforces "evidence" field; periodic audit.
- S5.4 Anomaly-detection on KPIs with structured-response runbooks.

### Standard 6 — Ethics, privacy, security

- S6.1 DPIA / threat-model / ethics-review freshness dashboard.
- S6.2 NCSC CAF assessment campaign for top-10 services.
- S6.3 AI assurance lab: red-team + bias-audit + drift-monitor pipeline.
- S6.4 ATRS-equivalent public AI register stood up.
- S6.5 Vulnerability SLA enforcement and reporting.

### Standard 7 — Empowered service owners

- S7.1 Service register single-owner reconciliation.
- S7.2 "Decisions in my gift" letters published per owner.
- S7.3 Annual service-owner empowerment + satisfaction survey.
- S7.4 Service-owner academy programme (onboarding + community of practice).

### Standard 8 — Multidisciplinary teams

- S8.1 Publish MVT specification.
- S8.2 Capability-gap analyser running quarterly; recommendations actioned.
- S8.3 Permanent-staffing pipeline: apprenticeships, graduates, conversions.
- S8.4 Diversity-of-hire programme with hiring-pool targets.
- S8.5 Cross-org team-contract template adopted for multi-organisation services.

### Standard 9 — Scalable technology

- S9.1 Publish v1 Wales-public-sector tech radar; quarterly refresh.
- S9.2 Stack records collected via service register.
- S9.3 API catalogue + OpenAPI/FHIR enforcement for new APIs.
- S9.4 Supplier-concentration review and remediation plan.
- S9.5 Exit-strategy drills for top-5 SaaS / cloud contracts.

### Standard 10 — Work in the open

- S10.1 Weeknote template + LLM co-pilot rolled out.
- S10.2 Open-source publication runbook + legal review fast lane.
- S10.3 Public-roadmap pattern shared across services.
- S10.4 Reuse-finder service indexing Wales public-sector repos.
- S10.5 Quarterly cross-government learning notes launched.

---

## Phase 6 — AI assurance and ethics (cross-cutting)

- A.1 Adopt or extend an existing assurance framework (NHS AI Lab, MHRA SaMD, ATRS pattern).
- A.2 Maintain a public AI register with risk class, owner, evaluation history.
- A.3 Red-team every clinical / decisional-impact model pre-go-live; repeat annually.
- A.4 Bias audits with disaggregated performance reporting (language, decile, age, AT-flag).
- A.5 Human-in-the-loop checkpoints for high-impact AI.
- A.6 Incident response playbook for AI failures (hallucination, drift, prompt injection).
- A.7 Welsh-language performance parity testing for every customer-facing model.

---

## Phase 7 — Communications and engagement

- C.1 "Standard on a page" + simple-language summary, bilingual EN/CY.
- C.2 Public dashboard with selected KPIs (Standard 10 alignment).
- C.3 Quarterly stakeholder bulletin; annual public report.
- C.4 Monthly storytelling feature: one team demonstrating the Standard in practice.
- C.5 Patient/public/citizen panel reviews of major service changes.
- C.6 External engagement at GovCamp / CDPS Conference / NHS-England comms forums to share and learn.

---

## Acceptance checklist (the final gate before "live")

- [ ] Every Standard has 2-3 Objectives, each with 3-5 Key Results.
- [ ] Every KR has at least one KPI with all template fields populated.
- [ ] Every KPI has a baseline measured before a target is committed.
- [ ] Each KPI has an equity disaggregation plan or a documented exemption reason.
- [ ] Each KPI has a named owner, source, and refresh cadence.
- [ ] Each Objective has a guardrail metric to detect gaming or harm.
- [ ] Each AI use case has a benefit case, an assurance class, and a monitoring plan.
- [ ] Welsh-language parity is verified for any user-facing KPI surface.
- [ ] WCAG 2.2 AA verified for any user-facing KPI surface.
- [ ] Methodology and definitions are publicly published, bilingual.
- [ ] An external/independent reviewer has stress-tested the OKR/KPI book.

---

## Open questions to resolve before publishing v1.0

1. Canonical service register location and authority (who has write-access, who arbitrates "in scope").
2. Final list of "well-being statement" minimum-viable contents (and the assessor of quality).
3. Welsh-language CSAT methodology at small sample sizes.
4. NCSC CAF target outcomes for each service tier.
5. ATRS-equivalent register location and publication cadence for Wales.
6. Default open-source licence and legal-review fast lane SLA.
7. Tech-radar ownership model (CDPS central, distributed, vendor-influenced safeguards).
8. £-per-FTE-hour assumption for any productivity benefit-case maths.
9. Equity disaggregation defaults — which dimensions are mandatory vs. optional.
10. How "the Standard as a whole" is graded by an assessor (weighted vs. holistic).
