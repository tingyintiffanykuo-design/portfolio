# Design Systems Deck: Phase 1 Blueprint

_Finalized Nov 15, 2026. Source of truth for continuing the deck in a new session._
**Figma Slides file:** https://www.figma.com/slides/P5NNQekTnLT58tfvLv7om7

---

## 1. Goal, audience, structure, narrative

**Goal:** an interview-ready deck presenting one combined design systems case study (Trend Micro + BenQ).

**Target audience:** the interview panel for Amazon Robotics, Sr. Product Designer (JD: `jobs/amazon-robotics-sr-product-designer.md`). The JD lines this deck answers:
- "Create scalable mechanisms and reusable design patterns that multiply team impact"
- "Standard work, playbooks"
- "Elevate UX maturity"

**Format:**
- 1-hour interview with 2-3 case studies; this one gets about **12-15 minutes of talking** plus Q&A.
- The other case studies will likely be Robot HMI and DMS (not final).
- Presented from Figma Slides.

**Order:** Opening → Trend Micro → BenQ → Synthesis.

**Narrative arc:**
- **Opening:** two companies, two starting points, and the same problem behind both (costs to users, designers, and the business).
- **Trend Micro (the core, about 8 minutes):**
  - Audit across 3 products, then the modal / drawer / page standoff.
  - Resolved by agreeing on decision points, shown in the tree and two examples.
  - Then governance (how the system grows) and honest outcomes.
- **BenQ (about 4 minutes):**
  - Built the system while building DMS, across 5 platforms.
  - Covers ownership, the inventory, rule anatomy, and the review and release process.
  - Larger scale, more stakeholders, still in use.
- **Synthesis:** define from zero vs. audit what exists. The point: I can work either way. Then the robotics parallel and how I'd build the next one.

**Three threads to land:**
1. Rules, not just components.
2. A process that keeps the system alive.
3. Influence without authority.

**Content rules:**
- Slides carry short text only. Full sentences go in the **speaker notes**.
- Never invent metrics, outcomes, or roles.
- Never call the owner's BenQ role "UI designer." Write "UX designer" for the owner and "GUI designers" for the visual designers.
- Internal artifacts are redrawn or annotated in English. No raw confidential screens.

---

## 2. Visual design system & Figma rules

**Canvas:** 1920 × 1080.

**Grid:**
- Left margin x=120, content width 1680 (right edge at x=1800).
- Section tag at y=96; title at y=140; content usually starts at y=290-380.
- Content stays within y≤1000.

**Fonts:** IBM Plex Sans (Light / Regular / Medium / SemiBold) and IBM Plex Mono (Medium / SemiBold). In Figma the style is named "SemiBold" (no space).

| Role | Font | Size |
|---|---|---|
| Title (content slides) | Plex Sans SemiBold, line height 105-110% | 56-64 (80 on statement slides) |
| Title slide / Thank you | Plex Sans SemiBold | 96 / 120 |
| Section tag (`SECTION · TOPIC`, uppercase) | Plex Mono Medium, letter spacing 8%, accent color | 22 |
| Label (uppercase) | Plex Mono Medium, letter spacing 6% | 20 |
| Body | Plex Sans Regular / Medium, line height 118-130% | 24-36 |
| Big number | Plex Sans Light | 160-240 |

**Colors:**

| Token | Hex | Use |
|---|---|---|
| ink | #101826 | Dark slide background, primary dark |
| ink2 | #2A3445 | Dark surfaces |
| ink3 | #444F61 | Secondary bars, connector lines |
| paper | #F5F3EE | Light slide background |
| white | #FFFFFF | Cards |
| text | #141A24 | Body text on light |
| muted | #5B6472 | Secondary text, labels |
| line | #D9D5CC | Dividers, card strokes, component chips |
| accent | #E2572B | The single accent: tags, highlights, "me" / outcome |
| accentSoft | #FBE3D8 | Tinted accent surfaces, result chips |
| placeholder | #ECE9E2 | Placeholder fill |
| onDarkMuted | #C2C9D6 | Secondary text on dark |

**Dark slides:** 1 Title, 6 Hardest call, 14 Who owned what, 18 BenQ outcome, 22 Thank you. All others are paper.

**Component styles:**
- **Signature motif:** three stacked rounded bars (accent / ink3 / ink2), each step offset right, often bleeding off the edge. It echoes the three-layer model. Used on slides 1, 3, 11, 18, and 22.
- **Story item:** 8px vertical bar (accent for the key item, ink3 otherwise) + Mono label + body text.
- **Card:** white, 2px #D9D5CC stroke, radius 12-14.
- **Result chip:** pill shape, accentSoft fill, accent SemiBold text.
- **Numbered marker:** 44-48px circle (accent or ink3) with a white Mono number.
- **Placeholder:**
  - Frame named `Placeholder — <label>`, fill #ECE9E2, radius 16, 2px dashed stroke #5B6472 (dash 12/10).
  - Inside: Mono "PLACEHOLDER" + label (Sans Medium 30) + instructions (Sans Regular 22).

**Figma build rules** (Slides via the `use_figma` tool):
- Load the `figma-use` and `figma-use-slides` skills first.
- `appendChild` **before** setting x/y at every nesting level (avoids a −240px offset).
- Load fonts before any text edit. Group related content in named frames.
- Each section is a `SLIDE_ROW` with a name: Opening, Trend Micro, BenQ, Synthesis.
- Write `speakerNotes` as markdown bullets.
- Edit existing slides in place; never delete and rebuild.
- After each batch, run the overlap / clip / bounds check. The motif bars are allowed out of bounds.
- `.claude/settings.json` lets Figma tools run without permission prompts.

---

## 3. Slide-by-slide breakdown

Copy below is exactly what's on each slide. "Notes" means speaker notes exist in Figma.

### Opening

**1. Title** (dark)
- **Message:** what this case study is about.
- **Layout:** tag top left; big title left; motif bars bleeding off the right.
- **Copy:**
  - Tag: DESIGN SYSTEMS CASE STUDY
  - Title: Building shared patterns for complex tools, twice
  - Role line: UX Designer · Trend Micro (2023–2024) · BenQ (2020–2023)
  - Name: Tiffany Kuo

**2. At a glance**
- **Message:** a side-by-side summary of the two companies.
- **Layout:** comparison table; column headers have a colored top rule (accent for Trend Micro, ink for BenQ).
- **Copy:** title "Two companies, two starting points".

| | Trend Micro | BenQ |
|---|---|---|
| Starting point | Audit across 3 products | No library; built inside DMS, for 5 platforms |
| My role | Solo UX designer | 1 of 2 UX designers |
| What I built | 5 pattern + 6 page guidelines · governance process | General rules + usage guidelines · review and release process |
| Outcome | Design team's shared reference | Adopted across 5 platforms; still in use |

**3. The problem behind both**
- **Message:** inconsistency costs users, designers, and the business.
- **Layout:** title on the left third; motif bars bottom left; three story items on the right.
- **Copy:**
  - USERS: relearn the same task in every product.
  - DESIGNERS: re-solve the same problems, and documentation can't keep up.
  - THE BUSINESS: ships products that don't look like one family.

### Trend Micro

**4. Context and scope**
- **Message:** 3 products, the goal, and my scope.
- **Layout:** left: title, products, goal. Right: three-layer diagram with the top two layers marked "MY SCOPE."
- **Copy:**
  - Title: Trend Micro: aligning 3 automotive security products
  - PRODUCTS: xNexus · xZETA · SUMO
  - GOAL: Faster design of recurring features / Consistency across products
  - Layers: Features & pages (shared across all products) / Patterns (how components combine into consistent behavior) / Components (Tonic) (existing library)
- **Notes:** yes.

**5. The audit**
- **Message:** a 6-step method.
- **Layout:** horizontal 6-step timeline; optional placeholder below.
- **Copy:**
  1. Collect: Every instance across 3 products
  2. Compare: Side by side
  3. Infer intent: Likely purpose; rationale wasn't documented
  4. Benchmark: Vision One · Carbon · Ant · Adobe
  5. Note: Gaps, inconsistencies, open questions, fixes
  6. Align: Walk designers through it; agree
- **Notes:** yes.

**6. The hardest call** (dark)
- **Message:** the conflict, and my move.
- **Layout:** conflict / move text on the left; wireframes of modal, drawer, and page on the right.
- **Copy:**
  - Title: Modal vs. drawer vs. page
  - THE CONFLICT: Every designer used them differently, each with their own reasons, and resisted change.
  - MY MOVE: Stop debating answers. Agree on the decision points first.

**7. The decision tree**
- **Message:** agreed criteria replaced opinions.
- **Layout:** full-width placeholder for the tree.
- **Copy:** title "Shared decision points replaced personal preference".
- **Notes:** yes.

**8. Example 1**
- **Message:** I listened, and the system got better.
- **Layout:** 4 story items on the left; decision-fork diagram on the right ("Edited again, or shown in view mode?" → YES: Drawer / NO: Modal).
- **Copy:**
  - Title: A case that didn't fit became a rule
  - My first rule: User input → drawer
  - A case that didn't fit: One-time input in a modal
  - Her reasoning: Drawers hold content users edit again; this input couldn't be edited later
  - Outcome: A new decision point for all products
- **Notes:** yes.

**9. Example 2**
- **Message:** criteria settled a team-wide disagreement.
- **Layout:** story items on the left; criteria diagram on the right; three product cards along the bottom.
- **Copy:**
  - Title: Viewing details needed criteria, not one answer
  - The problem: Details opened 4 different ways, with no shared logic
  - My first instinct: Pick one
  - What discussions revealed: It depends on what people do with the details
  - Criteria: "Large amount of information?" Then narrow it down:
    - Cross-checked with the original, or another function? → New tab
    - Dive deep, or take actions? → Page
    - Cross-checked with the primary content? → Drawer / collapsible table
  - Applied across all three products:
    - xNexus: Detection event details → New tab (why? [CONFIRM])
    - xZETA: Affected firmware list → Page + back button (why? [CONFIRM])
    - SUMO: Hardware version list → Page (users may act on it)
- **Notes:** yes.

**10. Governance**
- **Message:** how the system grows.
- **Layout:** two flows on the left; placeholder on the right.
- **Copy:**
  - Title: How the system grows
  - CREATE A GUIDELINE: Audit → propose → review → document → release → apply everywhere
  - APPLY A GUIDELINE:
    1. Follow it, or propose a change
    2. Not for every product → local exception
    3. Build review feeds limits back
- **Notes:** yes.

**11. Outcome and honest limits**
- **Message:** what came of it, and its limits.
- **Layout:** big number on the left; three story items on the right; one motif bar at the bottom right.
- **Copy:**
  - Title: Outcome and honest limits
  - Big number: "11 guidelines · 5 pattern · 6 page"
  - OUTCOME: Designers fixed misaligned designs after each review
  - LIMIT: Fixes ran alongside urgent work; adoption wasn't tracked
  - LIMIT: Some items were still open when I left

### BenQ

**12. Context**
- **Message:** 5 platforms built separately, with 3 challenges.
- **Layout:** 5 deliberately inconsistent mini-wireframes; challenges below.
- **Copy:**
  - Title: BenQ: 5 platforms, built separately
  - Platforms: DMS / AMS / IAM / X-Sign Broadcast / X-Sign Signage
  - CHALLENGES:
    1. Same users, different experiences
    2. Each product designed in isolation
    3. Slow designer–engineer handoff
- **Notes:** yes.

**13. Approach**
- **Message:** the system came out of real product work.
- **Layout:** 5-step horizontal flow; step 4 is expanded.
- **Copy:**
  - Title: Build the system while building the product
  - 01 Design DMS → 02 Spot pieces that repeat → 03 Generalize into components + rules → 04 Two filters → 05 Document
  - The two filters:
    - Buildable on Vuetify? (Customize only when worth defending)
    - Fits the other 4 platforms? (AMS · IAM · X-Sign Broadcast · X-Sign Signage)
- **Notes:** yes.

**14. Who owned what** (dark)
- **Message:** clear credit.
- **Layout:** 4 stacked bars, each indented further; "Me" is in accent.
- **Copy:**
  - ME: General rules, including how each pattern should be used
  - ME + 1 UX DESIGNER: Lo-fi component structure, split between us
  - GUI DESIGNERS (2): Visual design of components and tokens
  - ENGINEERS: The coded library, built on Vuetify
- **Notes:** yes.

**15. What's in it**
- **Message:** the breadth of the system, organized.
- **Layout:** row of 7 accent rule boxes; below, 4 families of grey component chips.
- **Copy:**
  - 7 GENERAL RULES: Navigation · Header · Search / Filter / Sort · Dialog · Error page · Scroll · Onboarding
  - 29 COMPONENTS IN 4 FAMILIES:
    - Navigation & structure: Breadcrumb, Tab, Pagination, Page description, Tree view
    - Inputs: Text field, Text area, Dropdown, Search, Filter, Slider, Date picker, Time picker, Add button
    - Data display: Card list, Card title, List, Data table, Settings list, Sub-settings, Tags, Badge, Avatar
    - Feedback: Tooltip, Toast, Alert, Dialog, Progress indicator
- **Notes:** yes.

**16. Anatomy of a rule**
- **Message:** guidelines defined behavior.
- **Layout:** two side-by-side placeholders.
- **Copy:** title "Rules defined behavior, not just looks: one component, one pattern".
- **Notes:** yes.

**17. Review and release process**
- **Message:** this answers challenge 3.
- **Layout:** placeholder on the left; three numbered callouts on the right.
- **Copy:**
  - Title: Fixing the handoff: one review and release process for UX, GUI, engineering, PM, and QA
  - Callouts:
    1. Version tags on every comment: everyone knew which spec version a comment was about
    2. Engineers confirm feasibility before a thread closes: no surprises at build time
    3. Changed areas color-marked for QA: testers saw exactly what changed in each release
- **Notes:** yes.

**18. Outcome** (dark)
- **Message:** a larger scale, more people to align, and still in use.
- **Layout:** three big numbers; team detail line; outcome bar; motif bars on the right.
- **Copy:**
  - Title: Bigger scale, more people to align
  - Numbers: 5 platforms · 4 cross-functional teams · 13 engineers on DMS alone
  - DMS team: 2 UX designers · 2 GUI designers · 1 PM · 13 engineers · QA
  - OUTCOME: Adopted across the platforms. Still in use today.

### Synthesis

**19. Two starting points**
- **Message:** I can work either way.
- **Layout:** two columns, each with a colored top rule and a placeholder below.
- **Copy:**
  - Title: Two starting points: define from zero, or audit what exists
  - TREND MICRO: Audit what exists (Established library; patterns branched out from it)
  - BENQ: Define from zero (No library yet; rules defined while building DMS)
- **Notes:** yes.

**20. Parallel to robotics maintenance tools**
- **Layout:** full placeholder. Content not written yet.

**21. How I'd build the next one**
- **Layout:** 4 placeholder cards, each holding one candidate principle (the owner confirms or rewrites):
  - Audit before you build
  - Agree on criteria before answers
  - Design contribution and exception paths from day one
  - Close the loop with build review

**22. Thank you** (dark)
- **Layout:** big title on the left; motif bars on the right.
- **Copy:**
  - Tag: DESIGN SYSTEMS CASE STUDY
  - Title: Thank you
  - Subtitle: Questions?
  - Contact: Tiffany Kuo · tiffanytykuo.webflow.io

---

## 4. Questions to revisit

**Facts to confirm**
1. **Slide 8:** was the one-time modal case SUMO's "add ECU firmware"? If so, name it in the notes.
2. **Slide 9:** which decision question sent xNexus detection event details to a new tab, and xZETA's affected firmware list to a page with a back button?
3. **Slide 3:** does "The business ships products that don't look like one family" hold for Trend Micro? If not, move it to BenQ or rephrase it.
4. **Slide 17:** are you comfortable showing the internal BenQ process diagram? Also check NDA limits on the Trend Micro screenshots (slides 5 and 10).

**Content still to write**
5. **Slides 19-21:** synthesis column content, the robotics parallel, and the final principles.
   - If Robot HMI is in the same interview, keep the robotics parallel to one sentence.
   - Present it as a parallel, not as robotics experience.
6. **Optional:** one concrete moment of disagreement for the slide 9 notes.
7. **Optional:** one Vuetify customization you fought for or dropped, for the slide 13 notes.

**Decisions after a timed run-through** (target 12-15 minutes)
8. Keep slide 15 or move it to an appendix?
9. Interview lineup: if DMS is presented in the same hour, shorten the BenQ section so it doesn't repeat DMS. The parked DMS rewrite then becomes urgent too.

**Interview prep (after the deck is final):** rehearse spoken answers to:
- What was yours vs. the team's?
- How did you handle pushback?
- How do you know it worked? (weakest point; answer honestly)
- What would you do differently?
- How does this apply to robotics?

---

## 5. Current status (checked in Figma, Nov 15, 2026)

All 22 slides exist in Figma, in 4 named sections. No visuals have been added since the build.

| Status | Slides |
|---|---|
| **Done** (copy and layout final) | 1, 2, 3, 4, 6, 8, 11, 12, 13, 14, 15, 18, 22 |
| **Built, but facts to confirm** | 9 (two [CONFIRM] reasons), 8 (case name, notes only) |
| **Built, needs the owner's visual** | 5 (optional audit comparison), 7 (decision tree, from Patterns_Page-Guideline node 8-475), 10 (Collaboration Practice flow screenshot; highlight the local-exception path and build review), 16 (Toast + Search/Filter/Sort redraws), 17 (original BenQ diagram with English box labels) |
| **Content not written** | 19 (column bodies), 20 (robotics parallel), 21 (principles) |

**Speaker notes:** written for slides 4, 5, 7, 8, 9, 10, 12, 13, 14, 15, 16, 17, 19. Missing on 1, 2, 3, 6, 11, 18, 20, 21, 22 (add them if needed).

**Source files:**
- Approved wording and rationale: `case-studies/design-systems/deck-rewrite.md`
- Raw facts: `case-studies/design-systems/notes.md`
