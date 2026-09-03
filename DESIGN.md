# PONS — Design System (Coder Handoff)

**Product**: Social provably-fair meme-coin table on Robinhood Chain  
**Visual lock**: Robinhood 2024 identity + unique technical bag illustration  
**Status**: Ready for implementation

---

## Brand Tokens (do not invent new ones)

### Color
- Canvas / BG: warm black `#110E08` (or `#1C180D`)
- Text primary: white `#FFFFFF`
- Text secondary / muted: `#8A8783` / `#B4B1AB`
- Surface / cards: `#1C180D` or slight lift
- **Robin Neon (CTA only)**: `#CCFF00`
- Error / fail: soft red `#FF4D4D` (sparingly)
- Success: Robin Neon or clean white check

### Typography
- Headlines: clean geometric sans (system or RH Phonic equivalent)
- Body / UI: same family, regular weight
- Short labels only. No lorem. Real tickers + $ + token amounts.
- One primary action per state.

### Spacing & Layout
- Modular 8px grid
- Generous empty space (less is more)
- One screen = one job. State only changes the table + the one button.

### Bag System (programmatic)
- Base asset: `design/design/bags/bag-base-empty-logo-plate.jpg`
- White circular plate = logo mask
- Drop any token logo (PNG transparent) into the plate
- Size / weight of bag = relative % of table
- Stack for piles when multiple

### Icons / Chrome
- Minimal. Thin white line icons only.
- No glass, glow, neon wash, purple, casino chrome, 3D blobs, Dribbble polish.

---

## Core Jobs (from MATRIX)
1. See pawns + relative worth (% + thin-pool warning)
2. Pawn (freeze weight at pawn time)
3. Watch lock → pick
4. Claim
5. Verify (hash / seed / payout — three checks only)
6. Bail only before lock

## States (one primary action each)
- empty
- filling
- blocked
- locked
- in-progress (pick theater)
- success
- partial
- error

## Defaults
- Settlement: winner gets the actual meme bags
- Weight frozen at pawn
- Lock: timer + min 2 pawns
- Fee: labeled sliver if any
- List: RH-chain meme with pool + min-liquidity floor
- Fairness: commit hash before lock, seed after settle, one Verify tap

## Screen Map
| # | State | File | Notes |
|---|-------|------|-------|
| 01 | empty | design/design/screens/01-empty.jpg | dotted table, Put a coin on |
| 02 | filling | design/screens/02-filling.jpg | bags + PFP + wallets + Pawn |
| 03 | locked | design/screens/03-locked.jpg | frozen, can't bail |
| 04 | claim | design/screens/04-claim.jpg | you won the bag |
| 05 | pawn | design/screens/05-pawn.jpg | select bag, freeze weight |
| 06 | verify | design/screens/06-verify.jpg | hash / seed / three checks |
| 07 | in-progress | design/screens/07-in-progress-crab.jpg | crab theater (result already committed) |
| 08 | partial-error | design/screens/08-partial-error.jpg | 2 of 3 bags, Retry |
| 09 | table-list | design/screens/09-table-list.jpg | discovery |
| 10 | success | design/screens/10-success.jpg | claimed |
| 11 | bail-confirm | design/screens/11-bail-confirm.jpg | leave before lock only |

## Social Identity (PFP + Wallet)
- Small circular PFPs next to each bag / pawn
- Truncated wallet only: `0x7f3a…b2c1` (muted gray)
- Never full address, never leaderboard, never dense wall
- Serves: see who is at the table, verify, claim, social proof

## Killed (do not ship)
- Giant wheel hero
- Chat dock
- Token encyclopedia
- Hex-dump wall
- 12-step approve
- Settings farm
- 3D roulette / coin rain / leaderboard ticker
- Spin as separate product (spin = later skin of in-progress)

## Coder Rules
1. One primary screen. State changes the table and the one button.
2. Animation is theater — result already committed.
3. Tickers on bags are meme coins only. Logos on bags. No fund names.
4. Mobile = same system, stacked modular cards if needed.
5. Do not invent tokens, typefaces, or a visual system. Tokens live in this doc.
6. If it could ship on Dribbble or looks like a casino mock, it failed.
