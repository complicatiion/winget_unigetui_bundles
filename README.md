# Windows Tool Bundles

This README summarizes the cleaned UniGetUI package bundles created for Windows desktop, admin and creative workstation setups.

The goal of these bundles is to provide practical, reproducible Windows application sets using trusted package manager sources, primarily **WinGet**, without random local installers, unknown sources, game launchers, vendor bloatware, cracked software, Adobe Creative Cloud, subscription clients or unnecessary trialware in the default bundles.

The packages are intentionally **not version-pinned**. UniGetUI/WinGet should resolve the current available package version during installation. This keeps the bundles easier to maintain, but it also means that package behavior, publisher metadata or installer behavior can change over time.

Before using any bundle in a company or managed environment, check the publisher, license terms, silent install behavior, data protection requirements and security impact. Some tools can install drivers, codecs, shell extensions or system-wide components.

## General Usage

1. Open **UniGetUI**.
2. Import the required `.ubundle` file.
3. Review the package list before installation.
4. Remove anything not needed for the target system.
5. Start the installation through UniGetUI.

Recommended approach:

- Use the smaller category bundles when you want better control.
- Use the all-in-one bundle only for personal admin workstations, lab systems or broad baseline setups where the full toolset is actually wanted.
- Keep optional freeware/shareware bundles separate from production/company rollouts unless licensing is explicitly cleared.

---

# Bundle Overview

## 1. AllInOne Safe Windows Tools

**Bundle:** `AllInOne_Safe_Windows_Tools_Winget.ubundle`  
**Source:** WinGet only  
**Purpose:** Clean combined baseline containing selected packages from the admin, design and desktop bundles, plus cleaned entries from the original uploaded UniGetUI bundle.

This is the broadest default bundle. It is intended as a practical all-in-one Windows toolset for personal admin systems, test machines or general-purpose IT workstations.

Excluded from this default bundle:

- Local or unmanaged UniGetUI inventory entries
- Microsoft Store inventory noise from the old export
- Steam, GOG, Ubisoft, EA and similar game/launcher entries
- pip, PSGallery and Chocolatey/community helper packages
- Beta, Canary and duplicate package variants
- Obvious trialware, subscription tools and vendor bloatware
- Risky or very specific tools such as Windows modding utilities, old runtimes, emulators and gaming tools

Typical included areas:

- Admin and troubleshooting tools
- Browsers and mail clients
- Archive tools
- Media players and codecs
- Office, PDF and text utilities
- Screenshot and productivity tools
- Creative/design applications
- Development and terminal basics
- Remote access and network tools

Recommended use:

- Personal IT admin workstation
- Lab/test desktop
- General-purpose technician setup
- Not recommended as an unreviewed company-wide rollout

---

## 2. Optional Personal Freeware / Shareware Add-on

**Bundle:** `AllInOne_Optional_Personal_Freeware_Shareware_Winget.ubundle`  
**Source:** WinGet only  
**Purpose:** Optional add-on for tools that are useful, but not ideal for a clean default or company rollout because of licensing or usage restrictions.

Typical examples:

- XnView MP
- IrfanView
- WinRAR
- XYplorer
- Similar personal/freeware/shareware-style tools

Important notes:

- Use only when the license situation is clear.
- Do not include automatically in corporate baselines.
- Prefer open or clearly free alternatives for default deployments.

Recommended alternatives from the default bundles:

- Archive tools: 7-Zip, PeaZip, NanaZip
- File managers: Files, Q-Dir, Double Commander, Explorer++, FreeCommander XE
- Image viewing/editing alternatives: digiKam, ImageMagick, Krita, GIMP, darktable, RawTherapee

---

## 3. Windows Admin Tools - Safe WinGet Bundle

**Bundle:** `Windows_Admin_Tools_Safe_Winget.ubundle`  
**Source:** WinGet only  
**Purpose:** Safe and typical Windows admin toolkit without local packages, pip, Chocolatey, Store-only packages, gaming/media bundles, VPN clients, random downloaders, driver packs or vendor bloatware.

Typical included tools:

- 7-Zip
- Notepad++
- Visual Studio Code
- Windows Terminal
- PowerShell
- Git
- Sysinternals Suite
- Microsoft PowerToys
- Everything
- WinDirStat
- CrystalDiskInfo
- CrystalDiskMark
- PuTTY
- WinSCP
- FileZilla
- mRemoteNG
- Wireshark
- Nmap
- Rufus
- Ventoy
- ShareX
- Greenshot
- SumatraPDF
- KeePassXC
- Azure CLI
- Azure Storage Explorer
- SQL Server Management Studio

Important notes:

- Wireshark and Nmap may install or require additional components such as Npcap.
- SQL Server Management Studio package availability can vary. If the package cannot be resolved, remove it from the bundle or search/install it manually in UniGetUI.
- Recommended for IT admin workstations, support systems and troubleshooting environments.

---

## 4. Windows Design / Creative Tools Bundle

**Bundle:** `Windows_Design_Creative_Tools_Winget.ubundle`  
**Source:** WinGet only  
**Purpose:** Broad creative workstation bundle with free or freely usable design, media and production tools.

Typical included areas:

- 3D and CAD
- Raster graphics
- Vector graphics
- Video editing
- Audio editing and production
- Photo/raw workflows
- Font and publishing tools
- Media conversion and encoding
- Game/interactive creation basics

Typical included tools:

- Blender
- Krita
- Kdenlive
- Inkscape
- GIMP
- Pinta
- MyPaint
- Drawpile
- Pencil2D
- Synfig Studio
- Scribus
- FontForge
- XnView MP
- IrfanView and plugins
- ImageMagick
- darktable
- RawTherapee
- digiKam
- OpenShot
- Shotcut
- Shutter Encoder
- HandBrake
- FFmpeg
- VLC media player
- OBS Studio
- Audacity
- LMMS
- MuseScore
- FreeCAD
- LibreCAD
- MeshLab
- OpenSCAD
- Godot
- ShareX

Important notes:

- No Adobe Creative Cloud, trial/subscription clients, cracked tools or local installers are included.
- Some video/audio/3D tools are large and may install additional runtimes, codecs or components.
- XnView MP and IrfanView should be license-checked before company or commercial use.

Recommended use:

- Personal creative workstation
- Design lab machine
- Hobbyist digital art setup
- Reviewed creative baseline for non-Adobe workflows

---

## 5. Windows Design / Creative Tools - Strict OSS Variant

**Bundle:** `Windows_Design_Creative_Tools_Strict_OSS_Winget.ubundle`  
**Source:** WinGet only  
**Purpose:** Stricter creative bundle variant without XnView MP and IrfanView.

Use this variant when you want to avoid tools that may require additional license checks for company or commercial use.

Recommended use:

- Cleaner company-friendly creative baseline
- Open-source-oriented creative workstation
- Environments where freeware licensing is intentionally avoided

---

## 6. Windows Desktop Essentials - Free WinGet Bundle

**Bundle:** `Windows_Desktop_Essentials_Free_Winget.ubundle`  
**Source:** WinGet only  
**Purpose:** Typical Windows desktop baseline with free or freely usable everyday applications.

Included categories:

### Browsers and Mail

- Mozilla Firefox German package
- Google Chrome
- Brave Browser
- Vivaldi Browser
- LibreWolf
- Mozilla Thunderbird German package

### Archive Tools

- 7-Zip
- PeaZip
- NanaZip

### Media and Codecs

- VLC media player
- MPC-HC
- MPC-BE
- K-Lite Mega Codec Pack
- MediaInfo GUI
- Icaros
- HandBrake

### Office, PDF and Text

- LibreOffice
- ONLYOFFICE Desktop Editors
- SumatraPDF
- PDF24 Creator
- Notepad++

### Desktop Utilities

- Microsoft PowerToys
- Everything
- ShareX
- Greenshot
- KeePassXC

### File Managers and Explorer Alternatives

- Files
- Q-Dir
- Double Commander
- Explorer++
- FreeCommander XE

Important notes:

- WinRAR is not included in the main bundle because it is trialware/nagware.
- XYplorer is not included in the main bundle because it requires a paid license.
- K-Lite Mega Codec Pack installs system-wide codecs and filters. Roll it out only when this is explicitly wanted.
- Firefox and Thunderbird use the German WinGet packages to avoid accidentally switching users to an English UI.

Recommended use:

- General desktop baseline
- Home/admin workstation
- Technician setup
- Non-specialized Windows installation

---

## 7. Windows Desktop Essentials - Optional Shareware Add-on

**Bundle:** `Windows_Desktop_Essentials_Optional_Shareware_Addon_Winget.ubundle`  
**Source:** WinGet only  
**Purpose:** Small optional add-on for tools requested by name but intentionally kept out of the free default desktop bundle.

Included tools:

- WinRAR
- XYplorer

Important notes:

- Use only when trial/shareware behavior and licensing are accepted.
- Keep separate from default/free company bundles.
- Prefer 7-Zip, PeaZip or NanaZip for archives when a fully free default is required.
- Prefer Files, Q-Dir, Double Commander, Explorer++ or FreeCommander XE as default file manager alternatives.

---

# Rollout Notes

These bundles are designed as clean starting points, not as blindly deployable corporate standards.

Before broader rollout:

- Import the bundle into UniGetUI and review every package.
- Remove tools that are not needed for the target group.
- Check license terms and commercial-use restrictions.
- Check whether tools install drivers, codecs, shell extensions or background services.
- Test installation and uninstall behavior on a clean Windows test machine.
- Keep optional/shareware bundles separate from default deployments.

For managed company environments, the safest structure is usually:

1. Start with `Windows_Desktop_Essentials_Free_Winget.ubundle`.
2. Add `Windows_Admin_Tools_Safe_Winget.ubundle` only for IT/admin systems.
3. Add the design bundle only for creative users or lab systems.
4. Use strict OSS variants where licensing needs to be simple.
5. Keep optional freeware/shareware add-ons out of default rollouts.

