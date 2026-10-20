# Changelog

## 1.0.7 (2026-10-20)
- Allowlist accuracy fixes (each with two sources, listed in the row notes): HitFilm discontinued by Artlist (15 Jan 2025); Haiper consumer app shut (Feb 2025), enterprise only; WeTransfer Public API retired (disabled May 2022); Pro Tools Scripting SDK (PTSL) is free to any Avid account holder, not partner-only; Playground has no self-serve API (partner only).
- Adobe Animate: note added that it is in maintenance mode since Feb 2026 (still sold, no new features). Its JSFL API is still not yet checked.
- 30 of 138 tools now checked; 108 not yet checked (README and TRANSLATIONS counts updated).
- Data and docs only; no behavior changes.

## 1.0.6 (2026-10-20)
- TRANSLATIONS.md: each of the 23 languages now includes this plugin's specific limits list (from the README's "Honest assessment: what this plugin cannot do" section) plus the marketplace status. Machine translations, not reviewed by native speakers.
- Docs only; no behavior changes.

## 1.0.5 (2026-10-20)
- README follows the shared template: title, plain description, logo, existing content (Rob Domaine's four pillars unchanged), and a new final section "Honest assessment: what this plugin cannot do" listing real limits and the compliance statement.
- TRANSLATIONS.md now covers the same 23 languages as every Omnipotent plugin (title, description and honest-assessment summary for each), all marked as machine translations not reviewed by native speakers.
- Docs only; no behavior changes.

## 1.0.4 (2026-10-20)
- Install steps pin the tested versions: opentimelineio 0.18.1, otio-fcpx-xml-adapter 1.0.0, otio-cmx3600-adapter 1.0.0, otio-aaf-adapter 2.0.0 (Python 3.13).
- Found in testing: AAF output is written but `otiostat` cannot read it back (pyaaf2 error). AAF is now marked UNVERIFIED in the skill and README; OTIO or FCPXML recommended.
- README: removed a duplicate Installation section and a duplicate license line; marketplace status corrected to submitted 2026-10-15.
- Multi-language: the rule file and both skills tell the AI to answer in the user's language and keep commands and file names unchanged. Added TRANSLATIONS.md with short summaries in 20 languages (machine-made, not yet reviewed by a native speaker).

## 1.0.3 (2026-10-15)
- README: added Installation (the Quick start pointed to a missing section), Testing (the exact commands, with expected results) and License sections.
- convert-timeline: lists the adapter package for each format, names the otiostat lines to compare, and warns that EDL output drops the audio and extra tracks without an error (found in testing).

## 1.0.2 (2026-10-15)
- Fix: convert-timeline and the sample route now use `otiostat` (the real OpenTimelineIO 0.18 command) instead of `otioinfo`, which does not exist.
- Tested on v1.0.1: end-to-end test PASS. OTIO to FCPXML kept 2 tracks, 6 clips, 144 frames; Dropbox upload and download byte-identical (SHA-256 match); re-parse matched.

## 1.0.1 (2026-10-15)
- Google and Meta tools (Google Imagen/Gemini, Google Veo, Google Drive, YouTube, Meta AI, Instagram, Facebook, Threads) added back to the allowlist with not-yet-checked status; exclusion wording removed. Suno note: API sign-in uses a Google account.

## 1.0.0 (2026-10-15)
- First release: route-creative-project and convert-timeline skills, pillars rule, allowlist of 138 tools, sample route, logo.
