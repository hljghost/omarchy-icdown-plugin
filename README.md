# icdown (Omarchy plugin)

Bar widget for [icdown](https://github.com/hljghost/icdown): iCloud Photos backup progress on the Omarchy Quattro bar.

Click the pill for progress, **Copy now**, open the photo folder, sign in / sign out, and start or stop the tray service.

## Requirements

- Omarchy with Quattro shell
- [icdown](https://github.com/hljghost/icdown) installed and on `PATH` (`icdown`, optional `icdown-tray`)
- Python 3 (for `status.py`)

This plugin does **not** ship the downloader. Install icdown first, then add the plugin.

## Install

```sh
omarchy plugin add https://github.com/hljghost/omarchy-icdown-plugin.git --enable
```

Place on the bar (if needed):

```sh
omarchy bar move io.github.hljghost.icdown --section right
```

## Usage

- Left click: open / close the details panel
- Right click: run `icdown copiar` in a floating terminal
- Panel actions: copy now, open folder, sign in, sign out, start/stop tray
- Press `R` in the panel to refresh

Sign-out clears the local iCloud session and Apple ID from `~/.config/icdown/`. It does **not** delete your local photo backup.

## Configure

```sh
omarchy bar set io.github.hljghost.icdown refreshIntervalSec 15
```

## Remove

```sh
omarchy plugin remove io.github.hljghost.icdown
```

Removing the plugin does not uninstall `icdown` or delete `~/Pictures/iCloud`.

## License

MIT. See [LICENSE](LICENSE).

icdown itself is a Linux port of [Z1Code/iCopy](https://github.com/Z1Code/iCopy) and uses [icloudpd](https://github.com/icloud-photos-downloader/icloud_photos_downloader). Not affiliated with Apple.
