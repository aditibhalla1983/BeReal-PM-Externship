# Distinct Notification Treatment – Flow Map

**Visual board:** [../assets/distinct-notification-flow-map.png](../assets/distinct-notification-flow-map.png)
**Clickable prototype:** [../prototypes/distinct-notification-canva-mockup.html](../prototypes/distinct-notification-canva-mockup.html)

## Notes on adapted states
- **No Intro/Permission screen** — default-on with zero new setup steps; the notification itself is the first moment.
- **Error state is invisible to the user, on purpose** — a failed sound/formatting silently falls back to a standard notification rather than showing a technical error message.

## Flow Summary (Template Format)

| Screen | User Action | System Reaction | State | Microcopy |
|---|---|---|---|---|
| Notification | Tap the notification | Opens camera screen | Success | "2 min left to capture today's moment" |
| Post | Submit photo | Shows confirmation | Success | "Nice one, Aditi — your BeReal is live!" |
| Repeat (Day 2+) | Recognizes cue instantly, taps | Opens camera screen | Success | Same as Day 1 — consistency by design |
| Fallback | Taps standard notification | Opens camera screen (silent) | Error | None shown — failure is invisible to the user |
| Settings | Taps "Daily BeReal Alert" toggle off | Reverts to standard notification | Success / Opt-out | "You'll get the standard notification now." |

## Why this flow is intentionally thin

The real new surface area is just: one notification treatment, one silent fallback, and one settings row. This feature protects an existing journey rather than adding a new one.
