<img width="1448" height="518" alt="image" src="https://github.com/user-attachments/assets/202d748e-9d21-4202-8143-b22be31783b0" />

# EurKey (Windows Installer Rebuild)

**Unofficial rebuild of [EurKEY v1.3](https://eurkey.steffen.bruentjen.eu/)
by Steffen Brüntjen: same layout, fixed Windows installer.**

This is **not** a modified layout. The keymap is identical to the
official EurKEY v1.3. The only difference is the build pipeline used
to create the Windows installer.

## Why this exists

The official Windows installer had several issues reported:

- Problems with keyboard shortcuts not working
- May not register correctly in the Windows language bar
- Math symbols from beta 1.3 not working
- Fails to install on ARM64 Windows
- Keymaps could not be loaded directly into [KbdEdit](http://kbdedit.com/)

## What I did

1. Exported the layout to an MSKLC source file
2. Imported this into KbdEdit
3. Added the math symbols. These were missing from the MSKLC import.
4. Added a handful of extra math symbols such as: ⋙ ⋘ ≟ ⊾ ≉  and a real minus character. See the PDF for the shortcuts.
5. Built a new installer package from KbdEdit directly

This installer works correctly on the systems I tested, including ARM64.

## Installation/Uninstall

 1. Download the installer from [Releases](../../releases)
 2. Run the installer
 3. Reboot or log out and log in again to Windows.

 4. Uninstall: Run the installer again and choose the uninstall option.

## Security / Virus Check

This repository provides a compiled Windows installer (`.exe`). If you want to verify it before running it, upload it to **[VirusTotal.com](https://www.virustotal.com/)** — it will be scanned by about 60+ antivirus engines simultaneously.

When I last checked, 68 of 69 engines reported the file as clean. The single flag came from Trapmine, which uses machine-learning heuristics and is [well known for false positives on legitimate installers](https://www.google.com/search?q=Trapmine+Malicious.moderate.ml.score+false+positive). No major antivirus vendor flagged it.

If you are not comfortable running the installer regardless, the KbdEdit source `.kbe` is also in this repo which you can use and build the installer with kbdedit yourself.

## Credit & License

The EurKEY layout is © Steffen Brüntjen, licensed under
[GPLv3](LICENSE). This repository redistributes it unmodified under the
same license, with a different installer build. All credit for the
layout design goes to the original author. Please check out the
[official site](https://eurkey.steffen.bruentjen.eu/) and consider
supporting it there.

This is an independent, unofficial project, not affiliated with or
endorsed by the original author.

## Future plans

I'm also working on a separate, modified layout inspired by EurKEY's
AltGr/diacritic approach which will live in its own repo under a
different name once it is ready.
