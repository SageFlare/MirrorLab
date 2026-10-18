# MirrorLab

MirrorLab is a two-storey free-for-all test map demonstrating the mirrors and reflection effects included in [MirrorKit](https://github.com/SageFlare/MirrorKit). The playable map name is `FFA_MirrorLab`.

Version 0.5.0. Built with [ArgonSDK](https://github.com/Chiv2-Community/ArgonSDK) (Unreal Engine 4.25). Requires MirrorKit 0.6.0 or later.

## Installation

MirrorLab requires both:

- `MirrorLab.pak`
- `MirrorKit.pak`

Follow the installation guidance supplied with MirrorKit, then place `MirrorLab.pak` in your Chivalry 2 `TBL/Content/Paks/` folder as well. Launch the game through the [Unchained Launcher](https://github.com/Chiv2-Community/UnchainedLauncher).

Without `MirrorKit.pak`, the map structure still loads, but its mirrors, breakable mirror tiles and other MirrorKit effects are missing.

## Rooms

MirrorLab has an octagonal hub with test rooms on two floors. The stairwell is at 12 o'clock; room letters run **clockwise from the stairs**, ground floor first (A-G), then the upper floor (H-M). Each doorway has its letter above it.

| Room | Floor | Effect |
| --- | --- | --- |
| **A** | ground | Headless reflection: you have no head in first person. |
| **B** | ground | Floor and ceiling mirror pair forming an infinite hall-of-mirrors tunnel. |
| **C** | ground | Reference wall-mirror pair with recursive reflections and a walk-through space behind the mirrors. |
| **D** | ground | Low-cost shiny floor and ceiling materials using screen-space reflections and baked environment fill; includes the dark-centre variant. |
| **E** | ground | Magnified, gappy funhouse mirrors; one is backed by a second funhouse mirror facing the back corridor. |
| **F** | ground | Two partnered mirrors, one deliberately turned 20 degrees. |
| **G** | ground | One-level mirror with the stretching-head effect. |
| **H** | upper | Independent (unpartnered) mirrors: a facing pair and an end-wall mirror showing each other's images, as used in mirror-heavy maps. |
| **I** | upper | A wall of breakable live-reflection tiles showing a mirror on each side; broken tiles leave walk-through openings. |
| **J** | upper | Ghost reflection: the body disappears while held weapons remain visible. |
| **K** | upper | Two live mirrors back to back versus a one-sided mirror, and full-body reflection stand-ins. |
| **L** | upper | A triangle of chained mirrors producing intentionally unusual multi-bounce reflections. |
| **M** | upper | Cheap breakable baked mirror tiles. The two halves demonstrate snow-wind and no-snow variants. |

Everyone spawns in the centre of the ground-floor hub, facing the stairs; there is no warm-up wait, and respawn waves start once the match is running. The opening in the upper hub floor drops back to the spawn area.

## Mirror quality

MirrorLab uses MirrorKit's default mirror settings. Players can change mirror quality with MirrorKit's launch options (for example `-MirrorQuality=Low` or `-MirrorQuality=Ultra`); hosts can set server values or an optional cap on the map URL. See the [MirrorKit README](https://github.com/SageFlare/MirrorKit#mirror-quality-for-players-and-servers).

## Performance

Measured solo on one PC with a 240 fps cap. These are relative comparisons, not hardware-independent targets; additional players visible in a live reflection add cost.

| Room | Setup | Measured frame rate |
| --- | --- | --- |
| Empty hub | No active mirrors in view | About 240 fps (cap) |
| **B** | Floor and ceiling tunnel, `Depth` 3 | About 170 fps |
| **C** | Facing wall pair, `Depth` 3 | 120-200 fps |
| **D** | Screen-space floor and ceiling materials | 150-220 fps |
| **I** | Live tiled wall (front and back mirrors), `Depth` 1 | About 210 fps |
| **M** | Baked breakable tiles | 200-300 fps |

Live mirrors render the scene once per visible reflection level. Results vary with view angle, visible mirror faces, hardware and the number of players in the captured scene.

## Known limitations

- Sheathed weapons do not appear in first-person reflections. Weapons in hand do appear, and third-person reflections show the full character.
- The stretching-head variant uses a deliberately stiff head pose.
- Live mirror tiles show one reflection level.
- The triangle room can produce unusual non-partner bounces and an occasional brief reflection freeze.

## Changelog

| Version | Changes |
| --- | --- |
| 0.5.0 | Rooms relettered clockwise from the stairs (A-M); new room H with independent mirrors; spawns moved to the centre of the hub, facing the stairs, with the quick start of the MirrorMaze tests; back faces are now separate mirrors (MirrorKit 0.6.0 removed the generated back face); the funhouse room's back mirror no longer tilts. Requires MirrorKit 0.6.0. |
| 0.4.0 | Published map. |

## License

Original MirrorLab work is licensed under the MIT License. See `LICENSE` and `THIRD_PARTY_NOTICES.md`.
