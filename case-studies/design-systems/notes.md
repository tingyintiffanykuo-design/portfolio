# Design systems case study: working notes

_Started Oct 28, 2026. Target: Amazon Robotics Sr. Product Designer (`jobs/amazon-robotics-sr-product-designer.md`)._

## 1. What the JD asks for that this case study can answer

| JD line | How this case study can speak to it |
|---|---|
| "Create scalable mechanisms and reusable design patterns that multiply team impact across multiple robotics programs" | Main point of the case study: patterns reused across 4-5 platforms at two companies |
| "We design for scale, creating reusable systems and patterns that drive simplicity across products" | Same |
| "Contributing to the architecture and design (architecture, design patterns...) of new and current systems" | Patterns as shared structure that engineering builds on, not just visuals |
| "Building launch readiness frameworks, standard work, playbooks" (preferred) | Usage guidelines, critique process, Figma collaboration norms as standard work |
| "Mentor junior designers and elevate UX maturity across the organization" | BenQ: first design critique, Figma norms, design backlog |
| "Partner cross-functionally with ... engineering" | Handoff and adoption with engineers |
| "Complex, data-rich interfaces" | Trend Micro: patterns spanning identify, detect, analyze, recover workflows |

**Bridge to robotics:** Trend Micro's threat workflow (identify, detect, analyze, recover) has the same shape as the JD's technician arc (receive alert, locate, access information, repair, confirm resolution). If the patterns were organized around workflow stages, that is the story worth telling. Present it as a parallel, not as robotics experience.

## 2. Evidence so far (from the resume; not yet verified with the owner)

**BenQ (Aug 2020 to Jun 2023)**
- "Created BenQ's first scalable design system for 5 platforms, streamlining workflows across 4 cross-functional teams ... through close collaboration with visual designers and engineers."
- From the spec: built the company's first web design system, led the first design critique, set up team collaboration norms in Figma, created a design backlog list.
- Spec open question 5 is still unanswered: who built it, and what was the owner's specific part?

**Trend Micro (Nov 2023 to Jul 2024)**
- "Led design audits and built a design system of 11 reusable UI patterns across 4 software platforms, enhancing cohesive experience across threat identification, detection, analysis, and recovery workflows."
- The spec describes this role as "mostly desktop research, small design changes, design patterns, and conceptual prototypes." Spec open question 15 is still unanswered: which patterns, and did the team adopt them?

## 3. Honesty checks before writing

1. **"First scalable design system for 5 platforms" vs. the spec's "first web design system."** Which is accurate? Interviewers will ask what the 5 platforms were.
2. **Built vs. co-built.** BenQ had two GUI (visual) designers who owned visuals. The case study has to say who owned what.
3. **"Streamlining workflows" and "enhancing cohesive experience"** are outcome claims. What evidence exists (adoption, fewer handoff questions, faster builds, feedback)? If none, use qualitative statements only.
4. **Adoption.** A design system nobody used is a different story from one teams adopted. Be specific about what shipped using it.
5. **Confidentiality.** Patterns can usually be redrawn generically (structure, states, rules) without product screens. Confirm NDA limits.

## 4. Working angle (proposal, not decided)

Title idea: "Building shared patterns for complex tools, twice."

Arc: BenQ, where the owner built a system from zero and learned what makes one get used → Trend Micro, where they started from an audit and organized patterns around the user's workflow across 4 products → what they would do at a third company.

This shows growth, puts the focus on systems thinking over visuals (matching spec 5.3), and ends on a point of view.

## 5. Proposed structure (draft)

1. At a glance: problem, what I did, key insight, outcome/status
2. Why patterns mattered here: the cost of inconsistency for users and for the team
3. BenQ: starting from zero (scope, what was included, who did what, how it was adopted, critique and Figma norms)
4. Trend Micro: starting from an audit (audit method and findings, how the 11 patterns were chosen, 1-2 patterns shown in depth with states and usage rules, adoption)
5. One pattern in depth: problem, alternatives considered, rules, edge/error states
6. What I learned / how I'd build the next one
7. Limits: evidence available, what was redrawn

## 6. Owner's answers (Oct 30, 2026)

**Rule:** where the resume and the spec disagree, the resume is correct.

**Format and order:** (1) an interview slide deck, thorough and ready to present, which is the priority; (2) a 1-page version for the website; (3) later, a full case study. One combined case study covering both companies.

**BenQ**
- **Platforms:** 5 web-only platforms in the education software suite: DMS, AMS, IAM, X-Sign Broadcast, X-Sign Signage (https://www.benq.com/en-us/education/software.html; Claude couldn't fetch this page from the cloud session).
- **Ownership:**
  - GUI designers owned the components and tokens; the owner reviewed them and gave UX advice.
  - The owner and one other UX designer designed the bare-bones wireframes and wrote the usage guidelines and documentation. They split the components between them.
  - **The owner defined the general rules** (cross-platform interaction rules).
  - Engineers built the coded component library.
- **Process:**
  - The system was built for the first time while designing DMS, one of the 5 platforms.
  - Components likely to be reused were pulled out of the DMS work.
  - Common patterns (search, navigation, error messages, etc.) were discussed and their interactions defined.
  - Each pattern was checked with engineers for feasibility and judged on whether it would scale to the other platforms.
- **Triggers:**
  - (a) Scaling the education business required better design efficiency and documentation.
  - (b) Customers complained about inconsistency across platforms.
  - (c) The products looked unrelated, which was bad for the brand.
- **Adoption:** adopted and still in use today. The owner doesn't remember specific feedback (about 4 years ago).
- **Artifacts (BenQ internal Figma, in Chinese):**
  - General guidelines: https://www.figma.com/design/dal2F03sF1fDpL9ZiFuKRX/DMS-3---UI-flow--draft---Copy-?node-id=101-12
  - Components: https://www.figma.com/design/6j2D7XvRMI4osaVycRkSYt/BenQ-Design-System-%E5%82%99%E4%BB%BD?node-id=204-6569

### What the Figma files contain (read by Claude, Oct 30)

**General rules page:** an index plus 7 rule areas:
1. Navigation
2. Header (an old and a new version exist)
3. Search / Filter / Sorting (each with dialog, criteria, and result states)
4. Dialog. Four documented cases:
   - Select devices
   - Co-editing conflict / edit restriction (site-wide)
   - Check properties (and check initial properties)
   - Policy apply & confirm
5. Error page
6. Scroll area
7. Onboarding (an old version kept and marked "don't look," plus a newer "simplified onboarding")

**Guideline format** (seen in 4.2, co-editing conflict):
- Purpose statement: when the dialog appears and why (duplicate data, data no longer exists, access restriction)
- Link to the design-system component (`q-dialog`)
- Annotated example
- Numbered behavior for each CTA (e.g. "Close → go back one level, refresh, return to the latest state")

This works well on a slide: it shows that guidelines spell out behavior and states, not just visuals.

**Component library ("clean-up components" page):** 29 components with a `q-` prefix:
- Navigation and structure: breadcrumb, tab, pagination, page-description, tree-view
- Inputs: text-field, text-area, dropdown, search, filter, slider, date-picker, time-picker, add-button
- Data display: card-list, card-title, list, data-table, settings-list, sub-settings-items, tags, badge, avatar
- Feedback: tooltips, toast, alert, dialog, progress-indicator

Designer notes left on the canvas show the library was being cleaned up and consolidated:
- "Actually only A is in use right now" (next to toast)
- "Merge with dropdown" (next to alert)

**Evidence of iteration worth asking about:** the old vs. new header, and the old vs. simplified onboarding.

**Confidentiality:** these files are BenQ internal and in Chinese. For the deck, redraw them in English and generically. Don't paste raw screenshots unless permission is confirmed.

## 7. Reminders for Claude

- **Bridge to robotics:** when building the Trend Micro and synthesis slides, ask the owner for more detail on how the patterns map to identify, detect, analyze, recover. Then decide whether the parallel to the JD's alert → locate → repair → confirm arc holds. Present it as a parallel, not as robotics experience.

## 8. Still open

See `PROGRESS.md` for the current list of questions.

## 9. Trend Micro: owner's answers and Figma review (Oct 30, 2026)

**Owner's answers**
- Audit and guidelines file: https://www.figma.com/design/FZTg7N8lsD83uimd7RdrfB/Patterns_Page-Guideline?node-id=0-1
- The 11 guidelines: modal/drawer/page, empty state, loading, error state, table/cards/charts, account setting & header & navigation, sign in, reports, third-party integration, roles, accounts.
- Guidelines include examples of what each product currently does. Rationale is backed by public systems: IBM Carbon, Ant Design, Adobe, and others.
- Solo work. The owner reviewed the audit findings and guidelines with the design team.

**What the file contains (read by Claude)**
- **Scope:** the products are VicOne's (Trend Micro's automotive cybersecurity business): **xNexus, xZETA, SUMO**. Trend Micro's **Vision One** is used as the internal benchmark ("Inspirations from VisionOne"). `[ASK]` What was the 4th platform on the resume?
- **Cover states two goals:** "Accelerate future design of similar features" and "Improve consistency across products."
- **Three-layer model** on the intro slide:
  1. Common features/pages (applied to all products)
  2. Common patterns ("how components are used and organized")
  3. Components (Tonic, the existing library)

  The owner's work sits in layers 1 and 2, above the component library.
- **Audit format, for each feature or pattern:**
  - Purpose
  - Side-by-side screenshots of each product
  - Inspirations from Vision One
  - "Thoughts": open questions, e.g. loading thresholds for skeleton vs. progressive loading, priority of inline actions, when to use a modal vs. a drawer, how to get value out of empty states
- **Self-aware caveat on the audit:** "This is just a summary of thoughts based on my observation, not suggestions or advice … I don't know the rationale behind most of the designs." `[ASK]` How did they move from observations to rationale?
- **Guidelines are separate pages** after the audit: 5 under "Patterns" and 6 under "Page" (11 total, matching the owner's list).
- **Modal / Drawer / Page guideline** (strongest candidate for an in-depth slide):
  - A decision tree: "Require user input/decision?", "Large amount of information?", "Often cross check with primary content?", "Will the same content be edited again or only viewed?"
  - Rules for overlays (full-page vs. in-page, with trade-offs)
  - Drawer (view) vs. drawer (edit) behavior, e.g. no slide transition when switching content; a confirmation if the user leaves with unsaved edits
  - Page rules (back button keeps state, e.g. returns to page 3 of the table)
  - "Cases to be verified" and "Trigger point (to be iterated)" sections
  - A real example: "Anomaly Events > View in Rule Management". `[ASK]` This is literally detect → act, a possible honest bridge to the robotics workflow.
- **README** points to a separate doc, "Patterns Guideline_Collaboration Practice," on how to CREATE and MAINTAIN the guideline. `[ASK]` This is governance, the JD's "scalable mechanisms."

**Mentor read (to confirm with the owner)**
- **The growth story is sharper than expected:**
  - **BenQ:** team effort; system extracted while building one product; components plus rules.
  - **Trend Micro:** solo; audit across products; built the layer above components (patterns and decision rules); benchmarked against an internal best-in-class product and public systems; wrote a maintenance process.
- **The robotics bridge needs new footing.** The patterns are organized by layer, not by the identify/detect/analyze/recover workflow. The resume phrase describes product scope. Better candidates:
  - the decision-rule approach
  - the Anomaly Events → Rule Management flow

## 10. Collaboration practice docs and more answers (Oct 30, 2026)

**Owner's answers**
1. The owner reviewed the guidelines with the designers of every product, using public systems as supporting evidence during those talks. ("Did anything change your view?" is deferred until slide building.)
2. **Hardest call: modal / drawer / page.** Each designer's existing designs differed, and they resisted change. The owner argued from the guideline's point of view, pointed out inconsistencies, and asked for clear reasoning behind each design.
3. Trend Micro collaboration practice (FigJam): https://www.figma.com/board/Knt2ai6QGEWngPHp4CnU2i/Patterns-Guideline_Collaboration-Practice?node-id=0-1
4. Adoption: "I think they did apply the patterns and used the page I created." `[ASK]` Is there a concrete instance?
5. **Correction:** there were **3 platforms** (xNexus, xZETA, SUMO), not 4. A mobile app existed but didn't use these guidelines. The owner will fix the resume.
6. **Origin: both.** As a new designer, the owner saw many inconsistencies in design reviews and started the audit; the manager had wanted this initiative for a while.
7. The "TBD" and "to be iterated" items were still open when the owner left. The Figma file is the latest version.

**BenQ: "Design review & document release process"** (owner-built; https://www.figma.com/design/dal2F03sF1fDpL9ZiFuKRX/DMS-3---UI-flow--draft---Copy-?node-id=2863-40957)
- **Flow:** initial draft → RD/GUI/PM comment → UX (the owner's team) replies and revises → RD/GUI/PM resolve the thread → finalize → UX notifies "done revising" → big revamp needed? Yes: release an updated version. No: go back into the loop.
- **Comment protocol,** with comments tagged by UI-flow version `[vX]`:
  1. New feature or design: UI adds the definition; RD reacts with an emoji to confirm it can be built, then resolves.
  2. Additions or changes to a definition: RD/GUI/PM comment; UI revises and replies with the new version plus "update"; the commenter resolves.
  3. Pure questions: no version tag; UI replies and the asker resolves.
- Revised areas are color-marked so **QA can see what changed in each release**, and changes are logged in the version history.
- "UI" in the original doc = the owner's team. BenQ's title was "UI designer," but the work was UX. **Always write UX designer.**

**Trend Micro: "Patterns Guideline: Collaboration Practice"** (FigJam, owner-built). Two linked processes:
- **A. Creating a pattern or page guideline:**
  1. Identify a common pattern or page.
  2. Collect the relevant designs from current products. The person in charge is each product's designer, and the pattern creator can also run a quick audit.
  3. Identify problems (inconsistency or usability).
  4. Necessary to fix?
     - Yes: point out the problem and propose a solution → design review (loop until it passes) → document wireframe, spec, and interaction → visual designer adds a visual spec if needed.
     - No: copy the existing design into the guideline.
  5. Release the new pattern, then apply it everywhere the pattern occurs. Process A then feeds into B.
- **B. Applying the guideline when designing:**
  1. New feature or page → is there an existing pattern or page guideline?
  2. If there is one and it applies, follow it.
  3. If it doesn't apply: propose an adjustment → design review → does it apply to all products?
     - Yes: document it in the guideline.
     - No: adjust only in the product file and note it in the guideline.
  4. If no guideline exists: is this likely to be a common page? Yes: design it and create a new guideline. No: design and document it in the product file only.
  5. Every path ends in a **build review** ("ensure front-end developers implement the design correctly") → successful? If not, identify the problem (technical limitation or design issue) and loop back.

**Mentor read**
- **A third thread across both jobs:** the owner builds the process that keeps a system alive, not just the system.
  - BenQ: handoff and release hygiene between UX, GUI, engineering, PM, and QA.
  - Trend Micro: governance of the pattern library itself, with a contribution path, an exception path, and a feedback loop from build review back into the guideline.
- This maps directly to the JD: "scalable mechanisms," "standard work, playbooks," "elevate UX maturity."
- **The resistance story** (modal / drawer / page, as a new designer with no authority) is the most interview-worthy moment. It needs one specific scene.
- **The audit's screenshot dates** (Dec 20, 2023 to Jan 3, 2024) suggest it started about 6 weeks after joining (Nov 2023). `[ASK]` Confirm.
- **Resume wording to fix:** "11 reusable UI patterns across 4 software platforms" → 3 platforms. The 11 are really 5 pattern guidelines plus 6 page guidelines.

## 11. Final discovery answers (Oct 30, 2026)

**Terminology rule:** never say "UI designer" for the owner's BenQ role. It was a BenQ title, but the work was UX. Write "UX designer" for the owner and their peer, and "GUI designers" or "visual designers" for the two people who owned components and tokens. This also applies to the spec's DMS section, where "two UI designers" means the GUI/visual designers.

**Resolving the modal / drawer / page conflict**
- The owner said: "there were a lot of inconsistencies of how designers use modal, page, drawer … they are pretty resistant to changes and all have their own reasoning. I ended up building the guidelines and get alignment on every decision point … once this was agreed, it's hard for them to keep selling on their subjective ideas."
- **Decision tree** (https://www.figma.com/design/FZTg7N8lsD83uimd7RdrfB/Patterns_Page-Guideline?node-id=8-475):
  1. Requires user input or a decision to do the task?
     - Yes, and the same content will be edited again or shown in a view mode → **drawer**.
     - Yes, otherwise → **modal** (confirmation, warning).
  2. No input needed, and a large amount of information?
     - Often cross-checked against the original content, or belongs to a different function → **new tab**.
     - Otherwise → **page**.
  3. No, or unsure → often dive deep into details or take actions to complete the task?
     - Yes → **page**.
     - No, but often cross-checked against the primary content → **drawer** (less information) or **collapsible table** (tabular information).
     - Neither → **page**.
- **Key insight:** the owner turned a debate about preferences into agreement on criteria. Align on the questions first; the answers follow. This is the main moment for the case study.

**Adoption (wording to use):** after each guideline was reviewed, designers fixed what didn't match in their products, alongside more urgent work. Adoption was ongoing but not tracked. Don't claim more than that.

**Timing:** not important; many audit screenshots are mockups. Drop it.

**BenQ change path for the system:** it existed (the "need big revamp?" branch in the release process, https://www.figma.com/design/dal2F03sF1fDpL9ZiFuKRX/DMS-3---UI-flow--draft---Copy-?node-id=2863-40820) but was documented less clearly than at Trend Micro. That is an honest growth point.

**Owner's preference from now on:** ask only questions that matter for a strong case study or the deck outline. Detail questions come up while building slides together.
