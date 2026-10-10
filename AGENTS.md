# Instructions for coding agents

Read `design/DESIGN.md` and the JSON sheets in `design/` first. The sheets are the source of truth: change a sheet before changing code, and build only when `design/PREFLIGHT.md` shows zero unfilled first-version cells and zero broken references.

## Hard rules
- Assassin's Creed Unity is the host (role `primary`). Fortnite is a companion (role `companion`) and is never launched or modded. Do not swap the games.
- Never copy, extract into the repo, or upload any game content (models, textures, sounds, levels, archives). Read it from the player's installed copy at runtime (`{game:fortnite}` in the Melty recipe). Point at the owner's game folders; don't copy out of them.
- No look-alike stand-ins for either game.
- Never commit secrets, including Melty tokens, API keys and passwords. Send a Melty token only in Melty's Authorization header.
- If an obstacle blocks the design, explain it to the owner and get agreement before changing the design.
- Don't guess the content license, credits or remix choice: ask the owner.
- Ask the owner before calling Melty's `publish`.

## Starter prompt
> Build and publish the mashup designed in this repo. Assassin's Creed Unity is the host (role "primary") and Fortnite is a companion (role "companion"). It's solo only, and Fortnite's building pieces and weapons are read from the player's own install, never copied. Connect to Melty, then run `list_my_mods`, `search_mashups` and `game_info` on both games. Settle the hook route into Unity and how to read Fortnite's files. Fill the sheets until PREFLIGHT.md has zero gaps, build, test in the running game, and capture a real screenshot. Run the Melty checks (`inspect_package`, `validate_recipe`, `one_click_check`), upload as a draft, and ask me before calling `publish`.
