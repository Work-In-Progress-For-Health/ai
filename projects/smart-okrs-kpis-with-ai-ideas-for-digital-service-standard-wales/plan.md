# Plan: SMART OKRs & KPIs with AI Ideas for the Digital Service Standard for Wales

## Purpose

Translate the Centre for Digital Public Services (CDPS) Digital Service Standard for Wales into SMART OKRs, KPIs, AI-enabled tactics, telemetry, and benchmarks against adjacent organisations (NHS Wales partners, NHS England, NHS Scotland, GDS / GOV.UK).

The Digital Service Standard for Wales is a published set of principles for designing and delivering public services. It is owned by CDPS (now part of the Welsh Government Digital Public Services directorate). Services aim to meet the **Standard as a whole**, assessed via the **Digital Service Standard Review**.

## Source

- Primary: <https://digitalpublicservices.gov.wales/guidance-and-standards/digital-service-standard-wales>
- Welsh Government overview: <https://www.gov.wales/digital-service-standards>
- CDPS Knowledge Hub mirror: <https://cdps-wales.github.io/knowledge-hub/en/service-standard.html>
- First published: 11 March 2022.

## The Standard at a glance

10 points grouped into 3 themes. Teams aim to meet the standard *as a whole*, not point-by-point.

### Theme A — Meeting user needs

1. **Focus on Welsh well-being** — services drive outcomes that benefit users and contribute to the 7 Well-being of Future Generations goals.
2. **Promote the Welsh language** — Welsh speakers are treated equally with English speakers; the language is designed-in, not bolted on.
3. **Understand users and their needs** — user needs drive design; complete user journeys across online, phone, in-person are considered; accessible by default.
4. **Iterate and improve frequently** — incremental, fast-paced development; ship working software to users repeatedly.
5. **Use data and user research to make decisions** — measure performance objectively; supplement with regular user research.
6. **Consider ethics, privacy and security throughout** — protect sensitive information; assess ethical implications at every stage.

### Theme B — Creating good digital teams

7. **Every service needs an empowered service owner** — single accountable owner with authority over business, product, and technical decisions.
8. **Every service needs a multidisciplinary team** — diverse mix of people, expertise, and disciplines; team composition reasoned and resourced.

### Theme C — Using the right technology

9. **Use scalable technology** — simplest appropriate tool; open standards; avoid vendor lock-in; cloud and widely-supported tech.
10. **Work in the open** — communicate decisions and learning in public; share code, patterns, insights.

## SMART criteria recap

- **Specific** — target one area clearly and precisely.
- **Measurable** — quantify progress using metrics.
- **Actionable** — able to start, sustain, complete.
- **Relatable** — relevant, reasonable, connected to context.
- **Timely** — timing is favourable, schedulable, boundable.

## OKR/KPI template

- **Objective**: {do action} {about topic} {for amount} {during timeframe}.
- **Key Result**: {output | outcome | impact}.
- **KPI**: Title · OKR · Scope · Owner · Formula · Units · Source · Frequency · Comments.

---

## Standard 1 — Focus on Welsh well-being

> "Services should drive outcomes that benefit them, not by lists of technical specifications or requirements." Teams must consider the well-being of future generations: social, economic, environmental, cultural.

### Strategic context

- Well-being of Future Generations (Wales) Act 2015 mandates 7 well-being goals (prosperous, resilient, healthier, more equal, cohesive, Welsh-language vibrant, globally responsible).
- Services are expected to articulate how they contribute to one or more goals and avoid harm to others.
- Outcome-based, not output-based.

### OKR examples

**Objective 1.1** — Every in-scope public-facing digital service publishes a measurable well-being contribution statement by 2027-03-31.

- **KR 1.1.a**: 100% of services in the CDPS service catalogue have a published well-being statement mapped to ≥1 of the 7 goals by 2026-12-31.
- **KR 1.1.b**: ≥80% of those statements include at least one quantified outcome metric (not just an output count) by 2027-03-31.
- **KR 1.1.c**: ≥50% of services demonstrate year-on-year improvement on their lead outcome metric by 2028-03-31.

**Objective 1.2** — Reduce average carbon intensity per service transaction by 30% versus 2025 baseline by 2029-03-31.

- **KR 1.2.a**: Publish per-service kgCO2e/transaction baseline by 2026-09-30.
- **KR 1.2.b**: −10% by 2027-03-31; −20% by 2028-03-31; −30% by 2029-03-31.

### KPI examples

| Title | OKR | Scope | Owner | Formula | Units | Source | Frequency | Comments |
|---|---|---|---|---|---|---|---|---|
| Well-being statement coverage | 1.1 | Public-facing digital services | CDPS Standards Lead | Services with statement ÷ catalogue total × 100 | % | Service catalogue | Quarterly | Statement must name ≥1 of 7 goals. |
| Outcome-metric quality | 1.1 | Statements published | Service Owner | Statements with quantified outcome ÷ total × 100 | % | Standards review register | Quarterly | Reviewed by independent assessor. |
| Carbon per transaction | 1.2 | All metered services | Sustainability Lead | tCO2e ÷ completed transactions | kgCO2e / txn | Cloud billing + green-hosting reports | Quarterly | Scope 2 + in-scope Scope 3. |
| Service contribution to inequality reduction | 1.1 | Services with equity hypothesis | Service Owner | Δ(uptake decile-1) − Δ(uptake decile-10) | pp | Service analytics + ONS LSOA | Quarterly | Guardrail; alerts on widening. |

### AI ideas and tactics

- **LLM-assisted well-being statement drafting**: a template-bound LLM helps teams articulate the contribution to the 7 goals and surface trade-offs.
- **Outcome-vs-output classifier**: an LLM reviews KPI definitions and flags those that measure activity rather than outcome.
- **Carbon-aware orchestration**: AI schedules batch workloads in low-carbon-intensity windows; KPI on kgCO2e per workload.
- **Future-generations impact reviewer**: prompt-engineered checklist applied automatically to service design docs.

### Telemetry and observability

- Service catalogue with well-being statement field and outcome-metric link.
- Per-service carbon dashboard (Scope 2 from cloud bills; Scope 3 via supplier data).
- Quarterly outcome-tracker comparing baseline → current per service.
- Public-facing transparency page summarising contribution per goal.

### Comparisons

- **GOV.UK Service Standard** point 1 ("Understand users and their needs") — Wales adds the well-being framing on top.
- **NHS Scotland**: digital strategy framing of digital as a cross-cutting Principle.
- **Greener NHS / Greening Government Commitments**: methodology for Scope 2/3 measurement.

### Open questions

- Which of the 7 well-being goals are mandatory vs. optional mappings per service type?
- Where is the canonical service catalogue and who maintains it?
- Carbon measurement methodology — adopt Greening Government Commitments verbatim?

---

## Standard 2 — Promote the Welsh language

> Services should "promote and facilitate the Welsh language" and treat Welsh speakers equally with English speakers.

### Strategic context

- Welsh Language (Wales) Measure 2011 and Welsh Language Standards apply to most public bodies.
- Cymraeg 2050 target: 1 million Welsh speakers by 2050.
- "Welsh by design" rather than "Welsh by translation after the fact".

### OKR examples

**Objective 2.1** — All in-scope public-facing services offer parity-quality Welsh and English experiences by 2027-12-31.

- **KR 2.1.a**: 100% of new services launch with simultaneous Welsh + English by 2026-09-30.
- **KR 2.1.b**: Backlog of English-only legacy screens cut by ≥70% by 2027-12-31.
- **KR 2.1.c**: Welsh-language user-satisfaction score within ±5 points of English-language score by 2027-12-31.

**Objective 2.2** — Increase Welsh-language usage share across digital services by ≥50% versus 2025 baseline by 2028-03-31.

- **KR 2.2.a**: Welsh-language session share rises from baseline to baseline × 1.25 by 2027-03-31.
- **KR 2.2.b**: Active Welsh-language switching prompts on ≥80% of journeys by 2026-12-31.

### KPI examples

| Title | OKR | Scope | Owner | Formula | Units | Source | Frequency | Comments |
|---|---|---|---|---|---|---|---|---|
| Welsh parity coverage | 2.1 | Service screens & content | Welsh Language Lead | Welsh-available screens ÷ total × 100 | % | Content audit + CMS | Monthly | Excludes archived content. |
| Welsh CSAT parity gap | 2.1 | Surveyed users | Service Owner | CSAT(en) − CSAT(cy) | points | In-product survey | Monthly | Gap >5 triggers remediation. |
| Welsh session share | 2.2 | All sessions | Analytics Lead | Welsh sessions ÷ total × 100 | % | Web/app analytics | Weekly | Stratify by service. |
| Translation freshness | 2.1 | Bilingual content pairs | Content Lead | Pairs updated within 5 working days ÷ total × 100 | % | CMS audit log | Weekly | English-first releases tracked. |
| Welsh-accessible interactions | 2.1 | Form fields, error msgs, comms | Service Owner | Welsh-available ÷ total × 100 | % | Component scan | Quarterly | Includes outbound email/SMS. |

### AI ideas and tactics

- **LLM-assisted translation pipeline**: drafts Welsh content for human editor review; track edit-distance and rejection rate.
- **Welsh-English content consistency checker**: flags drift when one language is updated without the other.
- **Voice-enabled Welsh services**: STT/TTS in Welsh; benchmark error rates against English.
- **Welsh-language UX evaluator**: model trained on Welsh-language design heuristics critiques new screens.
- **Bilingual dataset curation**: build and publish a Welsh public-services corpus to improve future model performance (work-in-the-open dividend).

### Telemetry and observability

- Bilingual coverage scoreboard per service.
- Translation freshness alerts in the CMS.
- Language-switch funnel: how often users switch, where, and why.
- Welsh-language error-rate dashboard (form errors, search no-results in Welsh).

### Comparisons

- **Welsh Government bilingual delivery standards**.
- **Ireland**: Official Languages Act and Irish-language digital obligations.
- **Canada**: Official Languages Act bilingual digital service patterns.

### Open questions

- Which body certifies "parity quality" — CDPS, Welsh Language Commissioner, or internal review?
- What is the agreed methodology for measuring Welsh-language CSAT at small sample sizes?
- Are AI-generated Welsh translations acceptable for production without human review for certain content classes?

---

## Standard 3 — Understand users and their needs

> "User needs should drive service design." Cover complete journeys across online, phone, in-person; accessibility for all.

### Strategic context

- WCAG 2.2 AA is the legal baseline; the Standard expects more than the floor.
- Users include the public *and* internal staff (clinicians, caseworkers).
- "Whole journey" means service boundaries (and channels) are user-defined, not org-chart-defined.

### OKR examples

**Objective 3.1** — Every in-scope service maintains an evidenced user-needs artefact updated at least every 6 months by 2027-03-31.

- **KR 3.1.a**: 100% of services have a documented top-10 user-needs list signed off by a researcher by 2026-09-30.
- **KR 3.1.b**: ≥80% of services have refreshed that list within the last 6 months on rolling check by 2027-03-31.
- **KR 3.1.c**: ≥1 named accessibility test (with assistive-tech users) per service per year by 2027-03-31.

**Objective 3.2** — Reach WCAG 2.2 AA conformance on 100% of public-facing services by 2027-03-31.

- **KR 3.2.a**: Automated WCAG scan coverage = 100% of public services by 2026-06-30.
- **KR 3.2.b**: Manual audit coverage ≥80% per year by 2027-03-31.
- **KR 3.2.c**: Critical/serious accessibility issues closed within 30 days (≥90% of cases).

### KPI examples

| Title | OKR | Scope | Owner | Formula | Units | Source | Frequency | Comments |
|---|---|---|---|---|---|---|---|---|
| User-needs artefact freshness | 3.1 | All in-scope services | Head of User Research | Services refreshed ≤6 months ÷ total × 100 | % | Service register | Monthly | Date-stamped artefact required. |
| Research participants per service per quarter | 3.1 | All in-scope services | Service Owner | Sessions × participants | count | Research repository | Quarterly | Min recommended: 6. |
| WCAG AA conformance | 3.2 | Public-facing services | Accessibility Lead | Pages passing audit ÷ tested × 100 | % | Automated + manual audit | Monthly | Tracks critical/serious separately. |
| Assistive-tech test coverage | 3.2 | All in-scope services | Accessibility Lead | Services tested with AT users in last 12m ÷ total × 100 | % | Research log | Quarterly | Include screen-reader, switch, voice. |
| Top-task completion rate | 3.1 | Defined top tasks | Service Owner | Task completions ÷ task starts × 100 | % | Analytics + research | Monthly | Stratify by user segment. |
| Service equity gap | 3.1 | Adoption by group | Service Owner | (Uptake top decile) ÷ (uptake bottom decile) | ratio | Analytics + ONS | Quarterly | Lower = more equitable. |

### AI ideas and tactics

- **Research synthesis assistant**: clusters interview transcripts and surfaces themes; sample-validated against human coders.
- **Accessibility co-pilot**: LLM-integrated linter that catches WCAG issues in PR.
- **Plain-language scorer**: model rates content for reading age; targets ≈ age 9.
- **Journey mining**: process-mining + LLM to reconstruct cross-channel journeys from telemetry + call-centre transcripts.
- **Synthetic-user testing**: persona-bound LLMs sense-check flows for confusing wording (do not replace real users).

### Telemetry and observability

- Service-level user-research repository with searchable insights.
- Accessibility dashboard: automated scan + manual audit + AT-test calendar.
- Journey analytics across online + phone + in-person where data permits.
- Equity dashboards on every public-facing service.

### Comparisons

- **GOV.UK Service Manual** user research, content design, and accessibility chapters.
- **NHS digital service manual** with health-specific guidance.
- **WAI-ARIA / WCAG 2.2** authoritative source.

### Open questions

- Is there a shared Wales-wide research repository or per-org silos?
- Who funds AT-user testing (often the most expensive form of research)?
- How are non-digital channels measured against the same user-needs artefacts?

---

## Standard 4 — Iterate and improve frequently

> Employ an "incremental, fast-paced development approach" to deliver working solutions to users quickly and repeatedly.

### Strategic context

- Agile delivery culture; small batch sizes; production-first.
- DORA metrics (deployment frequency, lead time, change-fail rate, MTTR) are the de-facto benchmark.
- A precondition for points 3 (user needs) and 5 (data-driven decisions) to be real rather than ceremonial.

### OKR examples

**Objective 4.1** — Every in-scope service reaches DORA "Elite" or "High" performance by 2028-03-31.

- **KR 4.1.a**: Deployment frequency ≥ weekly for ≥80% of services by 2027-03-31.
- **KR 4.1.b**: Lead time for changes ≤7 days (median) for ≥80% of services by 2027-09-30.
- **KR 4.1.c**: Change-failure rate ≤15% for ≥80% of services by 2028-03-31.
- **KR 4.1.d**: MTTR ≤ 24h for ≥80% of services by 2028-03-31.

**Objective 4.2** — Reduce average cycle time from idea-to-production from current baseline to ≤4 weeks (median) by 2027-09-30.

- **KR 4.2.a**: Publish baseline by 2026-06-30.
- **KR 4.2.b**: −25% by 2027-03-31; ≤4 weeks median by 2027-09-30.

### KPI examples

| Title | OKR | Scope | Owner | Formula | Units | Source | Frequency | Comments |
|---|---|---|---|---|---|---|---|---|
| Deployment frequency | 4.1 | All in-scope services | Engineering Lead | Deployments per service per week | freq | CI/CD logs | Weekly | Median across portfolio. |
| Lead time for changes | 4.1 | Merged changes | Engineering Lead | Median(commit → prod) | hours | Git + CI/CD | Weekly | 90p reported. |
| Change-failure rate | 4.1 | Production deployments | Engineering Lead | Failed deployments ÷ total × 100 | % | CI/CD + incident tracker | Monthly | "Failed" defined in runbook. |
| MTTR | 4.1 | Production incidents | SRE / Service Owner | Median(detect → resolve) | hours | Incident tracker | Monthly | Severity 1/2 only. |
| Idea-to-production cycle | 4.2 | Initiatives in flight | Product Lead | Median(idea logged → first user) | days | Product tracker | Quarterly | "First user" = production with ≥1 real user. |
| Live experiments per service | 4.2 | A/B and feature-flag releases | Product Lead | Experiments active in period | count | Experiment platform | Monthly | At least one per quarter target. |

### AI ideas and tactics

- **AI code-review co-pilot**: speeds review without lowering quality; track time-to-first-review and merge defect rate.
- **Test generation**: LLM produces unit/integration tests from changed code; measure coverage delta and false-positive rate.
- **Release-risk classifier**: ML on PR metadata to predict change-fail risk before deploy.
- **Incident-runbook assistant**: LLM walks responder through runbook; KPI on MTTR reduction.
- **Backlog grooming assistant**: clusters tickets, deduplicates, and surfaces priority candidates.

### Telemetry and observability

- DORA dashboard per service and portfolio rollup.
- Flow metrics (WIP, throughput, cycle time) per team.
- Experiment registry with hypothesis, sample size, decision.
- Deployment-pipeline health (build pass rate, flaky-test rate).

### Comparisons

- **GOV.UK** service team norms (weekly+ deploys).
- **NHS England** Digital Maturity Assessment includes development-pace dimensions.
- **DORA / DevOps Research and Assessment** annual State of DevOps benchmarks.
- **Internal**: pilot-for-public-dora-metrics-by-claude-code work in this repo.

### Open questions

- What's the canonical definition of a "deployment" across services (some ship daily, some quarterly)?
- Which services are exempt from weekly deploys for safety reasons (and what is the alternative cadence)?
- How do regulated change controls coexist with elite DORA performance?

---

## Standard 5 — Use data and user research to make decisions

> "Measure how well services are performing" using objective, automated, real-time data where possible, supplemented by regular user research.

### Strategic context

- Standard 5 is the connective tissue: it powers points 1 (well-being outcomes), 3 (user needs), and 4 (iteration).
- Risk: dashboards that nobody acts on; or research that nobody reads.
- "Decisions" should be visibly traceable to data and research.

### OKR examples

**Objective 5.1** — Every in-scope service publishes a performance scorecard with at least 5 metrics (≥1 outcome metric, ≥1 equity metric) by 2027-03-31.

- **KR 5.1.a**: 100% of services have a published scorecard URL by 2026-12-31.
- **KR 5.1.b**: ≥80% of scorecards refresh automatically (no manual upload) by 2027-03-31.
- **KR 5.1.c**: ≥80% of scorecards include a research-insight feed alongside metrics by 2027-09-30.

**Objective 5.2** — Reach a state where ≥90% of in-flight changes cite a data or research signal as motivation by 2028-03-31.

- **KR 5.2.a**: PR/ticket template requires "evidence" field by 2026-06-30.
- **KR 5.2.b**: Sampling audit: ≥70% of audited tickets cite evidence by 2027-03-31; ≥90% by 2028-03-31.

### KPI examples

| Title | OKR | Scope | Owner | Formula | Units | Source | Frequency | Comments |
|---|---|---|---|---|---|---|---|---|
| Scorecard coverage | 5.1 | All in-scope services | Performance Lead | Services with live scorecard ÷ total × 100 | % | Service register | Monthly | Public scorecards preferred. |
| Scorecard automation rate | 5.1 | Live scorecards | Analytics Lead | Auto-refresh ÷ total × 100 | % | BI tool inventory | Quarterly | Manual = brittle, deprioritised. |
| Decision-evidence rate | 5.2 | Sampled changes | PMO | Audited tickets with evidence ÷ audited × 100 | % | Ticket-tracker audit | Quarterly | Sample size ≥ 50 per quarter. |
| Research recency | 5.1 | Services with research | UR Lead | Days since last research activity | days | Research repository | Monthly | Per service. |
| Data quality SLO | 5.1, 5.2 | KPI data feeds | Data Steward | Feeds passing freshness/completeness ÷ total × 100 | % | Data observability tool | Weekly | <2% stale target. |

### AI ideas and tactics

- **LLM scorecard generator**: bootstraps scorecards from service catalogue + telemetry sources, then humans refine.
- **Anomaly-detector**: ML flags KPI excursions and prompts a structured response.
- **Causal-inference helper**: pre-experiment power analysis and post-experiment uplift estimation.
- **Decision-log Q&A**: chat-with-your-decision-log for exec briefings; surfaces what changed and why.
- **Research-insight retrieval**: vectorised research repository; surfaces relevant studies when a team starts a new feature.

### Telemetry and observability

- Service performance scorecards (public where possible).
- Cross-service "data quality SLO" dashboard.
- Research repository with insight-of-the-week feed.
- Experiment ledger: hypotheses tested, results, decisions.

### Comparisons

- **GOV.UK Performance Platform** historical pattern of public scorecards.
- **NHS England** publishes outcomes dashboards on `digital.nhs.uk`.
- **Estonia / Singapore** open-data public-service dashboards.

### Open questions

- Are scorecards public-by-default or internal-by-default?
- Who owns the cross-service data dictionary (so KPIs are comparable)?
- What is the acceptable lag between event and dashboard refresh for each KPI tier?

---

## Standard 6 — Consider ethics, privacy and security throughout

> "Protect sensitive information and keep data secure." Assess ethical implications at every stage.

### Strategic context

- UK GDPR + Data Protection Act 2018; Caldicott principles in health; NHS DSPT.
- Cyber: NCSC Cyber Assessment Framework (CAF); zero-trust direction of travel.
- Ethics: emerging area; algorithmic transparency increasingly expected.
- Risk surface grows with AI adoption (point 5 plus point 6 = AI assurance).

### OKR examples

**Objective 6.1** — Every in-scope service has current DPIA, threat model, and ethics review attached to its service record by 2027-03-31.

- **KR 6.1.a**: 100% of services have a DPIA ≤12 months old by 2026-12-31.
- **KR 6.1.b**: 100% of services have a threat model ≤6 months old or post-major-change by 2027-03-31.
- **KR 6.1.c**: ≥80% of services with AI components have an ethics review by 2027-09-30.

**Objective 6.2** — Reach NCSC CAF "Achieved" against priority outcomes for in-scope services by 2028-03-31.

- **KR 6.2.a**: Baseline CAF assessment for top-10 services by 2026-09-30.
- **KR 6.2.b**: Priority "Partially Achieved" → "Achieved" within 12 months for ≥80% of cases.

**Objective 6.3** — Zero unresolved Critical/High vulnerabilities older than 30 days in production services by 2027-06-30.

- **KR 6.3.a**: SLA on Critical patch ≤7 days, High ≤30 days.
- **KR 6.3.b**: ≥95% adherence by 2027-06-30.

### KPI examples

| Title | OKR | Scope | Owner | Formula | Units | Source | Frequency | Comments |
|---|---|---|---|---|---|---|---|---|
| DPIA coverage | 6.1 | All in-scope services | DPO | Services with current DPIA ÷ total × 100 | % | IG register | Monthly | "Current" = ≤12 months. |
| Threat model freshness | 6.1 | All services | CISO | Services with current threat model ÷ total × 100 | % | Security register | Monthly | Re-do post major change. |
| Ethics review coverage (AI) | 6.1 | Services with AI components | Ethics Lead | Reviewed ÷ total × 100 | % | AI register | Quarterly | Risk-tier-aware. |
| Open Critical/High vulnerabilities | 6.3 | Production services | CISO | Count open > SLA | count | Vuln scanner | Weekly | Target: 0. |
| Incident MTTC | 6.2 | Security incidents | CISO | Median(detect → contain) | hours | SOC tickets | Monthly | Severity-weighted. |
| Privacy complaint volume | 6.1 | All services | DPO | Complaints in period | count | Complaints log | Quarterly | Trend matters more than absolute. |
| Algorithmic transparency record | 6.1 | Production AI use cases | AI Assurance Lead | Models with public record ÷ total × 100 | % | AI register | Quarterly | Aligned to ATRS-equivalent. |

### AI ideas and tactics

- **AI assurance lab**: red-team, bias-audit, drift-monitor every model pre- and post-deploy; KPI on assurance turnaround.
- **Privacy co-pilot**: scans new features for PII handling drift and flags missing DPIA fields.
- **Threat-model generator**: STRIDE-style first-pass from architecture diagrams.
- **Anomaly detection** on identity / access logs for early breach signals.
- **Synthetic data pipeline** for safer dev/test environments.

### Telemetry and observability

- Security dashboard: CAF posture, open vulnerabilities, incident MTTR/MTTC.
- AI register with risk class, last evaluation, monitoring status, owner.
- DPIA / threat-model / ethics-review freshness dashboard.
- SIEM-driven alerts routed by service owner.

### Comparisons

- **NCSC CAF** as the security yardstick.
- **NHS DSPT** for health-context data security.
- **GDS / CDDO Algorithmic Transparency Recording Standard (ATRS)** for AI transparency.
- **EU AI Act** risk-tiering pattern as a cross-border reference.

### Open questions

- Which ethics framework is mandated (NHS AI Lab, MHRA SaMD, local CDPS-defined)?
- Who arbitrates publish-or-not for AI transparency records (especially negative results)?
- How are supply-chain and third-party risks (e.g., LLM API providers) assured?

---

## Standard 7 — Every service needs an empowered service owner

> A single empowered service owner with authority and responsibility over business, product, and technical decisions; accountable for how well the service meets users' needs.

### Strategic context

- Without empowered ownership, the rest of the Standard cannot be delivered consistently.
- "Empowered" implies budget authority, hire/release authority, vendor-decision authority.
- The pattern: one accountable person per service; not a committee.

### OKR examples

**Objective 7.1** — Every in-scope service has a single, named, empowered service owner with documented delegated authorities by 2026-09-30.

- **KR 7.1.a**: 100% of services list a single owner in the service register by 2026-06-30.
- **KR 7.1.b**: 100% of those owners have published "decisions in my gift" letters by 2026-09-30.
- **KR 7.1.c**: ≥90% of service owners agree (annual survey) that they have the authority to do their role.

**Objective 7.2** — Median service-owner tenure ≥18 months at steady state by 2028-03-31.

- **KR 7.2.a**: Capture tenure baseline by 2026-06-30.
- **KR 7.2.b**: Median tenure trends to ≥18 months by 2028-03-31.

### KPI examples

| Title | OKR | Scope | Owner | Formula | Units | Source | Frequency | Comments |
|---|---|---|---|---|---|---|---|---|
| Service ownership coverage | 7.1 | All in-scope services | CDPS Standards Lead | Services with single owner ÷ total × 100 | % | Service register | Monthly | Co-ownership counts as 0. |
| Empowerment index | 7.1 | Service owners | People Lead | Survey: % strongly agree "I can decide X without escalation" | % | Annual survey | Annual | Disaggregate by Y/N decision types. |
| Owner tenure | 7.2 | Service owners | People Lead | Median(months in role) | months | HRIS | Quarterly | Excludes interim/cover. |
| Decision-escalation rate | 7.1 | Sampled decisions | PMO | Decisions escalated above owner ÷ sampled × 100 | % | Decision log | Quarterly | High value = empowerment problem. |
| Service-owner satisfaction | 7.1 | Service owners | People Lead | Mean satisfaction 1-5 | score | Annual survey | Annual | With role, support, mandate. |

### AI ideas and tactics

- **Decision-pattern analyser**: LLM reviews decision-log entries and clusters them to surface where authority is unclear or escalated unnecessarily.
- **Onboarding co-pilot for new service owners**: indexed briefing pack drawn from prior owners' decisions, runbooks, stakeholders.
- **Service-owner workload analyser**: flags overcommitted owners (too many services, too many meetings).
- **Stakeholder-map generator**: from communications metadata (with consent), surfaces who an owner should be talking to.

### Telemetry and observability

- Service register with owner field as a first-class object.
- Decision log per service: what was decided, by whom, when.
- Annual service-owner survey and exit interview corpus.
- Cross-service "owner load" dashboard.

### Comparisons

- **GOV.UK Service Standard** point on service-owner accountability.
- **NHS England SRO model** for digital programmes.
- **Spotify / Amazon "single-threaded leader"** pattern from industry.

### Open questions

- Where do interim service owners sit in the model (especially for cross-org services)?
- Are owners always Welsh-public-sector employees, or can they be contracted in?
- How is service-owner authority reconciled with health-board sovereignty?

---

## Standard 8 — Every service needs a multidisciplinary team

> A diverse mix of people, experience, expertise and disciplines; teams should be able to explain composition changes and future funding needs.

### Strategic context

- The default mix typically includes: product, delivery, user research, content design, interaction design, accessibility, engineering, ops/SRE, data, security.
- Multi-org teams (CDPS + health board + supplier) are normal — need clear team contracts.
- Risk: rotating contractors hollow out institutional memory.

### OKR examples

**Objective 8.1** — Every in-scope service team meets the agreed "minimum viable team" composition standard by 2027-03-31.

- **KR 8.1.a**: Publish the MVT spec (roles, ratios, FTE minima) by 2026-06-30.
- **KR 8.1.b**: ≥80% of services pass MVT review by 2027-03-31.

**Objective 8.2** — Move from contractor-majority to permanent-majority composition in digital teams by 2028-03-31.

- **KR 8.2.a**: Permanent FTE share ≥60% by 2027-03-31; ≥70% by 2028-03-31.
- **KR 8.2.b**: ≥80% of services have a documented hand-back plan for contractor roles.

**Objective 8.3** — Diversity in digital teams reaches or exceeds Welsh public-sector benchmark across recruited roles by 2028-03-31.

- **KR 8.3.a**: Baseline diversity report by 2026-09-30.
- **KR 8.3.b**: Hiring-pool diversity targets met for ≥90% of campaigns by 2028-03-31.

### KPI examples

| Title | OKR | Scope | Owner | Formula | Units | Source | Frequency | Comments |
|---|---|---|---|---|---|---|---|---|
| MVT compliance | 8.1 | All in-scope services | Capability Lead | Services passing MVT review ÷ total × 100 | % | Capability register | Quarterly | Review every 6 months. |
| Permanent-staff share | 8.2 | Digital team roles | Workforce Lead | Perm FTE ÷ total FTE × 100 | % | HRIS + contractor register | Monthly | Excludes specialist temp roles. |
| Discipline coverage | 8.1 | All in-scope services | Capability Lead | Disciplines present ÷ required × 100 | % | Capability register | Quarterly | Per service. |
| Team-tenure stability | 8.2 | Digital team members | People Lead | Median(months in current team) | months | HRIS | Quarterly | Anti-churn indicator. |
| Diversity representation | 8.3 | New hires | DEI Lead | Group representation vs. Wales benchmark | pp | Recruitment data | Quarterly | Multiple dimensions tracked. |
| Time-to-fill priority roles | 8.1 | Open priority roles | Recruitment Lead | Median(open → hire) | days | ATS | Monthly | <60 days target. |

### AI ideas and tactics

- **Capability-gap analyser**: LLM reviews service plans + team composition and recommends additions.
- **Inclusive job-description writer**: with debias prompts and accessibility-language scoring; track candidate diversity uplift.
- **Skills graph**: model staff skills and surface successors for priority roles.
- **Multi-org collaboration assistant**: drafts team contracts and clarifies decision rights across organisations.

### Telemetry and observability

- Team-composition dashboard per service vs. MVT.
- Workforce-mix dashboard: perm/contract/secondment.
- Skills-graph view: coverage, redundancy, single-points-of-failure.
- Diversity-of-hire dashboard with hiring-pool comparator.

### Comparisons

- **GDS DDaT capability framework** for role design.
- **NHS Digital Academy** for skills uplift patterns.
- **GOV.UK Spend Controls** model that pushes back on contractor-heavy proposals.

### Open questions

- What is the "minimum viable team" definition for very small services?
- How are cross-org teams legally structured (lead employer, secondment, joint controllers)?
- Where does the line sit between empowered owner (S7) and a true team (S8) on decisions?

---

## Standard 9 — Use scalable technology

> Simplest, most appropriate tool; open standards; avoid vendor lock-in; cloud-based; widely supported.

### Strategic context

- Tech radar approach: adopt, trial, assess, hold.
- Cloud-by-default with exit-strategy hygiene.
- Open standards: identifiers (NHS number, UPRN), data exchange (FHIR, OpenAPI), accessibility (WCAG).
- "Scalable" includes social and economic scalability — can the next team also use the choice?

### OKR examples

**Objective 9.1** — Every in-scope service publishes a tech stack record aligned to the Wales public-sector tech radar by 2027-03-31.

- **KR 9.1.a**: Tech radar published v1 by 2026-06-30 with quarterly cadence.
- **KR 9.1.b**: 100% of services have a stack record by 2026-12-31.
- **KR 9.1.c**: ≥80% of services align to "Adopt"/"Trial" tier with documented exemption process by 2027-03-31.

**Objective 9.2** — Reduce single-supplier concentration risk: no single supplier in >30% of critical services by 2028-03-31.

- **KR 9.2.a**: Concentration baseline by 2026-06-30.
- **KR 9.2.b**: Top supplier share ≤40% by 2027-03-31; ≤30% by 2028-03-31.

**Objective 9.3** — All new APIs ship with OpenAPI specs and FHIR-where-applicable by 2026-12-31.

- **KR 9.3.a**: 100% of new public APIs published in the API catalogue by 2026-12-31.
- **KR 9.3.b**: ≥80% of in-flight APIs retrofitted with OpenAPI by 2027-12-31.

### KPI examples

| Title | OKR | Scope | Owner | Formula | Units | Source | Frequency | Comments |
|---|---|---|---|---|---|---|---|---|
| Tech-radar alignment | 9.1 | All in-scope services | CTO | Components in Adopt/Trial ÷ total × 100 | % | Stack records | Quarterly | Exemptions documented. |
| Supplier concentration | 9.2 | Critical services | Procurement Lead | Top supplier services ÷ total × 100 | % | Contracts register | Quarterly | Top-3 share also tracked. |
| API catalogue coverage | 9.3 | Production APIs | API Platform Lead | Cataloged APIs ÷ total × 100 | % | API catalogue | Monthly | Public-discoverable counts double. |
| Open-standard adoption | 9.3 | Data interfaces | Data Platform Lead | Interfaces using open standards ÷ total × 100 | % | Interface register | Quarterly | FHIR, OpenAPI, OIDC, etc. |
| Exit-strategy readiness | 9.2 | Major SaaS / cloud contracts | Procurement Lead | Contracts with tested exit plan ÷ total × 100 | % | Contracts register | Annually | "Tested" requires drill. |
| Cloud unit cost | 9.1 | Cloud-hosted services | FinOps Lead | Cloud £ ÷ active users | £ / user / month | Cloud billing | Monthly | FinOps target curves. |

### AI ideas and tactics

- **Tech-radar curator**: LLM ingests vendor docs, security advisories, community signals to propose radar moves; humans decide.
- **Lock-in detector**: model scans IaC for proprietary primitives and suggests open-standard alternatives.
- **Spec-from-code**: auto-generate OpenAPI specs from running services and reconcile with hand-written specs.
- **Right-sizing assistant**: cost+performance recommendations from observability traces.
- **Exit-plan stress-tester**: AI runs tabletop "lose this supplier" exercises against the runbook.

### Telemetry and observability

- Tech-radar live page with movement history.
- Supplier concentration dashboard.
- API catalogue with usage metrics and deprecation status.
- FinOps dashboards: unit cost, idle resource, anomaly alerts.
- Architecture-drift detector: nightly comparison vs. target reference.

### Comparisons

- **GOV.UK Technology Code of Practice**.
- **NHS England API and Standards Strategy**, FHIR UK Core.
- **ThoughtWorks Technology Radar** as a public model.

### Open questions

- Who owns the Wales-public-sector tech radar (CDPS, Welsh Govt CIO, distributed)?
- What is the canonical identifier hierarchy (NHS number, UPRN, etc.) for cross-service work?
- How do we count "exit-readiness" — desk plan vs. tested drill?

---

## Standard 10 — Work in the open

> Communicate decisions and learning in public; share code, patterns, and insights.

### Strategic context

- Public-by-default is hard for traditional public-sector culture; high payback over time.
- Forms include: open source repos, weeknotes, public roadmaps, public decision records, conference talks.
- "Open" includes within-Wales (cross-team) as well as outwardly public.

### OKR examples

**Objective 10.1** — Every in-scope service maintains a public-facing "show-the-thing" presence (e.g., weeknotes, blog, repo readme, public roadmap) by 2027-03-31.

- **KR 10.1.a**: ≥80% of services publish weeknotes or equivalent at least monthly by 2026-12-31.
- **KR 10.1.b**: 100% of services have a public roadmap page by 2027-03-31.

**Objective 10.2** — Reach 50% of in-scope production code released under an open-source licence (where lawful) by 2028-03-31.

- **KR 10.2.a**: Open-source policy and approval pipeline published by 2026-06-30.
- **KR 10.2.b**: ≥20% of code open-sourced by 2027-03-31; ≥50% by 2028-03-31.

**Objective 10.3** — Publish quarterly cross-government learning notes summarising what worked and didn't by 2027-03-31.

- **KR 10.3.a**: Format and channel agreed by 2026-06-30.
- **KR 10.3.b**: ≥4 issues published per year from 2027.

### KPI examples

| Title | OKR | Scope | Owner | Formula | Units | Source | Frequency | Comments |
|---|---|---|---|---|---|---|---|---|
| Weeknote cadence | 10.1 | All in-scope services | Communications Lead | Services with weeknote in last 30d ÷ total × 100 | % | Blog/wiki audit | Monthly | Min frequency = monthly. |
| Public roadmap coverage | 10.1 | All in-scope services | Service Owner | Services with public roadmap ÷ total × 100 | % | Audit | Quarterly | Includes link from service page. |
| Open-source code share | 10.2 | In-scope repositories | Engineering Lead | OSS-licensed repos ÷ total ÷ 100 | % | Repo register | Quarterly | Excludes legitimate exemptions. |
| External-engagement reach | 10.3 | Talks, blogs, posts | Communications Lead | Audience-reach estimate | count | Comms register | Quarterly | With link list. |
| Reuse rate | 10.2 | Reusable patterns/components | Architecture Lead | Services consuming reusable component ÷ candidates × 100 | % | Component registry | Quarterly | Headline reuse indicator. |
| Time-to-public-decision | 10.1 | Major service decisions | Service Owner | Median(decision → public note) | days | Decision log | Quarterly | Target ≤14 days. |

### AI ideas and tactics

- **Weeknote co-pilot**: drafts a weeknote from tickets + commits + decision-log entries.
- **Sanitisation assistant**: flags PII/security content before publication.
- **Reuse-finder**: LLM searches across all Wales public repos for prior implementations of a need.
- **Translation pipeline** for Welsh-language versions of weeknotes/blogs.
- **Engagement-analytics summariser**: turns public-facing analytics into narrative for retrospectives.

### Telemetry and observability

- Public publication calendar across services.
- Open-source repo dashboard with licence, last-commit, contributors.
- Reuse dashboard: who's using whose components.
- External engagement counts (talks, posts, citations).

### Comparisons

- **GDS / GOV.UK blogs** as a long-running pattern.
- **CDPS Knowledge Hub** as a Welsh exemplar.
- **NHS digital service manual** is itself a "work in the open" artefact.
- **18F (USA), Service Innovation Lab (NZ)** as international references.

### Open questions

- What's the default licence (MIT? Apache 2.0? OGL?) for open-sourced code?
- Who handles legal review for first-time-public artefacts (especially around third-party content)?
- How is "work in the open" balanced against security-by-obscurity arguments?

---

## Cross-cutting design choices

### Cadence

- **Annual**: standard refresh and public report; OKR re-baseline.
- **Quarterly**: KR check-ins; tech-radar movement; equity-gap review.
- **Monthly**: scorecards to leadership; programme RAG.
- **Weekly**: DORA review; product SLO/error-budget review; weeknotes.

### Governance and assurance

- A single accountable owner per Standard within CDPS / Welsh Government Digital Public Services.
- Independent "Digital Service Standard Review" for any service before launch and at major milestones.
- Public reporting of assessment outcomes (positive and not-yet-meeting), aligned with Standard 10.

### Equity and inclusion guardrails

- Disaggregate every adoption KPI by language (cy/en/other), deprivation decile, age band, accessibility-needs flag where collected.
- Trigger remediation if any disparity widens by >10% quarter-on-quarter (mirror DHCW pattern).

### Risk register themes

- Centralisation drift: standards co-opted into top-down control, killing iteration.
- Bilingual fatigue: Welsh-language work treated as a cost rather than a feature.
- AI-assurance debt: model proliferation outpacing assurance capacity.
- Open-source paralysis: legal review queues blocking publication.
- Tech-radar capture: vendor influence skews "Adopt"/"Hold" decisions.

### Tooling shortlist (illustrative)

- Service register + scorecards: Backstage or equivalent.
- Observability: OpenTelemetry + Grafana/Prometheus.
- Accessibility: axe + manual audits + AT-user testing partner.
- Welsh-language QA: bilingual CMS + LLM-assisted translation review.
- AI assurance: model registry (MLflow/Vertex/Bedrock) + monitoring + ATRS-equivalent register.
- Open source: GitHub org with publication runbook.

---

## Comparators table (snapshot)

| Theme | Wales (DSSW) | NHS Wales partners | NHS England | NHS Scotland | GDS / GOV.UK |
|---|---|---|---|---|---|
| Standard points | 10 across 3 themes | Aligned via CDPS | 14 GOV.UK + 3 NHS = 17 | Scottish Digital Service Standard (22 principles) | 14 points |
| User research focus | Standard 3 | Same | NHS Service Manual | Same | GOV.UK Service Manual |
| Welsh language | Standard 2 (unique) | Inherits | n/a | Gaelic obligations | n/a |
| Well-being framing | Standard 1 (unique) | Inherits | Sustainability principle | Net-zero alignment | GovTech sustainability |
| Open source default | Standard 10 | Aligned | NHS App OS components | OS-where-possible | GOV.UK published OS |
| Assessment | DSS Review | DSS Review | Service Assessment | Standard Review | Service Assessment |

---

## Risks to the OKRs themselves

- Setting targets before baselines exist → publish "baseline-then-target" sequence.
- Counting documents (DPIAs, statements) instead of measuring outcomes — pair every coverage KPI with an outcome KPI.
- Welsh-language CSAT having small samples that swing results — define minimum-sample rules.
- Open-source share rising while reuse falls (publishing without uptake) → keep both metrics paired.
- DORA targets driving unsafe deploys in regulated services → pair with change-failure-rate and incident metrics.

## Next step

See `tasks.md` for the step-by-step plan to produce, validate, publish, and operate these OKRs/KPIs.

---

## Sources

- [Digital Service Standard for Wales (CDPS / Digital Public Services Wales)](https://digitalpublicservices.gov.wales/guidance-and-standards/digital-service-standard-wales)
- [Welsh Government: Digital Service Standards](https://www.gov.wales/digital-service-standards)
- [CDPS Knowledge Hub — Service Standard](https://cdps-wales.github.io/knowledge-hub/en/service-standard.html)
- [Digital Service Standards for Wales — our next iteration](https://digitalpublicservices.gov.wales/digital-service-standards-for-wales-our-next-iteration/)
- [Embedding standards and guidance (CDPS 2022-2023 review)](https://digitalpublicservices.gov.wales/looking-back-cdps-year-review-2022-2023/4-embedding-standards-and-guidance)
- [Welsh journey towards Digital Service Standards (2003-2023)](https://medium.com/user-centered-design-ucd-in-healthcare-in-wales/welsh-journey-towards-digital-service-standards-2003-2023-a0d63817660f)
- [NHS service standard](https://service-manual.nhs.uk/standards-and-technology/service-standard)
- [About the NHS service standard](https://service-manual.nhs.uk/standards-and-technology/about-the-service-standard)
- [NHS digital service manual — Design principles](https://service-manual.nhs.uk/design-system/design-principles)
- [Scotland — Care in the Digital Age delivery plan 2025-2026](https://www.gov.scot/publications/care-digital-age-delivery-plan-2025-2026/)
- [GOV.UK Service Standard](https://www.gov.uk/service-manual/service-standard)
- [Well-being of Future Generations (Wales) Act 2015](https://www.futuregenerations.wales/about-us/future-generations-act/)
- [Welsh Language Standards](https://www.welshlanguagecommissioner.wales/welsh-language-standards)
- [WCAG 2.2](https://www.w3.org/TR/WCAG22/)
- [NCSC Cyber Assessment Framework](https://www.ncsc.gov.uk/collection/cyber-assessment-framework)
- [DORA — DevOps Research and Assessment](https://dora.dev/)
