Fix audio crackling caused by jittery capture packet timestamps.

System and microphone audio packets were continuous at the device, but independently rounded timestamps inserted small silent gaps and overlaps into the recorded PCM. The capture path now keeps adjacent device samples continuous while retaining the initial A/V timing anchor. Real discontinuities and large clock changes still reanchor.

On a controlled ten-second repeat, system placement improved from 188 gaps / 188 overlaps to zero; microphone placement improved from 180 / 180 to zero. This is a measured capture-path fix, not a claim that every possible audio fault is resolved. No mixer gains, encoder settings or fixed A/V offset changed.

Applies to replay and manual recording, mixed and separate tracks. All existing HUD and startup-update features remain. This is a normal update, not an emergency.

Download Setup-x64.exe for installation, or extract the complete Windows-x64.zip. Settings and recordings survive upgrades. Windows 11 x64 and an NVIDIA NVENC-compatible GPU/driver with a primary SDR landscape monitor are required. Windows binaries are unsigned; application source remains private.
