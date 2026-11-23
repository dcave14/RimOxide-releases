# Changelog

The newest version is at the top.

## 0.9.0-beta.4

Built on 2026-11-22.

- Fixed: in 0.9.0-beta.2 and 0.9.0-beta.3 the mod list stayed empty at start until you pressed
  Reload. Your mods and lists were never touched; the first load was simply not started.
- While RimOxide reads your mods at start, the window now says it is loading. It no longer says
  that no mods are installed.
- The taskbar and title-bar icon follow the theme, and rimoxide.exe has its icon in File Explorer.
- Details shows a mod's own version; the game versions it supports are under "For game".
- A copy of the game that no store knows is found from the game's own log, once the game has been
  started at least once.
- Opening Rules in Details scrolls the rules into view.

Good to know:

- Do not go back to an older beta after using a newer one.
- This beta is not code-signed and has been tried on two PCs only.

## 0.9.0-beta.3

Built on 2026-11-22. Small fixes from a test run on a second PC.

- After a sort that puts the list back in its saved order, the status no longer asks you to save.
- In the sort proposal, a long reason for a move is shown in full on more lines, not cut off.
- The Search field has a name for screen readers.

Good to know:

- Do not go back to an older beta after using a newer one.
- This beta is not code-signed and has been tried on two PCs only.

## 0.9.0-beta.2

Built on 2026-11-22. It fixes what the first try on a second PC found.

- After a download without Steam (through SteamCMD), RimOxide now confirms what was installed.
  Before, that check answered "unreadable" for every mod.
- The library-guard folder in RimOxide's data folder no longer grows with every download run.
- New: logs\session.log. It notes the start, the game that was found, the notices shown, download
  runs, saves and launches, so a problem report always has a log to attach. It holds no mod list.

Good to know:

- Do not go back to an older beta after using a newer one.
- This beta is not code-signed and has been tried on two PCs only.

## 0.9.0-beta.1

The first public beta, built on 2026-11-21.

- Finds RimWorld, your Steam libraries and your Workshop mods by itself. You can choose each folder in Settings.
- Shows your active and inactive mods and sorts them, with a reason for every move.
- Lists problems such as missing dependencies or a wrong order, with a fix where there is one.
- Writes the game's mod list only when you press Save, and backs it up first.
- Keeps named profiles. A profile can have its own RimWorld settings and saves.
- Checks Workshop mods for updates and downloads them through Steam, or through SteamCMD without Steam.
- Keeps checkpoints of your whole setup, so you can go back to one that worked.
- Brings your mod lists, rules and colours over from the mod manager you used before.
- Starts the game, and backs up your newest save before it does.

Good to know:

- The first start after an update reads all your mods again, once. That start takes a little longer.
- Do not go back to an older beta after using a newer one.
- This beta is not code-signed and has not yet been tried on a clean PC.
