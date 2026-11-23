# Known issues

This is an early beta. These are the problems we know about. If you meet one that is not here,
please report it: see "Report a problem" in the [README](README.md#report-a-problem).

## This beta

- It is not code-signed. The first time, Windows SmartScreen says "Windows protected your PC":
  click More info, then Run anyway. Some antivirus programs may also warn about it.
- It has been tried on two PCs only.
- With Smart App Control on, it will not run.
- There is no installer. The download is a zip: unzip it and run rimoxide.exe.
- Windows only. Tested with RimWorld 1.7.
- A Steam copy of the game is found by itself. Any other copy is found once it has been started at
  least once on this PC: RimOxide reads the folder from the first lines of the game's own log. A copy
  that has never been started, or was only started by another Windows user, is not found: choose its
  folder in Settings.
- The Workshop tab needs Microsoft Edge WebView2, which most Windows PCs already have. Without it,
  RimOxide tells you so and the rest of the app still works.
- Only one RimOxide window runs at a time. A second start is refused, because two windows would
  overwrite each other's settings and would both tidy the same download folders as they start.
- Log files are never deleted by themselves. session.log, stalls.log and downloads.log each stop
  growing at 256 KB by dropping their oldest lines; crash reports (panic-*.log) are one file per crash.
  "Open logs folder" in Settings shows where they are.
- A crash report names the error message and the line of code where it happened, not every step
  that led there. A report that says what you did just before helps most.
- Uninstalling means deleting the folder that holds rimoxide.exe. Your data stays in
  %LOCALAPPDATA%\RimOxide until you delete it yourself. Deleting that folder also deletes the
  settings and saves of every profile that keeps its own folder there. Copies of mods that RimOxide
  placed in the game's Mods folder stay where they are. Read "Your data" in the
  [README](README.md#your-data) first.

## Speed

- Starting RimOxide, sorting, saving and launching the game take seconds, also with about 1,500 mods.
- A checkpoint is an optional backup of your whole setup, made only when you ask for one. The first
  checkpoint of a very big setup is slow, because it copies every file of every mod: about 21 minutes
  for about 1,500 mods. Nothing is downloaded, and the next checkpoint took well under a minute.
- Restoring a full checkpoint of a big setup can take a long time.
- Very large lists (4,000 mods) work, but adding or removing a mod can take a noticeable moment.

## Features still being proven

- Playing from a restored profile has not had its game launches checked by a player yet.
  Treat it as experimental.
- Guided bisect (finding the mod that breaks the game) can find a problem at start-up, but has not
  been proven for problems that show while playing. It may end with "inconclusive".
- Rule inference (guessing the load order from what is inside mods) is off by default and experimental.
- Bringing lists, rules and colours over from the mod manager you used before has not yet been
  checked against every format that manager writes.
- "Unsubscribe" and "Download again from Steam" in the Manage menu are new. Through RimOxide's own
  buttons they have been tested against a simulated Steam only.

## Steam and downloads

- While RimOxide talks to Steam (subscribe, unsubscribe, update), Steam may briefly show you as
  playing RimWorld.
- Unsubscribing in the Workshop tab hides the mod at once. Steam removes its files later, and RimOxide
  does not watch for that.
- Downloading mods without Steam needs SteamCMD, which RimOxide sets up for you.
- Starting the game from the Steam library, not from RimOxide, loads whichever copy of a mod RimOxide
  last placed in the game's Mods folder: the one for the profile you launched last from RimOxide.
- When a profile's chosen copy of a mod is missing, "Get the chosen copy again" can offer a different
  Workshop item for that mod. Read the list before you start the download.

## Pictures in mod descriptions

- Pictures in mod descriptions load from the web. Settings let you load only Steam's, all, or none.
  See [Privacy](README.md#privacy) in the README.
- Small badge pictures in some mod descriptions (SVG files) are not shown.

## Look and layout

- In the Backups window the table can look cramped when backup names are long.
- At 150% Windows scaling the top bar can drop the number of inactive mods; the number of active mods stays.
- In the light look some secondary text reads thin.
- With Windows at 150% and the Details panel at its narrowest, the two buttons at its bottom are cut short.
- On the update log page, a row's menu opened with the keyboard near the bottom can cover the row it
  belongs to.

## Going back to an older beta

- An older beta may set aside profiles made by a newer one that it cannot read. They are kept as
  files ending in .broken- and a date, not deleted. Do not go back to an older beta after using a newer one.
