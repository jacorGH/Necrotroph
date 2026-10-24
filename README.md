# Necrotroph

**Every death feeds something.**

Necrotroph is a mobile-first real-time strategy game where four alien lifeforms fight over a world that runs on corpses. Every unit that falls leaves a body behind, and what each race can do with the dead decides who grows strongest. It runs in the browser as a single HTML file, with peer-to-peer online play for up to four players.

▶ **Play:** `https://<your-username>.github.io/<repo-name>/`

---

## The corpse economy

There are two resources:

- **Matter** comes from pink blooms on the map and from scavenging the dead.
- **Essence** comes *only* from corpses. It pays for elite units and every upgrade, so the side that feeds best evolves first.

A corpse is worth half the cost of the unit that died, multiplied by how well your race digests that kind of body. Bodies rot away after 75 seconds, and Carrion Mites wander in to steal them if nobody claims them first.

## The lifeforms

| Race | Nature | Feeds by | Ability |
|---|---|---|---|
| **NecrosisPhagi** | An undead plague. Combat units take less damage, and Shamblers often get back up. | Raising organic and hybrid corpses as Husks, including your enemies' fallen | Mass Raise |
| **Kytinos** | Giant insects. Fast hatching, fast legs, regenerating, and bog doesn't slow them. | Devouring flesh to heal, and turning it into rich biomass | Frenzy |
| **Mechonized** | Inorganic minds with shields and long range. | Salvaging wrecks for huge yields, and burning flesh before it can rise | Overcharge |
| **Huminodiz** | Part flesh, part machine. Adaptable generalists. | Digesting every corpse type reasonably well | Stim Graft |

Each race has a worker, three combat units, an outpost, a core with its own aura, and six upgrades: three shared and three of its own.

## Features

- **Fog of war with line of sight.** Rock and thickets block vision. Teammates share sight.
- **Terrain that matters.** Rock blocks movement, chasms block movement but not shots, bog slows, and thickets hide ambushes. Ground where many die rots into bog as the match goes on.
- **Outposts and build points.** Expand to far blooms for drop-off points, vision and a smaller copy of your core's aura. Every finished outpost is also a second place to train units, with its own queue and rally point.
- **Faster builds.** *Quicken* at the core makes every building train 25% faster, up to two levels. Workers can help raise an outpost (each helper adds 60% speed, up to four) or repair a damaged building for free.
- **Workers to warriors.** *Muster* permanently transforms selected workers into your tier 1 unit for the price difference. *Call to arms* turns every worker near your buildings into militia for 25 seconds.
- **The wild.** Feral lairs guard rich blooms and keep spawning Gorgers. Carrion Mites compete for the dead.
- **An AI that plays fair.** It sees only through its own fog, scouts to find you, expands, evolves, counters what it has seen, masses before attacking and retreats when a push fails. Easy, Normal and Hard.
- **1v1, 2v2 and free-for-all**, against the AI or online, with up to four players.
- **Tutorials**, one per race, teaching the corpse cycle step by step.
- **Map designer.** Paint terrain, place blooms, bases and lairs, with rotate, mirror and four-way symmetry. Undo, validation, and export and import. Test-play your map instantly.
- **Race builder.** Design your own lifeform (see below).
- **Adaptive music.** A soundtrack generated live, with its own scale, tempo and instruments for each race and the menu. It builds from calm pads to bass, drums and racing arpeggios as fighting heats up on screen. Music and sound effects can be toggled separately.
- **Resume.** Reload or get interrupted mid-match and pick up where you left off.

## Race builder

Create a lifeform with its own name, background story, colors and four units.

- **Ecology:** what your dead leave behind, how well you digest each corpse type (within a fixed budget), plus one passive, one core aura and one ability.
- **Units:** a worker and three troop tiers, each with health, armor, damage, attack speed, range, speed and up to two traits: Splash, Medic, Shield, Regrowth, Undying, Necromancy, Burst or Leech.
- **Art:** each unit is built from parts (body, limbs, weapon, eyes), with a live animated preview.

**No overpowered builds.** You never set a price. Every unit is costed from its stats and traits, so stronger troops simply cost more Matter, and each tier has a ceiling. A few extreme combinations are blocked outright, such as very long range on a fast or tanky unit. In online play the host re-checks every guest's race, so editing the exported file won't get past the limits.

**Test balance** runs eight hidden AI matches against the built-in races and reports a win rate.

Races export and import as text, so you can share them.

## Online play

Online matches are **peer to peer** over WebRTC, using [PeerJS](https://peerjs.com/) only to find each other.

1. The host opens a room and gets a 4-letter code, or shares an invite link.
2. Up to three friends join. Empty seats can be filled with AI, and the host sets teams.
3. Once everyone is directly connected, all devices **disconnect from the PeerJS server**. The match runs entirely between players, with no polling and no server timeouts.

**Built to survive bad connections:**

- Brief network blips heal on their own while the match pauses.
- A dropped player reconnects automatically.
- A player who reloads the page resumes their seat, and so does the host.
- If someone is gone for good, the host can let the AI take over their side.

The host runs the simulation. Each guest only receives what their team can see, so fog of war can't be cheated.

## Controls

**Touch**

| Action | Gesture |
|---|---|
| Pan | Drag |
| Zoom | Pinch |
| Select a unit | Tap |
| Select all of one type on screen | Double-tap |
| Box select | Hold, then drag |
| Move, attack, harvest or scavenge | Tap the ground, an enemy, a bloom or a corpse |
| Save a control group | Hold a group button (1–3) |
| Recall a control group | Tap a group button; double-tap to jump the camera there |
| Train, evolve, set a rally point | Tap your core or an outpost |
| Help build or repair | Select workers, then tap your building |

**Keyboard and mouse**

| Key | Action |
|---|---|
| Right-click | Issue an order |
| Shift + drag | Box select |
| Mouse wheel | Zoom |
| `A` | Attack-move |
| `S` | Stop |
| `Q` | Select army |
| `W` | Select workers |
| `E` | Use race ability |
| `B` | Build outpost |
| `Space` | Jump to core |
| `Esc` | Clear selection |
| `1`–`3` | Recall group |
| `Ctrl` + `1`–`3` | Save group |
| `Ctrl` + `Z` | Undo (map designer) |

## How it's built

The whole game is one file.

```
index.html   the game
icon.png     app icon, favicon and title-screen logo
```

Open the game link on your phone and use **Add to Home Screen** for a full-screen app.

There's no build step. PeerJS and the Oxanium font load from CDNs. Skirmish, tutorials and the designers work offline once loaded. Online play needs a connection to reach the PeerJS server at the start.

Saved maps, races, settings and in-progress matches are stored in the browser's local storage on each device.

## Tech notes

- Plain HTML, CSS and JavaScript drawn on Canvas 2D.
- Fixed 20 Hz simulation running separately from rendering, so a host whose tab loses focus keeps the match alive.
- Pathfinding uses cached flow fields with line-of-sight smoothing.
- Fog of war is computed per team on a tile grid with sight-blocking terrain.
- All music and sound is synthesized with WebAudio. There are no audio files.

## Credits

- Networking: [PeerJS](https://github.com/peers/peerjs) (MIT License)
- Font: [Oxanium](https://fonts.google.com/specimen/Oxanium) via Google Fonts (SIL Open Font License)

## License

© 2026 Jacor. All rights reserved.

You're welcome to play Necrotroph. You may not copy, modify, redistribute or reuse its code, art, designs, names or text without written permission. See [LICENSE](LICENSE) for details.
