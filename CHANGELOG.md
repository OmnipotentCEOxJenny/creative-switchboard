# Changelog

## 1.0.18 (2026-10-23)
- README: new "Testing status" section. Local automated tests pass; in-app testing is not yet completed. Records that the marketplace submit form's "tested locally and in-app" confirmation (2026-10-15, v1.0.3) was checked in error before any in-app test; in-app testing is pending.
- Docs only; no behavior changes. Local tests re-run and passed. Not tested in-app. Not resubmitted.

## 1.0.17 (2026-10-23)
- Translations: each language section in TRANSLATIONS.md now starts with a one-line notice in that language saying it is a machine translation, not reviewed by a native speaker, and that the English version is authoritative. README Languages section notes this. No behavior changes.
- Local tests re-run and passed. Not tested in-app. Not submitted to the marketplace.

## 1.0.16 (2026-10-23)
- Search keywords: 38 to 40 (added subtitles, voiceover), per Rob's keyword rules.
- Local tests re-run and passed. Not tested in-app. Not submitted to the marketplace.

## 1.0.15 (2026-10-22)
- Logo resized from 512x512 to 1024x1024 to match the rest of the plugin set (same artwork, no visual change). No behavior changes.

## 1.0.14 (2026-10-21)
- Added `tests/check_frontmatter.py`: a strict YAML front-matter check (PyYAML `safe_load`) for every SKILL.md and rules .mdc file, plus a plugin.json JSON check. Run `python3 tests/check_frontmatter.py` from the repo root; it catches the unquoted-colon bug fixed in PluginPulse 1.0.2.
- No behavior changes to skills or rules.

## 1.0.13 (2026-10-20)
- Allowlist complete: all 138 tools checked with two sources (sources in each row's notes).
- YouTube: the official videos.insert reference (updated 2026-10-15) says uploads from unverified API projects are not restricted to private. The upload quota is 100 per day. The row is no longer a partial blocker.
- Clipchamp: no editing API; Microsoft Graph Files API only for basic video operations.
- Studio One: no official scripting API; PreSonus offers plug-in extensions, ARA and DAWproject.
- LMMS: GPL-2.0, no scripting API; the lmms render/rendertracks CLI handles headless export to WAV/FLAC/OGG/MP3.
- Boomy: API by application only via Boomy Corporation, no self-serve access or published pricing.
- Data and docs only; no behavior changes.

## 1.0.12 (2026-10-20)
- Allowlist pass finished: 133 of 138 tools checked with two sources (sources in each row's notes); 5 remain UNVERIFIED with the reason stated: Clipchamp and Studio One (one source each), LMMS (no primary source opened), Boomy (API page unreadable), YouTube (sources conflict on unverified-project upload privacy).
- Corrections: Meta AI image now has a paid public API (Muse Image, $0.01/image); pCloud new app creation is disabled (hard blocker for new integrations); Filmora has no editing API (separate Wondershare AILab API); Cubase/Nuendo API is controller-only; Threads API supports video posts.
- Second sources added for every earlier one-source row except Clipchamp and Studio One.
- Data and docs only; no behavior changes.

## 1.0.11 (2026-10-20)
- Important status changes, two sources each: OpenAI Sora API shut down on 24 Sep 2026 (now a hard blocker); Google Veo 3.1 preview models on the Gemini API shut down 22 Oct 2026 (replacement gemini-omni-1.1-flash), paid only; Avid is not onboarding new Media Composer Extensions partners; Google Imagen is paid only (no free tier).
- Pricing or access confirmed with two sources: Grok Imagine, X (pay-per-use, no free tier), Adobe Firefly and Photoshop API (enterprise contract), Adobe Express (add-ons SDK; Express API beta), After Effects (UXP private beta), Beatoven.ai, Houdini Apprentice, Unreal Engine royalty, Backblaze B2, OneDrive, LinkedIn, Pinterest, DistroKid, Apple Music, Ableton (Max for Live), Bitwig, FL Studio, Cinema 4D, Toon Boom Harmony.
- One source, still UNVERIFIED: Studio One (no public scripting API), Soundraw ($29.99/mo API), Stable Audio, Lightworks formats, VEGAS Pro, Unity Personal, MASV, Illustrator UXP timeline, Instagram Reels limits.
- 97 of 138 tools now checked; 41 not yet checked.
- Data and docs only; no behavior changes.

## 1.0.10 (2026-10-20)
- Corrections, two sources each: Subtitle Edit is MIT (CLI is LGPL-3.0), not GPL; LottieFiles' own API is "coming soon" (Lottie downloads via the IconScout API, free plan 250 credits/month); Loudly has a self-serve paid API; Spline code export needs Pro.
- Second sources and pricing for the earlier single-source notes: Deepgram ($200 free credit; expiry wording differs between pages), D-ID, Rev, MEGA (20 GB free, BSD SDK).
- Confirmed with two sources: Aegisub, Shotcut, GIMP 3, Krita, Penpot, REAPER ($60/$225 license), Ardour (GPL-2.0+), PeerTube, Archive.org, ComfyUI (GPL-3.0).
- One source only, still UNVERIFIED: OpenShot (libopenshot is LGPL-3.0); pCloud (new app registration reported disabled).
- 73 of 138 tools now checked; 65 not yet checked.
- Data and docs only; no behavior changes.

## 1.0.9 (2026-10-20)
- Second sources added for Rumble, Audiomack, Otter.ai, Kapwing and Veed (now VERIFIED; Veed priced per use).
- Corrections, two sources each: Descript API in open beta for all users since 16 Apr 2026; Resemble AI no longer sells voice generation or cloning; Rive editor free but production export needs the $9/mo Cadet plan.
- Confirmed with two sources and pricing filled in: CapCut, Synthesia, HeyGen, Kling, Hailuo/MiniMax, AssemblyAI, Murf, Recraft, Box.
- LottieFiles corrected from one source (no public animation API; offered via IconScout), still UNVERIFIED.
- 55 of 138 tools now checked; 83 not yet checked. README explains how the counts add up to 138.
- Data and docs only; no behavior changes.

## 1.0.8 (2026-10-20)
- Allowlist check batch (sources in each row's notes). Two-source VERIFIED: Kdenlive (native OTIO import and export since 25.04), Affinity (now free with a Canva account; in-app JS scripting SDK), Kaiber (no public API), Mubert (paid, no free tier), Twitch (no upload API since Feb 2022), Leonardo.ai and Ideogram (paid per use), Dailymotion (free upload API).
- Corrected from one source and still marked UNVERIFIED: Rumble (upload API for Rumble PRO only), Audiomack (no public upload API found), Otter.ai (API for Enterprise only), Kapwing (no public REST API, plugin API only), Veed (public REST API exists).
- 38 of 138 tools now checked; 100 not yet checked.
- Data and docs only; no behavior changes.

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
