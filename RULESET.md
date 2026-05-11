# Black Jack's BlackJack — Ruleset

Version: v0.0.15

---

## Overview

A strategy-first blackjack variant set at J. Black's underground lounge. You see all 8 cards before you commit, so the game is about smart placement, not luck of the draw.

---

## Setup

- 8 cards are dealt face-up on the felt.
- You tap a card to pick it up, then tap a hand slot to place it.
- Build 3 hands of 2 cards each from the 8 available. The 2 leftover cards are burnt.
- The house receives 6 cards split across 3 hands at random (no player choice on house placement).

---

## Hand Values

Standard blackjack values:
- Number cards (2-10): face value.
- Face cards (J, Q, K): 10.
- Ace: 11 or 1 (whichever keeps the hand below 22).
- Blackjack: Ace + 10-value card dealt as the first two cards = instant win for that hand.

---

## Playing a Round

After placement, hands are played in order: Hand 1 vs house Hand 1, then Hand 2, then Hand 3.

Each hand: you choose **Hit** (take another card) or **Stand** (hold your total).

House rules:
- House hits on 16 or under.
- House holds on 17 or above.

Outcomes per hand:
- Closer to 21 without busting = win.
- Over 21 = bust = lose that hand.
- Tie = draw (neither player wins the hand).
- Blackjack (21 on first two cards) beats a non-blackjack 21.

---

## Match and Series Structure

- **Match:** Win 2 of 3 hands to win the match.
- **Series:** Win 3 matches to win the series (best of 5).
- A new series starts fresh; matches carry over until one player reaches 3.

---

## ELO Rating

- Starting ELO: 1200.
- Win a match: ELO increases. Lose: ELO decreases.
- Standard ELO scaling: the stronger your rating relative to the opponent, the less you gain on a win and the more you lose on a defeat.
- Your ELO persists across sessions via localStorage.

---

## Strategy Notes

- All your cards are visible before placement. Optimal placement distributes strong totals across all 3 hands rather than stacking one.
- Aces are most valuable in Hand 1 to guarantee a high opener or Blackjack opportunity.
- A hand of 12-16 is dangerous: too high to hit safely, too low to hold reliably against a house that hits to 17.
- Placement is irreversible once confirmed — plan before you commit.
