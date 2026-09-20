# Project Journey — BeReal Feature Growth Case Study

A chronological walkthrough of this project, from the first concept explored through to the final, fully-specified feature ready to build.

---

## Phase 1 — RealWorld: A Privacy-First Alternative to Snap Map

The project began with a single concept: **RealWorld**, a map feature for BeReal inspired by Snap Map, but built around static, timestamped location stamps instead of continuous live tracking.

- [Product Teardown](research/realworld-product-teardown.md) — product mechanics, UX layers (Today's Moments / Footprints / RealWorld Public), growth loop analysis, AI suite integration (Smart Clusters, Predictive Meet-Up Triggers, Privacy Defending AI), and risk mitigation
- Initial prototype → revised after feedback that privacy controls were too buried → final version: [realworld-privacy-first-prototype.html](prototypes/realworld-privacy-first-prototype.html)
  - Persistent privacy status header, color-coded shield states (Protected / Adjusted / Higher Risk / Off), pre-post location decision, and a redesigned "Map Safety" sheet with a prominent "Pause all map sharing" action

**Key decision:** location sharing should always show *who* can see it and *how precise* it is, visible before, during, and after posting — not buried in settings.

---

## Phase 2 — Mapping the Existing User Journey

Before generating new ideas, the current BeReal user experience was mapped end-to-end.

- [BeReal User Journey Map](prototypes/bereal-user-journey-map.html) — 10 stages (Discovery through Returning Tomorrow) × 5 rows (Objectives, Need, Touchpoints, Pain Points, Opportunities)
- Refined collaboratively — several pain points/opportunities were corrected or removed after being challenged (e.g., "First-Time Setup" pain point was invalidated once confirmed multi-channel friend invites already exist)

**Key decision:** don't accept a first-draft pain point at face value — validate each one against actual product behavior before treating it as real.

---

## Phase 3 — Competitive Landscape

- [Competitive Analysis](research/bereal-competitive-analysis.md) — direct clones (Snapchat Dual Camera, Instagram Instants, TikTok Now — discontinued), independent apps (Locket, Poparazzi, Dispo), and adjacent apps (Gas, Rawly)
- Full feature comparison matrix across 8 apps and 14 features
- Identified whitespace: **no competitor has solved structured collaborative posts** (merging multiple people's photos into one shared post) — this directly informed later feature ideas

---

## Phase 4 — Feature Brainstorming (Multiple Rounds)

Several rounds of structured ideation, each solving a different engagement problem:

- [10 Feature Remixes](research/bereal-feature-remix.md) — Instagram/Snapchat/TikTok mechanics reimagined for authenticity + minimalism (e.g., Streaks → "Honesty Streaks," Duets → "Same Moment")
- [Collaborative Posts](research/bereal-collaborative-posts.md) — Same Moment, Group BeReal, Moment Request, and 7 other ideas for shared moments
- [Drop-off Fixes](research/bereal-dropoff-fixes.md) — solving three distinct problems: forgetting to post, boredom after posting, and low friend-checking ([table version](research/bereal-dropoff-fixes-table.docx))
- A running **Feature Idea Table** (10 → 16 ideas) was built and maintained in Notion, scored against three questions: *exciting, fast to build, reflects BeReal's values*

Individual flow prototypes were built for several ideas to test them concretely:
[Daily Question](prototypes/daily-question-flow.html) · [Friend Check-In](prototypes/friend-checkin-flow.html) · [Friend Throwback](prototypes/friend-throwback-flow.html) · [Real-Life Prompt](prototypes/real-life-prompt-flow.html) · [Today's Circle](prototypes/todays-circle-flow.html) · [Reply Prompt](prototypes/reply-prompt-flow.html) (later removed — redundant with existing notifications) · [Friend's Duet](prototypes/friends-duet-flow.html)

**Key decision:** several near-duplicate ideas were caught and resolved rather than shipped separately — Today's Circle was deprioritized in favor of Friend Check-In (same data, worse scope), and Friend's Duet was folded into Golden Memory as a rotating type instead of a standalone feature.

---

## Phase 5 — Golden Memory Deep Dive

The most heavily developed concept before the final feature: **Golden Memory**, a "post to unlock a memory" system using event-first, rules-based selection (not heavy AI).

- Full MVP backlog (GM-01 through GM-35+), a decision-tree selection model (event tag → anniversary → AI-personalized → fallback), and a scoring formula using only existing data signals
- [MVP Prototype](prototypes/golden-memory-mvp-prototype.html) — reveal screen with rotating types (Event Memory, On This Day, Friend Duet, Personal Ritual), visible selection-rule badges, an expandable "How was this picked?" decision tree, and a Memories home screen (Calendar/People/Places)
- [Golden Memory flow](prototypes/golden-memory-flow.html)

**Key decision:** Friend's Duet was merged into Golden Memory as one of several rotating reveal types rather than kept as a separate feature — reducing feature clutter while increasing variety.

---

## Phase 6 — Prioritization (RICE)

All ideas were scored using RICE (Reach × Impact × Confidence ÷ Effort) in a Notion backlog, alongside a simpler 3-question prioritization pass (Exciting / Fast to Build / Reflects BeReal Values).

Initial read: Daily Question led on ease of build; Golden Memory scored slightly lower but carried a stronger emotional/retention case.

**Turning point:** a late addition — **Distinct Notification Treatment** — was added to address a specific, previously under-examined problem (the daily notification blending into other app alerts). Once scored, it had the **highest RICE score of any idea in the backlog (15.3)**, driven by the broadest reach, lowest effort, and highest confidence of any feature on the list.

**Key decision:** re-framed the project's primary recommendation from a "growth feature" (Golden Memory, RealWorld Map) to a "retention infrastructure" feature (Distinct Notification Treatment) — explicitly reasoned as *ship this first to protect the baseline*, with the bigger, more exciting ideas sequenced after it.

---

## Phase 7 — PRD-Lite: Distinct Notification Treatment

- [PRD-Lite](prds/distinct-notification-treatment-PRD-lite.md) — Problem, Target User, MAU Success Metrics, Assumptions & Non-Goals, User Stories, Acceptance Criteria, Guardrails
- Acceptance criteria were converted to **BDD (Given/When/Then)** format, then iteratively refined:
  - Split overloaded scenarios (too many "And" clauses) into clean, single-behavior scenarios
  - Removed a criterion that wasn't user-observable ("no new backend required" — moved to Assumptions, where it belongs)
  - Added missing **negative and edge cases**: OS blocking rich notification formatting, sound asset failing to load, A/B control-group behavior, and a regression check confirming existing settings stay unaffected
  - Labeled every scenario **(Happy Path)** or **(Negative Case)**

**Key decision:** a "User Story 3" (keeping the feature simple) was identified as a guardrail wearing a user-story costume, not a genuine user goal — clarifying that the feature's real value lives entirely in Stories 1 and 2.

---

## Phase 8 — MVP Flow Map

- [Flow Map](prds/distinct-notification-treatment-flow-map.md) — 5–6 screens (Notification → Camera → Post Confirmation → Repeat Loop → Fallback → Settings), each with User Action / System Reaction / State / Microcopy
- Two deliberate deviations from the standard template, both explained explicitly: **no onboarding screen** (feature is default-on, zero new steps) and **an invisible error state** (failures fall back silently rather than showing a technical error message)
- Microcopy was refined collaboratively (e.g., the Settings toggle-off state needed its own confirmation message — *"You'll get the standard notification now."* — since the original copy wasn't actually responding to the user's action)

---

## Phase 9 — Prototype

Two versions were built to make the flow tangible:

- [Distinct Notification Flow (detailed walkthrough)](prototypes/distinct-notification-flow.html) — matches BeReal's real Notifications settings screen exactly, with the new row inserted in place
- [Clickable Canva-style Mockup](prototypes/distinct-notification-canva-mockup.html) — 5 linked, navigable screens simulating a real click-through prototype
- [Visual Flow Diagram](assets/distinct-notification-flow-map.png) — exportable board for Canva import
- [Canva Build Spec](prds/canva-build-spec-distinct-notification.md) — full screen-by-screen content (headers, visuals, microcopy, button links) for rebuilding the prototype directly in Canva

**Key decision:** MAU-oriented "hooks" (streaks, reminders, return banners) requested by a later module were deliberately *not* added, since they directly contradicted this feature's own Non-Goals. Instead, the feature's existing elements (the countdown as trigger, the warm post-confirmation as reward) were reframed to answer the exercise honestly — this feature increases MAU by protecting an existing loop, not manufacturing a new one.

---

## The Throughline

Across all nine phases, a few principles held constant:

1. **Validate before building** — pain points, ideas, and even "obvious" additions were challenged and sometimes rejected (contact-access framing, Today's Circle vs. Friend Check-In, the countdown-as-AC question)
2. **Privacy and simplicity as constraints, not features** — from RealWorld's shield states to Distinct Notification's silent error handling, restraint was treated as a design decision worth defending, not a gap to fill
3. **Retention over manufactured growth** — the project's final recommendation deliberately favors a low-glamour, high-confidence fix over a flashier feature, because it protects the habit loop every other idea depends on
