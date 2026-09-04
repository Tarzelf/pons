# PONS Design Tokens

**Source of truth for coding agents.**  
Do not invent colors, radii, shadows, or type scales. Use these tokens only.

---

## 1. Color tokens

| Token | Hex | CSS var | Usage |
|-------|-----|---------|--------|
| `bg` | `#110E08` | `--pons-bg` | App canvas |
| `bg-elevated` | `#1C180D` | `--pons-bg-elevated` | Cards, modals, list rows |
| `bg-hover` | `#24201A` | `--pons-bg-hover` | Hover surface |
| `border` | `#2A2620` | `--pons-border` | Hairline borders |
| `border-strong` | `#3D3830` | `--pons-border-strong` | Selected / focus ring (non-CTA) |
| `text` | `#FFFFFF` | `--pons-text` | Primary text |
| `text-muted` | `#8A8783` | `--pons-text-muted` | Secondary, wallets, captions |
| `text-subtle` | `#B4B1AB` | `--pons-text-subtle` | Tertiary labels |
| `text-inverse` | `#110E08` | `--pons-text-inverse` | Text on Neon buttons |
| `neon` | `#CCFF00` | `--pons-neon` | **Primary CTA only** |
| `neon-hover` | `#D4FF33` | `--pons-neon-hover` | CTA hover |
| `neon-pressed` | `#B8E600` | `--pons-neon-pressed` | CTA pressed |
| `error` | `#FF4D4D` | `--pons-error` | Fail / partial X only |
| `warning` | `#F5A623` | `--pons-warning` | Thin-pool warning only |
| `success` | `#CCFF00` | `--pons-success` | Checks (or pure white ✓) |

### Rules
- Canvas is always `bg`. Never pure `#000000`.
- `neon` is **only** for primary action buttons (and winner highlight ring if needed).
- Never use blue, purple, cyan glow, gradients, or glass.
- Muted wallets / secondary labels = `text-muted`.

---

## 2. CSS variables (paste into `:root`)

```css
:root {
  /* color */
  --pons-bg: #110E08;
  --pons-bg-elevated: #1C180D;
  --pons-bg-hover: #24201A;
  --pons-border: #2A2620;
  --pons-border-strong: #3D3830;
  --pons-text: #FFFFFF;
  --pons-text-muted: #8A8783;
  --pons-text-subtle: #B4B1AB;
  --pons-text-inverse: #110E08;
  --pons-neon: #CCFF00;
  --pons-neon-hover: #D4FF33;
  --pons-neon-pressed: #B8E600;
  --pons-error: #FF4D4D;
  --pons-warning: #F5A623;
  --pons-success: #CCFF00;

  /* space (8px grid) */
  --pons-space-1: 4px;
  --pons-space-2: 8px;
  --pons-space-3: 12px;
  --pons-space-4: 16px;
  --pons-space-5: 24px;
  --pons-space-6: 32px;
  --pons-space-7: 48px;
  --pons-space-8: 64px;
  --pons-space-9: 96px;

  /* radius */
  --pons-radius-sm: 6px;
  --pons-radius-md: 10px;
  --pons-radius-lg: 14px;
  --pons-radius-xl: 20px;
  --pons-radius-full: 9999px;

  /* type */
  --pons-font: ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  --pons-text-xs: 12px;
  --pons-text-sm: 13px;
  --pons-text-md: 15px;
  --pons-text-lg: 18px;
  --pons-text-xl: 24px;
  --pons-text-2xl: 32px;
  --pons-leading: 1.35;
  --pons-tracking-tight: -0.02em;

  /* motion */
  --pons-ease: cubic-bezier(0.2, 0.8, 0.2, 1);
  --pons-duration: 160ms;

  /* shadow — almost none */
  --pons-shadow: none;
  --pons-shadow-modal: 0 8px 32px rgba(0, 0, 0, 0.45);
}
```

---

## 3. Tailwind theme extend (optional)

```js
// tailwind.config.js — theme.extend
colors: {
  pons: {
    bg: "#110E08",
    elevated: "#1C180D",
    hover: "#24201A",
    border: "#2A2620",
    "border-strong": "#3D3830",
    text: "#FFFFFF",
    muted: "#8A8783",
    subtle: "#B4B1AB",
    inverse: "#110E08",
    neon: "#CCFF00",
    "neon-hover": "#D4FF33",
    "neon-pressed": "#B8E600",
    error: "#FF4D4D",
    warning: "#F5A623",
  },
},
borderRadius: {
  pons: "10px",
  "pons-lg": "14px",
  "pons-xl": "20px",
},
fontFamily: {
  pons: ['ui-sans-serif', 'system-ui', 'sans-serif'],
},
```

---

## 4. Spacing scale

| Token | px | Use |
|-------|-----|-----|
| 1 | 4 | tight icon gaps |
| 2 | 8 | inline gaps, chip padding y |
| 3 | 12 | label stacks |
| 4 | 16 | card padding, list row gap |
| 5 | 24 | section gaps |
| 6 | 32 | screen padding (mobile) |
| 7 | 48 | screen padding (desktop), between major blocks |
| 8 | 64 | hero empty space |
| 9 | 96 | table margin |

**Layout rule:** generous empty space. Prefer larger gaps over dense packing.

---

## 5. Typography

| Role | Size | Weight | Color | Notes |
|------|------|--------|-------|-------|
| Screen title | 15–18px | 500–600 | `text` | e.g. `PONS · FILLING` |
| State headline | 24–32px | 500 | `text` | e.g. `you won the bag` |
| Body | 15px | 400 | `text` | |
| Label | 13px | 400 | `text-muted` | tickers, % |
| Meta | 12px | 400 | `text-muted` | wallets `0x7f3a…b2c1` |
| Button | 15px | 600 | `text-inverse` on neon | |

- One type family only (system geometric sans).
- No display serifs, no mono walls (verify uses short labels only).
- Real sample data only: tickers, `$12.2k`, `21.4M PEPE`, timers, hashes truncated.

---

## 6. Component primitives

### Button — primary (only one per screen)
```
bg: neon
text: text-inverse
radius: radius-md (10px) or radius-lg
height: 48px desktop / 44px mobile
padding-x: 24px
hover: neon-hover
pressed: neon-pressed
disabled: opacity 0.4, no pointer
```
Labels by state: `Put a coin on` · `Pawn` · `Pawn · freeze 8%` · `Claim` · `Copy proof` · `Done` · `Retry WOJAK` · `Leave` · `Join`

### Button — secondary / ghost
```
bg: transparent
border: 1px border
text: text
radius: radius-md
height: 48px
```
Examples: `Verify` · `Stay` · `Done` (when not primary)

### Button — locked / disabled primary look
```
bg: transparent
border: 1px border-strong
text: text-muted
icon: lock line
label: Locked
```

### Bag
- Asset: `design/bags/bag-base-empty-logo-plate.jpg`
- White circle = logo mask → composite token logo PNG
- Scale bag by weight % (visual size ∝ weight)
- Label stack beside bag: `TICKER` / `%` / `amount` / `$value`
- Optional thin ring for selected (white) or winner (neon 1–2px)

### PFP + wallet
```
PFP: 24–32px circle
Wallet: 12px text-muted, format 0x + 4 … + 4  (e.g. 0x7f3a…b2c1)
Gap: 8px between pfp and wallet
Never full address. Never dense avatar walls.
```

### Table (round)
- Thin white circle stroke, low opacity (~0.2)
- Bags arranged inside; empty state = faint bag outlines only
- One primary CTA below center

### List row (table list)
```
height: ~64–72px
bg: bg-elevated or transparent
border-bottom: 1px border
left: bag thumbs + PFP stack
middle: id · $ · pawns · timer
right: neon Join
```

### Modal (bail)
```
bg: bg-elevated
radius: radius-xl
padding: 32px
shadow: shadow-modal
max-width: 400px
```

### Input (amount)
```
bg: bg-elevated
border: 1px border
radius: radius-md
height: 48px
text: text
placeholder: text-muted
```

### Warning chip
```
text: warning
size: 12–13px
e.g. thin pool · mark can move until you pawn
```

---

## 7. State → primary action map

| State | Primary CTA | Notes |
|-------|-------------|--------|
| empty | Put a coin on | neon |
| filling | Pawn | neon |
| pawn | Pawn · freeze N% | neon |
| locked | Locked | disabled outline, can't bail |
| in-progress | (none / wait) | theater only |
| claim | Claim | neon; secondary Verify |
| verify | Copy proof | neon |
| partial | Retry TICKER | neon; secondary Done |
| success | Done | neon |
| bail | Leave | neon; secondary Stay |
| table-list | Join | neon per row |

**One primary action per view.** Never two neon buttons competing.

---

## 8. Do not invent

- No new brand colors
- No glass / blur / glow / gradient fills
- No purple, cyan, electric blue
- No 3D blobs, coin rain, roulette chrome
- No mono hex-dump walls
- No extra typefaces
- No dense leaderboards

If a mock looks like Dribbble casino UI, rewrite to these tokens.

---

## 9. Minimal React token object

```ts
export const pons = {
  color: {
    bg: "#110E08",
    bgElevated: "#1C180D",
    bgHover: "#24201A",
    border: "#2A2620",
    borderStrong: "#3D3830",
    text: "#FFFFFF",
    textMuted: "#8A8783",
    textSubtle: "#B4B1AB",
    textInverse: "#110E08",
    neon: "#CCFF00",
    neonHover: "#D4FF33",
    neonPressed: "#B8E600",
    error: "#FF4D4D",
    warning: "#F5A623",
  },
  space: [0, 4, 8, 12, 16, 24, 32, 48, 64, 96],
  radius: { sm: 6, md: 10, lg: 14, xl: 20, full: 9999 },
  font: 'ui-sans-serif, system-ui, sans-serif',
  text: { xs: 12, sm: 13, md: 15, lg: 18, xl: 24, "2xl": 32 },
} as const;
```

---

**Start every implementation by wiring these tokens first**, then Bag component, then Empty → Filling → Locked.
