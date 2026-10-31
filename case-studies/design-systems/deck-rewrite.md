# Design systems deck: rewrite (owner's words + Claude's suggestions)

_Started Oct 31, 2026. Builds on `deck-outline.md` (v2, kept as is). For each slide: the owner's draft, Claude's suggested wording, and why. The owner decides the final wording._

**Order (owner's decision):** Opening → **Trend Micro** → BenQ → Synthesis.

---

## Opening

### 1. Title

**Your draft:** "Building shared patterns for complex tools, twice." Role line: UX Designer, BenQ (2020-2023) and Trend Micro (2023-2024).

**Suggested:**
> Building shared patterns for complex tools, twice
> UX Designer · Trend Micro (2023-2024) · BenQ (2020-2023)

**Why:** list the companies in the order the deck presents them, so the role line previews the structure. The title itself works: "twice" promises a comparison, and the deck delivers one.

### 2. At a glance

**Your draft:** v2 table with Trend Micro on the left and BenQ on the right.

**Suggested:** no wording changes. Keep the rows identical across both columns (starting point, my role, what I built, outcome) so the eye compares across.

### 3. The problem behind both

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

### 4. Context and why I started (was 11)

**Your draft:** looks good; you'll add product screenshots after the deck is built.

**Suggested wording for the "why I started" line:**
> As a new designer, I kept seeing the same pattern solved differently in design reviews. My manager had wanted this initiative for a while, so I took it on.

**Why:** this shows both initiative (you spotted it) and alignment (your manager wanted it) in two sentences. "Kept seeing" carries the evidence without needing numbers.

### 5. Goal and scope (was 13, moved before the audit)

**Your draft:** move this before the audit and add the goals "Accelerate future design of similar features" and "Improve consistency across products."

**Suggested:**
> **Goal:** accelerate future design of similar features, and improve consistency across products.
> **Scope:** three layers: common features and pages → common patterns → components (Tonic, the existing library). My work: the top two layers.

**Why:**
- Lead with the goal, so the model reads as the way you reached it.
- The "my work" line answers "what was yours?" before anyone asks, and shows you worked above the component level.
- The goal wording comes straight from your audit's cover page. Keep it, because it's real.

### 6. The audit (was 12, merged with the first half of 14)

**Your draft:**
> I tried to find the design and identify patterns in all three products, compare them, guess what the purpose is based on the design and my past experience, benchmark external library and internal parent library (VisionOne) that we're deriving from, note down the gaps, inconsistencies, open questions, and potential suggestions, then I walked these through during design meetings and get alignment with all designers.

**Suggested** (6 steps, one verb each):
> 1. **Collect:** find every instance of a pattern across the 3 products.
> 2. **Compare:** put them side by side.
> 3. **Infer intent:** work out the likely purpose from the design and my experience, since the rationale wasn't documented.
> 4. **Benchmark:** against Vision One, the parent product our design language derives from, and public systems (IBM Carbon, Ant Design, Adobe).
> 5. **Note:** gaps, inconsistencies, open questions, and possible fixes.
> 6. **Align:** walk each product's designers through it in design meetings and agree on the guideline.
>
> Transition line (spoken or at the bottom of the slide): *Most patterns aligned quickly. One didn't.*

**Why:**
- A numbered list of verbs scans in seconds; the paragraph version makes the listener hold six ideas in one breath.
- **"Guess" → "infer intent."** Same honesty, but it sounds like a method rather than a shot in the dark. Keeping "since the rationale wasn't documented" stays truthful about the limit.
- **"Internal parent library" → "parent product our design language derives from."** Vision One is a product with its own guidelines. Calling it a "library" could invite "so you copied its components?"
- The transition line builds tension and leads straight into the standoff. It's the cheapest storytelling move in the deck.

### (was 14: From observation to reasoning). Removed

The first half is merged into slide 6 (step 6). The second half, "one thing that changed my view," is now covered by your two new example slides. See the note at the end of this file.

### 7. The hardest call: modal vs. drawer vs. page (was 15)

**Your draft:** good as is.

### 8. The decision tree (was 16)

**Your draft:** you'll add the full tree visual yourself.

**Suggested slide headline:**
> We agreed on the questions, so the answers stopped being opinions.

**Why:** a headline that states the takeaway means the slide makes its point even if the listener only glances at it. This line puts your own words ("hard for them to keep selling on their subjective ideas") in a positive form.

### 9. Example 1: a designer's exception became a new branch (new)

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

### 10. Example 2: viewing details needed criteria, not one answer (new)

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

### 11. Governance: how the system grows (was 17)

**Your draft:** looks good; you'll add screenshots of the flow. Answer to your question about redrawing is at the end of this file.

### 12. Outcome and honest limits (was 18)

**Your draft:** looks good.

---

## Part 2: BenQ

_Owner is writing this section._

## Synthesis

_Owner is writing this section._

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
