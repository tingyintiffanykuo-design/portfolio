# Design systems deck: outline (v2)

_Oct 30, 2026. Interview presentation for Amazon Robotics Sr. Product Designer. Structure and prompts by Claude; speaker narrative written by the owner. v1 replaced; see git history._

`[NEED]` = a detail to fill in while building slides. `[REDRAW]` = an internal artifact to rebuild in English and generically.

## Interview format and priorities (Oct 30, 2026)

**Format:** 1 hour, with 2-3 in-depth case studies → about **12-15 minutes of talking** for this one, plus questions. Built in **Figma Slides**, but only when the owner asks. Slide count doesn't matter; time on each idea does.

**What matters most, ranked:**

| Rank | Content | Time | Why it earns the time |
|---|---|---|---|
| 1 | **The modal / drawer / page standoff → decision tree → one real case run through it** (slides 15-16) | ~4-5 min | Influence without authority, rules over pixels, systems thinking. The moment interviewers will remember and dig into. |
| 2 | **Trend Micro governance: create and apply flows, exception path, build review** (slide 17) | ~2-3 min | Direct match to "scalable mechanisms and reusable patterns that multiply team impact." Few candidates can show this. |
| 3 | **BenQ, compressed:** context, who owned what, one rule's anatomy, the review and release process with engineering and QA (slides 4-6, 8, 9) | ~3-4 min | Scale (5 platforms, still in use), engineering partnership, honest credit. Sets up the growth arc. |
| 4 | **Close: how I'd build the next one, tied to multiple robotics programs** (slides 20-21) | ~1-2 min | Ends on a point of view and connects to the role. |
| 5 | **Opening frame: the problem plus at a glance** (slides 2-3) | ~1-1.5 min | Tells the listener what to watch for. |

**Shrink or merge:**
- Audit and three-layer model (slides 12-13): one slide, ~1 min.
- Context slides: one line each.
- Outcome and limits: a sentence each, said out loud.

**Move to the appendix:**
- Component inventory and rule-area list (slide 7)
- The 11-guideline grid
- Audit comparisons
- Full flow diagrams

**Questions to prepare for** (answers, not slides):
1. "What exactly was yours vs. the team's?"
2. "How did you handle pushback?" (the standoff)
3. "How do you know it worked?" Weakest point; answer honestly and specifically.
4. "What would you do differently?"
5. "How would this apply to robotics?"

## The story in one line (working; owner to put in their own words)

> Consistency at scale is a people problem before it's a pixel problem. I build the shared rules and the process that keeps them alive.

**Three threads** run through both jobs:
1. **Rules, not just components:** behavior, states, and decision criteria.
2. **Process that keeps a system alive:** review, release, contribution, and exceptions.
3. **Influence without authority:** getting designers and engineers to agree.

**Arc:**
- **BenQ:** team effort; built the system from inside one product; fixed how work moved between people.
- **Trend Micro:** solo; audited from outside across products; designed how the system itself grows.

---

## Opening (3 slides)

**1. Title.** Working title: "Building shared patterns for complex tools, twice." Role line: UX Designer, BenQ (2020-2023) and Trend Micro (2023-2024).

**2. At a glance.** Two columns: BenQ | Trend Micro. Rows:
- Starting point: inside one product | audit across 3 products
- My role: team of 2 UX designers | solo
- What I built: general rules, guidelines, release process | 5 pattern + 6 page guidelines, governance process
- Outcome: adopted and still in use | adopted by the design team as the reference; ongoing fixes

**3. The problem behind both.** Inconsistency costs users (customers complained), the team (design and documentation couldn't keep up with growth), and the brand (the products looked unrelated).

## Part 1: BenQ, building from inside a product (7 slides)

**4. Context.** 5 web platforms in BenQ's education suite (DMS, AMS, IAM, X-Sign Broadcast, X-Sign Signage), all built with the same system.

**5. Build the system while building the product.** The loop:
1. Design DMS.
2. Spot repeated pieces.
3. Generalize them.
4. Check two filters: can engineering build it, and does it fit the other 4 platforms?
5. Document it.

**6. Who owned what.**
- **Me:** the general rules.
- **Me + UX peer:** bare-bones wireframes, usage guidelines, documentation; components split between us.
- **GUI designers:** components and tokens; I reviewed them.
- **Engineers:** coded library.

Names `[NEED]`.

**7. What's in it.** 7 rule areas (navigation, header, search/filter/sort, dialog, error page, scroll, onboarding) and 29 components. `[REDRAW]` an inventory map.

**8. Anatomy of a rule.** One redrawn guideline with callouts: purpose → linked component → annotated example → what each action does. Example: the co-editing conflict dialog. `[REDRAW]`

**9. The process that kept it alive.**
- Review and release process across UX, GUI, engineering, PM, and QA:
  - Comments tagged with the spec version
  - Engineers confirm feasibility before a thread closes
  - Changed areas marked so QA sees what's new in each release
- Plus the first design critique and Figma norms.

`[REDRAW]` the flow.

**10. Outcome and what I took forward.**
- Adopted across the platforms and still in use.
- Lesson: the path for changing the system existed, but it wasn't documented clearly. This sets up Part 2.

## Part 2: Trend Micro, building from an audit (8 slides)

**11. Context and why I started.** 3 automotive cybersecurity products (xNexus, xZETA, SUMO). As a new designer, I saw inconsistencies in design reviews, and my manager had wanted this initiative for a while.

**12. The audit.**
- Method for each feature or pattern: purpose → compare all 3 products → benchmark (Vision One, Carbon, Ant, Adobe) → open questions.
- Honest about limits: "I don't know the rationale behind most designs yet."

`[REDRAW]` one comparison.

**13. A three-layer model.** Features/pages → patterns → components (Tonic). My work was the top two layers: how components combine into consistent behavior.

**14. From observation to reasoning.** I reviewed every guideline with each product's designer and used public systems as supporting evidence. `[NEED]` one thing that changed my view (owner deferred this to slide building).

**15. The hardest call: modal vs. drawer vs. page.**
- **Conflict:** every designer used them differently, with their own reasons, and resisted change.
- **Move:** stop debating answers; get agreement on the decision points first.

**16. The decision tree.** `[REDRAW]` the full tree, then 1-2 real cases run through it, e.g. Anomaly Events → View in Rule Management. Once the criteria were agreed, subjective arguments stopped carrying weight.

**17. Governance: how the system grows.** Two linked flows:
- **Create:** audit → propose → review → document → release → apply everywhere.
- **Apply:** follow the guideline, or propose a change. If the change doesn't apply to every product, record it as a local exception. A build review feeds technical limits back into the guideline.

`[REDRAW]`

**18. Outcome and honest limits.**
- 5 pattern and 6 page guidelines.
- Designers fixed misaligned designs after each review, alongside urgent work; adoption wasn't tracked.
- Some items were still open when I left.

## Synthesis (4 slides)

**19. What changed between the two.** Table: starting point / scope / layer / governance / influence.

**20. Parallel to robotics maintenance tools.** `[NEED]` owner input when building (reminder in `PROGRESS.md`).
- Candidate bridge: decision criteria plus governance carried across several robotics programs ("multiply team impact").
- Possibly the detect → act flow.
- Present it as a parallel, not as robotics experience.

**21. How I'd build the next one.** 3-4 principles, written by the owner. Candidates from the evidence:
- Audit before you build.
- Agree on criteria before answers.
- Design the contribution and exception paths from day one.
- Close the loop with build review.

**22. Limits.** Artifacts redrawn; no quantitative metrics; adoption described qualitatively.

**23. Thank you / questions.**

## Appendix (backup slides for Q&A)

- Full BenQ component inventory and the 7 rule areas
- All 11 Trend Micro guidelines in a grid
- Another guideline in depth (loading or empty state)
- Full collaboration practice flows from both companies
