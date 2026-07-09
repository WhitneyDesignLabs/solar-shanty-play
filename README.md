# Solar Shanty — play in browser

A public landing page + mirror of `SolarShanty.html`, the current
single-file build of **Solar Shanty**, a first-person solar houseboat
life simulator. Source lives in a private repo; this one exists only to
present and serve that one file publicly via GitHub Pages — not tied to
any Anthropic/Claude account, plan, or subscription.

**Play:** https://whitneydesignlabs.github.io/solar-shanty-play/

- `index.html` is the landing page — intro, "your first hour" quick
  start, and the full keybinding reference — with a "Play in browser"
  button linking to `SolarShanty.html`.
- `SolarShanty.html` is the real playable build and keeps its canonical
  name so it can be diffed/synced directly against the private repo's
  copy.

**Keeping `SolarShanty.html` in sync:** whenever the private repo's copy
is refreshed, copy it here verbatim (same filename) and push — no other
changes needed. The embedded version stamp (Esc → Credits, in-game) is
the fastest way to check whether this mirror is behind.

**Keeping `index.html` in sync:** its content (intro copy, controls list,
first-hour summary) should track the private repo's `README.md` — update
by hand if that copy changes materially.

No install, no account — runs entirely in your browser. Progress autosaves
locally each game hour.
