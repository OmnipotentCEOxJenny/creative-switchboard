---
name: convert-timeline
description: Convert an editing timeline between OpenTimelineIO (OTIO), FCPXML, AAF, EDL and other interchange formats with the free OpenTimelineIO tools, and report what survives. Use when a user wants to move an edit between Premiere Pro, Final Cut Pro, DaVinci Resolve, Avid, Kdenlive or other editors.
---

# Convert a timeline

1. Ask for the source file and the target editor. Check the target's import formats in `skills/route-creative-project/references/allowlist.csv`; if UNVERIFIED, check the editor's manual first.
2. Use OpenTimelineIO (open source, Academy Software Foundation): `pip install "opentimelineio==0.18.1"`. Since OTIO 0.17 most format adapters are separate packages: `"otio-fcpx-xml-adapter==1.0.0"` (FCPXML), `"otio-cmx3600-adapter==1.0.0"` (EDL), `"otio-aaf-adapter==2.0.0"` (AAF). These pinned versions are the tested ones; if the user already has other versions, check `otiostat --help` before relying on these steps. Install only if the user agrees.
3. Inspect: `otiostat source.ext`. Note the lines `number of tracks`, `number of clips` and `total duration`.
4. Convert: `otioconvert -i source.ext -o target.ext`.
5. Verify: run `otiostat` on the output and compare track count, clip count and total duration with the source. Report differences.
   - AAF: the file is written, but in testing `otiostat` could not read it back (pyaaf2 error). Treat AAF output as UNVERIFIED until it opens in the target editor; prefer OTIO or FCPXML.
   - EDL (CMX 3600) holds one video track: a multi-track source converts with exit code 0 but audio and extra tracks are dropped. Expect fewer tracks and clips but the same duration, and tell the user. Use OTIO, FCPXML or AAF to keep all tracks.
6. Warn: interchange keeps cuts, clip names, media references and basic timing; effects, color grades, plugins and some transitions are usually lost. Media paths must be relinked if files moved; keep media in the Dropbox hub or the same folder.
7. Never invent adapter names or flags; check `otioconvert --help` and the OTIO docs.

## Language
Answer in the user's language; keep commands, file names, header and format names, and status labels unchanged. See the Language section of the rule file.
