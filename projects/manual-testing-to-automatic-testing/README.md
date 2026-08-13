# Manual Testing to Automatic Seting

IMPORTANT: This document is AI generated. This document is for fictitious
sandbox experimentation, not for actual real-world work. This document AI uses
all public/published/open information, no private/confidential/secret
information.

If you're a manual software tester at Digital Health and Care Wales (DHCW), and
your team is shifting towards test automation, this document is for you.

Your years of QA experience may include aspects such as requirement analysis,
edge-case thinking, defect management, stakeholder communication, and much more.
These are foundational knowledge and skills. Automation is a new way of working with these skills.

Automatic testing is good for the systems DHCW builds, and for the clinicians
and patients who depend on them.

This guide focuses on building your automation skills.

- It makes the case that this kind of learning should ideally happen steadily
  and all the time.

- It offers reflective questions to help you think through what you want.

- It provides a reference section near the end that covers formal protections.

- It provides everything is in this one file, so you can save it, print it, or
  search it as a single document.

This guide is general guidance, not legal or HR advice. Your POD/HR contact and
your trade union rep are your best sources of advice for your circumstances.

Also see [NHS Wales Organisational Change
Policy](https://heiw.nhs.wales/files/key-documents/policies/human-resources-policies/all-wales-organisational-change-policy-docx/)
(the "OCP", December 2025 edition) which describes your prioritising training,
upskilling, Knowledge and Skills Framework (KSF), and Continuous Professional Development (CPD).

IMPORTANT: This document is AI generated. This document is for fictitious
sandbox experimentation, not for actual real-world work. This document AI uses
all public/published/open information, no private/confidential/secret
information.

## Contents

1. [You're part of a worldwide, cross-sector shift](#1-youre-part-of-a-worldwide-cross-sector-shift)
2. [The upside of automatic testing](#2-the-upside-of-automatic-testing)
3. [Training and upskilling](#3-training-and-upskilling)
4. [Continuous professional development](#4-continuous-professional-development)
5. [Questions:for reflection, coaching, and exploration](#5-questions-for-reflection-coaching-and-exploration)
6. [What "good enough" looks like](#6-what-good-enough-looks-like)
7. [Ways of working you'll meet along the way](#7-ways-of-working-youll-meet-along-the-way)
8. [Coming into the office: the value of in-person work](#8-coming-into-the-office-the-value-of-in-person-work)
9. [Your learning toolkit: many ways to grow](#9-your-learning-toolkit-many-ways-to-grow)
10. [A simple skills roadmap for manual → automatic testing](#10-a-simple-skills-roadmap-for-manual--automatic-testing)
11. [Psychometric assessments: what to expect and how to prepare](#11-psychometric-assessments-what-to-expect-and-how-to-prepare)
12. [Your PADR: Performance Appraisal and Development Review](#12-your-padr-performance-appraisal-and-development-review)
13. [Building your own CPD / personal development plan](#13-building-your-own-cpd--personal-development-plan)
14. [Setting your own KPIs and OKRs](#14-setting-your-own-kpis-and-okrs)
15. [Using AI as a coach](#15-using-ai-as-a-coach)
16. [Your action checklist, starting today](#16-your-action-checklist-starting-today)
17. [Get it in writing](#17-get-it-in-writing)
18. [Good questions to ask your POD/HR contact](#18-good-questions-to-ask-your-podhr-contact)
19. [Looking after yourself: workplace stress and support](#19-looking-after-yourself-workplace-stress-and-support)
20. [Neurodiversity, reasonable adjustments, and your paperwork](#20-neurodiversity-reasonable-adjustments-and-your-paperwork)
21. [Your safety net, briefly](#21-your-safety-net-briefly)
22. [Where to get support](#22-where-to-get-support)
23. [Sources and further reading](#23-sources-and-further-reading)
24. [A note on this guide](#24-a-note-on-this-guide)

---

## 1. You're part of a worldwide, cross-sector shift

The move from manual to automatic testing spans every industry, across the world
— government, healthcare, finance, retail, and more — and has done for well over
a decade.

A few points for perspective:

- The tools are established. Selenium has been a mainstay of the industry since
  the mid-2000s. Playwright, newer and increasingly popular, has matured since 2020. Both are mature, well-documented tools with large global user bases.

- Large software organisations everywhere have made this move. For example,
  manual testers at banks in Singapore, retailers in the US, telecoms in
  Germany, and health services across Europe have shifted from purely manual
  testing to a blend of manual judgement and automated execution. You're joining
  a well-trodden path.

- International professional bodies reflect this shift. ISTQB (the International
  Software Testing Qualifications Board) is a global, vendor-neutral
  certification body. It has offered automation-focused qualifications for
  years, because testers worldwide have needed this path.

- Global communities have formed around this shift. For example, Ministry of
  Testing has tens of thousands of members worldwide, many of whom are, or were,
  manual testers building automation skills and sharing what worked.

- Automatic tests can check the same things quickly and repeatedly. Human
  testers can explore, judge risk, and ask "what if...?" then automate these
  decisions. The strongest teams combine both automatic tests and human testers.

### The same pattern across public sector organisations

This pattern repeats across public sector organisations worldwide, well beyond healthcare:

| Sector                         | Illustrative examples                                                                                                              | What's been changing                                                                                                                                                                                                                   |
| ------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| UK central government          | HMRC, DWP, the Home Office, the Ministry of Justice                                                                                | All use the cross-government Digital, Data and Technology (DDaT) Profession Capability Framework, which has included automated/test-engineering career paths for years — the same broad tradition DHCW's GDaD/PCF mapping sits within. |
| Other UK health services       | NHS England, NHS Scotland, NHS Northern Ireland                                                                                    | Each has invested in test automation as part of its own digital transformation, independently of Wales.                                                                                                                                |
| UK local government            | Councils running citizen-facing digital services (council tax, planning, benefits portals)                                         | Have modernised legacy manual QA processes alongside broader service redesign.                                                                                                                                                         |
| International public sector    | The US Digital Service/18F, Australia's Digital Transformation Agency, Government of Canada's Digital Service, Singapore's GovTech | Each publishes engineering/QA standards that treat automatic testing as standard practice.                                                                                                                                             |
| Private sector, for comparison | Banks, retailers, telecoms, airlines worldwide                                                                                     | Made this transition years earlier — often the model public sector digital teams have deliberately followed.                                                                                                                           |

_(Programmes, timelines, and frameworks vary by organisation. The pattern is consistent: this is what modernising a QA function looks like, in government and beyond.)_

This means the road ahead is mapped. Free courses, videos, books, forums, and
mentoring communities exist, built by people worldwide who've made this move
before you. You're walking a path that people in government departments,
hospitals, banks, and councils worldwide have already walked.

### Welsh Government oversight of DHCW

DHCW, like every NHS Wales organisation, is monitored under the Welsh Government's NHS Wales Oversight and Escalation Framework, a five-level scale:

1. Routine arrangements
2. Areas of concern
3. Enhanced monitoring
4. Targeted intervention
5. Special measures

Level 4 (targeted intervention) applies when an organisation has serious problems it's judged unlikely to resolve without external support; Welsh Government takes and co-ordinates direct intervention to strengthen the organisation's capability and capacity to improve. Level 5 (special measures) is the highest tier, where Welsh Ministers can intervene directly under the NHS (Wales) Act 2006.

Published Welsh Government reporting places DHCW at level 3 in an assessment in early 2025, and at level 4 in reporting during 2026 — read the current framework page yourself to confirm today's position, since these levels are reviewed and can change:

- [Digital Health and Care Wales oversight and escalation framework: May 2026, gov.wales](https://www.gov.wales/digital-health-and-care-wales-oversight-and-escalation-framework-may-2026-html)
- [NHS Wales escalation and intervention arrangements, gov.wales](https://www.gov.wales/nhs-wales-escalation-and-intervention-arrangements)

The escalation encourages looking at ways of working, and spcifically describes
seeking ways to deliver software faster. This is a key area where automatic
tests can help, and where there is an high priority need for upskilling in
automation ways of working.

### Checklist: understanding DHCW's oversight status

- [ ] I have read the DHCW oversight and escalation framework page at gov.wales.
- [ ] I understand which escalation level DHCW is currently at, and what that level means.
- [ ] I've asked my POD/HR contact any questions I have about what this means for my team or role.
- [ ] I've asked my union rep any questions I have about what this means for my team or role.
- [ ] I understand that my individual rights under the OCP apply regardless of DHCW's escalation status.

---

## 2. The upside of automatic testing

Automatic testing is good work to be good at — for the systems you help build,
your colleagues, and the clinicians and patients NHS Wales serves.

### Better system quality

Automatic tests run the same checks the same way, every time — staying fresh and
completing every step, even at the end of a long shift. Run regularly, they
catch regressions (things that used to work, breaking again) more reliably than
repeated manual runs, especially across large, interconnected systems like the
ones DHCW builds and maintains. That's a real quality improvement.

### Real pace speedups

A well-built automated regression suite can run in minutes, covering ground that
would take days to click through by hand. Problems get caught close to when
they're introduced — while they're fresh and cheap to fix — instead of surfacing
weeks later in a pre-release scramble. Faster, more confident releases mean
fixes reach people sooner.

### Health-economic benefits

A defect caught early costs a fraction of one caught late — a long-established
principle in software engineering. Every hour spent firefighting a production
issue is an hour a good automatic test could have avoided. In a public health
service, money saved on emergency fixes and repeat support calls can go toward
frontline care instead. Investing in automatic testing is investing in value for
the health service.

### Clinician benefits

Clinicians depend on digital systems — patient records, scheduling, prescribing,
results reporting — working correctly every time, often while focused entirely
on the person in front of them. A strong automated regression suite gives
clinicians confidence that today's update hasn't broken something they rely on
tomorrow.

### Patient benefits

More reliable software means fewer disruptions to care: fewer moments where a
clinician can't access a result, fewer scheduling errors, fewer near-misses from
a software defect slipping through. Building a strong automatic test suite is a
contribution to patient safety, and part of the caring mission of the NHS.

---

## 3. Training and Upskilling

The transition from manual testing to automatic testing will surely require training.

NHS Wales has a policy about this, that says that employers must:

> "...support employees who wish to retrain and are qualified to undergo training for posts in other disciplines/areas, where reasonable; and by means of the development review/personal development plan process, assist and support employees to overcome constraints which may prevent them undertaking a new role." — OCP §4.2

When a role is judged "substantially unchanged" (your current job covers two-thirds or more of the new one), a gap — like moving from manual scripts to Selenium, WebDriver, or Playwright automation — might be treated as a variance in tools, not a new job. The gap might be consider via a training plan, funded and supported by your employer, on a reasonable timeframe based on your starting point and the scope of what you need to learn. Policy leaves the number of weeks flexible — the timeframe is meant to fit you.

You can expect your organisation, led by your POD/HR team, to:

- [ ] Give you a written, structured training plan.
- [ ] Fund courses, materials, and study time where reasonable.
- [ ] Give you a trial period (minimum four weeks, extendable) in a new role, with real time to learn.
- [ ] Recognise your existing Knowledge and Skills Framework (KSF) competencies (communication, service improvement, analysis) as assets alongside the technical skills you're building.

Your POD/HR contact is the right person to request this formally — they own the training and development obligations under the policy. In NHS Wales, the "development review/personal development plan process" the OCP names has an official structure: your PADR — see [section 12](#12-your-padr-performance-appraisal-and-development-review).

- [ ] I know the right POD/HR person to contact to request this.
- [ ] I've requested this.
- [ ] I've received this.

---

## 4. Continuous professional development

Continuous professional development means continuous — a steady part of a career, not something that starts when a restructure is announced. If training time, courses, and development conversations have been light over the last few years, that's worth highlighting in your next conversation with POD/HR.

A few things worth knowing:

- NHS Wales's appraisal and KSF process assumes ongoing development. Every staff member is meant to have a personal development plan, reviewed regularly — typically at least annually, via your PADR — with training needs identified and protected time set aside. This is business as usual.
- The tech industry treats ongoing learning as part of the job. Professional bodies like ISTQB expect members to log CPD activity to keep credentials current. Learning is a steady part of a career, worldwide.
- If the last few years have been light on training, you're not alone. A simple way to raise it: _"I don't think I've had much protected training time over the past few years — can we build that in, and keep it going?"_
- This moment is a chance to establish a rhythm — regular training time, regular check-ins, and a standing training budget that continues beyond this transition.

### Checklist: reflecting on the last 4 years

- [ ] What training, courses, conferences, or development opportunities did I get in approximately the last 4 years?
- [ ] Was there anything I wanted or asked for that didn't happen? Do I know why?
- [ ] Did I have regular appraisal/PADR conversations that included a real personal development plan?
- [ ] Did I get protected time during work hours to study or practise new skills?
- [ ] What would good, ongoing development have looked like, and what do I want it to look like from here?
= [ ] If CPD has been light past few years, have I had a conversation with POD/HR about this?

For a deeper set of questions, see [section 5](#5-challenge-questions-for-reflection-coaching-and-honest-exploration).

---

## 5. Questions for reflection, coaching, and exploration

These questions are for your own reflection, and help you think about where
you've been, where you are, and where you want to go, and make conversations
with your POD/HR contact, a mentor, or your union rep richer when you have them.
Answer them in a notebook, out loud to a trusted friend, or with a coach or
mentor.

### Looking back: the last four years

- [ ] In each of the past four years, what upskilling or training did you do, and how did each experience feel?
- [ ] What's one thing you learned in the last few years that you're proud of?
- [ ] Was there a course, conference, secondment, or opportunity you wanted but didn't get? What got in the way, and does that obstacle still exist?
- [ ] Who supported your development over the last few years, and who could you lean on more, going forward?
- [ ] Has your own growth over the last four years kept pace with the change happening around you? What does that tell you?

### Looking at now: how you're feeling

- [ ] What's your gut reaction to the word "automation" — curiosity, dread, excitement, boredom, something else? What might be behind that reaction?
- [ ] What part of your current, manual way of working would you be sad to see disappear?
- [ ] What part of your current role do you find yourself avoiding, tolerating, or hoping changes?
- [ ] How confident do you feel, right now, in your ability to learn something technical and new? Where does that confidence come from?
- [ ] Is there a colleague whose approach to this change you admire? What are they doing that you could try yourself?

### Looking ahead: the next year or two

- [ ] When you think about your work over the next few years, how drawn are you to transitioning into automatic testing, versus a different kind of work or role altogether?
- [ ] If you imagine your complete freedom, such as with your full confidence, open logistics, and a blank slate on what's "realistic" — what would your ideal day-to-day role look like in a few years?
- [ ] Would you rather go deep on one automation tool and become your team's go-to expert, or stay broad across manual and automatic testing? What draws you to that?
- [ ] Is there a different path that appeals to you — business analysis, product ownership, training and mentoring others, quality coaching, delivery/scrum roles, or something else?
- [ ] What would "this went well" look like for you personally, at the end of this transition?

### Values and motivation

- [ ] What first drew you to testing as a career? Is that still true for you today?
- [ ] What matters most to you day-to-day at work — variety, mastery, stability, challenge, connection with colleagues, or something else? How does that shape what you want next?
- [ ] On a scale from "reluctantly going along with this" to "excited about it," where are you today, and what would move you a notch further along?
- [ ] What would make this transition feel meaningful to you?

### Skills and confidence

- [ ] What's the one skill that, if you built confidence in it, would make the biggest difference to how you feel about the future?
- [ ] Think of a time you learned something completely new and it went well. What made that work? Can any of those conditions be recreated here?
- [ ] Do you learn best with structure and deadlines, or with freedom to explore at your own pace? Does your current plan reflect that?
- [ ] Is there a skill you already have — from testing, a hobby, a previous job, life outside work — that people might not realise is relevant here?

### Support, identity, and purpose

- [ ] Who do you want in your corner during this transition — a POD/HR contact, a mentor, a union rep, a colleague, or a mix?
- [ ] Have you told anyone how you're feeling about this change? Would it help to?
- [ ] Does "tester" still feel like the right word for who you want to be at work, or is a different title or identity starting to feel more like you?
- [ ] Looking back on this chapter of your career in few years, how do you want to describe it?

Revisit a few of these questions every few months, as your thinking evolves.

---

## 6. What "good enough" looks like

Automatic testing skills build in layers, and most manual testers already have a head start on the first one or two:

| Layer              | What it involves                                                                         | You probably already have some of this |
| ------------------ | ---------------------------------------------------------------------------------------- | -------------------------------------- |
| Testing mindset    | Requirements analysis, risk-based thinking, edge cases, defect lifecycle                 | Yes — this transfers directly          |
| Tooling literacy   | Using a test automation tool (Selenium, WebDriver, Playwright) to drive a browser or app | New, but learnable                     |
| Scripting basics   | Reading and writing simple scripts in Python, JavaScript, or C#                          | New, builds gradually                  |
| Pipeline awareness | Understanding how automatic tests fit into CI/CD and DevOps workflows                    | New, mostly conceptual at first        |
| Stretch skills     | Using AI-assisted tools to help write or maintain tests                                  | New, evolving quickly                  |

A demonstrated learning trajectory is what a reasonable training plan supports. You don't need to master every layer to be ready for the new role. These are the same layers testers worldwide, across government, healthcare, and industry, have built one at a time, often through steady, ongoing CPD.

### You've done this before: familiar ways to learn something new

Learning test automation follows the same shape as other kinds of learning, such as these comparisons:

- Learning a new language. A learner starts with a few words, then simple sentences, then real conversations. Automation works the same way: a line of code, then a small script, then a full test.
- Baby steps, then walking, then running.
- Learning a musical instrument. Scales and simple exercises come before songs, and songs come before performances. The repetitive practice — a kata, a small automatic test repeated with variations — is the scales-and-arpeggios stage of automation.
- Learning a sport. You practise the basic moves and rules before you play a full match, and you keep practising even once you can play. Fundamentals first, then applying them to real complex situations.
- Learning to ride a bicycle. Wobbly and uncertain at first, with someone holding the seat or with training, then a little steadier, then one day you're just riding, and the hard part is a distant memory.

Every one of these skills started slow and became natural with practice. Automatic testing follows the same path.

### Checklist: know your target role

- [ ] I have read my UK GDaD PCF role summaries page at [github.com/joelparkerhenderson/uk-gdad-pcf-roles/tree/main/summaries/](https://github.com/joelparkerhenderson/uk-gdad-pcf-roles/tree/main/summaries/).
- [ ] I have read my UK GDaD PCF role upskills page at [github.com/joelparkerhenderson/uk-gdad-pcf-roles/tree/main/upskills/](https://github.com/joelparkerhenderson/uk-gdad-pcf-roles/tree/main/upskills/).
- [ ] I know which specific GDaD/PCF role profile my new post is being mapped against.
- [ ] I've compared that role profile's essential skills against my own, using the layers in the table above.

### Checklist: check your understanding (part 1)

- [ ] I understand that this shift is happening across the whole industry and public sector, not just at DHCW.
- [ ] I understand the two-thirds test for whether my role counts as "substantially unchanged."
- [ ] I understand that training and upskilling is my employer's obligation, not just something I have to sort out myself.
- [ ] I understand that CPD is meant to be continuous, not a one-off response to this change.
- [ ] I've sat with at least a few of the challenge questions in section 5, and thought honestly about my answers.
- [ ] I understand what "good enough" looks like at this stage — I don't need to be an expert overnight.
- [ ] I will find a mentor.
- [ ] I have read the NHS Wales Organisational Change Policy, or at least the parts that apply to me.

---

## 7. Ways of working you'll meet along the way

Automation comes with new team habits and vocabulary too. None of this needs to click on day one — you'll pick up most of it by being in the room. Here's an orientation for your first few meetings.

Worth knowing upfront: Agile and Scrum are often said in the same breath, but they're different things. Agile is a mindset — values like people, conversation, and flexibility, over rigid process. Scrum is one specific framework for structuring work, built around a set of ceremonies. A team can run Scrum's ceremonies closely and still lose sight of Agile's underlying values, so the two are worth understanding separately.

| Term                                                 | What it means                                                                                                                                                                        | Why it matters for you                                                                                     |
| ---------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------- |
| Agile                                                | A mindset and set of values, from the Agile Manifesto — prioritising people, conversations, working software, and responding to change, over rigid processes and heavy documentation | Your judgement, questions, and flexibility matter as much as following any fixed process                   |
| Scrum                                                | One specific framework for structuring work, built around short cycles ("sprints") with regular standups, sprint planning, sprint review, and retrospective meetings                 | Testing happens throughout the sprint's ceremonies — your voice is wanted at each one, not just at the end |
| Kanban                                               | A continuous-flow way of working, visualised on a board of columns (e.g. To Do / In Progress / Done)                                                                                 | Common in support/maintenance teams; testing is a visible, tracked step on the board                       |
| Shift-left testing                                   | Involving testers earlier — during requirements and design, alongside after code is written                                                                                          | Your domain knowledge and risk-based thinking add value at this earlier stage                              |
| DevOps                                               | A culture where development, testing, and operations work closely together, sharing responsibility for quality                                                                       | "Quality is everyone's job" — testers are core team members shaping the work                               |
| CI/CD (Continuous Integration / Continuous Delivery) | Automatic tests run automatically whenever code changes, often many times a day                                                                                                      | This is where your automatic tests live and do their work                                                  |
| Version control (Git)                                | A system for tracking changes to code (and test scripts) over time, usually via GitHub, GitLab, or similar                                                                           | You'll likely commit, share, and review test scripts this way — a learnable, well-documented skill         |
| BDD / Gherkin                                        | Writing test scenarios in structured plain English (Given / When / Then)                                                                                                             | A friendly bridge into automation — it reads like a clear manual test script, in a specific format         |
| Definition of Done                                   | The agreed checklist a piece of work must meet before it's complete                                                                                                                  | Increasingly includes "automatic tests written and passing" as standard                                    |
| Three amigos                                         | A short session where a developer, tester, and business/clinical representative discuss a piece of work before it starts                                                             | A chance for your testing perspective to shape the work upfront                                            |

You'll pick up this vocabulary the way you'll pick up the tools (see [section 9](#9-your-learning-toolkit-many-ways-to-grow)): by being in the room, asking questions, and trying things out gradually. Many of the courses and communities in section 9 cover these ways of working directly.

### Checklist: getting comfortable with new ways of working

- [ ] I've attended (or watched a recording of) an agile interaction, such as an agile discovery.
- [ ] I've attended (or watched a recording of) a sprint planning, standup, or retrospective, to see how it works.
- [ ] I have a basic idea what a CI/CD pipeline does, even if I couldn't build one yet.
- [ ] I've seen an example of a Gherkin/BDD-style test scenario (Given / When / Then).
- [ ] I know where my team's "Definition of Done" is documented.
- [ ] I've asked to sit in on a "three amigos" or similar planning conversation.
- [ ] I've asked a colleague to explain any term from the table above that's still unclear. It's a normal question.

---

## 8. Coming into the office: the value of in-person work

Many teams now work in a hybrid pattern — some days remote, some days together. Both have real value, and knowing how to use each well makes this transition smoother. For automatic testing and relevant upskilling, coming into the office can help, and is worthwhile to do.

### Why in-person time is worth it

- Whiteboarding test strategy. Talking through what to automate, what to keep manual, and where the risks sit works well in a room with a whiteboard.
- Pairing on tricky problems. Sitting side by side with an automation engineer to untangle a failing test, or work through a new tool, often moves faster than a chat message thread.
- Faster relationships. Building trust with developers, product owners, and your wider team tends to happen quicker face to face, which helps everything else on this list.
- Easier questions. Some people find it easier to ask "silly questions" in person than in a group chat — and in-person conversations often surface follow-up questions nobody thought to type.
- Visibility of your growth. Presenting at a team show-and-tell, or simply being seen working through a new skill, is useful evidence to bring to your [PADR](#12-your-padr-performance-appraisal-and-development-review).
- Team all-hands. Many organisations run a monthly all-hands or town hall, in person or hybrid. These build shared context and culture that's harder to get from a recording alone.
- Helping your colleages. When coworkers come into the office and can work directly together, this favours in-person interactions, including agile ways of working, and ways of working in groups to help your teammates and stakeholders.

### Practical logistics

- [ ] Check your team's monthly all-hands schedule and other regular in-person commitments, so you can plan around them.
- [ ] If your role covers travel between cities or sites (common across NHS Wales, with staff and offices spread across the country), ask your POD/HR contact or your organisation's finance/travel team about the travel and expenses process — mileage, public transport costs, and how to claim them.
- [ ] Block travel days in your calendar in advance, and build in a buffer either side for delays.
- [ ] Use travel time for learning where it suits you — a testing podcast, a video course, or reading — see [section 9](#9-your-learning-toolkit-many-ways-to-grow).

### Travelling between cities, such as Swansea and Cardiff

Staff across NHS Wales and DHCW often travel between cities for team all-hands, training days, or office visits — the Swansea–Cardiff corridor is a common example. Swansea to Cardiff is approximately 45 minutes to an hour by train, or by car via the M4 — a well-used South Wales commute route, though traffic and engineering works can add time either way.

- [ ] Check train times and any off-peak or advance ticket options ahead of the day; prices and availability change as the date gets closer.
- [ ] If driving, check parking availability and cost at your destination in advance — some sites have limited spaces.
- [ ] Confirm with POD/HR or your finance/travel team whether a given trip counts as ordinary commuting (usually not reimbursed) or business travel (usually reimbursed) — this affects what you can claim.
- [ ] Keep tickets, receipts, or a mileage record, in line with your organisation's expenses policy.
- [ ] Build in a time buffer for delays, especially for a meeting or all-hands with other people.
- [ ] Have a plan for the journey itself — a podcast, an audiobook, or course notes to review.
- [ ] If a disability or health condition affects your travel, ask POD/HR about reasonable adjustments to travel arrangements too — see [section 20](#20-neurodiversity-reasonable-adjustments-and-your-paperwork).

### Balancing remote and in-person time

Both modes suit different parts of this transition:

- Remote, focused time suits solo hands-on practice, working through a course, or writing your first automatic tests without interruption.
- In-person time suits mentoring, pairing, three amigos sessions, and team ceremonies, where being in the room adds value.

- [ ] Aim to use each for what it's good at, rather than treating one as automatically better than the other.
- [ ] Be aware that agile ways of working favour in-person face-to-face communication, and the Agile Manifesto describes more about this.

### Checklist: making the most of in-person time

- [ ] I know my team's monthly all-hands (or equivalent) schedule.
- [ ] I've planned at least one in-person pairing or mentoring session for this month.
- [ ] I have a specific goal for my next in-person day (a question to ask, a session to attend, a person to meet).
- [ ] I use travel or commute time for learning, when it works for me.

---

## 9. Your learning toolkit: many ways to grow

People learn differently. Some like a structured course; others learn by tinkering, watching, reading, or talking things through with someone experienced. Mix and match what works for you. This transition is global and cross-sector (see [section 1](#1-youre-part-of-a-worldwide-cross-sector-shift)), so most of what follows is free or low-cost, built by the worldwide testing community. CPD is ongoing (see [section 4](#4-continuous-professional-development)) — treat these as resources to return to over months and years.

### Find a mentor

A mentor is someone more experienced who guides you.

- [ ] Ask your POD/HR contact about a formal mentoring scheme.
- [ ] Ask a colleague who is already doing automation if they'd mentor you informally.
- [ ] Shadow an automation engineer for an hour: watch how they write and run a test, ask "why" a lot.
- [ ] Pair-program with your mentor on a real test script — even 30 minutes a week compounds fast.

### Find a study buddy

A study buddy is a peer at a similar stage to you, learning alongside you rather than guiding you — both relationships are useful, and neither replaces the other.

- [ ] Find a study buddy among fellow manual testers going through the same transition.
- [ ] Work through the same course together, compare notes, and keep each other motivated.
- [ ] Global communities (below) can also connect you with a study partner anywhere in the world.

### Take a structured course

- [ ] Ask your POD/HR team what's available and funded first — via your organisation's e-learning platform (e.g. Learning@Wales/ESR) or an approved external provider.
- [ ] Test Automation University (by Applitools) — free, tester-focused courses on Selenium, WebDriver, Playwright, and more, used by testers worldwide.
- [ ] Read about Ministry of Testing's "Dojo" — a learning platform for software testers internationally, including automation paths.
- [ ] Visit websites like Coursera, Udemy, LinkedIn Learning, or Codecademy have well-reviewed beginner courses in Python, JavaScript, Selenium, WebDriver, and Playwright.
- [ ] Consider an internationally-recognised certification when you're ready, such as the ISTQB Advanced Level – Test Automation Engineering syllabus, respected by employers globally.
- [ ] Ask POD/HR about attending a training course, workshop, or conference every year, as a standing part of your role.

### Watch a video

- [ ] Visit online tool channels: the Playwright, Selenium, and WebDriver YouTube channels show real, working examples.
- [ ] Start with search-friendly channels like "Automation Step by Step" that cover automatic testing from first principles for beginners.
- [ ] Watch conference talk recordings from international testing conferences give you the "why" behind the "how" — often what makes techniques click.

### Read a book

- [ ] _Experiences of Test Automation_ — Dorothy Graham & Mark Fewster, on automation strategy.
- [ ] _The Selenium Guidebook_ — Dave Haeffner, a practical, beginner-friendly introduction.
- [ ] _Agile Testing_ / _More Agile Testing_ — Lisa Crispin & Janet Gregory, on how testing (manual and automated) fits into modern delivery.
- [ ] _Python Crash Course_ — Eric Matthes, for starting from zero with programming.
- [ ] _Continuous Delivery_ — Jez Humble & David Farley, on where automatic tests fit into CI/CD.

### Browse a website or read the docs

- [ ] Learn via official docs: [playwright.dev](https://playwright.dev), [selenium.dev](https://www.selenium.dev), [webdriver.io](https://webdriver.io)
- [ ] Try MDN Web Docs for web/JavaScript fundamentals.
- [ ] Read blogs and newsletters from the global testing community explain concepts in approachable, real-world terms.

### Join a community

- Ministry of Testing — an international community of testers, with forums, meetups, and a club welcoming people moving into automation.
- Local or NHS-adjacent tech meetups and internal DHCW/NHS Wales communities of practice, if they exist — your POD/HR team can point you to any that are running.
- International conferences (in person or virtual) show what "good" looks like and connect you with people worldwide who were where you are now.

### Practise hands-on

- [ ] Try sandbox practice sites built for learning automation (e.g. "the-internet" by Dave Haeffner) that let you write real automatic tests against a safe target.
- [ ] Start small: automate one login form, then one search box, then one form submission. Small wins build confidence.
- [ ] Ask to shadow or contribute to a real automatic test suite at work, once you have the basics.
- [ ] Try a weekly "kata": one small automation exercise, repeated and varied, like practising scales on an instrument. Keep it up as a recurring habit — that's what makes it stick.

### Checklist: pick at least one to start

- [ ] I've identified a possible mentor, buddy, or someone to shadow.
- [ ] I've bookmarked or enrolled in at least one structured course.
- [ ] I've found at least one video channel to follow.
- [ ] I've picked at least one book to read (even a chapter at a time).
- [ ] I've bookmarked the official docs for one tool (Playwright, Selenium, or WebDriver).
- [ ] I've joined at least one community (e.g. Ministry of Testing).
- [ ] I've tried at least one hands-on exercise on a sandbox site.

---

## 10. A simple skills roadmap for manual → automatic testing

A realistic, flexible order used by manual testers worldwide, across every sector, making this move:

1. Get comfortable with one scripting language. Python is a friendly starting point for testers new to code.
2. Learn the basics of one automation tool. Playwright is increasingly popular and beginner-friendly; Selenium/WebDriver is the long-standing industry standard. Either is a good place to start, and the concepts transfer between them.
3. Automate something small and real. One test case. Get it running, get it passing, celebrate it.
4. Learn what a CI/CD pipeline does conceptually, and how your automatic test slots into one.
5. Grow your test suite gradually, pairing new automation skills with the testing judgement you already have — that combination makes you effective.
6. Explore AI-assisted testing tools when you're ready — useful for speeding up writing and maintaining tests, alongside your own understanding.

Each step, however small, builds toward the quality, speed, and patient-safety benefits in [section 2](#2-the-upside-of-automatic-testing) — you're building something that makes real systems more dependable.

Spread over months, with steady, protected time each week, this roadmap is achievable — one reason ongoing, protected training time (see [section 4](#4-continuous-professional-development)) matters.

### Checklist: hands-on automation milestones

Small, concrete milestones you can tick off as you go — each one is a real, practical step, not a test of how much you already know.

- [ ] I can write and run "hello world" in a programming language such as JavaScript, Python, or C#.
- [ ] I can write and run an automatic test in a framework such as WebDriver, Selenium, or Playwright.
- [ ] I can write and run an AI prompt to help me generate code, tests, or tasks.
- [ ] I can install and set up a testing framework on my own machine, following a guide.
- [ ] I can sign in to a Unix/Linux cloud server, navigate the file system, edit files, run programs, and ask AI for help when I'm stuck.
- [ ] I can use basic command-line commands (e.g. listing files, changing directories, viewing a file's contents) in a terminal.
- [ ] I can open a project in a code editor (e.g. VS Code), navigate its files, and make a small edit.
- [ ] I can install a package or dependency using a package manager (e.g. npm or pip).
- [ ] I can find a button, fill in a form field, and read text from a web page, using code.
- [ ] I can write a test that checks a page has loaded correctly (e.g. the title, or a key piece of text).
- [ ] I can run a small set of automatic tests and read the pass/fail results.
- [ ] I can read someone else's automatic test and explain, in plain English, what it does.
- [ ] I can find and fix a simple failing automatic test.
- [ ] I can read an error message or stack trace and work out roughly what went wrong.
- [ ] I can save a test script using version control (e.g. Git), and share it with someone else.
- [ ] I can create a branch, commit a change, and open a pull request in Git.
- [ ] I can set up environment variables or configuration needed to run a test locally.
- [ ] I can automate one full manual test case, from start to finish.
- [ ] I can explain, in plain English, the difference between a unit test, an integration test, and an end-to-end test.
- [ ] I can add an automatic test to a CI/CD pipeline, or watch someone else do it once, step by step.

---

## 11. Psychometric assessments: what to expect and how to prepare

If you go through prior consideration, restricted competition, or apply for another role, the selection process may include psychometric assessments alongside your interview — common practice across NHS Wales and the wider public sector for many technical and digital roles. These tests measure a specific skill on the day. They're one part of a broader decision that includes your experience, interview, and application.

### The common types

- Cognitive ability tests — general reasoning and problem-solving, usually timed and multiple choice.
- Verbal reasoning / literacy — reading a passage and deciding whether statements are true, false, or "cannot say" based on the text.
- Numerical reasoning / literacy — interpreting charts, tables, percentages, and ratios, and doing basic calculations.
- Situational judgement tests (SJTs) — workplace scenarios where you rank or choose the best and worst response. Widely used in NHS recruitment to see how you'd act in line with NHS values: respect, compassion, teamwork, and improving lives.

### How to prepare

- Ask POD/HR in advance which type(s) of assessment will be used, and which provider (e.g. SHL, Talent Q) — this tells you what to practise.
- Try free or low-cost practice tests online for each type you'll face.
- Do at least one practice test under timed conditions, so the format is familiar beforehand.
- For situational judgement questions, think about NHS values-based responses rather than a first instinct.
- Ask for reasonable adjustments if you need them — extra time, an alternative format, or assistive technology (see [section 20](#20-neurodiversity-reasonable-adjustments-and-your-paperwork)).
- Plan rest and a calm routine before the day.

### Checklist: preparing for a psychometric assessment

- [ ] I've asked POD/HR which type(s) of assessment will be used and which provider.
- [ ] I've found and tried a free practice test for each type I'll face.
- [ ] I've done at least one practice test under timed conditions.
- [ ] I know I can request reasonable adjustments, and have asked if I need them.
- [ ] For situational judgement questions, I've thought about NHS values-based responses.
- [ ] I've planned rest and a calm routine before the assessment.
- [ ] I remember this is one part of a bigger picture, alongside my experience and interview.

### Checklist: check your understanding (part 2)

- [ ] I understand the difference between Agile (a mindset) and Scrum (a specific framework of ceremonies).
- [ ] I understand how in-person time and remote time each add value in different ways.
- [ ] I've found at least one learning resource that genuinely suits how I learn.
- [ ] I understand the rough order of skills in the roadmap: one language, one tool, one small test, then a pipeline, then growth.
- [ ] I understand that psychometric assessments, if I face them, are only one part of a bigger decision.
- [ ] I know where to find practice material for any assessment I might face.
- [ ] I will try at least one hands-on exercise this week.

---

## 12. Your PADR: Performance Appraisal and Development Review

If you work for an NHS Wales health board or organisation like DHCW, there's a formal, named process for this conversation: your PADR — Performance Appraisal and Development Review. It's your best formal opportunity to get automation training written down, agreed, and reviewed on a proper cadence, and in many parts of NHS Wales, it connects to your pay progression.

### What a PADR is

A PADR is a continuous feedback mechanism, not a once-a-year form, with two halves:

- Performance Appraisal — reviewing what you've done, evaluating how you've gone about it, and agreeing objectives for what's ahead.
- Personal Development Plan (PDP) — identifying skills gaps (like automation), mapping the training needed to close them, and supporting your longer-term career.

The PDP half is the "development review/personal development plan process" named in the OCP (see [section 3](#3-your-right-to-training-in-plain-english)). Your PADR is the formal mechanism for your training rights.

### Why it matters

- It connects to pay progression. In many parts of NHS Wales, an up-to-date PADR — with evidence you've met your objectives, demonstrated the right values, and completed mandatory training — is a prerequisite for your next pay increment. Letting it lapse has a real cost.
- It's your written record. A completed PADR documents your objectives, your development plan, and the agreement to support it — the kind of paper trail in [section 17](#17-get-it-in-writing).
- It's ongoing, not annual-only. Treat "at least once a year" as the minimum. Ask for a shorter, informal check-in every quarter while you're building new skills.

### Making the most of your PADR

- Ask your POD/HR contact when your PADR is due, and keep it on schedule.
- Bring your [challenge questions](#5-challenge-questions-for-reflection-coaching-and-honest-exploration) reflections and your draft [personal development plan](#13-building-your-own-cpd--personal-development-plan) to the meeting.
- Ask for automation-related training to be written into your objectives and PDP.
- Ask how your PADR connects to pay progression for your band — confirm this directly.
- Get the outcome of the PADR in writing, and keep your own copy.

### Checklist: your PADR

- [ ] I know when my last PADR happened, and when my next one is due.
- [ ] If it's overdue, I've asked my POD/HR contact to schedule it.
- [ ] I've prepared my reflections and a first-draft personal development plan for the meeting.
- [ ] I've asked for automation training to be included as a specific, written objective.
- [ ] I understand how my PADR connects to pay progression at my band.
- [ ] I've received (and saved) a written copy of the agreed objectives and development plan.
- [ ] I have a date in the diary for my next check-in.

_(PADR processes, forms, and pay progression rules vary between NHS Wales health boards and organisations. Your POD/HR contact or your organisation's staff intranet has the specifics that apply to you.)_

---

## 13. Building your own CPD / personal development plan

A personal development plan (PDP) doesn't need to be a formal document to start. Writing one down, even as a first draft, makes conversations with your POD/HR contact easier and shows your training plan is being taken seriously. This is the same PDP inside your [PADR](#12-your-padr-performance-appraisal-and-development-review) — a living document to revisit regularly.

A simple format:

- Where I am now: the manual testing skills and domain knowledge I already bring.
- Where I want to get to: e.g. "confidently write and maintain Playwright tests for our regression suite."
- How I'll learn it: 2–3 methods from the toolkit above — e.g. one course + a mentor + hands-on practice.
- What support I need from my employer: funded course time, protected study hours, a trial period, access to a mentor.
- How we'll know it's working: a check-in date to review progress.
- How we'll keep it going: a recurring cadence — a brief check-in every quarter, a fuller review every year — so this continues past the current transition.

### Checklist: does my PDP cover the essentials?

- [ ] It names my current skills and experience, alongside my gaps.
- [ ] It has a clear, realistic goal.
- [ ] It lists 2–3 concrete learning methods.
- [ ] It names exactly what support I need from my employer (funded time, mentor, trial period, etc.).
- [ ] It has a first check-in date.
- [ ] It has a recurring review cadence (quarterly or annual).
- [ ] It's been shared with, and agreed by, my POD/HR contact, in writing, ideally as part of my PADR.

Take this to your POD/HR contact to agree formally, through the development review/personal development plan process the OCP names as the mechanism to support this transition. POD/HR own the process and confirm funding, timeframes, and the ongoing cadence.

---

## 14. Setting your own KPIs and OKRs

Beyond the formal PADR process, many people find it motivating to set their own lightweight goals for a skills transition like this, using two simple, well-known frameworks: KPIs and OKRs. Neither needs to be formal or corporate-sounding — think of them as a way to turn "I should probably learn automation" into something concrete you can track and feel good about achieving.

### KPIs: Key Performance Indicators

A KPI is a measurable sign of progress. For your automation journey, useful personal KPIs include:

- Number of manual test cases you've automated, tracked month by month.
- Hours of protected learning/CPD time used per month or quarter.
- Number of courses, videos, or books completed.
- Reduction in regression suite run-time as your automated coverage grows.
- Number of mentoring or pairing sessions attended.

KPIs work best as an ongoing trend to glance at occasionally, rather than a strict target under pressure. They help you see your own progress, especially on weeks when it doesn't feel like much is happening.

### OKRs: Objectives and Key Results

An OKR pairs one inspiring, qualitative Objective with two to four measurable Key Results that show whether you've achieved it. This method started at Intel and spread across the tech industry — part of the same culture you're growing into.

A worked example for a manual tester building automation skills:

> Objective: Become confidently productive writing and maintaining automatic tests for our regression suite.
>
> - Key Result 1: Complete a beginner Playwright, Selenium, or WebDriver course by [date].
> - Key Result 2: Automate 10 existing manual test cases by [date].
> - Key Result 3: Pair with an automation engineer at least twice a month.
> - Key Result 4 (stretch): Sit the ISTQB Foundation or an automation-focused exam by [date].

A good personal OKR is:

- Inspiring and honest — a goal you want, not one you think you're supposed to want.
- Time-bound — usually set for a quarter or two.
- Measurable — each Key Result is a number, a completion, or a clear yes/no.
- Kind to yourself — a stretch, and realistic enough that missing a Key Result is useful information, not a personal failure.

### How this connects to everything else

Your own OKRs and KPIs work alongside the formal process:

- They give you dated evidence to bring to your [PADR](#12-your-padr-performance-appraisal-and-development-review).
- They make your [personal development plan](#13-building-your-own-cpd--personal-development-plan) trackable.
- They give you something satisfying to update in your [written record](#17-get-it-in-writing) of training and progress.

### Checklist: setting your own OKRs/KPIs

- [ ] I've written one honest, inspiring Objective for the next quarter or two.
- [ ] I've defined 2–4 Key Results under it, each one measurable.
- [ ] Each Key Result has an approximate target date.
- [ ] My goals are realistic given my actual workload and protected training time.
- [ ] I've picked one or two ongoing KPIs to casually track (e.g. CPD hours per month, test cases automated).
- [ ] I've shared these with my POD/HR contact or mentor, and linked them to my PDP/PADR.
- [ ] I've put a date in the diary to revisit and revise them — quarterly is a good rhythm.

---

## 15. Using AI as a coach

AI tools (such as Claude, ChatGPT, or Copilot) can be a useful, always-available thinking partner for this transition — for practising explanations, planning, drafting, and rehearsing conversations. Treat AI as a coach, not a decision-maker: your POD/HR contact and your union rep are the people with real authority and accountability for your actual situation.

### Ways to use AI as a coach

- Learning and skills. Ask for a realistic learning plan based on your experience and the time you have, practice quizzes, or plain-English explanations of unfamiliar terms (from [section 7](#7-ways-of-working-youll-meet-along-the-way)).
- Workplace organisational development. Ask AI to explain concepts like your PADR, the KSF, Agile ceremonies, or the OCP's two-thirds test in plain language — a useful starting point, worth checking against the real policy or POD/HR afterwards.
- Conversations with POD/HR and your union rep. Ask AI to help draft an email requesting your overdue PADR, or to role-play a conversation about reasonable adjustments or an ongoing training cadence, so you walk in prepared.
- Planning documents. Ask AI to help draft your personal development plan, your OKRs, or notes from the [challenge questions](#5-challenge-questions-for-reflection-coaching-and-honest-exploration) in section 5.
- Practice for assessments. Ask AI to generate general practice questions in verbal, numerical, or situational judgement styles (see [section 11](#11-psychometric-assessments-what-to-expect-and-how-to-prepare)) — useful practice, not a substitute for official provider materials.
- Summarising dense documents. Ask AI to turn a long policy document into plain English — a helpful starting point, always worth checking against the source.

### A few boundaries worth keeping

- AI is a coach and a thinking partner, not an advocate. POD/HR and your union rep are the people with real authority over your situation.
- Keep sensitive personal, health, or diagnostic information for your organisation's approved, secure systems, where you understand how the data is stored.
- Check your organisation's policy on which AI tools are approved for work use before pasting in anything work-related.
- Treat anything AI tells you about policy specifics — numbers, dates, entitlements — as a starting point. Verify important details against the real published policy, or with POD/HR or your union rep.

### Checklist: using AI as a coach

- [ ] I've asked AI for coaching about what to learn and how to learn.
- [ ] I've asked AI about workplace organisational development, such as what a PADR is, or how ways of working like Agile or DevOps work.
- [ ] I've asked AI how to prepare for conversations with POD/HR and my union rep.
- [ ] I've asked AI to help me draft or rehearse an email, a PDP, or my OKRs.
- [ ] I've asked AI to explain an unfamiliar term or concept in plain English.
- [ ] I've checked my organisation's policy on which AI tools are approved for work use.
- [ ] I've kept sensitive personal or medical information to approved, secure systems only.
- [ ] I've double-checked anything AI told me about policy specifics against the real source, or with POD/HR or my union rep.

---

## 16. Your action checklist, starting today

- [ ] Pick one learning method to start this week — 20 minutes with a free video or a sandbox site counts.
- [ ] Contact your POD/HR team to ask about funded training, mentoring schemes, and how to start a personal development plan.
- [ ] Ask if there's a mentor or automation buddy you could shadow or pair with.
- [ ] Check when your PADR is due and ask for automation training to be written into your objectives — see [section 12](#12-your-padr-performance-appraisal-and-development-review).
- [ ] Draft a first-draft personal development plan using the template in [section 13](#13-building-your-own-cpd--personal-development-plan).
- [ ] Draft a first personal OKR for the next quarter, using [section 14](#14-setting-your-own-kpis-and-okrs).
- [ ] Try AI as a coach for one of your questions or a piece of drafting — see [section 15](#15-using-ai-as-a-coach).
- [ ] Sit with a few of the challenge questions in [section 5](#5-challenge-questions-for-reflection-coaching-and-honest-exploration), and bring what you notice into your next POD/HR conversation.
- [ ] Ask for an ongoing training cadence to be agreed — e.g. quarterly check-ins and a standing annual training budget.
- [ ] Bookmark one free resource from each category in [section 9](#9-your-learning-toolkit-many-ways-to-grow).
- [ ] Sit in on one team ceremony (standup, retro, or similar) to get a feel for the ways of working in [section 7](#7-ways-of-working-youll-meet-along-the-way).
- [ ] Get key agreements in writing — see [section 17](#17-get-it-in-writing).
- [ ] Celebrate small wins. Your first automatic test that runs and passes is a milestone.
- [ ] Talk to a colleague going through the same thing. Shared learning is faster and less lonely.

---

## 17. Get it in writing

This is good practice during any organisational change. It protects everyone involved, including you.

### Checklist: getting things in writing

- [ ] After any verbal conversation with POD/HR about training, timelines, or your role, I send a short follow-up email or chat message summarising what was agreed — "Just to confirm what we discussed today..." is enough.
- [ ] I've asked for my training plan and PADR outcome in writing, including the ongoing cadence.
- [ ] I've saved copies of relevant published policies, job descriptions, role profiles, and any scoring or mapping outcome I've been given, kept somewhere easy to find, like a personal folder or email label.
- [ ] I keep a simple, running log of key dates, training received, and conversations — a handy personal CPD record for my next PADR.
- [ ] I've requested written confirmation of anything important: my mapping outcome, a training plan, a funding approval, a redeployment status change, or an agreed training cadence.
- [ ] When a conversation feels significant, I say: "Would you mind sending that to me in an email as well, so I have it for my records?" — a standard, professional request.

Having things in writing gives your POD/HR team, your union rep, and you a shared record, this year and in the years that follow.

---

## 18. Good questions to ask your POD/HR contact

- What funded training or courses are available to me, and how do I formally request them?
- Can we put together a written personal development plan together, with a realistic timeframe, and can I get a copy of it?
- When is my next PADR due, and can we make sure automation training is written into my objectives?
- How does my PADR connect to pay progression at my band?
- Is there a mentor, buddy, or automation engineer I could shadow or pair with, and is this a recognised scheme?
- Is protected time built in for me to study, practise, or attend training during work hours, and can this be confirmed in writing?
- What would "good progress" look like at 1 month, 3 months, and 6 months, and can we agree that in writing too?
- Going forward, could we agree a regular cadence (e.g. quarterly, or as part of my PADR) for reviewing my training and development?
- Is there a standing annual training or CPD budget I can access every year?
- Are there internal communities of practice or peer groups I could join?
- Could you point me to the published policy or intranet page that covers this?

### Checklist: before the conversation

- [ ] I've written down my questions in advance (this list is a good start).
- [ ] I've sat with a few of the [challenge questions](#5-challenge-questions-for-reflection-coaching-and-honest-exploration), so I can speak to specifics.
- [ ] I know when my PADR is due, and I've prepared what I want in it (see [section 12](#12-your-padr-performance-appraisal-and-development-review)).
- [ ] I know whether I want to bring my union rep to this conversation.
- [ ] I've decided which 2–3 questions matter most to me, in case time is short.
- [ ] I plan to follow up afterwards in writing (see [section 17](#17-get-it-in-writing)).

---

## 19. Looking after yourself: workplace stress and support

Organisational change is stressful, even when it's handled well and even when the news is good. Feeling it is a normal, expected human response.

The UK's Health and Safety Executive (HSE) uses a well-known "Management Standards" framework for work-related stress, covering six areas: demands, control, support, relationships, role, and change. Change is one of the six recognised factors — so if this transition feels stressful, that's a recognised response, and employers have a duty to manage it.

### What you can ask POD/HR for

- A confidential conversation about how you're feeling and what might help.
- A referral to your organisation's Occupational Health service.
- Access to your organisation's Employee Assistance Programme (EAP) — usually free, confidential counselling and support, often available at any time.
- A stress risk assessment if workload or change feels unmanageable — a structured conversation about what's causing pressure and what adjustments could help.
- Reasonable adjustments to workload, deadlines, or working pattern while you're building new skills.

Your union rep can support you in these conversations too, especially if you're unsure how to raise it.

### A few basics

- Naming what feels stressful, specifically, makes it easier to address.
- Telling someone — a colleague, mentor, friend, or family member — how you're feeling helps.
- Struggling with something new is part of learning it.
- Breaking learning into smaller pieces, with realistic deadlines, reduces pressure.

### Checklist: if you're feeling stressed

- [ ] I've named, to myself, what specifically feels stressful right now.
- [ ] I've told someone — a colleague, mentor, friend, or family member — how I'm feeling.
- [ ] I know how to contact my organisation's Employee Assistance Programme (EAP), if available.
- [ ] I know how to request an Occupational Health referral through POD/HR.
- [ ] I've asked POD/HR about a stress risk assessment if things feel unmanageable.
- [ ] I know my union rep can support me in raising workload or wellbeing concerns.
- [ ] I've built at least one small, protected break or boundary into my week.

---

## 20. Neurodiversity, reasonable adjustments, and your paperwork

Neurodivergent traits — including ADHD, autism, dyslexia, and dyspraxia — often bring real strengths to testing and automation work: pattern recognition, sustained focus on detail, structured thinking, and creative problem-solving.

Reasonable adjustments are a right. The OCP requires reasonable adjustments "to posts in accordance with the Equality Act 2010" during selection and redeployment, and the same principle applies to your day-to-day role and training.

### Adjustments that might help

- Extra time, or an alternative format, for any assessment, including psychometric tests (see [section 11](#11-psychometric-assessments-what-to-expect-and-how-to-prepare)).
- Information provided in writing, in advance of meetings.
- A quieter workspace or noise-cancelling headphones.
- Flexible pacing for completing training courses.
- Written instructions alongside verbal ones.
- Regular, predictable check-ins.
- Assistive technology or software.

You can ask for reasonable adjustments with just your own account of what would help — supporting evidence, for example from a GP or specialist, is useful and can help POD/HR put the right support in place, though it's optional. Access to Work, a UK government scheme, can fund workplace adjustments and support for disabled and neurodivergent employees — worth asking POD/HR whether it applies to you.

### How to raise it

- Contact POD/HR directly to ask for a reasonable adjustments conversation, or go through your union rep if that feels easier.
- Share as much or as little detail as you're comfortable with. POD/HR can guide you on any paperwork involved.
- Ask for agreed adjustments to be written into your [PADR and personal development plan](#12-your-padr-performance-appraisal-and-development-review), so they carry forward at each review instead of needing to be renegotiated every time.
- Be specific: how adjustments apply to course pacing, timed assessments, meeting formats, or your working environment.

### Checklist: requesting and documenting reasonable adjustments

- [ ] I've identified what adjustments would help me.
- [ ] I've contacted POD/HR to ask for a reasonable adjustments conversation.
- [ ] I understand what, if any, supporting evidence is useful.
- [ ] I've asked whether Access to Work applies to my situation.
- [ ] I've asked for agreed adjustments to be written into my PADR and PDP.
- [ ] I know I can involve my union rep in this conversation.
- [ ] I know these adjustments can be reviewed and updated as things change.

### Building your reasonable adjustments record

A short, living document — sometimes called a workplace adjustments passport — captures the practical details so everything stays clear and portable, whoever holds the role. Six things are worth pinning down.

1. What you're requesting

- [ ] I've written down, specifically, what I'm asking for (e.g. "25% extra time on timed assessments," "instructions given in writing in advance," "noise-cancelling headphones at my desk").
- [ ] I've noted, briefly, why this helps — useful context for POD/HR, though optional.
- [ ] I've noted whether the request covers training/assessments, day-to-day work, or both.
- [ ] I've noted whether the request is temporary, ongoing, or under review.

2. What POD/HR has agreed to do

- [ ] I have a written summary of what's actually been agreed, not just discussed.
- [ ] I know who is responsible for putting each agreed adjustment in place.
- [ ] I know the start date, and, where relevant, an end or review date.
- [ ] I know what to do if an agreed adjustment isn't happening in practice.

3. Where the information is recorded

- [ ] I know exactly where this is documented (e.g. my PADR, an HR system, an Occupational Health report, a workplace adjustments passport).
- [ ] I have my own copy, saved somewhere I control (see [section 17](#17-get-it-in-writing)).
- [ ] I know how this record carries forward if I change team, project, or role within NHS Wales.

4. Who is authorised to know

- [ ] I know exactly who has been told, and what they've been told (e.g. "POD/HR knows the full detail; my team lead only knows I need instructions in writing").
- [ ] I've agreed that only the minimum necessary detail is shared, unless I choose to share more.
- [ ] I know how my information is stored, and who can access it within POD/HR.
- [ ] I've confirmed this is handled under my organisation's confidentiality and data protection obligations.

5. Union aspects

- [ ] I know whether I want my union rep involved, and at what stage.
- [ ] If involved, my union rep knows what's been requested and agreed, so they can support me if something doesn't happen as planned.
- [ ] I know I can raise it through my union rep if an agreed adjustment isn't honoured.

6. Team aspects

- [ ] I've decided, for myself, what — if anything — I want colleagues to know.
- [ ] If I want the team told, I've agreed with POD/HR who tells them, what's said, and when.
- [ ] If I'd rather keep it private, that's been respected, and adjustments are put in place discreetly.
- [ ] I know I can change my mind about what's shared, later.

---

## 21. Your safety net, briefly

The formal protections are strong, and they're the backup, not the main plan. In short:

- If your role is judged substantially unchanged (two-thirds or more match with your current job), you move into the new structure with a training plan.
- If a suitable role can't be found straight away, you become a Redeployment Candidate, with priority access to vacancies across NHS Wales before they're advertised externally, for around 3 months.
- If you move to a lower-paid post through no fault of your own, your pay is protected for a period based on your length of service — from a few months up to several years for long-serving staff.
- Any disagreement about how the process has been applied to you can be raised through your trade union rep and, formally, the All-Wales Respect and Resolution Policy.
- If you need reasonable adjustments at any point in this process, see [section 20](#20-neurodiversity-reasonable-adjustments-and-your-paperwork).

For full detail on thresholds, timelines, and pay protection tables, see the [official policy document](https://heiw.nhs.wales/files/key-documents/policies/human-resources-policies/all-wales-organisational-change-policy-docx/), or ask your POD/HR contact or union rep for a walkthrough, and ask for the specifics of your own situation in writing.

---

## 22. Where to get support

- Your POD/HR contact or a named HR Case Manager — your primary point of contact for funded training options, your PADR, your personal development plan, and formal process questions.
- Your trade union (e.g. UNISON) — for advice, representation, and help understanding your training plan and rights.
- A mentor or automation-minded colleague — a fast, friendly route into new skills.
- Ministry of Testing and similar global communities — for peer support from testers worldwide who've made this transition.
- Occupational health, your Employee Assistance Programme, or staff counselling services — see [section 19](#19-looking-after-yourself-workplace-stress-and-support); learning something new while things are changing around you is tiring, and support is there to be used.

### Checklist: know who to contact

- [ ] I know who my POD/HR contact is, by name.
- [ ] I've connected with my POD/HR contact directly.
- [ ] I know who my union rep is, by name.
- [ ] I've connected with my union rep directly.
- [ ] I know who my named HR Case Manager is, if I have one.
- [ ] I know how to contact my organisation's Occupational Health service.
- [ ] I know how to contact my organisation's Employee Assistance Programme (EAP).
- [ ] I know who to ask about reasonable adjustments.
- [ ] I have at least one mentor or colleague I can turn to for automation questions.
- [ ] I know how to raise a disagreement formally, if I ever need to (the grievance route).

---

## 23. Sources and further reading

- [NHS Wales Organisational Change Policy](https://heiw.nhs.wales/files/key-documents/policies/human-resources-policies/all-wales-organisational-change-policy-docx/) — the full national policy document (December 2025 edition, approved by the Welsh Partnership Forum), the source for your training rights, the two-thirds test, redeployment, and pay protection.
- [`spec/index.md`](spec/index.md) — the canonical specification of the OCP-derived facts used throughout this guide.
- [`spec/padr.md`](spec/padr.md) — the canonical specification of the PADR process referenced in [section 12](#12-your-padr-performance-appraisal-and-development-review).
- [playwright.dev](https://playwright.dev) and [selenium.dev](https://www.selenium.dev) — official documentation for Playwright and Selenium/WebDriver, the most common automation tools, used by the global testing community.

---

## 24. A note on this guide

This guide leans toward learning and growth, matching the emphasis in the policy and the place where you have the most agency day to day. Three things are worth holding onto: this shift is happening to testers across governments, health services, and industry worldwide; ongoing training is a steady part of your career; and automatic testing is worth being enthusiastic about — better system quality, faster and safer release pace, economic benefit to a stretched public health service, and benefit to the clinicians and patients NHS Wales serves. Your PADR and your own OKRs give this shape. [Section 21](#21-your-safety-net-briefly) covers your formal protections — real, worth knowing, and a safety net rather than the headline. For most manual testers, the story is: new skill, same valuable person, same career, still growing, doing work that makes patient care safer.

Confirm your training plan, timeframe, and entitlements with your POD/HR contact and union rep, and get the important parts in writing. This guide is here to help you walk into those conversations informed and prepared.
