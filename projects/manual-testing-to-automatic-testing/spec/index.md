# Spec: NHS Wales Organisational Change Policy facts

This file is the single source of truth for facts about the NHS Wales Organisational Change Policy (OCP) used in README.md. If README.md and this file ever disagree, this file is correct, and README.md needs updating to match it.

Primary source: [NHS Wales Organisational Change Policy](https://heiw.nhs.wales/files/key-documents/policies/human-resources-policies/all-wales-organisational-change-policy-docx/), December 2025 edition, approved by the Welsh Partnership Forum. Section and appendix references below (for example "OCP §4.2") point into that document.

## Context for this project

When technological change happens — such as a shift from manual testing roles to automated testing roles — NHS Wales and Digital Health and Care Wales (DHCW) treat the change as a skills gap, not an automatic redundancy trigger, under the OCP. The policy requires employers to prioritise training and internal redeployment over dismissal, and to explore reasonable adjustments and upskilling before concluding a role cannot be filled by its current holder.

DHCW's specific programme maps technical and QA roles onto the UK Government Digital and Data (GDaD) Product Capability Framework (PCF) as part of a People and Organisational Development (POD) restructure. This mapping exercise is DHCW's local application of the OCP's general "filling posts during organisational change" procedure (OCP §9), described below.

Note on scope: the paragraph above (DHCW's use of GDaD/PCF) is organisational context supplied for this project, not text quoted from the national OCP document, which does not name GDaD, PCF, or DHCW specifically — it is a Wales-wide policy that applies the same way to any NHS Wales organisation's restructure. Treat the GDaD/PCF mapping as one real-world example of the OCP's general "filling posts" procedure in action, not as a distinct legal process.

## Core principle

> "It is the policy of NHS Wales to prevent all avoidable compulsory redundancies... As such, it is the aim of this policy to ensure that the NHS retains the valuable knowledge, skills and experience of its workforce, by utilising a number of strategies, to assist displaced employees to find suitable alternative employment and/or retraining opportunities." — OCP §4.1

## The two-thirds test (verified)

A post is considered "substantially unchanged" if the scope of the role remains unaltered and it matches two-thirds (66.6%) or more of the employee's existing job description and person specification. — OCP §9.2, §9.4–9.5

This is the only numeric threshold stated in the national policy. There is no officially documented 25%-per-category weighting scheme, four-quarter breakdown, or similar formal scoring rubric in the OCP itself — any such breakdown used locally (e.g. by DHCW's POD/HR team during a mapping exercise) is a local implementation detail, not a national policy requirement. Confirm the actual scoring method used in any specific mapping exercise directly with the relevant POD/HR team.

## The filling-posts procedure (OCP §9)

1. Job descriptions and a person specification are produced for each post in the new structure.
2. Management runs a mapping exercise: existing employees are compared against posts in the new structure, using the two-thirds test above.
3. Selection criteria for prior consideration/restricted competition are objective: qualifications, relevant experience, skills and knowledge, suitability for a trial period or retraining, and reasonable adjustments under the Equality Act 2010 (OCP §9.3).
4. Slotting in — applies when a post is substantially unchanged AND there is one candidate, or an equal number of posts and candidates. No interview; the outcome is confirmed in writing. (OCP §9.4)
5. Prior consideration — applies when a post is substantially unchanged AND there is more than one potential candidate. Selection is by interview. (OCP §9.5)
6. Restricted competition — applies when a post is new or substantially changed. It is advertised first to employees directly affected by the change, before external advertisement. (OCP §9.6)
7. Disagreement about whether a post is "substantially unchanged" is reviewed by an independent panel (a Workforce & OD representative, a manager, and a trade union representative, none of whom have had prior involvement with the case). Further disagreement is escalated via the All-Wales Respect and Resolution Policy. (OCP §9.4)

## Redeployment (OCP §9.8, Appendix 5)

- An employee not appointed via slotting in or prior consideration becomes a Redeployment Candidate.
- Redeployment Candidates get priority sight of, and consideration for, suitable vacancies across NHS Wales before external advertisement.
- The Redeployment Candidate designation normally lasts a maximum of 3 months, extendable by taking a secondment or fixed-term post (which pauses/reactivates the remaining balance depending on its length — Appendix 5 §8).
- Wherever possible, the employee remains in their original post throughout; where that isn't possible, their manager finds meaningful interim work at a broadly commensurate pay band (Appendix 5 §7).
- Compulsory redundancy is a last resort, only considered if no suitable alternative employment has been found by the end of the 3-month period (Appendix 5 §6.8).

## Pay protection (OCP §10)

Short-term protection of earnings (applies to any change affecting earnings, such as a shift-pattern change, without a band change):

| Reckonable service | Protection period |
|---|---|
| Up to 2 years | 2 months |
| After 2 years | 4 months |
| After 3 years | 6 months |
| After 4 years | 8 months |
| After 5 years | 12 months |

Long-term protection of basic salary (applies when a change results in a downgrade):

| Reckonable service | Protection period |
|---|---|
| After 2 years | 6 months |
| After 3 years | 1 year |
| After 4 years | 2 years |
| After 5 years | 3 years |
| After 6+ years | 6 years |

Both can apply at once: short-term protection tops up earnings while long-term protection covers the base salary difference for its full period. Long-term protection also carries a duty on the employee to apply for suitable posts at their previous band; refusing three such offers ends protection. NHS Pension Scheme members with 2+ years' pensionable service may apply to the NHS Pensions Agency to protect their pension at the higher rate, within 3 months of the salary reduction.

Excess mileage/travel and car parking costs arising from a change of base are reimbursed for up to 4 years, or as a lump sum equivalent to 2 years (OCP §11).

## Training obligation (OCP §4.2)

> "...support employees who wish to retrain and are qualified to undergo training for posts in other disciplines/areas, where reasonable; and by means of the development review/personal development plan process, assist and support employees to overcome constraints which may prevent them undertaking a new role."

The "development review/personal development plan process" this section names is, in NHS Wales practice, the PADR — see [`spec/padr.md`](padr.md).

There is no fixed timeframe for retraining specified in the national policy; the OCP treats "reasonable timeframe" as dependent on the scope of the change, the employee's baseline capabilities, and operational practicality.

## Consultation (OCP §5)

- Consultation with staff and their representatives runs for a minimum of 4 weeks for any organisational change with workforce implications.
- Collective consultation under s188 of the Trade Union and Labour Relations (Consolidation) Act 1992 is triggered when 20 or more redundancies are proposed at one establishment within 90 days.

## Appeals

- Disputes about the selection process, mapping outcome, or redundancy are raised via the All-Wales Respect and Resolution Policy.
- Redundancy notices carry a 21-day right of appeal from the date of the notice letter (Appendix 2 §4.2).

## Welsh Government oversight and escalation of DHCW

Separate from the OCP itself: DHCW, like every NHS Wales organisation, is monitored under the Welsh Government's NHS Wales Oversight and Escalation Framework. This framework has five levels:

1. Routine arrangements
2. Areas of concern
3. Enhanced monitoring
4. Targeted intervention
5. Special measures

Level 4 (targeted intervention) applies when an organisation has serious problems it is judged unlikely to resolve without external support; Welsh Government takes and co-ordinates direct intervention to strengthen the organisation's capability and capacity to improve. Level 5 (special measures) is the highest tier, where Welsh Ministers can intervene directly under the NHS (Wales) Act 2006, including suspending or removing powers from board members.

Published Welsh Government reporting places DHCW at level 3 (enhanced monitoring) in an assessment in early 2025, and at level 4 (targeted intervention) in reporting during 2026. This project could not directly retrieve the primary gov.wales page to quote it verbatim (the site blocks automated fetches); the summary above is built from search-indexed summaries of that page and related gov.wales pages, not a direct quotation. Treat it as a starting point, and confirm the current position directly:

- [Digital Health and Care Wales oversight and escalation framework: May 2026, gov.wales](https://www.gov.wales/digital-health-and-care-wales-oversight-and-escalation-framework-may-2026-html)
- [NHS Wales escalation and intervention arrangements, gov.wales](https://www.gov.wales/nhs-wales-escalation-and-intervention-arrangements)

This status doesn't change any individual right described elsewhere in this file — the two-thirds test, redeployment, pay protection, and training obligations all apply regardless of DHCW's escalation level. It's useful context because a higher escalation level means more direct Welsh Government involvement in how DHCW governs, resources, and paces major change programmes, including a restructure like the GDaD/PCF mapping.

## Terminology used in this project

- OCP — NHS Wales Organisational Change Policy.
- GDaD/PCF — Government Digital and Data / Product Capability Framework; DHCW's local role-mapping framework, not a national OCP term.
- POD — People and Organisational Development; the DHCW/NHS Wales function equivalent to HR in most other organisations. This project always says "POD/HR contact," not "HR" alone, and never "your manager," reflecting DHCW's actual escalation route.
