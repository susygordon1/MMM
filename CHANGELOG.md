# Mega Mission Media — Update Log

Drop `index.html` and `susy-story.jpg` into your repo, replacing the old
index.html. Everything else in the repo stays as-is.

---

## What changed

### Palette — teal is now primary
- `--teal` is now **#22E0E0** (hot cyan) instead of #5EEAD4
- Gold **retired**. `--gold` and `--gold-dim` are aliased to teal so nothing
  breaks — no markup had to change. Delete the aliases whenever you like.
- New: `--paper` #F5F8F8 (light ground), `--ink` #0B0F10 (type on light),
  `--teal-deep` #0E9EA0 (teal that stays readable on white)

### Sections now alternate dark and light
Hero (dark) → Roadmap (**light**) → Portfolio (dark) → Story (dark) →
Ride & Share (**light**) → Reviews (dark) → Booking (**light**) →
CTA (dark) → Contact (**light**) → Footer (dark)

This is what makes the teal pop. Black everywhere gave it nothing to pop against.

### Roadmap — short lists, phase names kept
Foundation / Growth / Authority stay. The long feature checklists are replaced
with Build the Brand / Build the House / Run the House. No pricing implied.

### Portfolio
- **Removed:** Cowtown Tour Company, MLK Pre Arrangements (Ride & Share only —
  MMM did not build those sites), FBI Network
- **Added:** 9-Line Financial → 9-lf.com

### NEW — "I Came Up In Broadcast"
Univision, CBS 11, Radio Intelligence brought forward. Photo + Philippians 1:6.

### NEW — Ride & Share video wall
All four episodes: Lena, Carrie, Yoel, Susy. Thumbnails pull live from YouTube,
so re-uploading a video updates the site automatically.

### NEW — Client reviews
Two real Google reviews, verbatim (Yoel Zehaie, 4TEC LLC).
Carrie, Lena and Tony are **commented out** in the HTML — uncomment each as
the real words arrive. Empty placeholder cards were advertising what's missing.

### NEW — Booking card + Free Assessment modal
- Every "Book a Call" → `calendar.app.google/7EeEp5VeZZvSwdrE6`
- Every "Free Assessment" → modal form, posts to the same Formspree endpoint
- Closes on X, click-outside, or Escape

### Footer
Social icons added (Facebook, Instagram, LinkedIn, YouTube), phone and email.

### Details
- Phone → **682-484-1335** everywhere (was 817-860-8989)
- GA4 → **G-TD5J4DJ1WB** (was a placeholder — it was never tracking)

---

## Still outstanding

1. **info@megamissionmedia.com** — using susy@ for now, as agreed
2. **Footer scripture** — the Matthew line, when it comes to you
3. **New MMM YouTube IDs** — six places, once you've re-uploaded
4. **YouTube Follow link** — currently the playlist, wants the channel URL
5. **Carrie / Lena / Tony reviews** — uncomment as they arrive
6. **Logo** — MMM_Logo.png is still the gold version against a teal palette

## Verify after deploy
- Open the live site on your phone, then check GA4 **Realtime** — you should
  appear as an active user
- Click Book a Call, make a test booking, confirm it lands on your calendar,
  then delete it
- Submit the Free Assessment modal once and confirm it reaches your inbox
