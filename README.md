# dna-tool for Crusader Kings III

A free Windows app for character appearances (DNA) in Crusader Kings III. Keep a library of
characters with 3D previews and portraits, edit their genes, make new characters from groups of
similar faces, and give a character in your running game the appearance of one from your library.

It works with your own game and your own playsets: it reads the game's and your mods' files to
show characters exactly as your playset does. Everything stays on your PC. No account, no uploads,
no game files changed.

**[Download the latest version](https://github.com/whitenameb-dev/ck3-dna-tool/releases/latest)**

## What it does

- **Library**: add characters from Ruler Designer text or DNA codes (paste, files or whole
  folders). Folders, tags, stars, filters and portraits. Bulk actions: set genes on many characters
  at once, convert characters to another playset's genes, download.
- **Character screen**: a 3D preview with your playset's own models and textures (head, hair, body,
  clothes), every gene with its slider, colors and hairstyles. Copy the result as a DNA code or as
  Ruler Designer text.
- **Ethnicities**: group characters you like, then generate new characters from their genes, with
  limits per feature and per sex. Keep the drafts you like, throw away the rest.
- **In game**: give the character selected in your running game a library character's appearance,
  or open that character in the editor and change it live, then save it to your library.
- English and Korean.

## Requirements

- Windows 10 or 11, 64-bit.
- Crusader Kings III from Steam. Mods from the Steam Workshop and the launcher's local mods are
  read from your playsets.
- The In game tab works with game version 1.20. A new game version can stop it working until
  dna-tool is updated; the rest of dna-tool keeps working.

## Install

Two downloads, the same app:

- `dna-tool-<version>-setup.exe`: installs dna-tool with a Start menu entry and an uninstaller.
- `dna-tool-<version>-portable.exe`: runs without installing.

dna-tool is not code-signed yet, so Windows may show "Windows protected your PC". Choose
**More info**, then **Run anyway**. To check your download, compare its SHA-256 hash
(`Get-FileHash <file>` in PowerShell) with `SHA256SUMS.txt` in the same release.

On first start, dna-tool finds your game and your playsets and asks before it reads the launcher's
playset list.

## About the In game tab

To show and change the character selected in the game, dna-tool's helper (`game-link.exe`) reads
and writes the running game's memory: only the selected character's appearance, never your save
files or game files, and it does not change the game's code. It runs only while you use the In game
tab or "Give … this appearance", talks only to dna-tool (no network), and closes when dna-tool
closes.

> **Antivirus warning.** `game-link.exe` is not code-signed yet, and it opens another program (the
> game) to read and write its memory. Game trainers and some malware do the same, so your antivirus
> may warn about it, block it or quarantine it, sometimes without asking.
>
> - If it is quarantined, only the In game tab stops working; the rest of dna-tool works as before.
> - To use the In game tab anyway: first check your download against `SHA256SUMS.txt` in the same
>   release, then restore the file from quarantine or allow it in your antivirus. With the setup it
>   is in `resources\game-link\` in dna-tool's install folder; the portable program unpacks it to a
>   new temporary folder on each start, so if your antivirus keeps blocking it, use the setup.
> - Download dna-tool only from this repository's
>   [Releases](https://github.com/whitenameb-dev/ck3-dna-tool/releases). Copies from anywhere else
>   may not be what they claim.

It changes appearance only, nothing that affects play. Use it in single-player games only, never in
multiplayer games.

Changes made this way are part of the game's state like any other: save your game to keep them, or
use **Put back** to return the character's own appearance. Use it at your own risk, and keep a copy
of saves you care about.

## Your data

Settings, the library and the cache are in `%LOCALAPPDATA%\dna-tool` (the library can be moved to
another folder in Settings). Uninstalling dna-tool leaves them there; delete that folder to remove
them too.

## Questions and problems

Report problems in [Issues](https://github.com/whitenameb-dev/ck3-dna-tool/issues): what you did,
what happened, and your dna-tool version (shown at the bottom of the menu).

## Support

dna-tool is free. If it is useful to you, you can support it on
[Ko-fi](https://ko-fi.com/whitenameb).

## License

Free for personal, non-commercial use; you may share it unchanged and free of charge. See
[LICENSE](LICENSE). This repository holds the releases only.

dna-tool is a fan-made tool. It is not made, endorsed or supported by Paradox Interactive.
Crusader Kings is a trademark of Paradox Interactive AB.
