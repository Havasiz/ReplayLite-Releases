Game and microphone audio now play together normally, with separate audio files for easier editing.

- **Mixed + Separate** keeps isolated System Audio and Microphone tracks and adds a combined default playback track inside the same MP4. Default playback was checked with Windows' own decoder as well as FFmpeg.
- **Settings > Audio > Save game + mic files** optionally saves two audio files right beside each new replay or manual recording: ` - Game.m4a` and ` - Mic.m4a`. Enabling it selects Mixed + Separate. The setting is off by default on new installs.
- **Settings > Audio > Export clip audio...** extracts those files from an existing ReplayLite separate-track MP4. The original stays unchanged, and existing exports are never overwritten. A recording saved with only combined audio cannot be separated afterward.

**For Clipchamp:** import the MP4 and both M4A files, place the audio files at 0:00, and mute the video's attached sound. You can then change microphone volume independently. Clipchamp's Detach audio action selected only the game track in the tested clip; it did not expose all embedded tracks.

M4A exports copy the existing AAC audio without re-encoding. No FFmpeg installation or virtual microphone is needed. Automatic audio files add about 6 MB per 150-second clip and copy work when saving, with no extra continuous audio encoder for the export. The combined playback track adds one AAC encoder compared with the older two-track mode. Video capture, NVENC settings and video quality settings are unchanged.

Validation: all 11 native tests passed; controlled tones stayed isolated, a 60-second live-mic capture had zero dropped video frames, and replay/manual audio decoded identically. The installed-app save test produced paired M4As for three replays and one manual recording, matching the source audio exactly. Independent editing of embedded tracks inside Clipchamp is not promised; use the neighboring audio files.

Settings and recordings survive upgrades. Existing clips are not rewritten. This is a normal preview update. Windows binaries remain unsigned, and the application source remains private.
