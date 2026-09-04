# PONS

**Social provably-fair meme-coin table on Robinhood Chain.**

Design system locked. Tokens first. Ready for coding agents.

## Repo layout

```
├── README.md
├── TOKENS.md                 ← START HERE — colors, space, type, CSS, Tailwind, components
├── DESIGN.md                 ← product jobs, states, screen map, rules
├── GROK-BUILD-PROMPT.md      ← paste into Grok Build / Cursor
└── design/
    ├── bags/                 ← bag base (white circle = logo mask)
    ├── screens/              ← 11 desktop screens
    └── mobile/
```

## Quick start for coding agents

1. Open **`TOKENS.md`** and wire colors/spacing/type (CSS vars or Tailwind/TS)
2. Paste **`GROK-BUILD-PROMPT.md`** into the agent
3. Build Button + Bag from tokens
4. Match **`design/screens/`**

## Token snapshot

| Token | Value |
|-------|--------|
| bg | `#110E08` |
| elevated | `#1C180D` |
| text | `#FFFFFF` |
| muted | `#8A8783` |
| **neon (CTA only)** | `#CCFF00` |
| error | `#FF4D4D` |
| warning | `#F5A623` |

Full scale, components, and state→CTA map → **TOKENS.md**

## Product

A pawn is a bag. The table is a pile of bags. The winner takes the actual meme-coin bags. Fairness is commit-reveal.

## Status

Design + tokens complete. Images on `main`. Ready to build.
