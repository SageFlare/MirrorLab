<!-- Generated from README.md by the maintainer's site script; edit README.md instead. -->

# MirrorLab

MirrorLab is a two-storey free-for-all test map demonstrating the mirrors and reflection effects included in [MirrorKit](https://github.com/SageFlare/MirrorKit). The playable map name is `FFA_MirrorLab`.

Version 0.7.0. Built with [ArgonSDK](https://github.com/Chiv2-Community/ArgonSDK) (Unreal Engine 4.25). Requires MirrorKit 0.10.0 or later.

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
| **B** | ground | Floor and ceiling mirror pair forming a hall-of-mirrors tunnel. |
| **C** | ground | Reference wall-mirror pair with recursive reflections and a walk-through space behind the mirrors. |
| **D** | ground | Low-cost shiny floor and ceiling materials using screen-space reflections and baked environment fill; includes the dark-centre variant. |
| **E** | ground | Magnified, gappy funhouse mirrors; one is backed by a second funhouse mirror facing the back corridor. |
| **F** | ground | Two partnered mirrors, one deliberately turned 20 degrees. |
| **G** | ground | Partnered mirror pair with the stretching-head effect. |
| **H** | upper | Independent (unpartnered) mirrors: a facing pair and an end-wall mirror showing each other's images, as used in mirror-heavy maps. |
| **I** | upper | A wall of breakable live-reflection tiles showing a mirror on each side; broken tiles leave walk-through openings. |
| **J** | upper | Ghost reflection: the body disappears while held weapons remain visible. |
| **K** | upper | Two live mirrors back to back versus a one-sided mirror, and full-body reflection stand-ins. |
| **L** | upper | A triangle of three independent mirrors reflecting each other. |
| **M** | upper | Cheap breakable baked mirror tiles. The two halves demonstrate snow-wind and no-snow variants. |

Everyone spawns in the centre of the ground-floor hub, facing the stairs; there is no warm-up wait, and respawn waves start once the match is running. The opening in the upper hub floor drops back to the spawn area.

## Mirror quality

MirrorLab uses MirrorKit's default mirror settings. Players can change mirror quality with MirrorKit's launch options (for example `-MirrorQuality=Low` or `-MirrorQuality=Ultra`); hosts can set server values or an optional cap in the map options. See [Mirror quality in the MirrorKit README](https://github.com/SageFlare/MirrorKit#mirror-quality).

## License

Original MirrorLab work is licensed under the MIT License. See `LICENSE` and `THIRD_PARTY_NOTICES.md`.
