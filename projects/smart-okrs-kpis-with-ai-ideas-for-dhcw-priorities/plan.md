# Plan: SMART OKRs & KPIs + AI Ideas for DHCW Priorities

## 1. Purpose & Scope

Research Digital Health and Care Wales (DHCW) priorities (as published on the "What our priorities are and how we are doing" publication-scheme page and the 2024-2030 Organisational Strategy) and produce worked examples of how to express each priority as **SMART** **OKRs** with concrete **KPIs**. Compare with adjacent organisations (NHS Wales, NHS England, NHS Scotland) and propose AI-enabled tactics, metrics, telemetry and observability.

- Primary working directory: this folder.
- Outputs: this `plan.md`, plus `tasks.md` for the step-by-step delivery breakdown.
- Today's date: 2026-05-13.
- Audience: DHCW leadership, programme managers, digital service teams.

## 2. SMART / OKR / KPI Framework (Recap)

- **SMART**: Specific, Measurable, Actionable, Relatable, Timely.
- **OKR**:
  - **Objective** = `{do action} {about topic} {for amount} {during timeframe}`.
  - **Key Result** = `{output, outcome, impact}`; quantified, time-bounded.
- **KPI** = exact title, owner, formula, units, source, frequency, scope, comments.

Every OKR/KPI below uses this template. Where data sources are aspirational (i.e. don't yet exist), the KPI's "Source" field names the system/dataset DHCW would need to instrument.

## 3. DHCW Priority Landscape (2026)

Per the publication-scheme page, DHCW's priorities are set in three documents — **Annual Business Plan / Commissioning**, **Strategic Direction**, **Targets, Aims and Objectives** — and progress is reported via the **Annual Report**, **Quality & Safety Reports**, **Annual Quality Statement**, **Annual Governance Statement**, plus **Performance vs. Targets / KPI** packs.

The current operational frame is the **DHCW IMTP** (accepted by Welsh Government in August 2025 as 'satisfactory'). DHCW reports against **20 strategic objectives via a balanced scorecard and KPIs**. As of February 2025, **DHCW was at escalation level 3** for performance and outcomes of its major programmes — the first time DHCW has been escalated. This is the load-bearing context: the SMART OKRs below must visibly move escalation level down and rebuild stakeholder confidence.

### 3.1 The five DHCW missions (Strategy 2024-2030)

1. **M1 — Platform for digital transformation**: enable transformation capability across the health and care system.
2. **M2 — High-quality digital products & services**: deliver modern, secure, reliable digital products.
3. **M3 — Expand the digital health and care record**: a single, lifetime, all-Wales record across all settings.
4. **M4 — Innovation for better value and outcomes**: AI, automation, research, data insight at scale.
5. **M5 — Trusted strategic partner / high-quality inclusive ambitious organisation**: financial sustainability, engagement, net zero.

### 3.2 The three core programmes

- **National Data Resource (NDR)** — secure data environment, single national clinical data repository.
- **Digital Services for Patients and Public (DSPP)** — anchored by the NHS Wales App.
- **Digital Medicines** — end-to-end digitally enabled prescribing and medicines management by 2030.

### 3.3 Cross-cutting / mandated priorities (IMTP 2025-2026)

- National current/future target **enterprise architecture**.
- **NHS Wales App** delivery (DSPP).
- **Connecting Care** (interoperability).
- **Data architecture**, NDR, **Data Standards**.
- **Diagnostics** programmes.
- **Primary care** services.

## 4. Comparison with Adjacent Organisations

| Theme | DHCW (Wales) | NHS Wales (system) | NHS England | NHS Scotland |
|---|---|---|---|---|
| Top-level frame | 5 missions + 3 programmes (2024-2030) | 5 Strategic Priorities + Quadruple Aim ("A Healthier Wales") | "2025/26 Priorities & Operational Planning Guidance" | "Care in the Digital Age: delivery plan 2025-2026" |
| Patient app | NHS Wales App (target >1m users) | n/a (delivered by DHCW) | NHS App (mature, target 85% adult adoption) | Digital Front Door MVP (Lanarkshire Dec 2025) |
| Data platform | National Data Resource (NDR) | n/a | Federated Data Platform — FDP to 85% of secondary care trusts by Mar-2026 | National Digital Platform (NDP) — Data Storage Service live |
| Records | Single all-Wales lifetime record by 2030 | Quadruple Aim outcome measures | Shared Care Record (per ICS) | Digital Health & Care Record (Phase 1) |
| Access targets | DHCW enables; HBs deliver | RTT, cancer 62-day, MH access | 18-week RTT to 65% by Mar-2026; A&E 4hr ≥78%; Cancer 62d 75% / FDS 80% | Connect Me 113k users, 50% of GP practices |
| Productivity / AI | "Year-on-year productivity improvements via AI & automation" | Mapped to Quadruple Aim | 4% productivity improvement, ≥1% cost reduction | Digital Innovation strand of NHS Recovery Plan 2021-26 |
| Net zero | ≥34% carbon reduction by 2030 | NHS Wales decarb plan | Greener NHS targets | Climate emergency / NHS Scotland net zero |

**What we can learn / steal:**

- **From NHS England**: numeric, time-bounded percentage targets (e.g. "85% of trusts on FDP by March 2026", "4% productivity"). DHCW's wording today tends to be qualitative — adopting hard numbers improves the "Measurable" and "Timely" SMART axes.
- **From NHS Scotland**: a publicly-staged MVP/limited cohort rollout pattern (Digital Front Door → Lanarkshire pilot → national). This pattern reduces escalation risk and is directly transferable to NHS Wales App feature rollouts.
- **From NHS Wales Performance Framework**: explicit mapping of each KPI to the Quadruple Aim. DHCW should do the same — every KPI maps to one of the 5 missions AND one of the Quadruple-Aim outcomes.
- **From all three**: balanced-scorecard discipline (DHCW has it; the comparators show what "good" reporting cadence looks like).

## 5. SMART OKR / KPI Worked Examples — by Mission

The examples below are illustrative templates. Each one follows the AGENTS.md schema literally.

### Mission 1 — Platform for digital transformation

**Objective M1.O1**: *Establish a target enterprise architecture for NHS Wales for the 8 highest-priority data domains during FY 2026-2027.*

- KPI: M1.O1.KPI1 below.
- SMART: **S** = target architecture only (not current-state survey); **M** = % of priority domains with signed-off TO-BE diagrams; **A** = architecture team owns and runs governance board; **R** = unblocks NDR, DSPP, Digital Medicines; **T** = by 31-Mar-2027.

**Key Results**

- KR1: 8/8 priority data domains have a Welsh-Government-endorsed target architecture by Q4 FY26/27.
- KR2: ≥80% of new DHCW solution designs reference the target architecture in their design review by Mar-2027.
- KR3: Reduce duplicated platform spend identified by architecture review by ≥£2m annualised.

**KPIs**

- **M1.O1.KPI1 — Target architecture coverage**
  - OKR: M1.O1 / KR1.
  - Scope: NDR, Connecting Care, DSPP, Digital Medicines, Diagnostics, Primary Care, identity, integration. Excludes corporate IT.
  - Owner: Chief Architect, DHCW.
  - Formula: `(domains with endorsed TO-BE architecture) / (8 priority domains) × 100`.
  - Units: %.
  - Source: Architecture Review Board minutes; architecture repository (e.g. Sparx EA / Confluence).
  - Frequency: Monthly.
  - Comments: "Endorsed" = signed by SRO + WG digital lead.

- **M1.O1.KPI2 — Design-review conformance rate**
  - OKR: M1.O1 / KR2.
  - Scope: All new solution designs going through Technical Design Authority (TDA).
  - Owner: Head of TDA.
  - Formula: `(TDA submissions citing target arch ref) / (total TDA submissions) × 100`.
  - Units: %.
  - Source: TDA submissions log.
  - Frequency: Monthly.

### Mission 2 — High-quality digital products & services

**Objective M2.O1**: *Improve reliability of DHCW's top-10 clinical services to "four nines" availability during 2026-2027.*

- SMART: **S** = top-10 clinical services only; **M** = availability % and Sev-1 count; **A** = SRE/platform team; **R** = directly reduces escalation-level-3 risk; **T** = by end FY26/27.

**Key Results**

- KR1: Each top-10 service hits ≥99.9% monthly availability for 6 consecutive months by Mar-2027.
- KR2: Reduce Sev-1 incidents per quarter from baseline (set Q1 FY26/27) by ≥50% by Q4 FY26/27.
- KR3: 100% of top-10 services have a published, tested DR runbook executed within the last 12 months.

**KPIs**

- **M2.O1.KPI1 — Service availability (top-10)**
  - OKR: M2.O1 / KR1.
  - Scope: Welsh Clinical Portal, WCRS, WLIMS, WRRS, WPAS-equivalents, NHS Wales App backend, NDR query API, Choose Pharmacy, MyHealthOnline, Digital Medicines Transfer.
  - Owner: Director of Operations.
  - Formula: `1 − (unplanned downtime mins / total mins in month)`, expressed as %.
  - Units: %, monthly.
  - Source: Synthetic + RUM telemetry (Dynatrace / Grafana / Prometheus).
  - Frequency: Monthly published; real-time alerting.

- **M2.O1.KPI2 — Sev-1 incident rate**
  - OKR: M2.O1 / KR2.
  - Scope: Major Incident Process Sev-1 in top-10.
  - Owner: Head of Service Management.
  - Formula: Count of Sev-1s per quarter.
  - Units: incidents/quarter.
  - Source: ITSM (ServiceNow / equivalent).
  - Frequency: Weekly review; quarterly board report.

- **M2.O1.KPI3 — Mean time to recovery (MTTR)**
  - Formula: median minutes from Sev-1 declared to service restored.
  - Source: incident timeline tooling.
  - Frequency: monthly.

### Mission 3 — Expand the digital health and care record

**Objective M3.O1**: *Take the NHS Wales App from current adoption to 1,000,000 monthly active users by 31-Mar-2028 (interim ≥600,000 by Mar-2027).*

- SMART: **S** = MAU specifically (not registrations); **M** = MAU count + feature breadth; **A** = DSPP programme; **R** = headline mission target; **T** = staged.

**Key Results**

- KR1: ≥600,000 MAU by 31-Mar-2027; ≥1,000,000 MAU by 31-Mar-2028.
- KR2: ≥5 high-value transactional features live (e.g. view record, repeat prescriptions, appointment booking, results, referrals) by Mar-2027.
- KR3: System Usability Scale (SUS) score ≥75 for the App by Mar-2027.

**KPIs**

- **M3.O1.KPI1 — NHS Wales App MAU**
  - OKR: M3.O1 / KR1.
  - Scope: Authenticated users with ≥1 session in trailing 30 days.
  - Owner: SRO, DSPP.
  - Formula: `distinct user_ids with session in trailing 30d`.
  - Units: users (integer).
  - Source: App analytics pipeline (e.g. Snowplow / Mixpanel) into NDR.
  - Frequency: Daily refresh, monthly publish.

- **M3.O1.KPI2 — Feature transactional adoption**
  - Formula: `transactions per feature / eligible-user base / month`, per feature.
  - Frequency: monthly.

- **M3.O1.KPI3 — Digital inclusion (assisted-digital coverage)**
  - Formula: % of LSOAs in lowest-WIMD-quintile with at least one assisted-digital partner.
  - Source: Digital Communities Wales partner registry + WIMD.
  - Frequency: quarterly.
  - Comments: Equity guardrail — prevents MAU growth from skewing to already-online populations.

**Objective M3.O2**: *Deliver Phase 1 of a single, lifetime, all-Wales digital health and care record covering ≥3 care settings by 31-Mar-2028.*

- KRs: care settings live (target 3 of 7); % of population with a unified record view; clinician satisfaction score ≥75; data quality ≥98% conformant to FHIR Wales profile.

### Mission 4 — Innovation for better value and outcomes

**Objective M4.O1**: *Deploy AI and automation across DHCW operations to deliver a measurable 4% productivity uplift by 31-Mar-2027.*

- SMART: **S** = operational productivity (defined hours saved or throughput per FTE); **M** = uplift %; **A** = AI Office stood up; **R** = mirrors NHS England 4% productivity ambition; **T** = end FY26/27.

**Key Results**

- KR1: ≥10 AI/automation use-cases in production with audited benefit cases by Mar-2027.
- KR2: Cumulative ≥40,000 hours of clinical/administrative time released across NHS Wales by Mar-2027.
- KR3: NDR Secure Data Environment (SDE) live with ≥5 active accredited research projects by Mar-2027.

**KPIs**

- **M4.O1.KPI1 — AI use-cases in production with audited benefit**
  - OKR: M4.O1 / KR1.
  - Scope: Use-cases past TRL-8, with post-deployment benefit review signed by Finance.
  - Owner: Director of Innovation.
  - Formula: count.
  - Units: use-cases.
  - Source: AI use-case register (DHCW Innovation).
  - Frequency: quarterly.
  - Comments: Each entry must have hours-released, error-rate-change, and equity-impact note.

- **M4.O1.KPI2 — Hours released**
  - Formula: `Σ (baseline_minutes − post_deployment_minutes) × volume`.
  - Source: time-and-motion + workflow telemetry baselines.
  - Frequency: monthly per use-case; aggregate quarterly.

- **M4.O1.KPI3 — NDR SDE accredited projects**
  - Formula: count of live SDE projects with valid IG approval.
  - Source: SDE access registry.
  - Frequency: monthly.

### Mission 5 — Trusted strategic partner / high-quality, inclusive, ambitious organisation

**Objective M5.O1**: *Move DHCW off escalation level 3 to level ≤1 by 31-Mar-2027.*

- SMART: **S** = WG escalation level; **M** = ordinal level; **A** = whole-org programme of work; **R** = the most visible single confidence signal; **T** = by Mar-2027.

**Key Results**

- KR1: Audit Wales structured assessment 2026 reports "good" on governance & performance (vs. prior year baseline).
- KR2: ≥90% of IMTP milestones delivered on agreed quarter (currently below this).
- KR3: Staff engagement index ≥ top-quartile NHS Wales survey by 2027.
- KR4: Carbon emissions reduced by ≥10% vs. baseline by Mar-2027 (path to 34% by 2030).

**KPIs**

- **M5.O1.KPI1 — IMTP milestone delivery rate**
  - Formula: `(milestones delivered on agreed quarter) / (milestones due) × 100`.
  - Source: balanced-scorecard milestone tracker.
  - Frequency: monthly.

- **M5.O1.KPI2 — Staff engagement index**
  - Source: NHS Wales Staff Survey.
  - Frequency: annual; pulse quarterly.

- **M5.O1.KPI3 — Carbon emissions (Scope 1+2)**
  - Source: NHS Wales Decarbonisation Reporting.
  - Frequency: annual; modelled quarterly.

## 6. Telemetry, Observability, and "How we know we're moving"

To turn the OKRs above into a running pace signal rather than an annual report:

- **Single source of truth**: every KPI's source must be named, owned, and instrumented. Where missing, the first task is to instrument it.
- **Three-layer observability**:
  1. **Service layer** — uptime, latency, error budgets per service (Prometheus / Grafana / Dynatrace).
  2. **Product layer** — feature funnel analytics, SUS, NPS, digital-inclusion equity guardrails (Snowplow + NDR).
  3. **Outcome layer** — programme/mission KPIs rolled into a balanced scorecard (Power BI / Tableau over NDR).
- **Cadence**:
  - Real-time: service alerts, on-call.
  - Weekly: programme stand-up dashboards.
  - Monthly: mission scorecard to Exec.
  - Quarterly: balanced scorecard to Board; published KPI pack on publication-scheme page.
  - Annual: Annual Report, Quality Statement, Governance Statement.
- **Equity guardrails**: every adoption KPI is paired with a WIMD-quintile or Welsh-language-preference breakdown to avoid optimising for users who are already digitally engaged.
- **AI-specific observability** (M4): model performance drift, fairness, hallucination rate (for LLMs), human-override rate, audit log completeness — published per use-case.

## 7. AI Ideas — Concrete Tactics per Priority

- **NDR (M2, M4)** — synthetic data generation for safe development environments; LLM-based natural-language query layer over SDE; automatic data-quality scoring against FHIR Wales profiles.
- **NHS Wales App (M3)** — symptom triage assistant grounded in 111 Wales algorithms; bilingual (EN/CY) conversational booking; on-device summarisation of letters.
- **Digital Medicines (M2)** — anomaly detection on prescribing patterns; AI-assisted reconciliation at transfer of care; predictive medication-shortage alerting.
- **Clinical platforms (M2)** — ambient-listening clinical scribe pilots (mirroring NHSE FDP-adjacent rollouts); AI triage for radiology and dermatology waitlists.
- **Operations (M5)** — AI-assisted IT service desk first-line; automated incident-correlation; FinOps anomaly detection on cloud spend.
- **Governance (M5)** — LLM-assisted assurance: automated draft Board reports from balanced-scorecard data; consistency checks across IMTP / annual report / publication scheme.

Each tactic must be entered into the **AI use-case register** with: clinical safety classification (DCB0129/0160 equivalent), bias/fairness assessment, energy footprint, human-in-the-loop design, and benefit hypothesis.

## 8. Risks & Assumptions

- **Escalation context**: any plan must visibly contribute to de-escalation; "interesting but unmeasured" is not acceptable.
- **Data-source debt**: several KPIs above assume instrumentation that doesn't yet exist (e.g. consistent feature-funnel analytics). The first wave of work is plumbing, not metrics.
- **Equity**: headline counts (MAU, productivity) can mask widening inequality; equity guardrail KPIs are non-negotiable.
- **AI safety**: every M4 use-case must clear clinical safety, IG, and bias review before counting toward KR1.
- **Workforce capacity**: ambition is bounded by DHCW recruitment and retention — M5 staff-engagement KPI is a leading indicator for all four other missions.

## 9. Open Questions

- What is the *current* IMTP-milestone delivery rate (M5.O1.KR2 baseline)?
- What is the *current* NHS Wales App MAU? (Sets M3.O1.KR1 ambition curve.)
- Which 8 data domains constitute "priority" for M1.O1.KPI1?
- Which 10 services constitute the "top-10" for M2.O1?
- Is there an existing AI use-case register, or do we need to create it?

## 10. Sources

- DHCW — *What our priorities are and how we are doing*: https://dhcw.nhs.wales/about-us/publication-scheme/what-our-priorities-are-and-how-we-are-doing/
- DHCW — *Organisational Strategy 2024-2030 / Our Missions*: https://dhcw.nhs.wales/about-us/key-documents/strategies/organisational-strategy-2024-2030/our-missions/
- DHCW Draft Organisational Strategy (PDF): https://dhcw.nhs.wales/about-us/key-documents/dhcw-draft-organisational-strategy/
- HTN — *DHCW organisational strategy 2024-2030: in focus*: https://htn.co.uk/2024/07/03/digital-health-and-care-wales-organisational-strategy-2024-2030-in-focus/
- Audit Wales — *Structured Assessment 2025: DHCW*: https://www.audit.wales/sites/default/files/publications/dhcw_sa_1.pdf
- Welsh Government — *DHCW oversight and escalation framework: May 2025*: https://www.gov.wales/digital-health-and-care-wales-oversight-and-escalation-framework-may-2025-html
- NHS Wales — *Performance Framework 2025-2026*: https://www.gov.wales/sites/default/files/publications/2025-01/nhs-wales-performance-framework-2025-to-2026.pdf
- NHS England — *2025/26 Priorities and Operational Planning Guidance*: https://www.england.nhs.uk/long-read/2025-26-priorities-and-operational-planning-guidance/
- gov.scot — *Care in the Digital Age: delivery plan 2025-2026*: https://www.gov.scot/publications/care-digital-age-delivery-plan-2025-2026/
