# SpaceEdit

A desktop editor with two modes you switch between without closing anything:

- **Text mode**: nano-style, with four themes.
- **Markdown mode**: TextEdit-style pages, with a Read view and side-by-side editing.

This repo holds only the installers and updates.

**[Download the latest version](https://github.com/tkimbel/SpaceEdit-releases/releases/latest)**: open **Assets** at the bottom of the release and pick the file for your computer.

| Computer | File |
|---|---|
| Windows 11 (64-bit) | `SpaceEdit_<version>_x64-setup.exe` |
| Mac with Apple silicon (M1 or later), macOS 12 or later | `SpaceEdit-<version>-apple-silicon.dmg` |

There's no build for Intel Macs or Linux. To check a Mac, go to Apple menu → **About This Mac**. It needs to say **Chip: Apple M…**; one that says **Processor: Intel** can't run SpaceEdit.

You don't need the other files: `latest.json`, the `.app.tar.gz` and the `.sig` files are for SpaceEdit's own updates.

## Installing on Windows

1. Download `SpaceEdit_<version>_x64-setup.exe`. If your browser says the file isn't commonly downloaded, keep it. In Edge, that's **⋯** → **Keep** → **Show more** → **Keep anyway**.
2. Run it. The installer isn't code-signed yet, so Windows shows **Windows protected your PC** the first time. Choose **More info**, then **Run anyway**.
3. The installer asks two questions:
   - whether to register SpaceEdit for `.md`, `.markdown` and `.txt` files (Windows keeps your current default apps until you pick SpaceEdit);
   - whether to add **Open with SpaceEdit** to Explorer's right-click menu (on Windows 11 it's under **Show more options**).

It installs for your user only, so it doesn't need an administrator. On a work PC, company policy may block an unsigned installer completely. If **Run anyway** isn't offered, ask your IT team.

## Installing on a Mac

1. Download `SpaceEdit-<version>-apple-silicon.dmg` and open it.
2. Drag **SpaceEdit** onto **Applications**.
3. Open SpaceEdit from Applications. The first time, macOS asks whether to open an app downloaded from the internet, and says Apple checked it. Choose **Open**.

Run SpaceEdit from Applications, not from the disk image: a copy on the disk image can't update itself.

## Updates

You only install SpaceEdit by hand once. After that it updates itself:

- It looks for a new version 10 seconds after it starts, at most once a day. **Check for Updates…** looks right away. It's in the command palette (Ctrl+Shift+P, or ⌘⇧P on a Mac), on the settings page and in the Mac's SpaceEdit menu.
- A new version shows a banner with **Install and restart**, **What's new**, **Skip this version** and **Later**. Nothing is downloaded or installed until you choose **Install and restart**.
- Each update's signature is checked before it's installed. SpaceEdit then restarts, with your tabs and unsaved changes as you left them.
- To stop the check at launch, turn off **Check for updates at launch** in the settings page's **Updates** section (Ctrl+, or ⌘,).

## Reporting a problem

- **In SpaceEdit** (versions after 1.1.0): choose **Report a Problem…**. It's in the command palette, F1 help, the settings page and the Mac's Help menu. It opens GitHub's bug form in your browser with SpaceEdit's version, your system and the mode filled in. It never adds file names, paths, host names or your text, and you see everything before you send it.
- **Or open the [bug form](https://github.com/tkimbel/SpaceEdit-releases/issues/new?template=bug-report.yml) yourself.** In 1.1.0, **Check for Updates…** shows your version.
- You need a free GitHub account, and reports are public, so leave out private text, passwords and keys.
- **No GitHub account?** SpaceEdit's **Copy Details for a Problem Report** puts the same details on the clipboard. Paste them into an email or a message to the person who gave you SpaceEdit.

## Checking a download (optional)

`SHA256SUMS.txt` in each release lists each file's SHA-256 checksum. To see a downloaded file's checksum:

- **Windows (PowerShell):** `Get-FileHash .\SpaceEdit_<version>_x64-setup.exe`
- **Mac (Terminal):** `shasum -a 256 SpaceEdit-<version>-apple-silicon.dmg`

## Uninstalling

- **Windows:** Settings → Apps → Installed apps → SpaceEdit → **⋯** → **Uninstall**. Your saved session stays unless you tick **Delete app data**.
- **Mac:** quit SpaceEdit and move it from Applications to the Trash.
