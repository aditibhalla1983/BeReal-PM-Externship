# BeReal — Product Management Project

<aside>
🎯

**Goal:** Identify and prioritize product opportunities that could support BeReal MAU growth, then turn the highest-priority opportunity into a testable product concept.

</aside>

## Project at a glance

| Area | Focus |
| --- | --- |
| **Product** | BeReal |
| **Goal** | Increase MAU |
| **Primary lens** | Retention & Engagement |
| **Approach** | Product teardown → user journey → data & competitive research → feature ideation → RICE prioritization → PRD → prototype → user validation |
| **Current focus** | Distinct Notification Treatment |

## What I worked on

# 🚀 Building a High-Retention Social App: A Product Management Journey

Welcome to the lifecycle portfolio of a modern social product. This repository details the end-to-end framework of a 2026 feature backlog—moving from raw user discovery and competitive analysis into rigorous RICE engineering calibration, prototyping, focus group validation, and final roadmap sequencing.

---

## 📖 Chapter 1: Empathy & Exploration (The Discovery)

Our journey began by examining why users love real-time, authentic social networks but naturally abandon them or decay into passive scrolling over time. To map out the psychological reality of our users, we traced their emotional arcs.

- **The Problem:** When the daily app notification triggers, users hit an immediate "Blank Page" barrier. They face creative blocks on what to capture, and if they do post, they are frequently met with a quiet, inactive friends feed.
- **The Real Friction:** By mapping out user touchpoints, we discovered a fatal top-of-funnel drop-off. Users aren't ignoring our features because they dislike them; they are missing them entirely because our app notifications blend into a crowded sea of daily mobile device alert spam.

> 🛠️ **Artifact Box:** See our full User Journey Map Mapping Chart to explore our core touchpoint friction logs.
> 

---

## 🔬 Chapter 2: Scouting the Market (Competitive Research)

We brainstormed and scouted 9 specialized feature ideas designed to dismantle these friction blocks. To avoid reinventing the wheel, we anchored our exploration in proven competitor growth patterns:

- **Low-Friction Text Mechanics:** We looked at LinkedIn's Collaborative Articles, which generated a massive **270% traffic boom and a record-breaking 12.3% active engagement rate** by offering users low-pressure, structured text prompts instead of forcing them to write long posts from scratch.
- **Split-Screen Shared Objects:** We analyzed the home-screen widget app LiveIn and their highly viral 'Duet' co-shot framework, proving that merging parallel, same-moment friend shares into a singular, unified visual memory removes application isolation.

---

## 📊 Chapter 3: Eliminating Bias (The Calibrated RICE Audit)

Instead of relying on gut feelings, emotional feature picking, or executive bias, we funneled all 9 ideas through a strict, technically calibrated **RICE (Reach, Impact, Confidence, Effort)** optimization matrix to protect our engineering runway.

### The Prioritization Leaderboard

Our framework evaluated the features based on fixed engineering timelines (where Effort 1.0 represents simple client-side styling changes, and Effort 4.0 defines massive, backend-heavy architecture overhauls from scratch):

| Rank | Feature Name | Reach | Impact | Confidence | Effort | RICE Score | Status / Strategic Classification |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **1st** | **Distinct Notification Treatment** | 10 | 2.0 | 0.8 | 1.6 | **10.00** | 🚀 Tactical Quick Win (Champion) |
| **2nd** | **Post to Unlock Memories** | 9 | 2.0 | 1.0 | 2.0 | **9.00** | 🚀 Quick Win / Fast Follow |
| **3rd** | **Time Capsule** | 8 | 2.0 | 1.0 | 2.0 | **8.00** | 🚀 Quick Win / Fast Follow |
| **4th** | **Post to Unlock Friend's Duet** | 9 | 2.0 | 0.8 | 2.0 | **7.20** | 🚀 Quick Win / Fast Follow |
| **5th** | **Live Active Status (Friends Online)** | 7 | 2.0 | 1.0 | 2.0 | **7.00** | 🚀 Quick Win / Fast Follow |
| **6th** | **Daily Camera Prompts (MVP)** | 9 | 2.0 | 1.0 | 3.0 | **6.00** | 📈 Strategic Feature |
| **7th** | **Friend Throwback (Interaction)** | 7 | 2.0 | 0.8 | 2.0 | **5.60** | 📈 Strategic Feature |
| **8th** | **Today's Question** | 6 | 3.0 | 1.0 | 4.0 | **4.50** | 🏗️ Long-Term Pillar |
| **9th** | **RealMap (Private Opt-In Map)** | 5 | 2.0 | 1.0 | 4.0 | **2.50** | 🏗️ Long-Term Pillar |

### Champion Analysis: Picking the One Feature that Matters First

While high-concept features like *Today's Question* and *RealMap* are incredible long-term pillars, they are incredibly backend-heavy. We selected **Distinct Notification Treatment** as our immediate launch champion. It targets **100% of our active users (Reach: 10)** with minor engineering work (**Effort: 1.6**). Curing "alert blindness" right on the lock screen stabilizes the top of our user conversion funnel, protecting the primary daily login habit that every single downstream database architecture depends on to survive.

> 📊 **Data Source:** Access our raw spreadsheet calculations directly via the RICE Matrix Dataset.
> 

---

## 🎨 Chapter 4: Blueprinting the Champion (The PRD)

We shifted directly from data prioritization into concrete execution, mapping out the product rules and technical requirements for our new custom audio and visual alert system.

- **The Behavioral Loop:** Every 24 hours, the notification payload sends a distinct custom filename string directly to the client device, triggering a proprietary brand audio ping and a visual banner overlay.
- **User Control:** We designed a clean, low-friction privacy toggle within the native user settings dashboard to easily opt out or switch back to default system chimes.

> 📄 **Technical Deep Dive:** Read our full, developer-ready Product Requirements Document (PRD) to review the API payload parameters and setting schemas.
> 

---

## 🎯 Chapter 5: Focus Group Validation (Refine, Pivot, or Stay)

We put our interactive UI prototype to the test, gathering quantitative and qualitative feedback from a targeted focus group session ($N=7$).

- **The Quantitative Results:** Our focus group data yielded an **85% adoption intent metric**, proving that breaking alert fatigue with custom sensory cues successfully drives up instant click-through rates.
- **The Hard Qualitative Feedback:** Users explicitly told us: *"The new audio chime gets me to look at my screen immediately, but if I open the app and my friends haven't posted yet, I still get bored and leave."*

### The Strategic Verdict: Refine and Sequence

Based on this raw testing evidence, our ultimate decision was to **STAY** on the feature concept but **REFINE** the execution and pipeline order:

1. **Refinement:** We added a "Preview Sound" audio player button inside the user settings toggle menu so users can audit the chime before activation.
2. **Sequencing:** To address the "empty feed" problem exposed during user testing, we have updated our upcoming product sprint to instantly fast-track **Post to Unlock Memories** and **Post to Unlock Friend's Duet**. This guarantees an immediate personal, nostalgic payoff the second the user clicks our new notification sound.

---

## 🏗️ Chapter 6: Macro Risks & Ecosystem Interdependencies

Viewing our app roadmap as a complete product ecosystem, we outlined the core risks and architectural guidelines governing this 9-feature rollout:

1. **The Notification Opt-Out Danger:** Our downstream retention loops rely 100% on lock-screen access. If our custom audio chime or daily camera prompt text becomes annoying, users will completely turn off notification permissions at the OS system level, killing our Reach.
2. **The "Ghost Town" Data Dependency:** Content-unlocking features like *Friend's Duet* and *Friend Throwback* maintain a absolute data dependency on daily prompt creation. If users stop uploading content today, our historical memory tables run dry tomorrow, collapsing our social features.
3. **Privacy Architecture Foundations:** Niche geographic social layers like *RealMap* cannot be incrementally prototyped. They maintain a strict release dependency on an encrypted, mutual double-sided permission infrastructure to ensure total data compliance before any user coordinates are broadcasted.

### 01 — Understand the product

Mapped the BeReal user journey and identified key moments across sign-up, the daily prompt, posting, interaction, and return.

### 02 — Find growth opportunities

Used product analysis, user behavior, company data, and competitive benchmarking to identify opportunities connected to daily usage and repeat engagement.

### 03 — Generate & prioritize ideas

Developed a feature backlog and compared opportunities using **RICE: Reach × Impact × Confidence ÷ Effort**.

### 04 — Turn an opportunity into a product concept

Developed **Distinct Notification Treatment** around the problem of users missing the daily BeReal notification among other phone alerts.

### 05 — Define & validate

Created a PRD-Lite, prototype, acceptance criteria, and a focus-group discussion guide to test visibility, simplicity, and user control.

## Key deliverables

PRD-Lite: Distinct Notification Treatment

RICE Prioritization

Focus Group Plan — Distinct Notification Treatment

Test Summary Report — Distinct Notification Treatment

Distinct Notification Treatment – Flow Map

**Miro Board — Prioritization Workshop**

Focus Group Notes

## Product opportunity

**Problem**

Users who already intend to post can miss the daily BeReal notification because it can blend into the many alerts they receive on their phones.

**Opportunity**

Make the daily BeReal notification easier to notice without changing the core posting experience.

**Product concept**

Distinct Notification Treatment gives the daily notification a distinctive sound and visual treatment, with a live countdown, while keeping the capture and posting flow unchanged.

## User-centered requirements

The concept is designed around three user needs:

- **Notification Visibility** — Make the daily prompt easier to notice.
- **Keeping It Simple** — Do not add extra steps, management, or gamification.
- **Notification Control** — Let users control the distinct notification treatment.

## Prioritization → Product Definition

**Broad goal**

Increase MAU by creating stronger reasons for users to return to BeReal.

↓

**Research**

User journey + behavior + company data + competitive benchmarking

↓

**Opportunity backlog**

Multiple MAU-focused product ideas

↓

**RICE**

Compare Reach, Impact, Confidence, and Effort

↓

**Selected opportunity**

Distinct Notification Treatment

↓

**PRD + Prototype**

Define the target user, user stories, acceptance criteria, metrics, guardrails, and prototype

↓

**Validation**

Focus group to understand whether the treatment is noticeable, authentic to BeReal, simple, and useful

## Success metrics

**Primary:** Notification-to-post conversion rate

**Secondary:** D7 / D28 posting retention

**Guardrail:** Notification opt-out / mute rate should not increase

## Project takeaway

This project helped me practice moving from a broad business goal to a specific user problem, generating multiple product opportunities, prioritizing them with a structured framework, and translating the selected opportunity into a testable product concept.

<aside>
💡

**PM mindset:** Start broad, make assumptions explicit, prioritize with evidence, and validate before treating an idea as a product decision.

</aside>
