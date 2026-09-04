# PONS — Design System (Coder Handoff)

**Product**: Social provably-fair meme-coin table on Robinhood Chain  
**Visual lock**: Robinhood 2024 identity + unique technical bag illustration  
**Status**: Ready for implementation

---

## Start here for coding agents

1. **`TOKENS.md`** ← design tokens (colors, space, type, components, CSS/Tailwind/TS)
2. **`GROK-BUILD-PROMPT.md`** ← paste into the agent
3. **`design/screens/`** ← visual source of truth
4. **`design/bags/bag-base-empty-logo-plate.jpg`** ← bag component base

**Do not invent tokens.** Everything basic lives in `TOKENS.md`.

---

## Brand summary (see TOKENS.md for full)

| Role | Value |
|------|--------|
| Canvas | `#110E08` |
| Elevated | `#1C180D` |
| Text | `#FFFFFF` |
| Muted | `#8A8783` |
| **CTA only** | Robin Neon `#CCFF00` |
| Error | `#FF4D4D` |
| Warning | `#F5A623` |
| Grid | 8px |
| Radius primary | 10–14px |
| Type | system geometric sans only |

### Hard rules
- One primary Neon button per screen
- No glass, glow, gradient, purple, blue neon wash, casino chrome
- Bags: technical line art + white circular logo plate (token logo composited)
- Social: small PFP + truncated wallet `0x7f3a…b2c1` only
- One screen = one job; state only changes the table + the one button

---

## Core Jobs
1. See pawns + relative worth (% + thin-pool warning)
2. Pawn (freeze weight at pawn time)
3. Watch lock → pick
4. Claim
5. Verify (hash / seed / payout — three checks only)
6. Bail only before lock

## States (one primary action each)
empty · filling · blocked · locked · in-progress · success · partial · error

## Defaults
- Settlement: winner gets the actual meme bags
- Weight frozen at pawn
- Lock: timer + min 2 pawns
- Fee: labeled sliver if any
- List: RH-chain meme with pool + min-liquidity floor
- Fairness: commit hash before lock, seed after settle, one Verify tap

## Screen Map
| # | State | File |
|---|-------|------|
| 01 | empty | design/screens/01-empty.jpg |
| 02 | filling | design/screens/02-filling.jpg |
| 03 | locked | design/screens/03-locked.jpg |
| 04 | claim | design/screens/04-claim.jpg |
| 05 | pawn | design/screens/05-pawn.jpg |
| 06 | verify | design/screens/06-verify.jpg |
| 07 | in-progress | design/screens/07-in-progress-crab.jpg |
| 08 | partial-error | design/screens/08-partial-error.jpg |
| 09 | table-list | design/screens/09-table-list.jpg |
| 10 | success | design/screens/10-success.jpg |
| 11 | bail-confirm | design/screens/11-bail-confirm.jpg |

## Social Identity
- Small circular PFPs next to each bag / pawn
- Truncated wallet only: `0x7f3a…b2c1` (muted)
- Never full address, never leaderboard

## Killed (do not ship)
Giant wheel · chat dock · token encyclopedia · hex-dump wall · 12-step approve · settings farm · 3D roulette / coin rain / leaderboard ticker · spin as separate product

## Coder Rules
1. Wire **TOKENS.md** first — no freestyle colors
2. One primary action per state
3. Animation is theater — result already committed
4. Tickers are meme coins only
5. Mobile = same tokens, stacked layout
6. If it looks like a casino mock or Dribbble shot, rewrite to tokens

## Visual consistency lock (screens)
- One master system: warm black canvas, white wireframe technical bags on circular platform, right stats list, PFP + `0x…` wallets, Robin Neon primary bottom-left
- All desktop screens share that chrome — only state content changes
- Bags: faceted wireframe + white circular logo plate
- No light/cream paper backgrounds, no blue glow, no alternate bag styles
