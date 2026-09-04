# Grok Build / Coding Agent Prompt — PONS

Copy everything below this line into your coding agent to start implementation.

---

## Mission
Build **PONS** — a social, provably-fair meme-coin table on Robinhood Chain.

You are given locked design tokens and screen references.  
**Do not invent a new visual language.** Implement tokens first, then UI.

## Step 0 — Design tokens (mandatory first)
Read and implement `TOKENS.md` before any screen.

- Colors: only the named tokens (`bg`, `bg-elevated`, `text`, `text-muted`, `neon`, `error`, `warning`, …)
- Canvas: `#110E08` · CTA only: Robin Neon `#CCFF00` · Muted: `#8A8783`
- 8px spacing grid · radius 10–14px for controls
- One system sans font · no extra typefaces
- Paste the CSS variables (or Tailwind/TS object) from TOKENS.md into the project root styles
- **No glass, glow, gradients, purple, blue neon wash, casino chrome**

## Product in one sentence
A pawn is a bag. The table is a pile of bags. The winner takes the pile of actual meme-coin bags. Fairness is commit-reveal.

## Visual system (locked)
- Warm black canvas · white text · muted gray meta
- Robin Neon **only** on the single primary CTA per screen
- Technical geometric bags with flat white circular logo plate (composite any token logo)
- Sparse PFPs + truncated wallets (`0x7f3a…b2c1`)
- One screen = one job; state only changes the table + the one button

## Core loop
1. Empty → “Put a coin on”
2. Pawn meme bag (weight freezes) → filling
3. Lock (timer + min 2 pawns) + commit hash
4. Pick (theater — result already committed)
5. Winner claims actual bags
6. Verify (hash / index / payout — three checks)

## Jobs
See pawns + worth · Pawn · Lock→pick · Claim · Verify · Bail only before lock

## States → one primary action
See TOKENS.md §7 (empty→Put a coin on, filling→Pawn, claim→Claim, etc.)

## Screens (visual truth: design/screens/)
01 empty · 02 filling · 03 locked · 04 claim · 05 pawn · 06 verify · 07 in-progress · 08 partial-error · 09 table-list · 10 success · 11 bail-confirm  
Mobile: design/mobile/

## Bag component
`design/bags/bag-base-empty-logo-plate.jpg` — white circle = logo mask. Size ∝ weight %.

## Killed
Wheel · chat · encyclopedia · hex dump · 12-step approve · settings farm · roulette / coin rain / leaderboard · spin as separate product

## Implementation order
1. **Tokens** (CSS vars or `pons` TS object from TOKENS.md)
2. Button (primary neon / secondary / locked) + Input + Modal
3. Bag component (logo plate composite)
4. Empty → Filling → Locked
5. Pawn flow
6. Verify + Claim + Success
7. Table list + Bail
8. In-progress theater
9. Mobile

## Stack (suggested)
Next.js / React + Tailwind · Robinhood Chain · EVM wallet · commit-reveal

## Deliverable
Working UI matching `design/screens/` and **exactly** the tokens in `TOKENS.md`.  
Start by wiring tokens, then Bag, then Empty → Filling → Locked.

---
End of prompt.
