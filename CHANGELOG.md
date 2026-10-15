# Changelog

## 1.0.2 (2026-10-15)
- Fix: convert-timeline and the sample route now use `otiostat` (the real OpenTimelineIO 0.18 command) instead of `otioinfo`, which does not exist.
- Tested on v1.0.1: end-to-end test PASS. OTIO to FCPXML kept 2 tracks, 6 clips, 144 frames; Dropbox upload and download byte-identical (SHA-256 match); re-parse matched.

## 1.0.1 (2026-10-15)
- Google and Meta tools (Google Imagen/Gemini, Google Veo, Google Drive, YouTube, Meta AI, Instagram, Facebook, Threads) added back to the allowlist with not-yet-checked status; exclusion wording removed. Suno note: API sign-in uses a Google account.

## 1.0.0 (2026-10-15)
- First release: route-creative-project and convert-timeline skills, pillars rule, allowlist of 138 tools, sample route, logo.
