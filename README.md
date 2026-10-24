# ReplayLite

Lightweight Windows instant replay and recording with NVIDIA NVENC, system audio,
microphone capture and a native overlay.

## Download

Get the latest preview from [Releases](https://github.com/Havasiz/ReplayLite-Releases/releases).

- **Setup-x64.exe**: install for your Windows account with a Start menu shortcut
  and an uninstaller. No administrator rights needed.
- **Windows-x64.zip**: extract the whole folder and run ReplayLite.exe.
- **SHA256SUMS.txt**: checksums for the downloads.

Windows 11 x64 and an NVIDIA GPU with NVENC API 12.1-compatible drivers are
required. The primary monitor must be attached to the NVIDIA adapter and use SDR
in landscape orientation. Visual Studio and FFmpeg are not required.

This is experimental software, primarily tested on RTX 4070 Ti. Recording has
measurable game-performance overhead. HDR, rotated displays and other GPU vendors
are unsupported. A/V synchronization is not guaranteed to be sample-perfect.
Windows may warn about an unknown publisher because the downloads are unsigned.

## Controls

| Action | Default shortcut |
|---|---|
| Overlay | Ctrl + Alt + Z |
| Save replay | Alt + F10 |
| Start/stop recording | Alt + F9 |
| Toggle microphone | Ctrl + Alt + Shift + M |

Shortcuts are editable in Settings. The app remains in the tray when you close the
overlay. System audio is enabled by default; microphone and Windows startup are
opt-in. Choose your preferred recording folder in Settings.

## Separate game and microphone audio

For normal playback, Mixed + Separate includes game and mic together while
keeping their isolated tracks in the MP4. For editing in Clipchamp, enable
**Settings > Audio > Save game + mic files**. It saves ` - Game.m4a` and
` - Mic.m4a` right beside each new clip. Import all three files, put both audio
items at 0:00, and mute the MP4's attached audio. Adjust the Mic item separately.

For older ReplayLite separate-track clips, choose **Export clip audio...** in
Audio settings. A combined-only recording cannot be split afterward. Exports
copy the original AAC without re-encoding; no FFmpeg installation is needed.
Existing clips and exported files are never overwritten. Automatic audio files
are off by default on new installs and use about 6 MB per 150-second clip.

## Updates

Settings → General offers Check for updates, Install updates automatically
(off by default), and a link to these releases. Checks run at launch and every
24 hours. With automatic installation off, a newer version shows a notice. With
it on, normal updates install at the next app launch before capture starts.
No GitHub sign-in is needed; no settings or recordings are uploaded.

The publisher can sign an emergency security update that installs at app launch
even when normal automatic installation is off. Only verified newer installers
are accepted. Offline PCs cannot receive an update instruction. Versions older
than 0.3.3 require manual installation to gain the startup updater.

For manual installation, download the newer setup, close ReplayLite, and install
over the previous version. Settings and recordings survive upgrades and
uninstall. Installed and ZIP builds share `%LOCALAPPDATA%\ReplayLite` for data.
Automatically updating a ZIP copy adds an uninstaller in the same folder.

## About this repository

This is the public distribution repository. It contains compiled downloads,
documentation, release automation and update metadata. Application source code
and development history are maintained privately and are not included here.
GitHub's automatic “Source code” archives contain this distribution repository
only, not the application source.

The included NVIDIA NVENC header retains its original MIT notice. ReplayLite is
not affiliated with NVIDIA or any game publisher.
