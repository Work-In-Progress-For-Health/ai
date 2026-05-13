# Plan: SMART OKRs & KPIs with AI Ideas for DHCW Missions

## Purpose

Translate Digital Health and Care Wales (DHCW) Organisational Strategy 2024-2030 missions into SMART OKRs, KPIs, AI-enabled tactics, telemetry, and benchmarks against adjacent organisations (NHS Wales partners, NHS England, NHS Scotland).

## Source

DHCW Organisational Strategy 2024-2030: <https://dhcw.nhs.wales/about-us/key-documents/strategies/organisational-strategy-2024-2030/our-missions/>

- Vision: *"To provide world-leading digital services, empowering people to live healthier lives."*
- Purpose: *"To make digital a force for good in health and care."*
- Five missions, twenty strategic objectives.

## The Five DHCW Missions (summary)

1. **Mission 1 — Platform**: Provide a platform for enabling digital transformation.
2. **Mission 2 — Products**: Deliver high quality digital products and services.
3. **Mission 3 — Records**: Expand the digital health and care record and the use of digital to improve healthcare.
4. **Mission 4 — Innovation**: Drive better value and outcomes through innovation.
5. **Mission 5 — Organisation**: Be a trusted strategic partner and a high quality, inclusive and ambitious organisation.

## SMART criteria recap

- **Specific** — target one area clearly and precisely.
- **Measurable** — quantify progress using metrics.
- **Actionable** — able to start, sustain, complete.
- **Relatable** — relevant, reasonable, connected to context.
- **Timely** — timing is favourable, schedulable, boundable.

## OKR/KPI template

- **Objective**: {do action} {about topic} {for amount} {during timeframe}.
- **Key Result**: {output | outcome | impact}.
- **KPI**: Title · Scope · Owner · Formula · Units · Source · Frequency · Comments.

---

## Mission 1 — Platform: enable digital transformation

> "Provide a platform for enabling digital transformation."

### Strategic context

- Migrate data stores and services to the National Data Resource (NDR).
- Redesign applications with "clean architecture", secure by design, open standards.
- Extend data standards to social care and partners.
- All-Wales data-sharing framework.
- Migrate live services to cloud; decommission data centres.

### OKR examples

**Objective 1.1** — Migrate 100% of in-scope live services to cloud infrastructure by 2030-03-31 so that legacy data centres can be decommissioned.

- **KR 1.1.a**: Move 60% of services to cloud by 2027-03-31, 90% by 2029-03-31, 100% by 2030-03-31.
- **KR 1.1.b**: Reduce on-premise data-centre footprint (rack-units) by ≥80% by 2029-12-31.
- **KR 1.1.c**: Cut infrastructure cost per active user by ≥25% (baseline 2024-04-01) by 2028-03-31.
- **SMART notes**: targets are quantified, time-bound, tied to a published estate baseline.

**Objective 1.2** — Adopt the National Data Resource (NDR) as the single national clinical data repository across all NHS Wales health boards by 2030-03-31.

- **KR 1.2.a**: 7/7 health boards onboarded to NDR for at least one core domain by 2027-03-31.
- **KR 1.2.b**: ≥95% of new clinical data flows ingested via NDR within 6 months of go-live, measured monthly.
- **KR 1.2.c**: Time-to-onboard a new data flow ≤30 working days (median) by 2028-03-31.

**Objective 1.3** — Reduce technical debt across the DHCW estate by 50% (weighted SonarQube-style index) by 2029-03-31.

- **KR 1.3.a**: Inventory and score 100% of in-scope applications by 2026-09-30.
- **KR 1.3.b**: Retire or refactor ≥40 highest-debt components by 2028-12-31.

### KPI examples

| Title | OKR | Scope | Owner | Formula | Units | Source | Frequency | Comments |
|---|---|---|---|---|---|---|---|---|
| Cloud migration completion | 1.1 | All in-scope live services | CTO / Platform Director | Services migrated ÷ total in-scope services × 100 | % | Configuration mgmt DB (CMDB), migration tracker | Monthly | Excludes services scheduled for retirement. |
| Data-centre footprint reduction | 1.1 | Owned/leased racks | Infra Lead | (Baseline RU − current RU) ÷ baseline RU × 100 | % | Facilities asset register | Quarterly | Baseline = 2024-04-01 inventory. |
| NDR ingestion coverage | 1.2 | New clinical data flows | Data Platform Lead | Flows on NDR ÷ total new flows × 100 | % | NDR control plane catalogue | Monthly | Counts flows live ≥30 days. |
| Time-to-onboard a data flow | 1.2 | NDR onboarding requests | Data Platform Lead | Median(days approval → production) | days | NDR onboarding ticketing | Monthly | 90th percentile reported alongside median. |
| Technical-debt index | 1.3 | All in-scope apps | Engineering Director | Σ(weighted_debt_hours) ÷ Σ(LOC) × 1000 | hours / 1k LOC | Static analysis (SonarQube/similar) | Monthly | Weighted by criticality tier. |
| Cyber-incident rate | 1.1, 1.2 | Production platform | CISO | Confirmed incidents ÷ services-in-production | incidents / service / year | SOC tickets | Quarterly | Severity-weighted variant tracked too. |

### AI ideas and tactics

- **AI-assisted code migration**: use Claude/Copilot to draft refactors for clean-architecture conformance; track suggestion acceptance rate.
- **Automated dependency-graph analysis**: LLM agents summarise blast-radius before migration cutovers.
- **Synthetic-traffic test generation**: AI generates regression workloads for migrated services.
- **Cyber posture co-pilot**: LLM watches IaC PRs for misconfig drift against open standards.
- **Cost FinOps assistant**: AI recommends right-sizing actions based on cloud usage telemetry.

### Telemetry and observability

- OpenTelemetry traces/metrics/logs from every migrated service; dashboards by mission KR.
- SLO catalogue per service: availability, latency, error budget; published monthly.
- Migration "burn-up" chart against the 2027/29/30 milestones.
- FinOps dashboard: £ / active user / month, trend vs. baseline.
- Architecture drift detector: nightly job comparing service maps to the target reference architecture.

### Comparisons (adjacent organisations)

- **NHS England**: Federated Data Platform onboarding (provider-level adoption metrics); Frontline Digitisation EPR coverage.
- **NHS Scotland**: National Digital Platform; Digital Front Door cohort rollout (Lanarkshire, Dec 2025) → adoption KPI patterns.
- **Other NHS Wales bodies**: Public Health Wales Digital and Data Strategy; health-board-level digital strategies (e.g., Swansea Bay UHB March 2025).

### Open questions

- What is the exact 2024 baseline for "services in scope" for cloud migration?
- Which clinical data domains land on NDR first, and what is the order of health-board onboarding?
- Who owns the cross-Wales data-sharing framework (DHCW, Welsh Government, partners)?

---

## Mission 2 — Products: deliver high-quality digital products and services

> "Deliver high quality digital products and services."

### Strategic context

- Digital prescribing and medicines management end-to-end by 2030.
- Consolidate core health services into a single all-Wales EHR.
- Consolidate core social services into an EHR.
- Reduce fragmentation in the application estate.
- Benchmark digital maturity using internationally recognised assessments.

### OKR examples

**Objective 2.1** — Enable 100% of NHS Wales prescribing and medicines management to be digital end-to-end by 2030-03-31.

- **KR 2.1.a**: ≥80% of GP-issued prescriptions transmitted electronically to dispensers by 2027-03-31.
- **KR 2.1.b**: ≥95% of secondary-care inpatient medications administered with closed-loop verification by 2029-03-31.
- **KR 2.1.c**: Prescribing-error rate per 1,000 doses reduced by ≥30% versus 2025 baseline by 2029-03-31.

**Objective 2.2** — Move all 7 health boards onto the consolidated all-Wales EHR for core in-scope modules by 2030-03-31.

- **KR 2.2.a**: 3 boards live on the core EHR module by 2027-03-31.
- **KR 2.2.b**: 7 boards live by 2030-03-31; legacy core modules decommissioned within 12 months of go-live.
- **KR 2.2.c**: Reduce count of fragmented core applications by ≥50% by 2028-12-31.

**Objective 2.3** — Reach the top quartile of internationally benchmarked digital-maturity scores by 2029-03-31.

- **KR 2.3.a**: Complete a HIMSS EMRAM-equivalent or DMA assessment for every health board annually from 2026.
- **KR 2.3.b**: Lift the median maturity score by ≥2 stages versus 2025 baseline by 2029-03-31.

### KPI examples

| Title | OKR | Scope | Owner | Formula | Units | Source | Frequency | Comments |
|---|---|---|---|---|---|---|---|---|
| e-Prescription coverage | 2.1 | GP-issued prescriptions | Medicines Programme SRO | e-Rx items ÷ total Rx items × 100 | % | Prescribing data warehouse | Monthly | Excludes controlled-drug exceptions until policy lands. |
| Closed-loop med admin rate | 2.1 | Inpatient med administrations | EHR Product Lead | Verified admins ÷ total admins × 100 | % | EHR audit log | Monthly | Verified = scan-patient + scan-med matched. |
| Prescribing-error rate | 2.1 | All recorded prescribing events | Chief Pharmacist | Errors ÷ doses × 1000 | errors / 1k doses | Datix + EHR | Monthly | Severity grades tracked separately. |
| EHR module go-live count | 2.2 | All-Wales EHR rollout | EHR Programme Director | Cumulative health boards live | count | Programme RAID log | Monthly | Live = ≥80% intended users using daily. |
| Fragmented-app count | 2.2 | Production application portfolio | Apps Portfolio Lead | Count of distinct in-scope apps | count | Application portfolio register | Quarterly | Definition of "core" in scope statement. |
| Digital-maturity stage | 2.3 | All NHS Wales health boards | CCIO + DHCW CDIO | Median EMRAM-equivalent stage | stage 0-7 | HIMSS / DMA assessor | Annual | Compare to UK and international quartiles. |
| User satisfaction (DHCW products) | 2.2, 2.3 | Surveyed product users | Product Director | Mean CSAT 1-5 | score | In-product survey + annual panel | Monthly + annual | Top quartile vs. NHS UK benchmark. |

### AI ideas and tactics

- **LLM clinical-summary**: pre-populate discharge summaries from EHR events; clinician verifies.
- **AI prescription safety net**: real-time interaction/dose checks beyond rules-based; flag rate vs. true-positive rate tracked.
- **Voice-to-EHR (ambient AVT)**: mirror NHS England's AVT push; KPI on minutes saved per clinician per session.
- **Conversational EHR navigation**: clinicians query EHR in natural language; measure time-to-information.
- **AI-driven test generation** for EHR releases to keep regression coverage as scope consolidates.

### Telemetry and observability

- Per-product North-Star metric dashboards (e.g., prescriptions e-transmitted, EHR DAU/WAU).
- Funnel analytics for each EHR workflow (admit → assess → prescribe → discharge).
- Error-budget burndown for product SLOs.
- A/B-test platform for product improvements with statistical guardrails.
- Voice-of-customer pipeline: in-product feedback → product backlog with cycle-time KPI.

### Comparisons

- **NHS England**: Electronic Prescription Service mandated adoption; Frontline Digitisation EPR programme; 95% of appointments via NHS App from April 2026.
- **NHS Scotland**: 35 digital therapeutic treatments across all Health Boards; LIMS 2.0 (Wales) pattern.
- **HIMSS EMRAM**: international benchmark for EHR maturity (compare DHCW vs. NHSE acute trusts in stages 6-7).

### Open questions

- What is the agreed canonical "core EHR module" scope and the per-board sequence?
- Are social-care providers (local authorities) ready to consume the EHR via the all-Wales data-sharing framework?
- Which CSAT/NPS panel methodology is used today (to set a defensible top-quartile target)?

---

## Mission 3 — Records: expand the digital health and care record

> "Expand the digital health and care record and the use of digital to improve healthcare."

### Strategic context

- Single digital health and care record across all settings.
- Lifetime record per person.
- One million NHS Wales App users.
- Top-quartile user satisfaction.

### OKR examples

**Objective 3.1** — Reach 1,000,000 monthly active NHS Wales App users by 2027-03-31.

- **KR 3.1.a**: 500,000 MAU by 2026-03-31.
- **KR 3.1.b**: 800,000 MAU by 2026-12-31.
- **KR 3.1.c**: 1,000,000 MAU sustained for ≥3 consecutive months by 2027-03-31.
- **KR 3.1.d**: D30 retention ≥55% for new sign-ups by 2026-12-31.

**Objective 3.2** — Make a single integrated record available for 100% of Welsh residents who have any NHS Wales contact by 2030-03-31.

- **KR 3.2.a**: Coverage = ≥95% of GP-registered patients by 2028-03-31.
- **KR 3.2.b**: Record contains ≥10 defined data domains (e.g., problems, meds, allergies, results, letters, imaging, immunisations, care plans, social-care contacts, wearable) by 2029-03-31.
- **KR 3.2.c**: Mean staleness of any domain ≤24 hours by 2028-03-31.

**Objective 3.3** — Achieve top-quartile user satisfaction (vs. NHS UK app benchmarks) by 2027-03-31.

- **KR 3.3.a**: App store rating ≥4.5 sustained for ≥6 months.
- **KR 3.3.b**: In-app CSAT ≥4.3/5 (rolling 30 days).

### KPI examples

| Title | OKR | Scope | Owner | Formula | Units | Source | Frequency | Comments |
|---|---|---|---|---|---|---|---|---|
| NHS Wales App MAU | 3.1 | App users in last 30 days | App Product Lead | Distinct users with ≥1 session in 30d | count | App analytics | Daily | Bot/test users excluded. |
| D30 retention | 3.1 | New sign-ups in cohort | App Product Lead | Cohort returning on day 30 ÷ cohort size × 100 | % | App analytics | Cohort weekly | Stratify by age band & LSOA decile. |
| Record coverage | 3.2 | Population of Wales | Record Programme SRO | Persons with non-empty record ÷ resident pop. × 100 | % | NDR person index vs. NHAIS/Demographics | Monthly | Reconcile against Welsh Demographic Service. |
| Domain completeness | 3.2 | Defined record domains | Data Standards Lead | Domains present ≥1 entry ÷ 10 defined × 100 | % | NDR queries | Monthly | Per person, aggregated. |
| Record staleness | 3.2 | Each data domain | Data Platform Lead | Median(time now − last-updated) | hours | NDR audit | Weekly | 90p reported. |
| App CSAT | 3.3 | App users completing prompt | App Product Lead | Mean(rating) | 1-5 | In-app survey | Daily | Compare quarterly with NHS App UK. |
| Digital inclusion gap | 3.1, 3.3 | LSOA decile breakdown | Inclusion Lead | (MAU in decile 1) ÷ (MAU in decile 10) | ratio | App analytics + ONS | Quarterly | Equity guardrail metric. |

### AI ideas and tactics

- **Personalised, plain-language record summary**: LLM renders the patient's record at reading age ≈ 9; track comprehension via micro-quiz.
- **Multilingual support** (English/Welsh + community languages) using LLM translation; QA via clinician-back-translation.
- **Symptom triage assistant** linked to NHS 111 Wales pathways; safety net measured by false-reassurance rate.
- **Wearable integration**: AI normalises heterogeneous wearable signals into common observations; precision/recall against gold-standard devices.
- **Proactive nudges**: AI selects best-channel reminders (push/SMS) and measures uplift over control.

### Telemetry and observability

- App North-Star: weekly active users × actions per active user.
- Inclusion dashboard by age, language, LSOA, condition; alert on widening gaps.
- Record-coverage heatmap by health board and domain.
- Feature-flag analytics so every new capability ships with a measurable hypothesis.

### Comparisons

- **NHS England**: NHS App at >35M registered users (UK); 95% appointments via NHS App from April 2026 — useful adoption-velocity reference.
- **NHS Scotland**: Digital Front Door launching with Lanarkshire cohort December 2025 — cohort-driven rollout pattern.
- **Estonia / Denmark**: international top-quartile record-coverage benchmarks.

### Open questions

- What identity-assurance level is required for new app features (e.g., prescriptions, records)?
- How is "single record" reconciled when patients move across borders (Wales↔England)?
- What is the policy on patient-recorded data (wearables) flowing into the record?

---

## Mission 4 — Innovation: drive better value and outcomes

> "Drive better value and outcomes through innovation."

### Strategic context

- NDR Secure Data Environment (SDE) for research while protecting privacy.
- National information and data-insights service delivering net benefit.
- AI and automation for year-on-year productivity gains across NHS Wales.

### OKR examples

**Objective 4.1** — Stand up an NDR Secure Data Environment serving ≥50 approved research projects per year by 2028-03-31.

- **KR 4.1.a**: SDE in beta with 5 pilot projects by 2026-09-30.
- **KR 4.1.b**: 25 projects per year by 2027-03-31; 50 per year by 2028-03-31.
- **KR 4.1.c**: Time from data-access application to first query ≤30 working days (median) by 2027-03-31.

**Objective 4.2** — Deploy AI and automation initiatives delivering ≥£X million in measured productivity gains per year by 2028-03-31 (X to be set after 2025-26 baseline).

- **KR 4.2.a**: Publish productivity baseline (FTE-hours saved methodology) by 2026-06-30.
- **KR 4.2.b**: ≥10 production AI/automation use cases live by 2027-03-31, each with a measured benefit case.
- **KR 4.2.c**: ≥75% of live AI use cases pass quarterly post-deployment monitoring (accuracy, bias, drift) thresholds.

**Objective 4.3** — Deliver a national data-insights service used by all 7 health boards for management reporting by 2027-03-31.

- **KR 4.3.a**: Core dashboards (RTT, urgent care, workforce, finance) standardised across boards by 2026-12-31.
- **KR 4.3.b**: ≥80% of board execs report using the service weekly (survey) by 2027-03-31.

### KPI examples

| Title | OKR | Scope | Owner | Formula | Units | Source | Frequency | Comments |
|---|---|---|---|---|---|---|---|---|
| SDE active research projects | 4.1 | Approved & live projects | SDE Lead | Count of projects active in period | count | SDE control plane | Quarterly | Active = ≥1 query in 90 days. |
| SDE data-access cycle time | 4.1 | Approved applications | Information Governance Lead | Median(days submission → first query) | days | SDE workflow tool | Monthly | 90p reported. |
| AI use cases in production | 4.2 | Approved deployments | AI Programme Lead | Count of live deployments | count | AI model registry | Monthly | Excludes pilots ≤30 days. |
| Realised productivity (£) | 4.2 | Benefit-cased use cases | CFO / AI PMO | Σ(hours saved × £ rate) − run cost | £ | Benefits tracker | Quarterly | Methodology published openly. |
| Model-monitoring pass rate | 4.2 | Live AI models | AI Assurance Lead | Models meeting thresholds ÷ total × 100 | % | Model-monitoring platform | Monthly | Thresholds: accuracy, drift, fairness. |
| Insights service adoption | 4.3 | Board exec users | Insights Service Lead | Weekly active execs ÷ total exec roles × 100 | % | BI tool telemetry | Weekly | Survey-confirmed annually. |
| Research output | 4.1 | SDE projects | Research Director | Peer-reviewed outputs per year | count | Project registry | Annual | Stratify by impact factor. |

### AI ideas and tactics

- **Ambient documentation** for clinics (mirroring NHSE AVT direction); benefit case: minutes per consult, completeness.
- **Operational AI**: bed-flow prediction, theatre utilisation optimisation, DNA-risk scoring.
- **Coding & billing assistants**: improve SNOMED/ICD coding accuracy.
- **Clinical decision support copilots** (with explainability and human-in-the-loop sign-off).
- **AI assurance lab**: red-team, bias-audit, drift-monitor every model before & after deployment; KPI on assurance turnaround time.
- **SDE LLM workbench**: privacy-preserving RAG over de-identified corpora for researchers; track query patterns.

### Telemetry and observability

- Central model registry with lineage, owner, risk class, last evaluation.
- Continuous evaluation: golden datasets, canary prompts, drift signals.
- Benefits realisation pipeline: hypothesis → instrumentation → measurement → publish.
- Public dashboard of live AI services and their assurance status (transparency).

### Comparisons

- **NHS England**: FDP population-health management; AVT registry.
- **NHS Scotland**: Connect Me remote monitoring; 35 digital therapeutic treatments scaled across boards.
- **Health Data Research UK (HDRUK)**: SDE network; benchmark for project cycle time and outputs.
- **GDS / CDDO** productivity dashboards for public-sector AI use-case patterns.

### Open questions

- What is the £-per-FTE-hour assumption used for benefits maths (and who signs it off)?
- What is the assurance bar before a clinical-facing AI tool goes live?
- How does DHCW publish AI transparency (model cards / public registry)?

---

## Mission 5 — Organisation: trusted strategic partner, high-quality and inclusive

> "Be a trusted strategic partner and a high quality, inclusive and ambitious organisation."

### Strategic context

- Talent and leadership pipelines (academy-style).
- Prioritised programme/project pipeline.
- Long-term financial stability.
- Carbon footprint reduction (≥34% reduction with route to net zero).
- Top-quartile staff and stakeholder engagement.

### OKR examples

**Objective 5.1** — Reach top-quartile staff engagement (NHS staff survey or equivalent) by 2028-03-31.

- **KR 5.1.a**: Annual engagement index ≥75% by 2027-03-31; ≥80% by 2028-03-31.
- **KR 5.1.b**: Voluntary turnover ≤10% sustained for 12 months by 2027-03-31.
- **KR 5.1.c**: ≥90% of staff complete an annual development plan.

**Objective 5.2** — Reduce DHCW operational carbon footprint by ≥34% versus 2024 baseline by 2030-03-31.

- **KR 5.2.a**: Publish baseline + measurement methodology by 2026-03-31.
- **KR 5.2.b**: −15% by 2027-03-31; −25% by 2028-03-31; −34% by 2030-03-31.
- **KR 5.2.c**: Net-zero route map published and reviewed annually from 2026.

**Objective 5.3** — Build a future-skills pipeline so that 100% of priority roles have a named successor by 2028-03-31.

- **KR 5.3.a**: Academy programmes launched in data, software, cyber, AI by 2026-09-30.
- **KR 5.3.b**: ≥80 apprentices/graduates in flight by 2027-03-31.
- **KR 5.3.c**: Internal-fill rate for priority roles ≥50% by 2028-03-31.

### KPI examples

| Title | OKR | Scope | Owner | Formula | Units | Source | Frequency | Comments |
|---|---|---|---|---|---|---|---|---|
| Staff engagement index | 5.1 | All DHCW staff | Director of People | Composite from NHS staff survey items | % | NHS staff survey | Annual | Pulse surveys quarterly. |
| Voluntary turnover | 5.1 | All DHCW staff | HR Lead | Voluntary leavers ÷ avg headcount × 100 | % | HRIS | Monthly | Excludes retirements. |
| Carbon footprint | 5.2 | Scopes 1, 2, 3 (in scope) | Sustainability Lead | tCO2e per year | tCO2e | Energy & cloud bills + Greening Govt method | Quarterly | Cloud Scope 3 via provider tooling. |
| Apprentice / graduate intake | 5.3 | Academy programmes | Academy Lead | Persons enrolled per cycle | count | HRIS | Per intake | Diversity stratification. |
| Internal-fill rate | 5.3 | Priority roles | Talent Lead | Internal hires ÷ priority-role hires × 100 | % | ATS | Quarterly | Definition of "priority role" maintained. |
| Stakeholder NPS | 5.1 | Partners (HBs, Govt, suppliers) | Director of Partnerships | NPS = %promoters − %detractors | NPS | Annual partner survey | Annual | Pulse with key accounts twice yearly. |
| Programme delivery confidence | 5.1 | Tier-1 programmes | PMO Director | RAG-rated programmes Green or Amber ÷ total × 100 | % | PMO RAID | Monthly | Independent assurance every 6 months. |

### AI ideas and tactics

- **AI HR copilot**: drafts JD, screens applications fairly (bias-audited), accelerates time-to-hire.
- **Internal LLM knowledge assistant**: indexes policies, runbooks, architecture; KPI on questions-answered-without-escalation.
- **Procurement & contracts assistant**: surfaces risks, supports SME participation.
- **Carbon-aware scheduling** for compute jobs; track kgCO2e per workload.
- **Programme-health predictor**: LLM reads PMO updates and flags drift before RAG turns red.

### Telemetry and observability

- People dashboard: engagement, turnover, diversity, learning hours per FTE.
- Carbon dashboard: tCO2e by source, trend vs. trajectory.
- Programme dashboard: delivery confidence, dependencies, RAID trends.
- Finance dashboard: unit cost per service, run vs. change ratio.

### Comparisons

- **NHS England Greener NHS** and Greening Government Commitments → Scope 1-3 method.
- **NHS staff survey** national benchmarks → top-quartile thresholds.
- **TechUK / GDS** "Digital, Data and Technology Profession" capability framework → role/skill design.

### Open questions

- What is the 2024 carbon baseline and which scopes are in/out?
- Which engagement survey is canonical (NHS Wales staff survey, internal pulse, both)?
- Are academy programmes co-delivered with universities or stand-alone?

---

## Cross-cutting design choices

### Cadence

- **Annual**: strategy refresh, mission outcome reviews, public report.
- **Quarterly**: KR check-ins; portfolio rebalancing; FinOps and carbon review.
- **Monthly**: KPI scoreboard published to board; programme RAG.
- **Weekly**: SLO/error-budget review per product; experiment results review.

### Governance and assurance

- **OKR owners** per mission (executive sponsor + delivery lead).
- **Definitions of Done** for each KR (signed off before commitment).
- **Independent assurance** every 6 months on Tier-1 programmes.
- **Open by default**: methodology and definitions published; data tables shared with partners.

### Equity and inclusion guardrails

- Track every adoption KPI by deprivation decile, age band, language, and condition group.
- Trigger remediation if any disparity widens by >10% quarter-on-quarter.

### Risk register themes

- Identity assurance and patient safety in app-driven workflows.
- AI assurance, bias, hallucination in clinical contexts.
- Cyber: supply-chain, ransomware, identity, OT.
- Programme dependencies between Missions 1 (platform) and 2 (products).
- Workforce capacity for migration and AI assurance work.

### Tooling shortlist (illustrative)

- OpenTelemetry + Grafana/Prometheus for service observability.
- Power BI / Tableau on top of NDR for management reporting.
- Sonar / Snyk / Trivy for code and supply-chain health.
- Model registry: MLflow / Vertex / Bedrock equivalents.
- Survey/CSAT: Qualtrics or open-source equivalent.

---

## Comparators table (snapshot)

| Theme | DHCW (Wales) | NHS Wales partners | NHS England | NHS Scotland |
|---|---|---|---|---|
| App / Front Door | NHS Wales App → 1M MAU by 2027 | Health-board apps integrating | NHS App, 95% appts via app by April 2026 | Digital Front Door (Lanarkshire cohort Dec 2025) |
| EHR / Records | All-Wales EHR; single record by 2030 | Health-board EHRs consolidating | Frontline Digitisation EPR coverage | National Digital Platform; Digital Health & Care Record |
| Data platform | NDR + SDE | PHW data platforms | Federated Data Platform (FDP) | National Digital Platform |
| AI / Automation | Year-on-year productivity gains | Local AI pilots | AVT registry; FDP AI features | Connect Me; digital therapeutics |
| Skills | Academy programmes | Health-board academies | NHSE Digital Academy | NES Digital Health & Care |
| Sustainability | ≥34% carbon cut by 2030 | Greener NHS Wales | Greener NHS | Climate-emergency targets |

---

## Risks to the OKRs themselves

- Setting targets before baselines exist → publish "baseline-then-target" sequence.
- Over-indexing on output metrics (e.g., MAU) at the expense of outcomes (e.g., health gain).
- Vanity AI deployments without measured benefit → require benefit case + post-deployment evaluation.
- Equity blind spots → require disaggregated reporting on every adoption KPI.

## Next step

See `tasks.md` for the step-by-step plan to produce, validate, publish, and operate these OKRs/KPIs.

---

## Sources

- [DHCW Our Missions](https://dhcw.nhs.wales/about-us/key-documents/strategies/organisational-strategy-2024-2030/our-missions/)
- [DHCW Organisational Strategy 2024-2030](https://dhcw.nhs.wales/about-us/key-documents/strategies/organisational-strategy-2024-2030/)
- [DHCW Strategic Objectives](https://dhcw.nhs.wales/about-us/key-documents/strategies/organisational-strategy-2024-2030/our-strategic-objectives/)
- [DHCW Principles](https://dhcw.nhs.wales/about-us/key-documents/strategies/organisational-strategy-2024-2030/our-principles/)
- [HTN: DHCW strategy in focus](https://htn.co.uk/2024/07/03/digital-health-and-care-wales-organisational-strategy-2024-2030-in-focus/)
- [Digital Health: Wales single national clinical data repository by 2030](https://www.digitalhealth.net/2024/06/wales-sets-out-to-create-a-single-national-clinical-data-repository-by-2030/)
- [GOV.WALES: Digital and data strategy for health and social care in Wales](https://www.gov.wales/digital-and-data-strategy-health-and-social-care-wales-html)
- [NHS England: Digital transformation](https://www.england.nhs.uk/digitaltechnology/)
- [NHS England Digital Maturity Assessment 2024-2025](https://digital.nhs.uk/data-and-information/digital-maturity-assessment-report-2024-and-2025-results)
- [NHS Scotland: Care in the Digital Age delivery plan 2025-2026](https://www.gov.scot/publications/care-digital-age-delivery-plan-2025-2026/)
- [Scotland's Digital Health and Care Strategy](https://www.gov.scot/publications/scotlands-digital-health-care-strategy/)
- [Public Health Wales Digital and Data Strategy](https://phw.nhs.wales/about-us/working-together-for-a-healthier-wales/public-health-wales-digital-and-data-strategy/)
