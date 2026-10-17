Windows x64 preview with public downloads and optional update notifications.

- **Setup-x64.exe**: install for your account with Start menu shortcut and uninstaller. No administrator access required.
- **Windows-x64.zip**: extract the entire folder and run ReplayLite.exe.
- **SHA256SUMS.txt**: checksums for both downloads.

Settings > General now has **Check for updates**, an **Automatic update checks** toggle (off by default), and **View releases / Download update**. Optional checks run at launch and every 24 hours. New versions produce a status notification and an overlay download banner. Downloads use the public distribution repository; no GitHub login is required. Updates are installed only when you choose, so recordings are never interrupted by a silent installer.

Windows 11 x64, an NVIDIA GPU with NVENC API 12.1-compatible drivers, and a primary SDR landscape monitor connected to the NVIDIA GPU are required. No Visual Studio or FFmpeg runtime is needed. Testing has primarily used an RTX 4070 Ti.

Settings and logs live in `%LOCALAPPDATA%\ReplayLite`; installed and ZIP builds share this folder. Updates and uninstall preserve settings and recordings. Existing source-checkout settings require manual import. System audio defaults on; microphone and Windows startup are opt-in.

Capture, encoding, replay, manual recording, mixed/separate audio and A/V timing are unchanged. This is experimental software with measurable recording overhead and hardware limitations. The binaries are unsigned and Windows may show an unknown-publisher warning.

The application source remains private. This repository contains compiled downloads, release documentation and update metadata only.
