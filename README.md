# Necrotroph

**Every death feeds something.**

Necrotroph is a mobile-first real-time strategy game set inside **Varuun**, a dying star-leviathan drifting between galaxies. Four lifeforms, too small for Varuun to see, fight across its organs for every scrap of flesh and every corpse. Whoever holds the most of Varuun when it draws its last breath inherits the body, and in the dark, a leviathan's corpse is a seed.

Every unit that falls leaves a body behind, and what each lifeform can do with the dead decides who grows strongest. It runs in the browser as a single HTML file, with peer-to-peer online play for up to four players.

## The story

Varuun swallowed three things it should not have: a comet laced with ancient spores, the carcass of an older leviathan, and a derelict starship, the *Hesper*. Each carried something that woke up inside it. Varuun's own cells rose to fight back. Now four lifeforms war across its organs, while Varuun's hunter cells, the Wardens, attack them all.

The full story is in the game under **The story** on the main menu.

▶ **Play:** `https://<your-username>.github.io/<repo-name>/`

---

## The corpse economy

There are two resources:

- **Nutrient** comes from pink nutrient wells in Varuun's tissue and from scavenging the dead.
- **Essence** comes *only* from corpses. It pays for elite units and every mutation, so the side that feeds best evolves first.

A corpse is worth half the cost of the unit that died, multiplied by how well your lifeform digests that kind of body. Bodies rot away after 75 seconds, and Lumen Lice drift in to steal them if nobody claims them first.

## The lifeforms

| Lifeform | Nature | Feeds by | Ability |
|---|---|---|---|
| **NecrosisPhagi**, the Quiet Choir | A plague from a dead leviathan's corpse. Combat units take less damage, and Shamblers often get back up. | Raising organic and hybrid corpses as Husks, including your enemies' fallen | Mass Raise |
| **Kytinos**, the Brood | Chitin-walled parasites that ride leviathans from host to host. Fast hatching, fast legs, regenerating, and mucus doesn't slow them. | Devouring flesh to heal, and turning it into rich biomass | Frenzy |
| **Mechonized**, the Restoration | The *Hesper*'s repair swarm, rebuilding Varuun's flesh into a ship. Shields and long range. | Salvaging wrecks for huge yields, and burning flesh before it can rise | Overcharge |
| **Huminodiz**, the Grafted | Varuun's own cells fused with nanotech and the dead crew's memories. Adaptable generalists. | Digesting every corpse type reasonably well | Stim Graft |

Each lifeform has a worker, three combat units, a foothold, a core with its own aura, and six mutations: three shared and three of its own.

## Campaign: the Atlas

Each lifeform has its own story campaign across a map of Varuun's body: nine organs joined by Lumen channels.

- **Start in your home organ** (the Brood in the Baleen Reefs, the Quiet Choir in the Furnace Gut, the Restoration in the Hesper Wreck, the Grafted in the Lumen Sea) and invade neighbouring organs one battle at a time.
- **Every organ plays differently.** The Starlung is built from bone chambers, the Marrow Spires bristle with Warden Nests, the Lumen Sea is cut by blood channels, and the Hesper Wreck is a maze of metal corridors.
- **Organs you hold carry over** as rewards in later battles: extra Nutrient or Essence, extra workers, more supply, a free mutation, or a faster start.
- **Rivals spread too.** Between battles the other lifeforms claim free organs, and their strongholds fight back harder.
- **Five acts.** Infection, then Fever (Wardens surge and units burn hot), then Collapse (tissue rots and corpses decay faster), then the Last Breath, a four-way battle for Varuun's mind. Last comes the hidden Cradle, and an ending unique to each lifeform.

## Drift: the Lumen Sea

A second kind of battlefield, set on Varuun's bloodstream.

- **Bases sit on anchored islands** in the corners. Everything else drifts: three rings of islands wheel around a central heart-island at different speeds and in different directions.
- **Golden bridges** glow between islands whenever they pass within leaping distance. Units ordered across walk to the edge and leap; if no bridge is open, they hop toward the target where they can, or wait at the edge for the current to bring one.
- **Everything rides along.** Units, nutrient wells, corpses and buildings move with their island, so a foothold on a drifting cell becomes a moving base.
- **Spore rafts and wrecks** keep shedding fresh corpses, a steady supply of Essence worth fighting over.
- Anyone knocked into the sea is washed back onto the nearest island, hurt.

Pick **Drift** as the battlefield in skirmish or when hosting online. In the campaign, the Lumen Sea is always a Drift battle.

## The Deep Lumen

A dive down Varuun's vessels toward its heart, rendered in 3D perspective from just behind your colony-cell.

- **Steer** by dragging anywhere and hold **Boost** to surge. On a keyboard, use the arrow keys or WASD, and Space to boost.
- **Gather motes**: pink for Nutrient, green for Essence. They fill your stores.
- **Dodge Wardens** that home in on you, bump through tumbling blood cells, and stay off the vessel walls.
- **Dock with floating bodies** in the wider chambers: drifting cells, Hesper debris, spore rafts and Warden hives. Each one opens a battle, fought with everything in your stores. Every body you claim strengthens your later battles, and each win restores vitality.
- **Reach the Heart** and take it from two rival strains to finish the dive. Your best depth is remembered.

## Features

- **Fog of war with line of sight.** Rock and thickets block vision. Teammates share sight.
- **Varuun's flesh as terrain.** Bone blocks movement, Lumen channels (rivers of glowing blood) block movement but not shots, mucus marsh slows, and villi forests hide ambushes. Tissue where many die rots into marsh as the match goes on.
- **Footholds and build points.** Expand to far nutrient wells for drop-off points, vision and a smaller copy of your core's aura. Every finished foothold is also a second place to train units, with its own queue and rally point.
- **Faster builds.** *Quicken* at the core makes every building train 25% faster, up to two levels. Workers can help a foothold take root (each helper adds 60% speed, up to four) or repair a damaged building for free.
- **Workers to warriors.** *Muster* permanently transforms selected workers into your tier 1 unit for the price difference. *Call to arms* turns every worker near your buildings into militia for 25 seconds.
- **Varuun's defences.** Warden Nests guard rich nutrient wells and keep hatching Wardens, which attack every lifeform. Lumen Lice compete for the dead.
- **An AI that plays fair.** It sees only through its own fog, scouts to find you, expands, mutates, counters what it has seen, masses before attacking and retreats when a push fails. Easy, Normal and Hard.
- **1v1, 2v2 and free-for-all**, against the AI or online, with up to four players.
- **Tutorials**, one per lifeform, teaching the cycle of feeding step by step.
- **Maps set in Varuun's organs:** the Furnace Gut, the Baleen Reefs, the Heart Choir (four players), and Uncharted Tissue, a new random region every match.
- **Map designer.** Paint tissue, bone, channels, mucus and villi, place nutrient wells, bases and Warden Nests, with rotate, mirror and four-way symmetry. Undo, validation, and export and import. Test-play your map instantly.
- **Race builder.** Design your own lifeform (see below).
- **Adaptive music.** A soundtrack generated live, with its own scale, tempo and instruments for each race and the menu. It builds from calm pads to bass, drums and racing arpeggios as fighting heats up on screen. Music and sound effects can be toggled separately.
- **Resume.** Reload or get interrupted mid-match and pick up where you left off.

## Race builder

Create a new strain that rode into Varuun on something else it swallowed, with its own name, background story, colors and four units.

- **Ecology:** what your dead leave behind, how well you digest each corpse type (within a fixed budget), plus one passive, one core aura and one ability.
- **Units:** a worker and three troop tiers, each with health, armor, damage, attack speed, range, speed and up to two traits: Splash, Medic, Shield, Regrowth, Undying, Necromancy, Burst or Leech.
- **Art:** each unit is built from parts (body, limbs, weapon, eyes), with a live animated preview.

**No overpowered builds.** You never set a price. Every unit is costed from its stats and traits, so stronger troops simply cost more Nutrient, and each tier has a ceiling. A few extreme combinations are blocked outright, such as very long range on a fast or tanky unit. In online play the host re-checks every guest's race, so editing the exported file won't get past the limits.

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
| Move, attack, harvest or scavenge | Tap the ground, an enemy, a nutrient well or a corpse |
| Save a control group | Hold a group button (1–3) |
| Recall a control group | Tap a group button; double-tap to jump the camera there |
| Train, mutate, set a rally point | Tap your core or a foothold |
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
| `B` | Grow a foothold |
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

## Roadmap

1. **The Atlas.** Done: see Campaign above.
2. **Drift mode.** Done: see Drift above.
3. **The Deep Lumen.** Done: see above. It uses a lightweight built-in 3D renderer, so the game stays a single file. A full Three.js version is a possible future upgrade.

## Credits

- Networking: [PeerJS](https://github.com/peers/peerjs) (MIT License)
- Font: [Oxanium](https://fonts.google.com/specimen/Oxanium) via Google Fonts (SIL Open Font License)

## License

© 2026 Jacor. All rights reserved.

You're welcome to play Necrotroph. You may not copy, modify, redistribute or reuse its code, art, designs, names or text without written permission. See [LICENSE](LICENSE) for details.
