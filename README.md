# Solar Shanty — play in browser

A public landing page + mirror of `SolarShanty.html`, the current
single-file build of **Solar Shanty**, a first-person solar houseboat
life simulator. Source lives in a private repo; this one exists only to
present and serve that one file publicly via GitHub Pages — not tied to
any Anthropic/Claude account, plan, or subscription.

**Play:** https://whitneydesignlabs.github.io/solar-shanty-play/

- `index.html` **is** the playable build itself — the root URL loads
  straight into the game, no separate landing/intro page. (This
  replaced an earlier two-tier design where `index.html` was a small
  landing page linking out to `SolarShanty.html`; that landing page
  stopped being maintained a while back and this README kept
  describing it long after it was gone — corrected as of TC-049.)
- `SolarShanty.html` is a permanent, content-free redirect to
  `index.html` — kept only so old bookmarks/links to that URL still
  land somewhere. It is never rebuilt and carries no version of its
  own; there is exactly one shipped playable in this repo (`index.html`).
- `KNOWN_ISSUES.md` is copied verbatim from the private repo (source of
  truth lives there) and linked from the game's own credits/menu.
- `.github/ISSUE_TEMPLATE/bug_report.md` powers the "Found a bug?" link
  (`/issues/new/choose`) — F8 in-game downloads the report to attach.

**Keeping `index.html` and `KNOWN_ISSUES.md` in sync:** whenever the
private repo's playable is refreshed, `tools/publish.sh` there copies the
freshly built single-file bundle to this repo's `index.html` (never
`SolarShanty.html` — see above) and `KNOWN_ISSUES.md` verbatim, then
pushes. The embedded version stamp (Esc → Credits, in-game) is the
fastest way to check whether this mirror is behind.

No install, no account — runs entirely in your browser. Progress autosaves
locally each game hour.
