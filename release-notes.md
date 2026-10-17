Windows x64 preview with startup updates.

- The app checks for updates whenever it starts, even with automatic installation off.
- **Install updates automatically** is off by default. With it off, newer versions show a notice. With it on, normal updates install at the next app launch before recording starts.
- The publisher can sign an emergency security update that installs at startup regardless of the normal toggle. There is no remote command execution channel: only a newer-version installer matching the pinned signing key and SHA256 hash is accepted.
- Signature checks, HTTPS restrictions and downgrade checks protect the updater. Running recordings are not stopped. The existing replay buffer is not carried across app restarts; completed recordings remain on disk.
- Update checks do not send recordings, settings or account credentials. An offline app cannot receive an update instruction.

This release is a normal update, not an emergency. Versions older than 0.3.3 need a manual installation to gain the new updater.

Download **Setup-x64.exe** for a normal per-user installation, or extract the whole **Windows-x64.zip**. Settings and recordings survive upgrades and uninstall. The installer does not require administrator rights. Automatic updates of ZIP copies add an uninstaller in the same folder.

Windows 11 x64, an NVIDIA NVENC API 12.1-compatible GPU/driver, and an NVIDIA-connected primary SDR landscape display are required. The Windows binaries are unsigned and Windows may show a warning. This is experimental software with measurable recording overhead and hardware/A/V limitations. Application source remains private.
