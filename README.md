# Twilight Cursors for Windows

A native Windows port of the [Twilight Cursors](https://github.com/yeyushengfan258/Twilight-Cursors) theme by **[yeyushengfan258](https://github.com/yeyushengfan258)**, originally built for GNOME/Linux (inspired by macOS, based on capitaine-cursors).

This repo contains the same artwork converted into real Windows `.cur` / `.ani` files (32×32, PNG-compressed cursor resources), ready to install — no Linux, no XCursor tooling required.

The conversion was done with [https://github.com/Anshitas-12/linux-cursor-to-windows-converter](#) (link your tool repo here), a small Python tool that reads the theme's SVG source and per-cursor hotspot config directly, rather than guessing.

## What's included

- `cursors/` — 47 converted cursors: 45 static `.cur` files + 2 animated `.ani` files (`wait.ani`, `progress.ani`)
- `install_cursors.reg` — maps the 9 standard Windows pointer roles to these files

## Installation

1. Download/clone this repo to a permanent location (don't put it somewhere you'll delete later — Windows references these files by path, it doesn't copy them in).
2. Open `install_cursors.reg` in Notepad.
3. Find-and-replace `REPLACE_WITH_FULL_PATH` with the **full path** to this repo on your machine, e.g.:
   ```
   C:\Users\yourname\Twilight-Cursors-for-Windows
   ```
   Use double backslashes (`\\`) the way the rest of the file already does — don't add single ones.
4. Save the file, then double-click it. Click "Yes" when Windows asks to confirm.
5. Open **Settings → Bluetooth & devices → Mouse → Additional mouse settings → Pointers tab**, and click **Apply**.

Only the 9 standard roles (Arrow, Hand, IBeam, Wait, AppStarting, Crosshair, NWPen, No, and the 4 resize cursors) get auto-installed by the `.reg`, since those are the only roles Windows actually exposes a slot for. The rest of the theme (`copy`, `zoom-in`, `pirate`, `alias`, etc.) are still in `cursors/` — assign any of them manually from the same Pointers tab via the **Browse** button if you want them too.

## License

This is a derivative work of Twilight Cursors, which is licensed under **GPL-3.0**. As required by that license, this derivative is distributed under the same license — see [`LICENSE`](LICENSE).

All credit for the original artwork and design goes to yeyushengfan258. This repo only contains a format conversion; no new artwork was created.

## Credits

- Original theme & artwork: [yeyushengfan258/Twilight-Cursors](https://github.com/yeyushengfan258/Twilight-Cursors)
- Conversion tool: https://github.com/Anshitas-12/linux-cursor-to-windows-converter
