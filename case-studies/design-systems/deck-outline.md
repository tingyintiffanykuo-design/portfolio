# Design systems deck: outline (draft v1)

_Oct 30, 2026. Interview presentation for Amazon Robotics Sr. Product Designer. Structure and prompts by Claude; speaker narrative to be written by the owner._

Working title: **Building shared patterns for complex tools, twice**

Each slide has a **point** (the one thing the slide must land) and **content**. `[NEED]` marks facts still missing. `[REDRAW]` marks visuals to rebuild in English from internal files.

---

## Opening

**1. Title.** Working title, your name, role line: "UX Designer at BenQ (2020-2023) and Trend Micro (2023-2024)."

**2. At a glance**
- Point: two companies, two starting points, one way of thinking.
- Content: Problem / What I did / Key insight / Outcome, one line each for BenQ and Trend Micro. Outcome stays honest: BenQ's system was adopted and is still in use; Trend Micro `[NEED]`.

**3. Why patterns matter in complex tools**
- Point: inconsistency costs users, teams, and the business, not only looks.
- Content: three costs, tied to BenQ's real triggers: customers complained about inconsistency across platforms; design and documentation couldn't keep up with business growth; unrelated-looking products hurt the brand.

## Part 1: BenQ, starting from zero

**4. Context**
- 5 web platforms for K-12 IT (DMS, AMS, IAM, X-Sign Broadcast, X-Sign Signage), one suite, built by different teams.
- `[NEED]` one line on what each does (BenQ page wasn't reachable from here).

**5. The bet: build the system inside a real product**
- Point: we didn't design a system in the abstract. We built DMS and extracted what would repeat.
- Content: the loop: design DMS → spot repeated pieces → generalize → check engineering feasibility and fit with the other 4 platforms → document.

**6. Who owned what**
- Point: clear credit, and makes your part explicit.
- Content: a 3-column ownership map.
  - **Me + [other UX designer, name `[NEED]`]:** bare-bones wireframes, usage guidelines, documentation; components split between us.
  - **Me specifically:** defined the general interaction rules.
  - **GUI designers (names `[NEED]`):** components and tokens (I reviewed and advised).
  - **Engineers:** coded component library.

**7. What's in the system**
- 29 `q-` components grouped into navigation, inputs, data display, and feedback.
- 7 general rule areas: navigation, header, search/filter/sorting, dialog, error page, scroll, onboarding.
- `[REDRAW]` an inventory map.

**8. Anatomy of a guideline**
- Point: guidelines define behavior and states, so engineers and other teams build the same thing.
- Content: one redrawn guideline with callouts: purpose → linked component → annotated example → behavior for each action.
- Example: 4.2, co-editing conflict dialog. `[REDRAW]`

**9. Pattern in depth: search / filter / sort** (candidate)
- Point: one interaction model reused across 5 data-heavy platforms.
- Content: entry → criteria → results states; what had to work for each platform's data; trade-offs.
- `[NEED]` what was debated, alternatives considered, and engineering constraints.

**10. Pattern in depth: error and conflict states** (candidate)
- Point: designing for failure (duplicate data, deleted data, permission limits) site-wide, not screen by screen.
- Why it matters for this JD: reliability and failure states in operational tools.
- `[NEED]` how these cases were found, and whether engineering shaped them.

**11. Iterating the system**
- Point: the system changed as we learned.
- Content: old → new header; old → simplified onboarding; consolidation (alert merged into dropdown, unused toast variants).
- `[NEED]` why each changed.

**12. Feasibility and scale checks**
- Point: every rule passed two filters: can engineering build it, and does it work for the other 4 platforms?
- `[NEED]` one concrete example where a rule changed because of either filter.

**13. Standard work around the system**
- Point: the system needed habits to stay alive. This maps to the JD's "standard work, playbooks."
- Content: first design critique, Figma collaboration norms, design backlog.

**14. Outcome**
- Adopted across the platforms and still in use about 4 years later.
- Qualitative only; no invented metrics.
- `[NEED]` anything verifiable: which platforms use it today, or a public screenshot showing a shared pattern.

## Part 2: Trend Micro, starting from an audit

**15. Context:** 4 automotive cybersecurity platforms; workflows span identify, detect, analyze, recover. `[NEED]` platforms and users.

**16. The audit:** method and findings. `[NEED]`

**17. 11 patterns, organized by `[NEED: workflow stage or component type]`.**

**18. Pattern in depth.** `[NEED]` which one.

**19. Adoption and outcome.** `[NEED]`

## Synthesis

**20. What changed between the two**
- From extracting patterns out of one product → to auditing many products first.
- Possibly from component-first → to workflow-first. Confirm with the Trend Micro answers.

**21. The parallel to robotics maintenance** (reminder: ask for more Trend Micro detail first)
- Mapping identify → detect → analyze → recover onto receive alert → locate → repair → confirm.
- Framed as how you'd approach patterns across robotics programs, not as robotics experience.

**22. How I'd build the next one**
- Point of view, 3-4 principles from your two experiences.
- Owner writes this one.

**23. Limits and honesty**
- Artifacts redrawn for confidentiality.
- No quantitative metrics; based on memory from about 4 years ago.

**24. Thank you / questions**

---

## Appendix (backup slides for Q&A)

- Full component inventory
- Extra guideline examples: dialog cases, error page
- Your design system contribution at Tactile, if any (`[NEED]`: did you create patterns there?)
