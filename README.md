# MirrorLab

MirrorLab is a two-storey free-for-all test map demonstrating the mirrors and reflection effects included in [MirrorKit](https://github.com/SageFlare/MirrorKit). The playable map name is `FFA_MirrorLab`.

Version 0.4.0. Built with [ArgonSDK](https://github.com/Chiv2-Community/ArgonSDK) (Unreal Engine 4.25).

## Installation

MirrorLab requires both:

- `MirrorLab.pak`
- `MirrorKit.pak`

Follow the installation guidance supplied with MirrorKit, then place `MirrorLab.pak` in your Chivalry 2 `TBL/Content/Paks/` folder as well. Launch the game through the [Unchained Launcher](https://github.com/Chiv2-Community/UnchainedLauncher).

Without `MirrorKit.pak`, the map structure still loads, but its mirrors, breakable mirror tiles and other MirrorKit effects are missing.

## Bays and rooms

MirrorLab has an octagonal hub with test rooms across two floors:

| Room | Effect |
| --- | --- |
| **A** | Floor and ceiling mirror pair forming an infinite hall-of-mirrors tunnel. |
| **B** | Reference wall-mirror pair with recursive reflections and a walk-through space behind the mirrors. |
| **C** | Low-cost shiny floor and ceiling materials using screen-space reflections and baked environment fill; includes the dark-centre variant. |
| **D** | Two partnered mirrors at different angles. |
| **E** | Cheap breakable baked mirror tiles. The two sides demonstrate snow-wind and no-snow variants. |
| **F** | Magnified, gappy funhouse mirrors, including a two-sided mirror. |
| **G** | One-level mirror with the stretching-head effect. |
| **H** | Headless reflection variant. |
| **I** | One-sided versus two-sided live mirrors and full-body reflection stand-ins. |
| **J** | A two-sided wall of breakable live-reflection tiles; broken tiles leave walk-through openings. |
| **K** | Ghost reflection: the body disappears while held weapons remain visible. |
| **L** | A triangle of chained mirrors producing intentionally unusual multi-bounce reflections. |

The stairwell connects both floors. The opening in the upper hub floor drops back to the ground-floor spawn area.

## Performance

Measured solo on one PC with a 240 fps cap. These are relative comparisons, not hardware-independent targets; additional players visible in a live reflection add cost.

| Room | Setup | Measured frame rate |
| --- | --- | --- |
| Empty hub | No active mirrors in view | About 240 fps (cap) |
| **A** | Floor and ceiling tunnel, `Depth` 3 | About 170 fps |
| **B** | Facing wall pair, `Depth` 3 | 120-200 fps |
| **C** | Screen-space floor and ceiling materials | 150-220 fps |
| **E** | Baked breakable tiles | 200-300 fps |
| **J** | Two-sided live tiled wall, `Depth` 1 | About 210 fps |

Live mirrors render the scene once per visible reflection level. Results vary with view angle, visible mirror faces, hardware and the number of players in the captured scene.

## Known limitations

- Sheathed weapons do not appear in first-person reflections. Weapons in hand do appear, and third-person reflections show the full character.
- The stretching-head variant uses a deliberately stiff head pose.
- Live mirror tiles show one reflection level.
- The triangle room can produce unusual non-partner bounces and an occasional brief reflection freeze.
- Multiplayer/server behavior, including joining an active match, has not yet been verified.

## License

Original MirrorLab work is licensed under the MIT License. See `LICENSE` and `THIRD_PARTY_NOTICES.md`.
