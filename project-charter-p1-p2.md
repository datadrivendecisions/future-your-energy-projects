# Project Charter: From Data Lake to Queryable Knowledge — Ontology and Agent-Ready Access

| | |
|---|---|
| **Client** | Jeroen Veen, Researcher HAN — Future Energy (FyE) Research Group |
| **Team** | 4 students, Minor Data Driven Decision Making in Business |
| **Projects** | P1 (Structuring) + P2 (Making Accessible) |
| **Charter presented** | 3 September 2026 |
| **Team allocation by preference** | week of 7 September 2026 |
| **Kick-off / meet & greet with client** | 10 September 2026 |
| **Final presentation** | 14 January 2027 |
| **Starter document** | [Understand Electrification — Diana Gragg, Stanford Understand Energy](https://youtu.be/lOOQVyNERrs) |

## 0. Starter Document: The WHY of the Energy Transition

As an introduction to this project, the team watches the lecture *"Understand Electrification"* by Diana Gragg (Stanford Understand Energy, recorded June 2026). The lecture explains what electrification means — shifting space heating, water heating, industry, and mobility from fossil fuels to electricity — through the examples of heat pumps and electric vehicles, and discusses both the benefits and the challenges involved.

The core argument: electrification is attractive because the same energy service (heat, transport) is often delivered three to four times more efficiently through electricity, resulting in less air pollution at the point of use, less dependence on any single fuel or country, and a system that gets cleaner over time even while the appliance (heat pump, car) stays in service for fifteen to twenty years. But that same shift runs into real constraints: the grid must be able to absorb growing demand, electrification often requires costly upfront investment, reliability becomes more important once households depend on a single system, and how electricity tariffs are structured determines whether the transition unfolds fairly.

**Relevance to this project:** this exact tension between opportunity and obstacle is what the FyE data-lake case study Elsweide is about. Grid capacity and smart/grid-aware charging (a recurring theme in the video, framed as "being smart about when and where you add demand to the grid") are literally one of the data sources in the data lake. The investment barriers and tariff structures discussed in the video map onto the economic/business-case and social/support obstacle categories; the reliability and climate risks map onto the climate-risk & living-environment category. This team must make that web of relationships explicit — which concept relates to which obstacle, and which source substantiates it — in the ontology (P1), and then make it queryable through a natural-language interface (P2) so that a resident, policymaker, or grid operator can ask about it in plain language.

### Kick-off Assignment: Reflection Questions (Week 1)

After watching the video, each team member answers the following three questions individually, then discusses the answers together as input for the week-1 concept map:

1. At this point you have no access to the data lake itself — only this charter and the lecture. This charter already names six obstacle categories (grid/technical, ownership & organization, social support, permitting & spatial planning, economic/business case, climate risk & living environment). Based only on those categories and the lecture, which grid-capacity, cost, and reliability themes from the video do you expect to map onto which category — and for which theme do you suspect there may be no matching FyE source at all yet? Treat this as a first, testable guess at a blind spot, to be checked once you get access to the data lake.
2. The lecture argues that electrifying now can be worthwhile even without an immediate benefit, because the grid gets cleaner over time while the appliance keeps running. How would you capture that kind of "yes, but" nuance as a relation between a concept and an obstacle in an ontology, without it becoming a vague or misleading link?
3. If a resident, a grid operator, and a policymaker each asked the natural-language assistant a question inspired by the video (e.g. "why would a heat pump help here?", "does the grid have room for this?", "what would this cost me upfront?"), what would a good, sourced answer look like for each — and where do you expect the assistant to fail?

## 1. Background

Within FyE, work is underway on the energy transition in residential neighborhoods. For this purpose, a **data lake** exists: a collection of raw, unstructured data sources (grid capacity, cadastral parcels, liveability/energy poverty, zoning plans, climate-effect atlas, research agenda/business case) with no predefined database model. Meaning only emerges once you ask a question of it.

The 3DMiB challenge focuses on two layers needed to make that data lake usable:
- the **meaning layer**: what do the data mean, and which concepts and obstacles exist?
- the **access layer**: how do you query it in plain language?

P1 and P2 are a continuation of one another: without an explicit ontology (P1), there is no reliable foundation on which to build and test an agent/LLM wiki (P2). This team therefore takes on both projects together, as one continuous development track.

## 2. Objective

Deliver a working proof-of-concept in which:
1. the data lake is semantically structured through a defensible domain ontology (concepts + obstacles, layer A and layer B), applied to the Elsweide case;
2. that same ontology forms the basis for an agent-ready, natural-language interface to the data lake, which shows a source with every answer;
3. it is explicitly tested and documented where that interface works and where it breaks (factual correctness assessed separately from the presence of a citation, hallucination, stakeholder differences).

Besides a working PoC, a **well-maintained, documented repository** is an explicit end result, so that a following semester can build directly on this work (see also the link with P3, section 8).

**A note on ambition:** everything in this charter is a floor, not a ceiling. The ontology, the interface, the evaluation framework, the repository — these mark the minimum bar for "done," not a limit on how far the team can take this. The architecture, the depth of the ontology, and how rigorously the interface is tested are the team's own calls to make and defend in the final presentation. Treat unresolved questions — a blind spot with no obvious source, a stakeholder question the assistant keeps getting wrong — as puzzles worth chasing down, not problems to work around. This is a real research group's data lake: the ontology and the interface the team builds could genuinely be used by a resident, a policymaker, or a follow-up team next semester, not just graded and shelved.

## 3. Scope

**In scope**
- Domain ontology (layer A) for the Elsweide neighborhood-energy case: concepts, their relationships, and the mapping of each concept to the FyE data source(s) that populate it.
- Obstacle layer (layer B): obstacles categorized as grid/technical · ownership & organization · social support · permitting & spatial planning · economic/business case · climate risk & living environment.
- Explicit analysis of the interplay between concepts and obstacles, and of blind spots (a concept/obstacle without a source).
- Design and build of a no-code/low-code AI interface (e.g. NotebookLM-style, or a lightweight RAG/agent setup) on top of the data lake.
- Evaluation framework: score each answer on (a) is the number correct, (b) is there a source, (c) does it hallucinate — scored separately.
- Design of a stakeholder-specific interface (a resident vs. a grid operator vs. a policymaker ask different things).
- Exploratory review of data licenses versus the AI tools used.
- Documentation: ontology schema, architecture diagram, evaluation table, README, and handover notes.

**Out of scope (unless time permits)**
- Production hardening, security hardening, or scaling beyond Elsweide.
- Exhaustive legal license research (only an initial risk scan).
- Behavioral simulation with AI personas — that is P3.
- Actually building a digital twin — a possible follow-up project after this semester.

## 4. Research Questions

**P1 — Structuring**
1. Which concepts exist in the neighborhood in the energy domain (building, grid asset, household, energy flow, ownership, …), and which FyE data source populates each concept?
2. Which obstacles stand in the way of realizing a PED (Positive Energy District)? Organize them into clear categories.
3. How do concepts and obstacles relate to each other, and where is there a blind spot — a concept/obstacle with no source?

**P2 — Making Accessible**
1. Can you build a no-code AI assistant that answers neighborhood questions and shows a source with each answer? How do data licenses relate to the tools used?
2. Where is the answer correct, and where does the tool produce a citation-decorated wrong answer — and why? The correctness of the number is scored separately from the presence of a citation.
3. What does a stakeholder-specific interface look like?

## 5. Deliverables

| # | Deliverable | Linked to |
|---|---|---|
| 1 | Elsweide concept map (concepts + obstacles, tested against 3 concrete data anchors) | Week 1 quick win, P1 |
| 2 | Evaluation table: 3–5 snapshot documents in NotebookLM, 5 stakeholder questions, scored on correctness/source/hallucination | Week 1 quick win, P2 |
| 3 | Defensible domain ontology (layer A) with explicit relationships | P1 |
| 4 | Obstacle layer (layer B) with categorization and blind-spot analysis | P1 |
| 5 | Working PoC: natural-language interface to the data lake with source attribution | P2 |
| 6 | Detailed evaluation report (correctness/source/hallucination, per question type) | P2 |
| 7 | Design of stakeholder-specific interfaces | P2 |
| 8 | License risk scan: data sources vs. AI tools used | P2 |
| 9 | Maintained repository: README, architecture, ontology schema, evaluation data, handover notes | P1 + P2 |
| 10 | Final presentation on 14 January 2027 | P1 + P2 |

## 6. Approach and Phasing

> When planning, account for the regular HAN academic breaks (autumn and Christmas holidays) that fall within this period.

- **Phase 0 — 10 September 2026 (kick-off):** meet & greet with the client, team contract, task division, kick-off assignment (see section 0).
- **Phase 1 — week 1 (from 10 Sept):** quick wins for P1 (concept map) and P2 (NotebookLM evaluation table) in parallel. This is not yet an ontology — only once relationships and the layer-A/layer-B split are made explicit and defended does it become one.
- **Phase 2 (± week 2–6):** deepen and defend the ontology (layer A/B, interplay, blind spots); architecture design for the access layer starts as soon as the concept set is stable enough.
- **Phase 3 (± week 7–12):** build the PoC of the agent/AI interface on top of the (interim) ontology; test iteratively with representative stakeholder questions.
- **Phase 4 (± week 13–16):** finalize evaluation, refine stakeholder-specific variants, complete the license scan and blind-spot analysis.
- **Phase 5 (± week 17–18):** finalize documentation and repository handover, dry run, final presentation on 14 January 2027.

## 7. Team and Roles

Team of 4 students. The team owns its own role division and working process — the split below is a starting point to adapt, not a fixed structure to follow:
- **Ontology/domain lead** — owns layer A/B and the concept–obstacle interplay.
- **Data-integration lead** — links data sources to concepts, oversees the blind-spot analysis.
- **AI/architecture lead** — designs and builds the agent/AI interface.
- **Evaluation & documentation lead** — owns the measurement instrument (evaluation table) and the quality of the repository/documentation.

All four members contribute to both P1 and P2, given the substantive dependency between them.

## 8. Stakeholders

- Jeroen Veen — client/researcher HAN (owner of the research question and the data lake).
- The team's assigned M3DM supervising lecturer (coach) — every project team gets one from the minor; a genuine stakeholder to involve in decisions, not just an academic assessor to report status to.
- Proxy stakeholders for the agent interface: resident, grid operator, policymaker (via representative questions; real interviews are not required but recommended where possible).
- The P3 team (behavioral simulation) — potential exchange: P3 may later use the ontology/access layer; this team does not need to actively wait for that at the start.
- A possible follow-up team in the next semester, which can build further on this work (and the outcomes of P3) toward a digital twin of the neighborhood.

This list is a starting point, not a ceiling: the team is encouraged to actively bring in additional stakeholders as the project develops — other neighborhood or energy-sector contacts, other HAN research groups, anyone with a real stake in the outcome — rather than treat it as fixed.

## 9. Constraints and Assumptions

- Access to the FyE data-lake sources is arranged at the start of the project.
- The required no-code/low-code AI tooling (e.g. NotebookLM) is available under HAN licenses.
- Elsweide is the fixed focus area for the quick win and the first ontology iterations; scaling to other neighborhoods is optional.

## 10. Risks

| Risk | Impact | Mitigation |
|---|---|---|
| Ontology scope grows out of control (too broad/too detailed) | Delay, no defensible result | Scope early to Elsweide and the 6 obstacle categories; keep the explicit layer-A/layer-B split |
| LLM hallucinates or gives citation-decorated wrong answers | Undermines credibility of the PoC | Apply the evaluation framework from week 1; always score correctness separately from citation |
| Data licenses conflict with chosen AI tools | Legal/ethical risk, PoC cannot be shared | License scan early in the project, not just at the end |
| Unclear division of roles between P1 and P2 tasks | Work falls through the cracks | Lay down role division explicitly in the team contract, adjust weekly if needed |
| Repository/documentation only addressed at the end | Insufficient time for a proper handover | Documentation is ongoing work from phase 2 onward, not only in phase 5 |

## 11. Success Criteria / Definition of Done

- The ontology (layer A/B) is explicit, substantiated, and defensible in the final presentation.
- The PoC answers a representative set of stakeholder questions, with a transparent score on correctness, source attribution, and hallucination.
- Blind spots in the data lake are identified and substantiated.
- The repository is documented well enough that a new team can onboard without verbal explanation (README, architecture, ontology schema, evaluation data).
- The final presentation on 14 January 2027 addresses both the P1 and P2 research questions.

These are the floor for what "done" looks like, not the ceiling — where the team takes the ontology, the interface, and the repository beyond this list is entirely its own to decide and defend.

## 12. Communication and Meetings

- Weekly short check-in with the client and the supervising lecturer on progress and blockers.
- One interim progress presentation (timing to be agreed, e.g. around phase 3).
- Touchpoint with the P3 team on any potential link between the ontology/access layer and the behavioral simulation.
- Promote the team's work — and that of its stakeholders — within and outside HAN (e.g. through the minor's own channels, HAN communications, LinkedIn, or other PR opportunities); this is an explicit part of the project's value, not an afterthought, and something the team is expected to actively pursue.
- Final presentation on 14 January 2027.
