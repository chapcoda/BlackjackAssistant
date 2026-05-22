# 🃏 Blackjack Strategy Trainer

A browser-based Blackjack Strategy Trainer that combines a complete playable game with a real-time statistical analysis engine. Built to help players understand not just *what* the optimal play is — but *why*, backed by simulated data.

**▶ Play it live → **(https://chapcoda.github.io/BlackjackAssistant)**

## What It Does

Most blackjack strategy tools tell you what to do. This one shows you the math behind it.

The app runs two independent strategy engines simultaneously for every hand:

### 1. Basic Strategy Engine
A pre-computed decision table covering 350 unique hand situations:
- **Hard totals** (5–21) vs. all dealer upcards (2–A)
- **Soft totals** (soft 13–21) vs. all dealer upcards
- **Pairs** (2–2 through A–A) vs. all dealer upcards

Every decision is based on mathematically optimal basic strategy for a 4–8 deck shoe. The result — HIT, STAND, DOUBLE, or SPLIT — is displayed instantly as the primary recommendation.

### 2. Monte Carlo Simulation Engine
A live simulator runs **10,000 hands** for each possible action (Hit, Stand, Double) and returns:

| Metric | Description |
|---|---|
| **Win %** | Percentage of simulated hands won outright |
| **Loss %** | Percentage lost, including busts |
| **Push %** | Percentage that tied the dealer |
| **Bust %** | Percentage the player hand exceeded 21 |
| **Expected Value (EV)** | Average return per dollar wagered over the long run |

The **EV column** is the most important number — it tells you not just which action is best, but by how much.

---

## Two Modes

### Practice Trainer
A fully playable blackjack game with:
- $1,000 starting bankroll with chip betting ($5, $10, $25, $50, $100)
- Blackjack pays 3:2
- Double down, split, hit and stand options
- Live Monte Carlo analysis running in parallel every hand
- Session stats tracking win rate, net P&L, and correct play percentage

### Manual Assistant
Enter any hand you're currently holding at a real table and get:
- The optimal basic strategy play instantly
- Full statistical breakdown across all possible actions backed by 10,000 simulated outcomes

---

## Game Rules & Deck Model

- **6-deck shoe** (312 cards), shuffled with the Fisher-Yates algorithm
- Reshuffle triggered when fewer than 26 cards remain (~8% penetration)
- Dealer stands on all 17s (including soft 17)
- No suits — rank only, consistent with strategy simulation standards

---

## Tech Stack

| Layer | Details |
|---|---|
| Frontend | HTML, CSS, Vanilla JavaScript |
| Strategy Engine | Hardcoded lookup table (350 decisions) |
| Simulation Engine | Custom Monte Carlo simulator (10,000 iterations per action) |
| Hosting | GitHub Pages |

No frameworks, no dependencies, no build step. Runs entirely in the browser.

---

## Running Locally

```bash
git clone https://github.com/chapcoda/BlackjackAssistant.git
cd BlackjackAssistant
open index.html
```

No install required. Open `index.html` directly in any modern browser.

---

## License

MIT — free to use, modify, and distribute with attribution.
