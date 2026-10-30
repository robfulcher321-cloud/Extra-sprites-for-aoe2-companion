# Extra sprites for AoE2 Companion

Game graphics for the [AoE2 Companion](https://github.com/robfulcher321-cloud/AOE-2-companion-) app,
kept out of the app so the APK stays small and sprites can be updated without a new build.

- `manifest.json` lists every pack with its size and SHA-256. The app reads it at start-up,
  downloads any pack it doesn't have (or whose hash changed) and keeps it on the phone.
- `packs/units-*.aoe2pack`: unit animations (idle, walk, attack, death) for every land unit the app
  shows, including siege, camels and Monks, plus grass and projectiles.
- `packs/buildings.aoe2pack`: Barracks, Archery Range, Stable, Castle, Market, Blacksmith,
  Siege Workshop and Monastery for every architecture set, and which set each civ uses.

Format 2: each frame is stored once (facing right) with its player-colour mask; the app tints the
mask with each player's colour, the way the game does.

Made with `tools/make_sprite_pack.py` in the app repo from a copy of Age of Empires II: Definitive
Edition. The artwork belongs to Microsoft / World's Edge; it's here for a personal, non-commercial
companion app.

To update: rebuild the packs, copy them into `packs/`, replace `manifest.json`, commit and push.
Phones pick up the change the next time the app starts online.
