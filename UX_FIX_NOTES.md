# UX fix notes (2026-09-24)

Single-file rewrite of `index.html` against `ZEN_POKER_LANDSCAPE_GDD.md`.

## Blockers
- **No-scroll shell:** `html,body,#app { height:100%/100dvh; overflow:hidden }`. Stage is a column flex: HUD (~42–44px) | flex-1 content | footer tray+wells (~78px). Board area alone scrolls/clips with `overflow:hidden`.
- **Garden Road short landscape:** Path + detail panel stay side-by-side (`grid 1.2fr .9fr`) with compact 40–48px nodes so Play stays in view at ~844×390.
- **Table HUD:** Fixed-height header; back / ₱ paytable / gear; score pills; never scrolls away.

## High
- **Settings sheet** (gear): Tranquil pad, FX, Haptics, Silent, Paytable open, Review jump (unlock 1–100 + bed number). Separate ₱ on table HUD and Paytable on road panel.
- **Hint / Peek wells** added beside Undo / Joker / Shuffle (counts Hint 2, Peek 2 per bed).
- **Splash:** five garden faces deal-in, then **Zen** / **Poker**; tap → road. `?skipSplash=1` skips.
- **Portrait gate:** full-screen “Turn the garden” when portrait / height>width.
- **Gold bloom (~1.8s)** for Straight+ hands; auto-deal waits; Pair/Two Pair/Three stay toast-only.

## Medium
- **100 beds / 10 chapters**, seeded procedural layouts; difficulty Gentle / HARD / EXTREME HARD per GDD.
- Chrome targets: HUD ~42px, footer ~78px, wells ≥44px (prefer ~58–72), cards 2:3.
- Status line: 13px, high-contrast, overlaid at bottom of board.
- “GARDEN ROAD” is a non-interactive label (`.road-label`), not a button; selected node keeps glow.

## Other
- Save key bumped to `zen-poker-web-review-v3` (settings + review + 100 beds).
- Soft Web Audio pad/chimes + `navigator.vibrate`; respect Silent/FX/Haptics/music toggles.
- Wild table cards use `cards/JOKER.png`. Paytable High 25 … Royal 2000 unchanged.
