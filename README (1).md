# 🎓 Zolve Student Dash — UX Prototype

A browser-based mini-game designed as a UX case study proposal for [Zolve](https://zolve.com) — a fintech platform built for international students entering the US banking system.

---

## 💡 The Problem

When Zolve's onboarding servers are rate-limited or overloaded, users see a generic error screen:

> *"You don't have access to do this right now, or there have been too many requests. Please try again in a bit."*

For international students — already navigating an unfamiliar financial system in a new country — this creates **anxiety, confusion, and drop-off** at the most critical moment of their onboarding journey.

---

## 🎮 The Proposed Solution

Instead of a dead-end error screen, redirect users to a **branded mini-game** that:

- Keeps them **engaged** while the server recovers
- Reinforces **Zolve's identity** (student life, dollars, campus vibes)
- **Polls the server quietly** in the background every 60 seconds
- **Auto-notifies** users the moment they can continue — no manual refreshing needed

---

## 🕹️ Gameplay

- A Zolve student in a purple hoodie runs across a campus-style track
- **Jump** to catch floating dollar bills 💰
- **Dodge** flying textbooks 📚
- A countdown timer simulates server recovery time
- When the timer hits zero, a **"You're all set!"** overlay appears with a CTA to continue onboarding

**Controls:** `Tap` / `Click` / `Space` / `↑ Arrow` to jump

---

## 🎨 Design System

Matches Zolve's brand palette:

| Token | Value | Usage |
|---|---|---|
| Primary | `#6B5CE7` | Header, body, student hoodie |
| Accent | `#F4A14A` | Timer bar, hat, CTA buttons |
| Background | `#F4F1FF` | Page background |
| Surface | `#EDE8FF` | Score bar, UI elements |
| Success | `#22C55E` | Dollar bills, ready state |

---

## ⚙️ How It Works Technically

```
Error triggered on Zolve's server
        ↓
User redirected to game page (client-side, zero server load)
        ↓
Game runs entirely in the browser (HTML + Canvas + JS)
        ↓
Background polling pings server every 60s (tiny request)
        ↓
Overlay appears when server is ready → user clicks to continue
```

### Why This Doesn't Burden the Server

| Component | Runs on | Server load |
|---|---|---|
| Game engine | User's browser | ✅ Zero |
| Countdown timer | User's browser | ✅ Zero |
| Server ready-check | Browser → Server | ✅ One small ping/min |

> The current UX (users frantically refreshing) generates **far more** server load than a controlled 60-second polling interval.

---

## 📁 File Structure

```
zolve-student-dash/
├── index.html        ← The entire game (self-contained)
└── README.md         ← This file
```

No dependencies. No build step. Just open `index.html` in any browser.

---

## 🚀 Running Locally

```bash
git clone https://github.com/your-username/zolve-student-dash.git
cd zolve-student-dash
open index.html
```

Or simply drag `index.html` into any browser window.

---

## 📖 Case Study Context

This prototype was built as part of a UX case study analyzing Zolve's onboarding experience. Key findings include:

1. **Error screen UX** — vague messaging with no actionable path forward
2. **SSN flow hierarchy** — passport alternative exists but is visually de-prioritized for their core international student audience
3. **Brand-experience gap** — playful marketing tone vs. clinical error handling

This game prototype demonstrates how **error states can become brand moments** rather than drop-off points.

---

## 🛠️ Built With

- Vanilla HTML5 Canvas
- Zero external dependencies
- Zolve brand colors

---

*This is an independent UX concept and is not affiliated with or endorsed by Zolve.*
