# Project Charter: Simulacra — Behavioral Simulation of Neighborhood Residents for PED Interventions

| | |
|---|---|
| **Client** | Jeroen Veen, Researcher HAN — Future Energy (FyE) Research Group |
| **Team** | 3 students, Minor Data Driven Decision Making in Business |
| **Project** | P3 (Exploring) |
| **Charter presented** | 2 September 2026 |
| **Team allocation by preference** | week of 7 September 2026 |
| **Kick-off / meet & greet with client** | 9 September 2026 |
| **Final presentation** | 14 January 2027 |
| **Starter document** | [Understand Electrification — Diana Gragg, Stanford Understand Energy](https://youtu.be/lOOQVyNERrs) |

## 0. Starter Document: The WHY of the Energy Transition

As an introduction to this project, the team watches the lecture *"Understand Electrification"* by Diana Gragg (Stanford Understand Energy, recorded June 2026). The lecture explains what electrification means — shifting space heating, water heating, industry, and mobility from fossil fuels to electricity — through the examples of heat pumps and electric vehicles, and discusses the benefits (efficiency, energy security, health) and the challenges (grid capacity, investment cost, reliability, tariff structure) involved.

What is interesting for this project is that the lecture keeps bringing the technology back to **behavior**: electrification only pays off if people actually participate. A "virtual power plant," for example, only works if households are willing to shift their electricity demand to cheaper, sun-rich hours of the day — exactly the kind of grid-aware charging behavior that is central to the FyE case study. And the lecture shows that high upfront investment costs (for a heat pump or a charging point, for instance) form a barrier that is not equally easy for everyone to overcome, which directly relates to energy poverty and unequal participation.

**Relevance to this project:** the lecture substantiates the assumption behind P3 — that the technology of the energy transition (dynamic tariffs, grid-aware charging, solar panels, a neighborhood battery) only works if residents adapt their behavior, and that such behavior is far from a given. Those who cannot afford an upgrade drop out (split incentive, energy poverty); those who feel no direct incentive to shift their usage do not participate (free-riding, low participation). These are exactly the behavioral obstacles that the simulacra personas in this project must surface as hypotheses — grounded in realistic, neighborhood-seeded personas rather than in an assumption that everyone will simply respond "rationally" to the technology.

### Kick-off Assignment: Reflection Questions (Week 1)

After watching the video, each team member answers the following three questions individually, then discusses the answers together as input for the week-1 persona set and hypothesis list:

1. The lecture shows that electrification only pays off if people actually participate (e.g. a virtual power plant, shifting demand to cheap hours). Which of your three starter personas would realistically participate, and which would not — and why?
2. Upfront investment cost is named as a major barrier. How would you translate that barrier into a concrete behavioral hypothesis (free-riding, split incentive, low participation) for a specific persona?
3. The video treats electrification mainly as a technical/economic story. What behavioral nuance would you add to it when you let your AI persona react to one intervention (e.g. a dynamic tariff) — what might that reveal that the lecture does not address?

## 1. Background

Many obstacles to a Positive Energy District (PED) do not arise from technology or ownership, but from **behavior**: who participates — or does not — in a dynamic tariff, grid-aware charging, solar panels, or a neighborhood battery, and why? That behavior is hard to measure directly, but it can be explored with a lightweight simulation: AI personas ("simulacra") that respond qualitatively to interventions based on neighborhood data, surfacing hypotheses about behavioral obstacles (free-riding, split incentive, low participation).

Many of these obstacles are not new — they map onto well-studied dynamics in **game theory and behavioral economics**: free-riding and low participation are classic collective-action / public-goods problems (e.g. for a shared neighborhood battery), split incentive is a textbook principal-agent problem (e.g. between landlords and tenants), and reluctance to adopt a dynamic tariff or a heat pump often reflects present bias, loss aversion, or status quo bias rather than a simple cost-benefit calculation. Naming these mechanisms explicitly — not just describing the symptom — is what should make this project's hypotheses sharper and more transferable to other neighborhoods.

This project is a **serious-game/scenario lens**: explicitly a thinking tool, not a predictive model. It stands on its own at the start (to be picked up independently as an MVP), but has a growing relationship with P1/P2: the ontology and obstacle categorization that team builds can later enrich this project, and conversely the behavioral hypotheses from this project feed into P1's obstacle picture.

## 2. Objective

Build and iteratively refine **a first running simulacra system**: a working application in which AI personas — starting from plausible, general assumptions in week 1 and seeded on the neighborhood's reality (housing stock, energy labels, share of energy poverty, daily load curve) once data-lake access is arranged — can be simulated against one or more interventions on demand, rather than through one-off manual prompting, and produce a logged, qualitative response. Where relevant, persona decision-making is grounded in a recognized game-theoretic dynamic (e.g. a free-rider/collective-action structure for a shared asset, or a principal-agent/split-incentive structure between landlords and tenants) or a behavioral-economics bias (e.g. present bias, loss aversion, status quo bias), rather than relying solely on open-ended narrative. Each iteration of that system is tested through evaluation sessions with students from other FyE projects (Jeroen Veen's Computer Vision minor, and Master Applied Data Science students), and all learnings are logged.

By the end of the semester, the team delivers:
1. a **first running version of the simulacra system**, working end to end and demonstrable live — selecting a persona and an intervention produces a logged, qualitative response; and
2. a substantiated analysis of **what data would be needed to build a full digital twin of the neighborhood** — as a stepping stone for a follow-up team in a future semester, possibly in combination with the work of P1/P2.

![Concept illustration of a simulacra simulation interface, showing an agent-status panel, an energy-management readout (dynamic tariff, grid-aware charging, solar output, neighborhood battery), and a wealth-preservation metric over an isometric neighborhood view.](simulacra.png)

*Vision, not a spec: this mockup illustrates one possible direction for the running system's interface — a persona-status panel, live energy-management readouts, and an outcome metric. It is a spark, not a spec: the team decides what the interface actually becomes, and is encouraged to imagine further than what's shown here.*

**A note on ambition:** everything in this charter is a floor, not a ceiling. The reflection questions, the quick win, the running system, the game-theoretic/behavioral-economics grounding — these mark where to start and what "done" minimally looks like, not how far to go. The architecture, the depth of the behavioral modeling, and the shape the running system eventually takes are the team's own calls to make and defend. Treat obstacles — technical, theoretical, or in scheduling evaluation sessions — as puzzles to work through, not reasons to scale back; figuring them out is the point of an exploratory project like this one. And this is not an academic exercise in a vacuum: it feeds a real research group's understanding of a real neighborhood's energy transition, and a future team may build on exactly what this one leaves behind.

## 3. Scope

**In scope**
- A first running simulacra system: a genuine interactive application — not just a notebook or a no-code tool — built with the help of AI-assisted coding tools (e.g. Claude Code, Cursor, or similar), in which a persona and an intervention can be selected, a qualitative response is generated, and every run is logged automatically for later analysis.
- A set of resident personas, seeded on aggregate distributions of the neighborhood (housing stock, energy labels, share of energy poverty, daily load curve).
- AI-driven qualitative responses from personas to one or more interventions (dynamic tariff, grid-aware charging, solar panels, neighborhood battery), produced by the running system.
- Identification of behavioral obstacles as hypotheses (free-riding, split incentive, low participation, etc.), including how that picture shifts under different policy choices.
- Grounding persona decision-making, where relevant, in recognized game-theoretic dynamics (e.g. the free-rider/collective-action problem for a shared neighborhood battery, a principal-agent/split-incentive problem between landlords and tenants) and behavioral-economics biases (e.g. present bias/hyperbolic discounting, loss aversion, status quo bias, social norms), instead of relying only on open-ended LLM narrative.
- A short mapping of the behavioral obstacles observed to the game-theoretic dynamic or behavioral-economics bias that best explains each one.
- Iterative refinement of the system, its personas, and its scenarios based on external evaluation sessions.
- A learning log capturing all iterations, evaluation outcomes, and adjustments.
- A final document describing the data needed for a full digital twin of the neighborhood.

**Out of scope**
- A polished, production-grade, or publicly deployed application — the system only needs to run reliably enough to demonstrate the core loop live.
- Formal, mathematically rigorous game-theory proofs or empirically calibrated behavioral-economics parameters — these mechanisms are used as illustrative, hypothesis-generating lenses, not as a validated economic model.
- Statistically validated behavioral models or quantitative predictions.
- Actual validation with real residents (this project specifically identifies what would still need to be verified with residents — that verification itself is follow-up work).
- Building the digital twin itself — this project delivers the data-needs analysis, not the twin.

## 4. Research Questions

1. Build a set of resident personas seeded on the neighborhood's reality and let them — AI-driven — respond qualitatively to one or more interventions.
2. Which behavioral obstacles emerge as hypotheses (who would drop out, and why)? How does the picture shift under different policy choices?
3. What does this say about public support and design — which intervention seems feasible not only technically/financially but also behaviorally, and what therefore needs to be verified with residents?
4. Which of the behavioral obstacles you observe can be explained by a recognized game-theoretic dynamic (e.g. free-riding, a principal-agent/split-incentive problem) or a behavioral-economics bias (e.g. present bias, loss aversion, status quo bias) — and does naming that mechanism change how you would design the intervention?

## 5. Deliverables

| # | Deliverable |
|---|---|
| 1 | Week 1 quick win: 3 illustrative personas built from plausible, general assumptions rather than real neighborhood data — no data-lake access exists yet (e.g. energy-poor renter / homeowner / young family with EV), qualitative response to a dynamic tariff, first list of behavioral-obstacle hypotheses (manual/prompt-based, ahead of the running system) |
| 2 | First running version of the simulacra system: a working, interactive application — built with AI-assisted coding tools — that simulates persona responses to at least one intervention, with a usable interface and logging built in |
| 3 | A short mapping of observed behavioral obstacles to the game-theoretic dynamics and/or behavioral-economics biases that explain them, reflected in how at least one persona reasons about an intervention |
| 4 | Successive iterations (V2, V3, …) of the system, its persona set, and its intervention scenarios |
| 5 | At least 2–3 external evaluation rounds with students from the Computer Vision minor and/or Master ADS, run against the working system, each documented |
| 6 | Learning log: per iteration, what was changed, why, and what the evaluation revealed |
| 7 | Final analysis: what data is needed for a full digital twin of the neighborhood |
| 8 | Handover document for a follow-up team in the next semester, including the system's source/setup instructions and any touchpoints with the P1/P2 ontology/access layer |
| 9 | Final presentation on 14 January 2027, including a live demo of the running system |

## 6. Approach and Phasing

> When planning, account for the regular HAN academic breaks (autumn and Christmas holidays) that fall within this period.

This project runs on an **iterative core loop**, not linear phases:

1. (Re)define personas based on the best available neighborhood information — plausible, general assumptions before data-lake access is arranged, real aggregate data once it is.
2. Simulate AI-driven qualitative responses to an intervention.
3. Log behavioral obstacles as hypotheses.
4. Plan and run an external evaluation session with Computer Vision minor and/or Master ADS students.
5. Refine based on feedback → back to step 1.

Overall timeline:
- **Phase 0 — 9 September 2026 (kick-off):** meet & greet with the client, team contract, task division, kick-off assignment (see section 0).
- **Phase 1 — week 1 (from 9 Sept):** quick win: 3 personas built from plausible, general assumptions — no data-lake access exists yet — one intervention, first hypothesis list, done manually/via prompting. A tight, well-understood first pass through the core loop — the launchpad the team builds from all semester, not a limit on where it can go — and the direct input for the running system's first version.
- **Phase 2 (± week 2–8):** once data-lake access is arranged, validate and refine the week-1 personas against the real aggregate distributions; build the first running version of the simulacra system on top of that; first 1–2 iteration rounds of that system including external evaluation session(s); expand to multiple interventions and policy choices.
- **Phase 3 (± week 9–14):** further iterations of the running system, second/third evaluation round, deepen the behavioral-obstacle hypotheses and the public-support question.
- **Phase 4 (± week 15–17):** synthesize all learning logs, draft the digital-twin data-needs analysis, freeze and stabilize the system for a reliable live demo.
- **Phase 5 (± week 18):** finalize documentation and handover (including the system's source/setup instructions), dry run of the live demo, final presentation on 14 January 2027.

**Note — scheduling dependency:** the evaluation sessions with the Computer Vision minor and the Master ADS students depend on their schedules/calendars. Plan this early in consultation with Jeroen Veen and allow for at least 2–3 sessions spread across the semester.

## 7. Team and Roles

Team of 3 students. The team owns its own role division and working process — the split below is a starting point to adapt, not a fixed structure to follow:
- **Persona/data lead** — builds the week-1 personas from plausible, general assumptions, then translates aggregate distributions (energy labels, energy poverty, load curves) into realistic personas once data-lake access is arranged, and grounds each persona's decision logic in a relevant game-theoretic dynamic or behavioral-economics bias where applicable.
- **AI/system-build lead** — uses AI-assisted coding tools to build and maintain the running simulacra system (persona simulation logic, a usable interface, intervention selection, response generation and logging), refining it each iteration.
- **Evaluation & logging lead** — coordinates the external evaluation sessions with Computer Vision minor/Master ADS students and maintains the learning log.

## 8. Stakeholders

- Jeroen Veen — client/researcher HAN.
- The team's assigned M3DM supervising lecturer (coach) — every project team gets one from the minor; a genuine stakeholder to involve in decisions, not just an academic assessor to report status to.
- Students of the Computer Vision minor (also run by Jeroen Veen) — evaluation partner.
- Students of the Master Applied Data Science — evaluation partner.
- The P1/P2 team — potential exchange of ontology/obstacle categorization; not a hard dependency at the start.
- A possible follow-up team in the next semester, which uses the digital-twin data-needs analysis as a starting point.

This list is a starting point, not a ceiling: the team is encouraged to actively bring in additional stakeholders as the project develops — other neighborhood or energy-sector contacts, other HAN research groups, anyone with a real stake in the outcome — rather than treat it as fixed.

## 9. Constraints and Assumptions

- Aggregate distributions for Elsweide (housing stock, energy labels, share of energy poverty, daily load curve) become available once data-lake access is arranged, early in the semester — not from day one, so the week-1 personas are necessarily built on plausible, general assumptions rather than this data.
- AI tooling is available to drive persona simulation/response.
- AI-assisted coding tools (e.g. Claude Code, Cursor, or similar) are available to the team, making it realistic for students without a software-engineering background to build a genuine interactive application within the semester — the ambition is a proper working system, not just a notebook or no-code tool, though it still does not need to be production-hardened or publicly deployed.
- External evaluation groups (Computer Vision minor, Master ADS) are — in consultation with Jeroen Veen — actually schedulable within the semester; this must be confirmed early, not assumed.
- Basic game-theory and behavioral-economics concepts (e.g. the free-rider problem, principal-agent problems, present bias, loss aversion, status quo bias) are treated as illustrative, textbook-level lenses; the team is not expected to have prior formal training in economics.

## 10. Risks

| Risk | Impact | Mitigation |
|---|---|---|
| Team is new to building software | Could slow the initial build, even with AI-assisted coding tools | Treat this as a skill to build, not a blocker: lean on AI-assisted coding tools (e.g. Claude Code, Cursor) to accelerate learning; ship one persona flow working end to end early, then grow the system's ambition from that solid base |
| The team's ambition for the running system outpaces what fits in a semester | Half-built features, an application that cannot be reliably demoed | Sequence the ambition deliberately: get the core loop (select persona + intervention → generate and log a response) rock-solid first, then treat richer features (multi-persona views, a hypothesis dashboard, etc.) as the next challenge to take on, not as optional extras to skip |
| Calendars of Computer Vision minor/Master ADS do not align | Fewer or delayed evaluation rounds, fewer iterations | Lock in evaluation moments with Jeroen Veen as early as phase 0 |
| Scope drifts toward polishing the application instead of generating and testing behavioral hypotheses | Loss of time, project becomes an engineering exercise rather than a research one | Explicitly hold on to the "thinking tool" character; the application is the vehicle for hypotheses, not the end goal in itself |
| Team has no prior background in game theory/behavioral economics | Concepts applied superficially or incorrectly, undermining the credibility of the hypotheses | Treat the theory as something to learn and apply quickly, not avoid: start from well-established, textbook-level concepts (free-rider problem, principal-agent problem, present bias, loss aversion, status quo bias) and pressure-test understanding against a concrete Elsweide scenario |
| Personas reflect LLM bias rather than neighborhood reality | Hypotheses become unusable or misleading | Explicitly seed and test personas against aggregate data, not solely on LLM assumptions |
| No real resident validation | Hypotheses risk being overstated as "fact" | Explicitly state in every learning log and the final presentation what still needs to be verified with residents |
| Learning log is not maintained during iterations | The final analysis (digital-twin data needs) lacks substantiation | Logging is a fixed part of every iteration step, not reconstructed afterward |

## 11. Success Criteria / Definition of Done

- A first running simulacra system exists — a genuine interactive application, not just a notebook or script — and can be demonstrated live: selecting a persona and an intervention produces a logged, qualitative response.
- At least one behavioral obstacle is explicitly explained through a named game-theoretic dynamic or behavioral-economics bias, with that reasoning reflected in a persona's decision logic or the learning log.
- At least 3 personas, traceably seeded on aggregate data.
- At least 2–3 documented external evaluation rounds with Computer Vision minor and/or Master ADS students, run against the working system.
- A complete and traceable learning log across all iterations.
- A substantiated final document with concrete data needs for a neighborhood digital twin, usable as a starting point for a follow-up team.
- The final presentation on 14 January 2027 addresses all three P3 research questions and includes a live demo of the running system.

These are the floor for what "done" looks like, not the ceiling — where the team takes the running system, the personas, and the theory beyond this list is entirely its own to decide and defend.

## 12. Communication and Meetings

- Short iteration cycles (e.g. biweekly) with accompanying logging.
- Regular check-ins with the client and the supervising lecturer, not only at fixed evaluation moments.
- Early and ongoing coordination with Jeroen Veen on scheduling cross-project evaluation sessions.
- One touchpoint with the P1/P2 team on any overlap between the ontology/access layer and the behavioral simulation.
- Promote the team's work — and that of its stakeholders — within and outside HAN (e.g. through the minor's own channels, HAN communications, LinkedIn, or other PR opportunities); this is an explicit part of the project's value, not an afterthought, and something the team is expected to actively pursue.
- Final presentation on 14 January 2027.
