<img width="1448" height="518" alt="image" src="https://github.com/user-attachments/assets/202d748e-9d21-4202-8143-b22be31783b0" />

# EurKey (Windows Installer Rebuild)

**Unofficial rebuild of [EurKEY v1.3](https://eurkey.steffen.bruentjen.eu/)
by Steffen Brüntjen — same layout, fixed Windows installer.**

This is **not** a modified layout. The keymap is identical to the
official EurKEY v1.3. The only difference is the build pipeline used
to create the Windows installer.

## Why this exists

The official Windows installer had several issues for me:

- Doesn't register correctly in the Windows language bar
- Fails to install on ARM64 Windows
- Keymaps could not be loaded directly into [KbdEdit](http://kbdedit.com/)

## What I did

1. Exported the layout to an MSKLC source file
2. Imported this into KbdEdit
3. Built a new installer package from KbdEdit directly

This installer works correctly on the systems I tested, including ARM64.

## Installation/Uninstall

 1. Download the installer from [Releases](../../releases)
 2. Run the installer
 3. Reboot or log out and log in again to Windows.

 4. Uninstall: Run the installer again and choose the uninstall option.

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
