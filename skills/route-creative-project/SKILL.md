---
name: route-creative-project
description: Plan and run a transfer of a creative project or media between tools (video editors, DAWs, music and image generators, animation and 3D apps, design tools, voice and subtitle tools, storage hubs, posting platforms). Use when a user asks to move, send, hand off, export or import a project, timeline, stems, audio, images or video from one creative tool to another.
---

# Route a creative project

Follow `rules/pillars-and-scope.mdc`. Required.

## Workflow
1. **Identify source, destination and asset type** (timeline, audio stems, mix, images, 3D scene, subtitles, final render).
2. **Look up both tools** in `references/allowlist.csv`. Note the integration method, formats, whether the API needs a paid plan, terms limits, hard blockers, Google/Facebook exclusion, and verification status. If a tool is UNVERIFIED or missing, check the vendor's official docs first or tell the user it is unchecked.
3. **Pick the route, most open first:**
   1. Open format the destination imports (OTIO, FCPXML, AAF, EDL for timelines; WAV/FLAC/MIDI for audio; PNG/TIFF/SVG for images; glTF/FBX/USD for 3D; SRT/VTT for subtitles). See `skills/convert-timeline` for timeline work.
   2. Local scripting the app officially offers (for example Audacity mod-script-pipe, Blender Python, OBS WebSocket, Resolve Studio scripting).
   3. Hub: put the files in Dropbox (or local disk) so every tool reads the same copy, with no re-upload.
   4. Cloud API only with the user's own sign-in and within the vendor's terms.
   5. Otherwise: give the user manual export and import steps.
4. **Stop on hard blockers** (for example Midjourney bans automation; Spotify has no upload API). Say so and offer the manual route.
5. **Run or describe the steps.** Never run credit-spending generation without explicit approval.
6. **Verify the result** (pillar 3): the file exists and opens; duration, frame rate, sample rate and track count match; report any loss (effects and plugins usually do not survive interchange).
7. **Report**: route chosen and why, steps, what was verified, what was lost, unverified tool facts.

## Social platforms
Posting platforms are downstream targets only. The switchboard works upstream between creative tools; posting is the last optional step.
