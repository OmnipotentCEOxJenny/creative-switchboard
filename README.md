# Creative Switchboard

![Creative Switchboard logo](assets/logo.png)

Creative Switchboard is a free switchboard that routes projects between creative tools: video editing, audio, music generation, image generation, animation and 3D, design, voiceover and subtitles, mastering and more. It moves work through open formats (OTIO, FCPXML, AAF, EDL, WAV and others), a Dropbox hub and each vendor's official, allowed methods. Social platforms are only downstream posting targets; the switchboard works upstream, between the tools where the work is made.

Think of it like a surge protector for creative software, worded truthfully: open formats and local files need no vendor permission, while cloud tools connect only through your own sign-in and the vendor's official methods.

## Project status: done, pending, uncertain
**Done**
- 2026-10-15: v1.0.1 adds Google and Meta tools back to the allowlist (not yet checked).
- 2026-10-15: v1.0.0 built and tested (manifest, frontmatter, file links, skill and example consistency).
- 2026-10-15: allowlist of 138 tools in 10 categories; 25 checked against vendor docs, a second source or a connected connector.

**Pending**
- 113 tools are not yet checked; verify each against the vendor's docs before relying on it.
- Cloud tools need the user's own sign-in (OAuth or API key); nothing connects without it.
- Vimeo (free accounts need manual upload-access approval, up to 5 business days) and TikTok (unaudited apps post privately only; public posting needs an audit) have review delays.
- DaVinci Resolve scripting and its MCP server need the paid Studio version (21.1). Premiere Pro and Final Cut Pro are export-only routes (files, not live control).
- CapCut: no public API found. SoundCloud: API needs the paid Artist Pro plan. Spotify: no upload API (distributors only).
- Runway, Krea and ElevenLabs generation spends credits; never run without approval.
- Ableton Live: not checked. Lighting, camera, SFX library, mastering and instrument tools: not yet researched.
- Marketplace: not yet submitted.

**Uncertain**
- X API: possibly pay-per-use for new developers; not confirmed on X's own docs.
- DaVinci Resolve OTIO import: not confirmed in the Resolve manual.
- How the listing works on the Grok Bot and Grok side: not described in the publisher terms.


## Quick start
1. Install (see Installation).
2. Ask: "Move my Premiere timeline to DaVinci Resolve and send the dialogue to Audacity."
3. Get a route (most open method first), the steps, a verification of the result, and a list of anything lost or unchecked.

## Credits
- Inventor and publisher: Rob Domaine / Omnipotent Media LLC
- Builder: Jenny Echo

## Rob Domaine's four pillars
1. Trustworthy, honest, real data, truthful: never invent; anything unchecked is marked UNVERIFIED.
2. Use only legitimate means: legitimate, proven sources and methods; unreliable sources rejected.
3. Double-check everything: every finding is confirmed by two independent checks, and the report shows both.
4. Stay within the law and rules always: local, county, state, federal and platform rules.

## Components
- `skills/route-creative-project`: plans and runs a transfer, most open route first, and verifies the result.
- `skills/convert-timeline`: converts timelines with the free OpenTimelineIO tools and reports what survives.
- `skills/route-creative-project/references/allowlist.csv`: the full allowlist with methods, formats, paid-plan needs, terms limits, blockers and verification status.
- `rules/pillars-and-scope.mdc`: the pillars and scope.
- `examples/sample-route.md`: a planning example.

## Allowlist (138 tools; checked vs not yet checked)

### Video editing (16)
| Tool | Method | Status |
|---|---|---|
| DaVinci Resolve | Y: Python/Lua scripting + MCP server (21.1), Studio only | checked |
| Adobe Premiere Pro | Y: UXP plugins; exports FCPXML, AAF, OTIO | checked |
| Final Cut Pro | Y: FCPXML, Workflow Extensions, Apple Events | checked |
| iMovie | N: no public API known; exports to Final Cut | not yet checked |
| CapCut | N: no public editing API found | not yet checked |
| Avid Media Composer | partial: SDKs for partners | not yet checked |
| Kdenlive | partial: open source, MLT XML projects | not yet checked |
| Shotcut | partial: open source, MLT XML | not yet checked |
| OpenShot | Y: libopenshot Python API | not yet checked |
| Lightworks | partial | not yet checked |
| VEGAS Pro | Y: scripting API (C#) | not yet checked |
| HitFilm | N | not yet checked |
| Descript | partial: limited API | not yet checked |
| Clipchamp | N: Microsoft, no public API known | not yet checked |
| Filmora | N | not yet checked |
| Frame.io (review) | Y: V4 REST API, OAuth via Adobe IMS | checked |

### Audio production / DAWs (14)
| Tool | Method | Status |
|---|---|---|
| Audacity | Y: mod-script-pipe (named pipes), ships with app | checked |
| Ableton Live | partial: Max for Live (Suite), unofficial remote scripts | not yet checked |
| REAPER | Y: ReaScript (Lua, Python, EEL) | not yet checked |
| Logic Pro | partial: Scripter MIDI JS only | not yet checked |
| GarageBand | N | not yet checked |
| FL Studio | partial: MIDI scripting (Python) | not yet checked |
| Pro Tools | partial: scripting SDK for partners | not yet checked |
| Cubase / Nuendo | partial: MIDI remote API | not yet checked |
| Bitwig Studio | partial: controller scripting API (JS) | not yet checked |
| Ardour | Y: Lua scripting, open source | not yet checked |
| LMMS | partial: open source | not yet checked |
| Studio One | partial | not yet checked |
| BandLab | N: no public API known | not yet checked |
| Adobe Audition | partial: CEP/ExtendScript (legacy) | not yet checked |

### Music generation (10)
| Tool | Method | Status |
|---|---|---|
| Suno | Y: official API at platform.suno.com | checked |
| Udio | N: no public API (Udio help center) | checked |
| Stable Audio | Y: Stability API | not yet checked |
| ElevenLabs Music | Y: ElevenLabs API (connected) | checked |
| Mubert | Y: API for business | not yet checked |
| Soundraw | partial: API for partners | not yet checked |
| AIVA | N | not yet checked |
| Boomy | N | not yet checked |
| Beatoven.ai | partial: API | not yet checked |
| Loudly | partial: API | not yet checked |

### Image generation (13)
| Tool | Method | Status |
|---|---|---|
| Midjourney | N: no API; automation prohibited (ToS and guidelines) | checked |
| Stability AI (SD) | Y: REST API | checked |
| Krea | Y: connected connector | checked |
| Adobe Firefly | Y: Firefly Services API | not yet checked |
| Leonardo.ai | Y: API | not yet checked |
| Ideogram | Y: API | not yet checked |
| OpenAI image models | Y: API | not yet checked |
| Google Imagen / Gemini | Y: Gemini API (Imagen) | not yet checked |
| Meta AI image | N: no public image API known | not yet checked |
| Grok Imagine (xAI) | Y: xAI API | not yet checked |
| Recraft | Y: API | not yet checked |
| Playground | partial | not yet checked |
| ComfyUI (local) | Y: local HTTP API, open source | not yet checked |

### AI video (13)
| Tool | Method | Status |
|---|---|---|
| Runway | Y: connected connector | checked |
| Luma (Dream Machine/Ray) | Y: API, pay-as-you-go ($0.15+ per 5 s) | checked |
| Pika | Y: API, no free generation tier | checked |
| Krea video | Y: connected connector | checked |
| Kling | Y: API | not yet checked |
| Hailuo / MiniMax | Y: API | not yet checked |
| OpenAI Sora | Y: API | not yet checked |
| Google Veo | Y: Gemini API / Vertex AI | not yet checked |
| Synthesia | Y: API | not yet checked |
| HeyGen | Y: API | not yet checked |
| D-ID | Y: API | not yet checked |
| Haiper | partial | not yet checked |
| Kaiber | N | not yet checked |

### Animation / 3D / motion (14)
| Tool | Method | Status |
|---|---|---|
| Blender | Y: built-in Python API (bpy) | checked |
| Adobe After Effects | partial: ExtendScript/CEP (UXP in progress) | not yet checked |
| Cinema 4D | Y: Python SDK | not yet checked |
| Autodesk Maya | Y: Python/MEL | not yet checked |
| Houdini | Y: Python (hou) | not yet checked |
| Unreal Engine | Y: Python/Blueprint, Remote Control API | not yet checked |
| Unity | Y: C# Editor scripting | not yet checked |
| Spline | partial: API/export | not yet checked |
| Rive | partial: runtime APIs | not yet checked |
| LottieFiles | Y: API | not yet checked |
| Toon Boom Harmony | partial: scripting | not yet checked |
| Synfig | partial: open source | not yet checked |
| Moho | partial: Lua scripting | not yet checked |
| Adobe Animate | partial: JSFL | not yet checked |

### Graphics / design (12)
| Tool | Method | Status |
|---|---|---|
| Canva | Y: Connect API + Apps SDK (connected) | checked |
| Figma | Y: REST API, OAuth2 or tokens | checked |
| Adobe Photoshop | Y: UXP plugins; Photoshop API (Firefly Services) | not yet checked |
| Adobe Illustrator | partial: ExtendScript/UXP | not yet checked |
| Affinity apps | N: no public scripting known | not yet checked |
| GIMP | Y: Python-Fu scripting, open source | not yet checked |
| Inkscape | Y: extensions + CLI, open source | not yet checked |
| Krita | Y: Python scripting, open source | not yet checked |
| Photopea | partial: URL/JSON API | not yet checked |
| Sketch | partial: plugin API | not yet checked |
| Penpot | Y: API, open source | not yet checked |
| Adobe Express | partial: add-ons SDK | not yet checked |

### Subtitles / voice (12)
| Tool | Method | Status |
|---|---|---|
| ElevenLabs | Y: API (connected) | checked |
| Whisper (open source) | Y: local, open source (MIT) | not yet checked |
| Subtitle Edit | partial: CLI, open source | not yet checked |
| Aegisub | partial: Lua automation, open source | not yet checked |
| Rev | Y: API | not yet checked |
| Otter.ai | partial | not yet checked |
| AssemblyAI | Y: API | not yet checked |
| Deepgram | Y: API | not yet checked |
| Murf | Y: API | not yet checked |
| Resemble AI | Y: API | not yet checked |
| Kapwing | partial | not yet checked |
| Veed | partial | not yet checked |

### Storage / transfer hubs (11)
| Tool | Method | Status |
|---|---|---|
| Dropbox | Y: API (connected) | checked |
| Box | Y: API | not yet checked |
| OneDrive | Y: Microsoft Graph | not yet checked |
| Google Drive | Y: Drive API, user OAuth | not yet checked |
| iCloud Drive | N: no public file API | not yet checked |
| WeTransfer | partial: public API status not found | not yet checked |
| MASV | Y: API | not yet checked |
| pCloud | Y: API | not yet checked |
| MEGA | Y: SDK | not yet checked |
| Backblaze B2 | Y: S3-compatible API | not yet checked |
| Local disk / NAS | Y: file system | not yet checked |

### Export / distribution (23)
| Tool | Method | Status |
|---|---|---|
| Vimeo | Y: API upload, OAuth upload scope | checked |
| TikTok | Y: Content Posting API | checked |
| X | Y: API v2 media upload | not yet checked |
| SoundCloud | Y: API upload via OAuth | checked |
| Spotify for Artists | N: no upload API; distributors only | checked |
| Bandcamp | partial: API for labels/partners on request | checked |
| YouTube | Y: YouTube Data API upload, user OAuth | not yet checked |
| Instagram / Reels | Y: Instagram Graph API publishing (professional accounts) | not yet checked |
| Facebook | Y: Graph API video publishing to Pages | not yet checked |
| Threads | Y: Threads API publishing | not yet checked |
| Twitch | partial: API, no general VOD upload found | not yet checked |
| Dailymotion | Y: API | not yet checked |
| Rumble | N: no public upload API known | not yet checked |
| Apple Music | N: distributors only | not yet checked |
| Amazon Music | N: distributors only | not yet checked |
| DistroKid | N: no public API known | not yet checked |
| Audiomack | partial | not yet checked |
| LinkedIn | Y: API (approval) | not yet checked |
| Pinterest | Y: API (approval) | not yet checked |
| Bluesky | Y: AT Protocol, open | not yet checked |
| Mastodon | Y: open API | not yet checked |
| PeerTube | Y: open API | not yet checked |
| Archive.org | Y: S3-like API | not yet checked |

## Requirements
Free tools only by default (OpenTimelineIO, local apps, Dropbox free plan). No paid APIs required.

## Installation
Copy to `~/.cursor/plugins/local/creative-switchboard/`, or install from the marketplace once listed.

## Feedback and reviews
- Reviews and feedback: [Discussions](https://github.com/OmnipotentCEOxJenny/creative-switchboard/discussions)
- [Report a wrong route or tool fact](https://github.com/OmnipotentCEOxJenny/creative-switchboard/issues/new?template=wrong-route.md)
- [Feature request](https://github.com/OmnipotentCEOxJenny/creative-switchboard/issues/new?template=feature-request.md)

License: MIT.
