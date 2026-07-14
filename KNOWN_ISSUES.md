# Known issues

Solar Shanty is in open beta — this is the honest list of rough edges as
of the current build (check your in-game version at Esc → Credits).
Found something not listed here? [Report it](https://github.com/WhitneyDesignLabs/solar-shanty-play/issues/new/choose) — attach the file F8 downloads and it's basically a repro.

- **Boat/dock visuals can overlap at odd docking attitudes.** Physics and
  scoring are correct (you won't clip through anything, fees are fair);
  the hull mesh can visually poke into the dock at unusual angles before
  the tie-up snug settles it.
- **Traffic doesn't dodge you.** Kinematic NPC vessels hold their own
  course and speed regardless of what you do — v1 puts the avoiding on
  you, same as real right-of-way rules assume the other guy is paying
  attention.
- **Keyboard and mouse only.** No gamepad support yet.
- **Fixed in v0.1.12:** the "one save slot" limitation is gone — four
  named slots with a picker (Customize voyage) and a most-recent
  Continue; your older single save appears as slot 1 automatically.
  Listed here briefly so nobody hunts a limitation that no longer exists.
- **Tow-feel constants are first-pass, not tuned from playtesting**: the
  dinghy's astern distance/spring smoothness and the optional towing
  drag penalty are reasonable guesses, not measured. If towing something
  feels off, that's why — flag it and we'll adjust the numbers.
- **The three newest coves (Widow's Bluff, Sable Bend, Driftwood Reach)
  and the fat-tire e-scooter are new enough that nobody but the devs has
  played them.** Geography, scooter handling, and cove-evening pacing are
  all first-pass — this is exactly the kind of thing beta feedback is for.
- **Old Betsy's deck is a flat approximation.** The real derelict barge
  has a slight list that isn't reflected in the walkable deck surface —
  cosmetic only, well inside normal step-up tolerance.
- **Upriver — the Lock and the Millpond are brand new** (Kingfisher's
  first map expansion): a working lock past the lake gates onto a small
  elevated pond, with Locktender's Landing above it — the game's first
  settlement reached on foot, not by docking. HAIL LOCK at the helm
  requests passage when you're close enough; the gate leaves swing and
  the chamber rises or falls, no puzzle to it. Same "new enough that
  nobody but the devs has played it" caveat as the coves above — the
  lock's timing and the hamlet's siting are first-pass.
- **Mobile Bay (Customize voyage → Region) is experimental — real NOAA
  chart data, sparse services, on purpose.** The bathymetry is real
  survey data; everything else is deliberately minimal for this first
  pass: no quests, no gigs, no dockable marinas. Real landmarks (Middle
  Bay Light, Fort Morgan, Fort Gaines, USS Alabama, Fairhope Municipal
  Pier, Gaillard Island) are visual + discoverable by sailing near them,
  not walkable ashore yet. Channel markers trace the compiled bathymetry's
  own deepest corridor, red-right-returning — a real-data-derived
  approximation, not an extraction of official NOAA chart aid-to-
  navigation records. SET SAIL always launches Kingfisher Reach; Mobile
  Bay is opt-in only.
  **(Checked TC-032: giving the Fairhope pier a real tie-up-able body
  isn't a cheap reuse here — gridded-region POIs carry no `docks` data,
  the tie-up/dock-collision path only ever scans Kingfisher's hardcoded
  `worldData` registry, and gridded terrain has no walkable-collider
  system at all yet for a deck to sit on. Real docking at Mobile's
  landmarks is future-round work, not a bolt-on.)**

None of these affect saves, cause crashes, or lose progress. If one
does, that's a bug in its own right — please report it.
