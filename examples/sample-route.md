# Sample route plan (not run; planning example)

**Request:** move a Premiere Pro edit to DaVinci Resolve (free) and send the dialogue to Audacity for cleanup.

| Step | Tool | Method | Status of tool facts |
|---|---|---|---|
| 1 | Premiere Pro | UXP ProjectConverter exports FCPXML, AAF or OTIO (since 26.2) | Checked (Adobe docs + Adobe forum) |
| 2 | Hub | Save the OTIO file and media in one Dropbox folder | Checked (connected connector) |
| 3 | Resolve free | Import the timeline by hand (File > Import > Timeline). No scripting: Python scripting is Studio-only since 21.1 | Scripting fact checked (2 sources); OTIO import UNVERIFIED |
| 4 | Audacity | Export dialogue as WAV from Premiere; Audacity loads it; optional local control via mod-script-pipe | Checked (Audacity manual) |
| 5 | Verify | Compare clip count and duration (otiostat) and audio length; relink media if paths changed | n/a |

Lost in transfer: Premiere effects and Lumetri grades. Unverified: Resolve OTIO import (check the Resolve manual before relying on it).
