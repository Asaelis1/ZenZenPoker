# ZenZenPoker

Botanical landscape solitaire. Garden deck, 100 beds, landscape phone first.

## Run locally

```bash
# Keep cards/ next to index.html
python3 -m http.server 8765
```

Open `http://localhost:8765` (landscape). Append `?skipSplash=1` to skip the opening flash while testing.

## Layout

- `index.html` — splash, road, table, settings, clear, portrait gate
- `cards/` — 52 faces + Joker + back (2:3 PNGs)
- `ZEN_POKER_LANDSCAPE_GDD.md` — landscape addendum
- `UX_FIX_NOTES.md` — latest UX pass notes

## Review jump

Settings → Review jump, or tap the wordmark seven times. Unlock 1–100, type a bed number.

## Notes

Web preview only (not store APK). Host on https to install as a PWA later.
