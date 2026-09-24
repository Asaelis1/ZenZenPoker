# Zen Poker — Landscape GDD addendum
Updated 23 September 2026

## Device
Primary surface is a phone on its side (landscape). Portrait shows a turn-the-garden prompt. Safe areas are respected. HUD ~42px, tray/wells ~78px, board takes the rest.

## Screens
1. Opening flash — five garden faces flip, then centered **Zen** / **Poker**. Tap enters the road.
2. Garden Road — ten chapters, ten beds each. Difficulty tag on the bed card.
3. Table — overlapping deal, tray of five, wells.
4. Clear — stars, pay log, next bed.
5. Settings — tranquil pad, FX, haptics, silent, paytable, review jump.

## Difficulty tags
- Gentle: levels 1–30 except decade bosses
- HARD: levels 31–80 and every 10th bed
- EXTREME HARD: levels 81–100 and decade bosses from 60

## Cards
Garden black-suit pack, 1024×1536 (2:3). In play the box stays 2:3 and scales down on crowded beds. Levels 97–100 use two packs (55–60 cards). Joker art is `cards/JOKER.png` (gardener). A wild table card shows that face.

## New board wells
- Hint — lights one free card
- Peek — briefly turns one buried card
- Joker / Undo / Shuffle unchanged in rules

## Motion
- Deal-in on every bed start
- Soft lift on a free card
- Hands **above Three of a Kind** (Straight, Flush, Full House, Four, Five, Straight Flush, Royal) play a 1.8s gold bloom: large hand name + `base × combo = total`, a four-note chime, and a triple haptic. Auto-deal of the last five waits until the bloom ends. Pair / Two Pair / Three of a Kind stay on the small toast only.

## Feel
- Tranquil fifth-pad (196 + 247 Hz) as music
- Short sine chimes for pick / pair / bloom
- `navigator.vibrate` on pick, plant, and bloom
- All three can be silenced in Settings

## Review jump
Settings → Review jump, or tap the wordmark seven times. Unlock 1–100, then jump to a bed number.

## Paytable
Button on the table HUD (₱) and inside Settings. Same values: High 25 … Royal 2000.
