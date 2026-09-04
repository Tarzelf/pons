# Table.family — Brand

**Product name**: Table.family  
**Former internal name**: Pons (deprecated — do not ship)

Social, provably-fair meme-coin **table**. A pawn is a bag. The table is a pile of bags.

---

## Name usage

| Correct | Incorrect |
|---------|-----------|
| Table.family | Table Family |
| table.family (URL/domain) | TableFamily |
| Table (short UI) | PONS / Pons |

- Always include the period: **Table.family**
- Period may be rendered as Robin Neon `#CCFF00` solid circle
- "Table" = white primary weight
- ".family" = muted `#8A8783` (or same white at slightly smaller optical weight)

---

## Logo system

Files in `design/brand/`:

| File | Use |
|------|-----|
| `wordmark.jpg` | Primary horizontal wordmark |
| `lockup.jpg` | Mark + wordmark |
| `app-icon.jpg` | App icon / mark (table + 3 bags) |
| `monogram.jpg` | Favicon / tight spaces (T + ring) |
| `brand-sheet.jpg` | Full brand overview |
| `lockup-alt.jpg` | Alternate lockup |

### Mark concept
- Circular **table** from above (wireframe ring)
- Three seat/bag points on the ring
- Optional single neon seat (you / the action)
- Matches product master table visual language

### Clear space
- Minimum clear space = height of the letter "T" on all sides
- Do not stretch, add outlines, gradients, or glow

### On dark (default)
- Wordmark: white + muted `.family` + neon period
- Mark: white lines, neon accent optional

### On light (rare)
- Invert: warm black / dark gray mark on cream only if needed; product UI stays dark

---

## Master table

`design/master/master-table.jpg`

Source of truth for the product table:
- Warm black field
- White wireframe circular platform
- Three technical bags with **empty white logo plates** (programmatic token logos)
- Same language as UI screens

Bag base remains: `design/bags/bag-base-empty-logo-plate.jpg`

---

## Color (same as TOKENS.md)

| Role | Hex |
|------|-----|
| bg | `#110E08` |
| elevated | `#1C180D` |
| text | `#FFFFFF` |
| muted | `#8A8783` |
| **neon** (CTA + brand period) | `#CCFF00` |

Neon is for: primary buttons, brand period, rare winner ring. Not for large fills.

---

## Voice
- Sparse, precise, mature (Robinhood 2024 energy)
- Product language: pawn, bag, table, lock, claim, verify
- Not casino, not hype-bro, not encyclopedia

---

## Coding agents
1. Brand = **Table.family** everywhere (headers, titles, metadata)
2. Tokens = `TOKENS.md`
3. Master table + bag assets = visual components
4. Screens = `design/screens/` (rebrand headers to Table.family)
