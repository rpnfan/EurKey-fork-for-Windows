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

## Security / Virus Check

This repository provides a compiled Windows installer (`.exe`). If you want to verify it before running it, upload it to **[VirusTotal.com](https://www.virustotal.com/)** — it will be scanned by 70+ antivirus engines simultaneously.

When I last checked, 68 of 69 engines reported the file as clean. The single flag came from Trapmine, which uses machine-learning heuristics and is [well known for false positives on legitimate installers](https://www.google.com/search?q=Trapmine+Malicious.moderate.ml.score+false+positive). No major antivirus vendor flagged it.

If you're not comfortable running the installer regardless, the KbdEdit source `.kbe` is also in this repo which you can use and build the installer with kbdedit yourself.

### Hashes
```
File: C:\Program Files (x86)\KbdSoft\KbdEdit 25.1.0 Premium\KbdEditInstallerEurKey_rpnfan.exe
Size: 1,61 MB (1.690.624 bytes)
Date: 21.06.2026 20:53:35

CRC-32   16c879b1
MD5      1bc72b609ad8b8cfdc5fbb509745c542
SHA-1    0ccd22192b545c44d5ed5e71fa2e22aa41f16070
SHA-256  3e26b2cc0ec536bce24b4799e5244f51718982831c4af558e2aeec46f19359dc
SHA-384  03dd94acef9cae2b047340a62015f1f51ae165497abc3c1c539c16067ece31a0e071cfaea9535ef23638d6feaaec21a2
SHA-512  8f9b1f21a00ec2520f33caf0546346a81dd21569d78315f7d53cd786b64f0c8605b314bdfd5b33c061d6e19cbcd5d07970ce303d85f30c271d01a3fd2de31363
```

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
