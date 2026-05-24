#  Zolve Student Dash

A browser-based mini-game designed as a case study proposal for [Zolve](https://zolve.com) 

---

## 💡 The Problem

When Zolve's onboarding servers are rate-limited or overloaded, users see a generic error screen:

> *"You don't have access to do this right now, or there have been too many requests. Please try again in a bit."*

---

## 🎮 The Proposed Solution

Instead of a dead-end error screen, redirect users to a **branded mini-game** that:

- Keeps them **engaged** while the server recovers
- **Polls the server** in the background every 60 seconds
- **Auto-notifies** users the moment they can continue, no manual refreshing needed

---

## Gameplay

- A Zolve student in a purple hoodie runs across a campus-style track
- **Jump** to catch floating dollar bills 💰
- **Dodge** flying textbooks 📚
- A countdown timer simulates server recovery time
- When the timer hits zero, a **"You're all set!"** overlay appears with a CTA to continue onboarding

**Controls:** `Tap` / `Click` / `Space` / `↑ Arrow` to jump

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

## 🛠️ Built With

- Vanilla HTML5 Canvas
- Zero external dependencies
- Zolve brand colors

---

*This is an independent UX concept and is not affiliated with or endorsed by Zolve.*
