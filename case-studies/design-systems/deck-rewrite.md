# Design systems deck: rewrite (owner's words + Claude's suggestions)

_Started Oct 31, 2026. Builds on `deck-outline.md` (v2, kept as is). For each slide: the owner's draft, Claude's suggested wording, and why. The owner decides the final wording._

**Slide text rule (owner, Nov 9):** slides carry short, concise text only. Full sentences go in the **speaker notes**, which the owner says out loud. When the deck is built, split every kept suggestion this way.

**Review status (Nov 9):** slides 1-14 reviewed by the owner; each is marked **[KEPT]**, **[REVISED]**, or **[NO CHANGE]** below. Slides 15 onward are not reviewed yet.

**Order (owner's decision):** Opening → **Trend Micro** → BenQ → Synthesis.

---

## Opening

### 1. Title [KEPT]

**Your draft:** "Building shared patterns for complex tools, twice." Role line: UX Designer, BenQ (2020-2023) and Trend Micro (2023-2024).

**Suggested:**
> Building shared patterns for complex tools, twice
> UX Designer · Trend Micro (2023-2024) · BenQ (2020-2023)

**Why:** list the companies in the order the deck presents them, so the role line previews the structure. The title itself works: "twice" promises a comparison, and the deck delivers one.

### 2. At a glance [KEPT, exact content below]

**Your draft:** v2 table with Trend Micro on the left and BenQ on the right.

**Slide content:**

| | Trend Micro | BenQ |
|---|---|---|
| **Starting point** | Audit across 3 products | No library; built inside DMS, for 5 platforms |
| **My role** | Solo UX designer | 1 of 2 UX designers |
| **What I built** | 5 pattern + 6 page guidelines · governance process | General rules + usage guidelines · review and release process |
| **Outcome** | Design team's shared reference | Adopted across 5 platforms; still in use |

**Why:**
- Same four rows in both columns, so the eye compares across.
- Each cell is short enough to read in a glance; the detail comes in each section.
- "Design team's shared reference" is the honest outcome for Trend Micro; don't claim tracked adoption.

### 3. The problem behind both [KEPT]

**Your draft:** "Inconsistent user experience" / "Inefficient design and documentation workflow" / "Confusing brand representation/reputation"

**Suggested** (name who pays and how):
> **Users** relearn the same task in every product.
> **Designers** re-solve the same problems, and documentation can't keep up.
> **The business** ships products that don't look like one family.

**Why:**
- Your three labels name categories. The suggested lines name a cost, which is what makes an interviewer care.
- Starting each line with who pays (users, designers, business) also shows systems thinking.
- **Drop "reputation."** There's no evidence of reputational damage, so it overclaims. "Don't look like one family" describes what was actually true.
- **Check before keeping the third line:** the brand problem was BenQ's trigger. If it wasn't true at Trend Micro, put this line in the BenQ section instead, or rephrase it as "products that should feel related don't." Trend Micro's products all derive from Vision One, so that version likely holds there.

---

## Part 1: Trend Micro (new order: context → goal and model → audit → standoff → tree → 2 examples → governance → outcome)

### 4-5. Trend Micro: context, goal, and scope (merged) [REVISED]

**Owner's decision:** merge slides 4 and 5, keep the suggestions, move the long text to speaker notes, and add a visual diagram when building.

**Slide content:**
> **Title:** Trend Micro: aligning 3 automotive security products
> **Products:** xNexus · xZETA · SUMO
> **Goal:** faster design of recurring features · consistency across products
> **Diagram:** three stacked layers. **Features & pages** / **Patterns** / **Components (Tonic)**. The top two are highlighted and labeled "My scope."

**Speaker notes:**
> As a new designer, I kept seeing the same pattern solved differently in design reviews. My manager had wanted this initiative for a while, so I took it on. The goal was to speed up the design of recurring features and make the three products consistent. I worked on the top two layers: shared features and pages, and the patterns that combine components. Components themselves already existed in Tonic, our existing library.

### 6. The audit (was 12, merged with the first half of 14) [KEPT, without the transition line]

**Your draft:**
> I tried to find the design and identify patterns in all three products, compare them, guess what the purpose is based on the design and my past experience, benchmark external library and internal parent library (VisionOne) that we're deriving from, note down the gaps, inconsistencies, open questions, and potential suggestions, then I walked these through during design meetings and get alignment with all designers.

**Suggested** (6 steps, one verb each):
> 1. **Collect:** find every instance of a pattern across the 3 products.
> 2. **Compare:** put them side by side.
> 3. **Infer intent:** work out the likely purpose from the design and my experience, since the rationale wasn't documented.
> 4. **Benchmark:** against Vision One, the parent product our design language derives from, and public systems (IBM Carbon, Ant Design, Adobe).
> 5. **Note:** gaps, inconsistencies, open questions, and possible fixes.
> 6. **Align:** walk each product's designers through it in design meetings and agree on the guideline.

**Why:**
- A numbered list of verbs scans in seconds; the paragraph version makes the listener hold six ideas in one breath.
- **"Guess" → "infer intent."** Same honesty, but it sounds like a method rather than a shot in the dark. Keeping "since the rationale wasn't documented" stays truthful about the limit.
- **"Internal parent library" → "parent product our design language derives from."** Vision One is a product with its own guidelines. Calling it a "library" could invite "so you copied its components?"

### (was 14: From observation to reasoning). Removed

The first half is merged into slide 6 (step 6). The second half, "one thing that changed my view," is now covered by your two new example slides. See the note at the end of this file.

### 7. The hardest call: modal vs. drawer vs. page (was 15) [NO CHANGE]

**Your draft:** good as is.

### 8. The decision tree (was 16) [REVISED: headline]

**Your draft:** you'll add the full tree visual yourself.

**Owner's feedback (Nov 9):** the first suggested headline ("We agreed on the questions, so the answers stopped being opinions") was too ad-like and tried too hard to sell. Wanted something like "agreed on how we make decisions, no more subjective opinions."

**Suggested headlines** (plain and descriptive; pick one or adjust):
> A. Agreed on how we decide, instead of debating opinions
> B. Shared decision points replaced personal preference
> C. One way to decide: modal, drawer, or page

**Why:**
- All three state what happened without a punchline. They describe the change instead of selling it.
- **A** is closest to your wording.
- **B** names what was replaced.
- **C** is the most neutral: it names the artifact and lets the tree make the point.

### 9. Example 1: a designer's exception became a new branch (new) [KEPT; framing tweak suggested below]

**Your draft:**
> Initially I wanted to generalize that all actions that require user input should go with side drawer, but a designer pointed out that she made the decision to use a modal instead of a drawer bc most content that use drawer is editable later, but the one instance she designed for was only editable the first time. We then as a team agreed on this branched out pattern to differentiate it from the more common cases where contents are editable.

**Suggested:**
> **My first rule:** any task that needs user input opens in a drawer.
> **The pushback:** a designer had chosen a modal for a one-time input that can't be edited afterward. In our products, drawers usually hold content users come back to edit.
> **What we agreed:** a new question: *"Will the same content be edited again, or shown in a view mode?"*
> → Yes: **drawer.** → No (one-time input, confirmations, warnings): **modal.**

**Why:**
- The rule → pushback → agreement structure makes your listening visible. Your original rule changed because a colleague had a good reason.
- Name the real case if you can. Your audit lists **"SUMO: add ECU firmware (modal)"**, and the guideline notes modals for "one-time submission/upload; not allowed to edit after the data is added to the table." `[CONFIRM]` Is that the instance? A named case is much more convincing than "one instance."

### 10. Example 2: viewing details needed criteria, not one answer (new) [KEPT]

**Your draft** (summarized): details were viewed in a page, new tab, modal, or drawer. You first wanted one pattern, then found different reasons behind each (cross-checking, follow-up actions). You agreed on "Large amount of information?" and, since that's subjective, added three follow-up questions. You then gave xNexus, xZETA, and SUMO cases.

**Suggested:**
> **The problem:** details opened in a page, a new tab, a modal, or a drawer, with no shared logic.
> **My first instinct:** pick one.
> **What discussions revealed:** the right container depends on what people do with the details. Do they cross-check them against other data? Do they take follow-up actions?
> **What we agreed:** start with *"Large amount of information?"* Because that's a judgment call, add three questions to narrow it:
> - Often cross-checked with the original content, or belongs to a different function? → **new tab**
> - Often dive deep or take actions to complete the task? → **page**
> - Often cross-checked with the primary content? → **drawer** (or collapsible table for tabular data)
>
> **Applied across all three products:**
> - **xNexus**, detection event details → page in a new tab, because `[CONFIRM: which question decided it]`
> - **xZETA**, affected firmware list → page with a back button, because `[CONFIRM]`
> - **SUMO**, hardware version list → page, because users may act on it, and stacking modals or drawers would confuse them

**Why:**
- **Tie each case to the question that decided it.** That's what makes the tree look like a working tool rather than a justification after the fact. Your SUMO case already does this ("users may take actions"); the other two need the same "because."
- **Owning the subjectivity is a strength.** "Large amount of information" is a judgment call, and you added questions to narrow it. Saying so shows maturity. It replaces "this route may be a bit subjective," which sounds apologetic.
- One case per product shows the rule held across all three. That's the consistency goal from slide 5.
- **The two examples show different things on purpose:** in example 1, one designer's edge case added a branch; in example 2, team discussion turned an argument into criteria. Say that difference out loud so the second slide doesn't feel like a repeat.

### 11. Governance: how the system grows (was 17) [NO CHANGE]

**Your draft:** looks good; you'll add screenshots of the flow. Answer to your question about redrawing is at the end of this file.

### 12. Outcome and honest limits (was 18) [NO CHANGE]

**Your draft:** looks good.

---

## Part 2: BenQ (owner's draft Oct 31; v2 slides 4-10 → 13-19)

### 13. Context (was 4) [REVISED: concise slide text]

**Your draft:**
- The 5 platforms were built at different times by different designers. The design language was loosely shared but not consistent.
- Figma "didn't even have the feature components" then, so each product iterated on its own line instead of sharing components.
- The team wasn't used to sharing a library or aligning on patterns the way a product suite should.
- "All built with the same system" is misleading.
- Challenges: (1) inconsistent UX across apps that may have the same users; (2) a fragmented design workflow across products; (3) no streamlined workflow between designers and engineers, which slowed iteration.

**Slide content:**
> **Title:** BenQ: 5 platforms, built separately
> DMS · AMS · IAM · X-Sign Broadcast · X-Sign Signage
>
> **Challenges**
> 1. Same users, different experiences
> 2. Each product designed in isolation
> 3. Slow designer–engineer handoff

**Speaker notes:**
> These 5 web platforms serve K-12 IT teams. They were built at different times by different designers. The design language was loosely shared, but components weren't, and the team wasn't in the habit of aligning on patterns across the suite. That caused three problems. An IT admin using several of these apps had to relearn each one. Each product team designed on its own, with no shared components or patterns. And there was no shared workflow between designers and engineers, so every iteration took longer.

**Why:**
- **Correction, which matters:** Figma had components and shared team libraries well before 2020, so "Figma didn't have components" could be challenged by an interviewer who knows Figma's history. What was really missing was the *team's practice* of sharing them. "Components weren't shared" and "the team wasn't in the habit" say the true thing and can't be disputed. The same applies to slide 15.
- Your draft said "two challenges" but listed three. All three are worth keeping.
- **Challenge 3 sets up slide 18.** The review and release process is your answer to it. Say this out loud when you reach slide 18 so the listener connects problem and solution.
- I dropped "all built with the same system," as you asked.
- **Overlap check with slide 3:** slide 3 is the general problem; this slide is BenQ's specific version. Keep it concrete here (who the users are, what was split) so it doesn't sound like a repeat.

### 14. Build the system while building the product (was 5) [KEPT]

**Your draft:** "Can engineering build it?" needs more context. Engineers didn't build components from scratch; they built on the open-source framework Vuetify. That brought many technical limits, and bigger customizations needed strong justification.

**Suggested** (the loop from v2, with the engineering step made specific):
> 1. Design DMS.
> 2. Spot pieces that will repeat.
> 3. Generalize them into components and rules.
> 4. Check two filters:
>    - **Can we build it on Vuetify?** Our engineers built on this open-source framework, so we customized only when the user benefit was worth defending.
>    - **Does it fit the other 4 platforms?**
> 5. Document it.

**Why:**
- "Customize only when it's worth defending" turns a constraint into judgment. That's what senior roles screen for: designing within real technical limits instead of handing engineers a wishlist. It's also directly relevant to robotics, where hardware and software limits are everywhere.
- `[OPTIONAL, fill in while building]` One example of a customization you fought for, or one you dropped because it wasn't worth it, would make this slide memorable. If none comes to mind, the slide still works without it.

### 15. Who owned what (was 6, shortened)

**Your draft:**
- You worked on the general rules, including the usage guidelines for those patterns.
- You split the component building with another UX designer.
- Back then the GUI designers were just starting to build components, so the UX designers had to make the lo-fi versions first for them to base the visuals on.
- Keep this short and save the details for follow-up questions.

**Suggested:**
> - **Me:** general rules, including how each pattern should be used.
> - **Me + 1 UX designer:** lo-fi component structure, split between us, as the base for visual design.
> - **GUI designers (2):** visual design of components and tokens.
> - **Engineers:** the coded library, built on Vuetify.

**Why:**
- One line per role takes about 10 seconds to say and answers "what was yours?" before anyone asks. Keeping the details for Q&A is the right call.
- **"Component UI building" → "lo-fi component structure."** It avoids the word "UI" (your terminology rule) and makes it clear that your part was the structure the visuals were built on. That's the same "backbone" claim as your DMS case, which keeps your story consistent.
- I dropped the Figma-history line here for the reason given on slide 13. If someone asks why the UX designers went first, the answer is simple: the visuals needed a structure to start from.

### 16. What's in it (was 7)

**Your question:** what's my suggestion for redrawing the inventory map?

**Suggested:** one slide, two rows, no product visuals:
> **Row 1: 7 general rules:** Navigation · Header · Search / Filter / Sort · Dialog · Error page · Scroll · Onboarding
> **Row 2: 29 components in 4 families:**
> - **Navigation and structure:** breadcrumb, tab, pagination, page description, tree view
> - **Inputs:** text field, text area, dropdown, search, filter, slider, date and time pickers, add button
> - **Data display:** card list, card title, list, data table, settings list, sub-settings, tags, badge, avatar
> - **Feedback:** tooltip, toast, alert, dialog, progress indicator
>
> Shown as simple grey boxes with English labels, grouped by family.

**Why:**
- The slide's job is to show the breadth in 5 seconds, not to be walked through. Grouping into families shows the system was organized, not just a pile of components.
- **Grey boxes and English labels avoid two problems:** the confidentiality of real BenQ screens, and Chinese labels the interviewer can't read.
- **Showing rules and components together** mirrors your Trend Micro layer model (patterns above components). The listener sees the same way of thinking at both companies without you having to say it.
- **Option:** given your time budget, this could be a 10-second glance slide or move to the appendix. Decide once the deck is built and you can time it.

### 17. Anatomy of a rule (was 8)

**Your draft:** show two examples, one component guideline (toast) and one general rule (search / filter / sorting). Do this as a separate task after the deck is built.

**Suggested headline:**
> Rules defined behavior, not just looks: one component, one pattern.

**Why:**
- Two examples at two levels (a component and a pattern) show you work across layers, which again echoes Trend Micro.
- I've parked the details of the two examples as a task for after the deck is built, as you asked.

### 18. The process that kept it alive (was 9)

**Your draft:** keep the original diagram to keep it real, and maybe annotate it in English. Or should you translate the whole thing?

**Suggested:** keep the original. Put English labels over the box titles, which are short. Leave the detailed Chinese notes as they are, and add 3 English callouts for what matters:
> 1. **Version tags on every comment:** everyone knew which spec version a comment was about.
> 2. **Engineers confirm feasibility before a thread closes:** no surprises at build time.
> 3. **Changed areas color-marked for QA:** testers saw exactly what changed in each release.
>
> Headline idea: *Fixing the handoff: one review and release process for UX, GUI, engineering, PM, and QA.*

**Why the middle option (original + English box labels + callouts):**
- **Keeping the original:** you're right that a real artifact is more convincing than a clean redraw, and the Chinese shows real context (a Taiwan-based team).
- **But don't rely on annotations alone.** If the interviewer can't read any box, the diagram is just a shape and all the meaning sits in the callouts. Overlaying the short box titles (about 8 labels) is cheap and makes the flow itself readable.
- **Translating everything** costs much more and turns it into a redraw, which loses the authenticity you want. The detailed notes don't need to be read; the callouts carry them.
- The 3 callouts are the payoff for challenge 3 on slide 13 (slow handoff to engineering). The headline says so.
- `[CHECK]` It's an internal BenQ file. It's a process diagram, not product screens, so the risk is low, but confirm you're comfortable showing it.

### 19. Outcome: a larger scale with more people to align (was 10)

**Your draft:** frame BenQ as a larger-scale project with a lot more stakeholders to navigate.

**Suggested:**
> **Bigger scale, more people to align.**
> - 5 platforms, 4 cross-functional teams
> - On DMS alone: 2 UX designers, 2 GUI designers, 1 PM, 13 engineers, plus QA
>
> **Outcome:** adopted across the platforms and still in use today.

**Why:**
- Numbers make "a lot of stakeholders" concrete. All of these are facts you've already confirmed (the resume says 5 platforms and 4 cross-functional teams; the DMS page lists the feature team).
- It also completes the contrast with Trend Micro: there you worked alone with designers across 3 products, and here with every function across 5. That sets up the synthesis slide.
- "Still in use today" is your strongest outcome claim at either company. Give it its own line.

---

## Synthesis

### 20. Two starting points (was 19)

**Your draft:**
- **Title idea:** BenQ is more of a top-down process, since there was no existing library and auditing wasn't worth the time. Trend Micro is more of a bottom-up process, with an established library you wanted to branch out from.
- They had different challenges, and you want to show you can work either way.
- You'll fill in the content after both parts are built.

**Suggested title options:**
> A. *Two starting points: define from zero, or audit what exists*
> B. *Top-down at BenQ, bottom-up at Trend Micro*: your original framing, with a subtitle that explains it.

**Why I'd lean toward A:**
- "Top-down" and "bottom-up" mean different things to different people. At BenQ you pulled components *out of* DMS as you designed, which some interviewers would call bottom-up. That could turn into a debate over terminology instead of a point about your range.
- Option A says the same thing in plain words, and the contrast is easy to follow: no library vs. an established one; define first vs. audit first.
- **If you prefer B,** it works with a one-line subtitle, e.g. "BenQ: no library yet, so we defined rules first. Trend Micro: an established library, so I audited first."
- **Either way, the message is the one you named:** you can build a system from zero or grow one from what exists. That's a strong closing point.
- Order the comparison Trend Micro → BenQ to match the deck.

### 21-22. Robotics parallel and how I'd build the next one (was 20-21)

_The owner will think about these after the deck is built._

### Limits (was 22)

Skipped (owner's decision).

### 23. Thank you / questions

Kept.

---

## Answers to the owner's questions

### Why "one thing that changed my view" matters for storytelling (was slide 14)

The case study's core claim is that you got resistant designers to align. Told without a moment where you changed your own mind, that can sound like "the new designer imposed rules." Interviewers hiring a senior designer listen for whether you persuade or push.

A moment where a colleague's reasoning changed your rule shows three things:
1. You listen.
2. The guideline came out better because of the team.
3. Your process held up against your own first instinct.

**You already have two such moments:** both examples (slides 9 and 10) start with your first instinct and show how discussion changed it. So no separate slide is needed. Just make sure the "my first rule / my first instinct" lines stay in.

### Why I suggested redrawing the governance flow (slide 11)

My earlier redraw rule was about **confidentiality**: the BenQ files are internal and in Chinese. The Trend Micro governance FigJam is different:
- It's already in English.
- It shows a process, not product screens or customer data.

So a screenshot is likely fine, once you're comfortable with your NDA.

The remaining reason is **legibility**. The flow has about 30 boxes across two linked diagrams, and at slide size the text will be too small to read. Options, from least to most work:
1. **Screenshot plus highlights:** show the full flow, dim everything except the 2-3 parts you'll talk about (the local-exception path and the build-review loop), and add a callout on each.
2. **Screenshot, then zoom:** one slide with the whole flow ("this exists"), then one with a cropped close-up of the part that matters.
3. **Simplified redraw:** 5-6 boxes showing only the logic. Most legible, most work.

**Recommendation: option 1.** It keeps your real artifact, which shows authenticity, while directing attention to what matters.

### Is example 1 too bland, or does it make me look submissive? (slide 9, Nov 9)

**Short answer:** as written, it can read that way. The facts aren't the problem; the framing is.

"My first rule → the pushback → what we agreed" puts you in the role of the person who got corrected. What actually happened is stronger:
- You were defining rules for everyone, and a designer's choice didn't fit.
- You didn't overrule her, and you didn't wave it through as a one-off exception either. You took her reasoning seriously.
- Her reasoning held up, so instead of a local exception it became **a rule every product follows**.

Turning one person's judgment into a shared rule is a leadership move, not a submissive one. It's also exactly the method you described for the whole project: ask for the reasoning behind each design.

**Suggested framing tweak** (slide text):
> **Title:** Example 1: a case that didn't fit became a rule
> - **My first rule:** user input → drawer
> - **A case that didn't fit:** one-time input in a modal
> - **Her reasoning:** drawers hold content users edit again; this input couldn't be edited later
> - **Outcome:** a new decision point for all products: "Edited again, or shown in view mode?" Yes → drawer; No → modal

**Speaker notes:**
> Rather than overruling her or treating it as a one-off exception, I asked for the reasoning. It held up, so we made it a rule every product follows.

**On conflict:** this example isn't where you show conflict resolution, and it doesn't need to be. Its job is to show you listen and that your rules get better with input. Slide 7 (the standoff) and example 2 carry the conflict. Having one calm example next to one harder one is a good balance: it shows you can tell a reasonable point from resistance.

### Is example 2 strong enough to cover what example 1 doesn't show? (slide 10, Nov 9)

**Mostly, yes.** Example 2 shows what example 1 can't:
- **Many designers, many competing reasons,** not one person with one point.
- **Several rounds of discussion,** settled with criteria rather than a vote or your authority.
- **Judgment where judgment is unavoidable:** "Large amount of information" is subjective, so you added questions to narrow it.
- **Proof it worked across all 3 products,** one case each.

**One gap:** the conflict is still abstract ("after rounds of discussions"). The slide shows the result, but not a moment of disagreement. One concrete point of friction would make it the strongest slide in the section, said in the speaker notes rather than on the slide. For example: who argued for which container, and which question settled it.

`[OPTIONAL, fill in while building]` If one moment comes to mind, add it to the speaker notes. If not, the slide still works. The two `[CONFIRM]` items (which question decided the xNexus and xZETA cases) matter more, because they make the tree look like a tool you actually used.
