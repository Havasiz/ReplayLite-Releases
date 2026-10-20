Name new clips after their category using a readable, sortable timestamp.

Saved replays and manual recordings now use filenames such as "RUST 2026.10.20 - 18.06.22.mp4" and "Desktop 2026.10.20 - 18.06.22.mp4". The category matches the destination folder, preserving friendly names and internal spacing. There is no .DVR suffix or fractional second field. Names sort by category, then local date/time within that category.

Existing files are not renamed. If two clips have the same category and timestamp, the existing non-overwrite protection adds a numeric suffix. Capture, encoding, audio, replay length and recording quality are unchanged. The rejected GPU capture experiment is not included.

Settings and recordings survive upgrades. This is a normal update, not an emergency. Windows binaries are unsigned; application source remains private.
