# Distinct Notification Treatment – PRD-Lite

**Prototype:** [distinct-notification-flow.html](../prototypes/distinct-notification-flow.html) · [distinct-notification-canva-mockup.html](../prototypes/distinct-notification-canva-mockup.html)
**RICE Score:** 15.3 (highest-scoring idea in this project's backlog)

---

**Problem:**
Users often forget to post their daily BeReal because the notification looks and sounds identical to every other app alert, so it's easy to scroll past without noticing — even when they intend to post that day.

**Target User:**
Users who already want to post daily but have notification-heavy phone habits — for example, students and young professionals receiving dozens of alerts a day, where a generic BeReal push has no reason to stand out from the rest.

**MAU Success Metrics:**
- Primary: Notification-to-post conversion rate — % of users who post within the capture window after receiving the notification
- Secondary: D7 / D28 posting retention; notification opt-out/mute rate (guardrail — should not increase)

**Assumptions & Non-Goals:**

*Assumptions:*
- A visually and audibly distinct notification increases the chance it's noticed, without needing to be read first.
- Existing OS notification capabilities (custom sound, rich push formatting) are enough — no new backend infrastructure is required.

*Non-Goals:*
- Solving why unmotivated users don't want to post at all.
- Adding streaks, gamification, or a new reminder cadence.
- Personalizing notification timing (a separate feature — Context-Aware Nudge).
- Redesigning the Notifications settings screen — limited to one new row inside BeReal's existing settings.

**User Stories:**
1. As a user, I want the daily notification to look and sound different from my other app alerts, so that I actually notice it and don't miss posting.
2. As a user, I want the option to turn the distinct sound/glow off, so that I stay in control of my notification experience.
3. As a user, I want this change to add no extra steps, so that posting stays as quick and simple as it is today.

**Acceptance Criteria (BDD):**

*Story 1 — Noticing the alert*
- Scenario: Distinct sound and visual treatment (Happy Path) — Given notifications are enabled, When the daily alert is sent, Then it uses a unique sound and glow/border not shared with other notification types
- Scenario: OS blocks rich notification formatting (Negative Case) — Given the device doesn't support rich formatting, When the alert is sent, Then it falls back to a standard notification
- Scenario: Custom sound fails to load (Negative Case) — Given the sound asset fails, When the alert is sent, Then it falls back to the standard default sound

*Story 2 — Staying in control*
- Scenario: Toggle appears in existing settings (Happy Path) — a "Daily BeReal Alert" toggle is visible under Posts, styled like existing rows
- Scenario: Toggle is on by default (Happy Path)
- Scenario: Turning the toggle off (Happy Path) — future notifications revert to standard
- Scenario: Notification sent while toggle is off (Negative Case) — standard notification, no distinct treatment
- Scenario: Re-enabling the toggle (Happy Path) — applies to the very next notification, no delay
- Scenario: A/B test control group (Happy Path) — control group always gets the standard notification
- Scenario: Existing settings remain unaffected (Happy Path) — all other rows keep their current behavior

*Story 3 — Keeping it simple*
- Scenario: No gamification introduced (Happy Path)
- Scenario: Core flow stays unchanged (Happy Path)
- Scenario: No new curation introduced (Happy Path)

**Guardrails:**
- *Authenticity:* Doesn't change what's captured or shown — only the delivery of the alert itself.
- *Privacy:* No new data collected; uses the existing notification permission only.
- *Simplicity:* Refines one existing touchpoint; adds no new steps to the posting flow.
- *Positive Behavior:* Helps people act on an intention they already have, without pressure, comparison, or gamification.
