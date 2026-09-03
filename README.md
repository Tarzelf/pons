# PONS

**Social provably-fair meme-coin table on Robinhood Chain.**

Design system locked. Ready for coding agents (Grok Build, Cursor, etc.).

## Repo layout

```
├── README.md
├── DESIGN.md                 ← tokens, jobs, states, social rules, killed list
├── GROK-BUILD-PROMPT.md      ← paste this into your coding agent to start
└── design/
    ├── bags/                 ← programmatic bag (white circle = logo mask)
    ├── screens/              ← 11 desktop UI screens (source of truth)
    └── mobile/               ← key mobile screens
```

## Quick start for coding agents

1. Read `DESIGN.md`
2. Paste the full contents of `GROK-BUILD-PROMPT.md` into Grok Build / Cursor
3. Use `design/screens/` as the visual source of truth
4. Use `design/bags/bag-base-empty-logo-plate.jpg` for the bag component

## Visual lock (summary)

- Warm black canvas `#110E08` / `#1C180D`
- Robin Neon CTA only `#CCFF00`
- Technical geometric bags + flat white logo plate
- Sparse PFPs + truncated wallets (`0x7f3a…b2c1`)
- One screen = one job. State only changes the table + one button.
- No glass, glow, casino chrome, Dribbble polish

## Product in one sentence

A pawn is a bag. The table is a pile of bags. The winner takes the pile of actual meme-coin bags. Fairness is commit-reveal.

## Status

Design handoff complete. Visual system locked. Ready to build.
