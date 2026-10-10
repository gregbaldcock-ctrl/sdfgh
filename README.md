# Paris Bulwark (working title)

A solo build-and-defend mashup for [Melty](https://melty.gg): you play in **Assassin's Creed Unity's** Paris and use **Fortnite's** building pieces and weapons to hold a landmark against Parisian mobs.

> **Status: design only.** Nothing is built, tested or published yet. There is no playable build and no gameplay screenshot.

## The idea
- **Host game (Melty role `primary`):** Assassin's Creed Unity
- **Companion game (Melty role `companion`):** Fortnite. It is never launched or modded. Its building pieces and weapons are read from each player's own installed copy, and nothing from either game is ever copied into this repo or a release.
- **Players:** solo only for the first version
- **First minute:** you're already defending a landmark (Notre-Dame's courtyard first, a rooftop later)
- **First playable must have:** placing and editing Fortnite building pieces (walls, floors, ramps, roofs), and a few Fortnite weapons to find and use
- **Later:** escalating waves, win/lose, harvesting, outfits and emotes, music, co-op

## Repository layout
| Path | What it is |
|---|---|
| `design/DESIGN.md` | The design brief and open risks |
| `design/*.json` | Design sheets (the source of truth: change a sheet before code) |
| `design/PREFLIGHT.md` | Every unfilled cell in the first-version rows (91 at generation time, 0 broken references) |
| `AGENTS.md` | Instructions and a starter prompt for a coding agent (Claude Code, Codex) |

## Known risks
1. Assassin's Creed Unity has no Melty loader, so the hook route into the game still has to be found from its installed files.
2. Fortnite's content sits in encrypted Unreal archives, and reading it at runtime from the player's install may depend on keys that change with updates.

If either one blocks the design, the design changes only with the owner's agreement.

## Licensing and credits
Not chosen yet. The content license, credits and remix choice need the owner's decision before any release is listed.

Assassin's Creed and Fortnite belong to their respective owners. This project is an unofficial fan mashup and ships none of their content.
