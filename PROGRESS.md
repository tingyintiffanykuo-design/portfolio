# Progress

_Last updated: Oct 30, 2026_

## Current focus

**Design systems case study** (BenQ + Trend Micro), for the Amazon Robotics Sr. Product Designer application (`jobs/amazon-robotics-sr-product-designer.md`). Working notes: `case-studies/design-systems/notes.md`. Deck outline: `case-studies/design-systems/deck-outline.md`.

Order: (1) interview slide deck, which is the priority and must be thorough; (2) 1-page web version; (3) full case study.

Mode: **discovery done; outlining.** Don't build slides until the owner asks. Ask only questions that matter for a strong case study or the outline. Detail questions come up while building slides together.

**Terminology:** the owner was a UX designer at BenQ (the title said "UI designer"; never use it). The two people who owned components and tokens are "GUI designers" or "visual designers."

Status: BenQ facts collected and the BenQ Figma files reviewed. Trend Micro audit and guideline files reviewed (notes section 9). Deck outline revised to v2 around the sharpened story (Oct 30). Both collaboration practice docs reviewed (notes section 10). Open `[ASK]` items are in notes sections 9 and 10.

**Reminder for Claude:** while building the Trend Micro and synthesis slides, ask the owner for more detail on the identify → detect → analyze → recover mapping before using the robotics parallel.

## Decision log

| Date | Decision | Why |
|---|---|---|
| Oct 14, 2026 | Positioning, headline, AI claims policy, and case study lineup | See `portfolio-spec.md` sections 5, 6, and 10 |
| Oct 28, 2026 | This repo holds progress and decisions, not just the spec | Owner works across devices and needs the context to travel |
| Oct 28, 2026 | Drafting split: owner writes narrative; Claude drafts factual blocks and gives structure and line edits | Keeps the core writing in the owner's voice (spec requirement 9) |
| Oct 28, 2026 | Pause the DMS rewrite; prioritize a design systems case study | Amazon Robotics JD asks for "scalable mechanisms and reusable design patterns"; more urgent than DMS |
| Oct 30, 2026 | Resume is the source of truth where it conflicts with the spec | Owner confirmed the resume claims |
| Oct 30, 2026 | One combined BenQ + Trend Micro case study; deck first, then 1-page web, then full | Interview use is most urgent |
| Oct 30, 2026 | Hold off on slides; work in mentor/discovery mode first | Owner wants to surface the strongest material before producing anything |
| Oct 30, 2026 | Discovery done; stop detail questions and move to outlining | Owner will fill details while building slides |
| Oct 30, 2026 | Build the deck in Figma Slides (when the owner asks); about 12-15 min of talking in a 1-hour, 2-3 case interview | Owner's interview format; priorities ranked in the deck outline |
| Oct 30, 2026 | Redraw internal Figma artifacts in English for the deck rather than screenshot them | Files are internal and in Chinese; spec requirement 7 |

## Parked (resume later)

- **DMS case study**: open questions 1-10 in the Oct 28 conversation, which mirror spec section 11, questions 1-9. Next step after answers: Priority 1 package (spec 8.3).
- **Subtitle**: proposed dropping "lab teams" from candidate 1 ("Software that robot engineers and security analysts rely on, shaped by how they actually work."). Not yet confirmed.
- **DMS "See next project" link**: points to the excluded e-commerce page. Fix pending a decision (Robot HMI vs. remove).
- **Network:** www.benq.com is blocked by the cloud environment's network policy. To fix, add it under the environment's Network access > Allowed domains.
- **Screenshots** of the DMS page images and GIFs: the owner will add them later. Ask when the visual review is needed.

## Notes

- **Resume fix (owner):** the Trend Micro line should say 3 platforms, not 4. Also consider "5 pattern and 6 page guidelines" instead of "11 reusable UI patterns."

- Resume (`Resume_Amazon Robotics_Product Designer_Tiffany Kuo.pdf`) lists experience the spec doesn't cover: Tactile (UX Designer, Apr 2026 to present; this appears to be the Robot HMI project) and Fluke (UX Research Intern, 2025). The spec says "about 3 years"; the resume says "4+". Reconcile in the spec when convenient.
