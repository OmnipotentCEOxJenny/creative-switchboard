---
name: convert-timeline
description: Convert an editing timeline between OpenTimelineIO (OTIO), FCPXML, AAF, EDL and other interchange formats with the free OpenTimelineIO tools, and report what survives. Use when a user wants to move an edit between Premiere Pro, Final Cut Pro, DaVinci Resolve, Avid, Kdenlive or other editors.
---

# Convert a timeline

1. Ask for the source file and the target editor. Check the target's import formats in `skills/route-creative-project/references/allowlist.csv`; if UNVERIFIED, check the editor's manual first.
2. Use OpenTimelineIO (open source, Academy Software Foundation): `pip install opentimelineio`, plus the adapter for the format if needed (for example `otio-fcpx-xml-adapter`, `otio-aaf-adapter`, `otio-cmx3600-adapter` for EDL). Install only if the user agrees.
3. Inspect: `otiostat source.ext` (tracks, clip counts, duration).
4. Convert: `otioconvert -i source.ext -o target.ext`.
5. Verify (pillar 3): run `otiostat` on the output and compare track count, clip count and total duration with the source. Report differences.
6. Warn: interchange keeps cuts, clip names, media references and basic timing; effects, color grades, plugins and some transitions are usually lost. Media paths must be relinked if files moved; keep media in the Dropbox hub or the same folder.
7. Never invent adapter names or flags; check `otioconvert --help` and the OTIO docs.
