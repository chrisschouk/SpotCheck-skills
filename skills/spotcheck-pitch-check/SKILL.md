---
name: spotcheck-pitch-check
description: Use when a curator has offered a placement and you need to decide whether to pay. Reads the offer, checks the price against the risk, and names what the curator will not tell you.
---

# Curator pitch check

The offer arrives before the playlist. Read the offer first.

## When to use

- A curator has quoted a price for a placement.
- Someone asks "is this deal normal?"
- A pitch promises streams, saves, or playlist adds.

## Procedure

1. **Extract the terms.** Price, playlist name and link, placement length, promised
   outcome, payment method, and what happens if the track is removed early.
2. **Flag the promises.** Any specific stream count, any "guaranteed" language, any
   claim of playlist editorial support. These are the reliable tells.
3. **Check the playlist separately.** Run `spotcheck-verdict` on the link. Do not
   score the pitch and the list together.
4. **Compare price to risk.** State the cost of the placement against the cost of
   one dodged fake list. If the price is above the monthly cost of a checking tool,
   say so plainly.
5. **Name the gaps.** What the curator has not told you: removal policy, refund
   policy, who else is on the list, and whether the list is owned or rented.

## Hard rules

- Never approve a payment. The output is a read, not a decision.
- Never guess a market rate. If you do not know it, say you do not know.
- Never repeat a promise the curator made as if it were a fact.
- Public data only. Do not sign in to check anything.

## Output

The terms as understood, the promise flags, the playlist verdict reference, the gaps,
and a one-line recommendation: pay, negotiate, or walk.
