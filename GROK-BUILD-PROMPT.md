# Grok Build / Coding Agent Prompt — PONS

Copy everything below this line into your coding agent (Grok Build, Cursor, Claude, etc.) to start implementation.

---

## Mission
Build **PONS** — a social, provably-fair meme-coin table on Robinhood Chain.

You are given a locked visual design system and screen references.  
**Do not invent a new visual language.** Implement exactly what is specified.

## Product in one sentence
A pawn is a bag. The table is a pile of bags. The winner takes the pile of actual meme-coin bags. Fairness is commit-reveal.

## Visual system (locked)
- **Canvas**: warm black `#110E08` / `#1C180D`
- **Text**: white + muted gray `#8A8783`
- **Primary CTA only**: Robin Neon `#CCFF00`
- **Style**: Robinhood 2024 — modular, sparse, precise, mature. No glass, glow, neon wash, purple, casino chrome, 3D blobs, Dribbble polish.
- **One screen = one job.** State only changes the table + the one primary button.
- **Bags**: technical geometric line-art bags with a flat white circular logo plate. Drop any token logo into the plate. Bag size ≈ weight %.
- **Social**: small circular PFPs + truncated wallets (`0x7f3a…b2c1`) next to bags. Never full addresses, never leaderboard.

## Core loop
1. Empty table → “Put a coin on”
2. Pawn a meme bag (weight freezes at pawn time) → filling
3. Table fills → lock (timer + min 2 pawns) + commit hash
4. Pick (grid first; spin/crab is later skin of the same in-progress state) — animation is theater, result already committed
5. Winner claims the actual mixed meme bags
6. Anyone can Verify (hash / index / payout — three checks only)

## Jobs to implement
- See pawns + relative worth (% + thin-pool warning)
- Pawn (freeze weight)
- Watch lock → pick
- Claim
- Verify
- Bail only before lock

## States (each has exactly one primary action)
empty · filling · blocked · locked · in-progress · success · partial · error

## Defaults
- Settlement: winner receives the actual meme bags on the table
- Weight: frozen at pawn time
- Lock: timer + min 2 pawns
- Fee: labeled sliver on the table if any
- List: RH-chain meme with a pool + min-liquidity floor
- Fairness: commit hash before lock, seed after settle, one Verify tap

## Screens to build (visual source of truth in design/screens)
01 empty  
02 filling (+ PFP + truncated wallets)  
03 locked  
04 claim  
05 pawn  
06 verify  
07 in-progress (crab theater)  
08 partial-error  
09 table-list  
10 success  
11 bail-confirm  

Also mobile: m-filling, m-table-list (same system).

## Bag component
Use `design/design/bags/bag-base-empty-logo-plate.jpg` as the base.  
White circle = logo mask. Programmatically composite any token logo there.  
Stack for piles. Size by weight %.

## Killed (do not build)
- Giant wheel hero
- Chat dock
- Token encyclopedia
- Hex-dump wall
- 12-step approve
- Settings farm
- 3D roulette / coin rain / leaderboard ticker
- Spin as a separate product (it is only a later skin of in-progress)

## Implementation rules
1. Follow DESIGN.md tokens exactly. Do not invent colors, type, or chrome.
2. One primary action per state.
3. Animation is theater — result is already committed before pick plays.
4. Tickers are meme coins only. No stock/stable/portfolio language.
5. PFPs + truncated addresses only, sparse.
6. Mobile = same design language, stacked modular layout.
7. If a screen looks like a casino mock or Dribbble shot, rewrite it to match the locked style.

## Suggested start order
1. Design tokens + Bag component (with logo plate)
2. Empty → Filling → Locked (table round)
3. Pawn flow
4. Verify + Claim + Success
5. Table list + Bail
6. In-progress (crab) as theater skin
7. Mobile

## Stack (suggested, not mandatory)
- Next.js / React + Tailwind
- Robinhood Chain + standard EVM wallet
- Commit-reveal for fairness

## Deliverable
Working product UI that matches the screens in `design/screens` and the rules in `DESIGN.md`.  
Start by implementing the Bag component and the Empty → Filling → Locked loop.

---

End of prompt.
