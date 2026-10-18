Quietly recover from Windows permission-screen and desktop capture interruptions.

Expected capture access-denied, access-lost and disconnected-session errors no longer display the red "Recorder unavailable" notification. ReplayLite keeps its existing retry loop and resumes capture when desktop access returns. These interruptions also no longer switch the recorder from NV12 to the BGRA fallback path.

Real capture and encoder failures still show errors. This change does not capture the protected Windows permission screen. Existing interruption behavior is retained: a capture session restarts, the replay buffer rebuilds, and an active manual recording is finalized rather than silently continued across the interruption.

Includes the 0.3.5 system/microphone audio continuity fix. Settings and recordings survive upgrades. This is a normal update, not an emergency. Windows binaries are unsigned; application source remains private.
