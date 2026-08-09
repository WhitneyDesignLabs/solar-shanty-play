# Known issues

Solar Shanty is in open beta — this is the honest list of rough edges as
of the current build (check your in-game version at Esc → Credits).
Found something not listed here? [Report it](https://github.com/WhitneyDesignLabs/solar-shanty-play/issues/new/choose) — attach the file F8 downloads and it's basically a repro.

- **The Flowage (v0.1.44+, beyond the aqueduct) is brand new** — the
  whole country past the opened arch (the basin, the Spillway, Survey
  Base Camp, Kettle Cove) is dev-tested but nobody has played it yet.
  Two honest edges: the **drowned snags are visual dressing, not
  colliders** (the hull passes through a trunk if you aim at one — same
  rule as crab-pot buoys and pilings; the navigable channels are kept
  clear of them by construction), and the water surface near the new
  shores slopes with the datum falloff, same as the Millpond's own
  shores always have.
- **The night sky is brand new (v0.1.53+)** and it is real astronomy, not
  decoration: the Big Dipper, Cassiopeia, Polaris and Orion sit at their
  true coordinates, the sphere turns with sidereal time, and the moon's
  position now follows its phase (a new moon is up in the daytime, so
  midnight can be genuinely dark). Two honest caveats. The **sun is still
  not seasonal** — sunrise and sunset are fixed, so the stars know what
  month it is and the sun doesn't; if you sail six game-months you'll get
  Orion overhead on a 14-hour summer's day. And the sky is anchored to a
  declared latitude (44°N) chosen for the region the game describes,
  because the existing stylized sun doesn't correspond to any real one.
- **Bioluminescence is rare on purpose.** It needs a flat, warm, clear
  night and then still only sometimes happens. If you've never seen it,
  that's the feature working; anchor out on a calm summer night and be
  patient.
- **The boat under the tarp at the Boatyard can't be sailed yet (v0.1.51+).**
  She's a real, measured hull — the 33′ tritoon this whole project is
  the design review for — and the Yard Office posts a genuine restoration
  quote. But the yard won't take the job, and that's deliberate rather
  than a bug: she needs her own deck, cabin and walk paths built at her
  true dimensions before anyone can honestly charge for her. Pull the
  tarp, read the posting, take the letter. Coming.
- **Boat/dock visuals can overlap at odd docking attitudes.** Physics and
  scoring are correct (you won't clip through anything, fees are fair);
  the hull mesh can visually poke into the dock at unusual angles before
  the tie-up snug settles it.
- **Traffic doesn't dodge you.** Kinematic NPC vessels hold their own
  course and speed regardless of what you do — v1 puts the avoiding on
  you, same as real right-of-way rules assume the other guy is paying
  attention.
- **Xbox controller support is brand new** (the same Helm Control
  Contract that will later drive Scott's real boat). Deadzone, steering
  expo, throttle-lever rate/detent, and the docking-toggle hold time are
  all first-pass honest guesses, tunable in Settings → Gamepad — same
  "nobody's played it yet, that's what beta feedback is for" caveat as
  everything else below. Switching input devices mid-voyage (e.g. a
  gamepad connected while you're mid-throttle on the keyboard) can very
  occasionally leave the throttle-lever setting starting from a stale
  value the first time the pad takes over, rather than picking up
  smoothly from the boat's current speed — a known rough edge, not a bug
  report we need duplicated.
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
  settlement reached on foot, not by docking. HAIL LOCK on the VHF at the
  helm requests passage when you're close enough; the gate leaves swing and
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
  **(Checked TC-032; RE-CHECKED TC-053 after the render-truth/harness
  era: giving the Fairhope pier a real tie-up-able body still isn't a
  cheap reuse — gridded-region POIs carry no `docks` data, the tie-up/
  dock-collision path only ever scans Kingfisher's hardcoded `worldData`
  registry, and gridded terrain still has no walkable-collider system
  for a deck to sit on. Nothing in TC-044/050's instrumentation changed
  any of that — it made rendering honest, not structures solid. Real
  docking at Mobile's landmarks is future-round work, not a bolt-on.)**
  As of v0.1.48 the real regions DO have their first interactable
  things: salvage wrecks (one in the Keys, two in Mobile Bay) — beach
  nearby, walk up, and work the hull. The hull VISUALS are dressing
  (you can walk through them, like every gridded landmark); the chest
  is real.
- **Florida Keys / Marathon (Customize voyage → Region) is the second
  real-chart region, same experimental terms as Mobile Bay above.** The
  Seven Mile Bridge (modern span + the old bridge alongside it), Sombrero
  Key Light, Pigeon Key, and Boot Key Harbor's mooring field are visual +
  discoverable, not walkable ashore yet. **FIXED in v0.1.50: Pigeon Key
  is dry land now.** The old entry here ("compiled terrain reads as
  shallow water, not the small dry island it really is") is paid: the
  compiler learned a hand-scoped land-priority rule (the exact "defer to
  land data for small islands like this one" future-round this entry
  predicted — see region.toml's [[land_priority]] and compile_region.py),
  the pack was recompiled, and the island now carries a beached
  bridge-works barge you can salvage. Listed briefly so nobody hunts a
  bug that no longer exists. Real channel markers (Boot Key Harbor
  entrance) are hand-placed from the compiled bathymetry, same honest
  caveat as Mobile Bay's.
- **The Bayou (two new creeks off the Run's south bank), fog weather,
  and the hermit's shack are brand new.** Same "nobody but the devs has
  played it" caveat as the coves and the Lock above: creek siting,
  canopy density, fog's visibility collapse, and the shack's pricing/
  siting are all first-pass. Fog is a real Markov weather state now
  (rare on Easy, a real presence on Hard) — expect it to show up
  unannounced on a calm morning.

None of these affect saves, cause crashes, or lose progress. If one
does, that's a bug in its own right — please report it.
