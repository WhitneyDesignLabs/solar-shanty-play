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
- **One save slot.** New Voyage overwrites your current save; there's no
  slot picker yet. Export/import (Settings) is the only way to keep more
  than one voyage around.
- **Keyboard and mouse only.** No gamepad support yet.
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

None of these affect saves, cause crashes, or lose progress. If one
does, that's a bug in its own right — please report it.
