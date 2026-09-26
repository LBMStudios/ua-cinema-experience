# UA CINEMA MOTION & PROGRAMMATIC VIDEO ENGINE
### PROGRAMMATIC VIDEO GENERATION FOR THEATRICAL SCREENS & VERTICAL TOTEMS
`UNIVERSAL ASSISTANCE (A COMPANY OF ZURICH)` · `LBM STUDIOS ARCHIVE`

```text
┌─────────────────────────────────────────────────────────────────────────┐
│ PROJECT:    UA CINEMA MOTION & PROGRAMMATIC VIDEO ENGINE                │
│ CLIENT:     UNIVERSAL ASSISTANCE (A COMPANY OF ZURICH)                  │
│ EVENT:      CINEMA PREMIERE — THEATRICAL SCREENS & VERTICAL TOTEMS      │
│ ROLE:       CREATIVE TECHNOLOGIST & MOTION SYSTEMS ARCHITECT            │
│ STACK:      REMOTION · REACT 19 · TYPESCRIPT · WEBAUDIO · FFMPEG        │
│ STATUS:     PRODUCTION VERIFIED (THEATRICAL SCREEN PLAYBACK)            │
└─────────────────────────────────────────────────────────────────────────┘
```

---

## 01 // OVERVIEW & MOTION ARCHITECTURE

A programmatic video generation engine developed with **Remotion** for **Universal Assistance (A company of ZURICH)**. 

Designed to automate the generation of motion assets for theatrical brand activations (e.g. *Coyote vs. Acme* premiere):
1. **Theatrical Screen Composition (16:9 - 1920 × 1080):** High-impact animated case study video played in theatre auditoriums prior to feature presentation.
2. **Vertical Lobby Totem Composition (9:16 - 1080 × 1920):** Continuous motion loop for digital totems in cinema lobbies and entrance corridors.
3. **Dynamic Synthetic Voiceover Integration:** Automated synchronization of Rioplatense regional Spanish voice tracks (`generate_rioplatense_audio.js`) aligned to frame-accurate kinetic typography.
4. **Programmatic Data Injection:** Directly renders animated event metrics (guest counts, partner sponsor tags, QR accreditation counters) from raw JSON data.

```
[ EVENT METADATA / STATS ] ──▶ [ REMOTION ENGINE ] ──▶ [ HARDWARE RENDER ] ──▶ [ CINEMA DCI / TOTEMS ]
  (JSON / Audio Stems)          (React Canvas)            (H.264 / 60fps)         (1080p / 4K Playback)
```

---

## 02 // TECHNICAL MATRIX

| Dimension | Specification |
|:---|:---|
| **Video Engine** | Remotion 4.x + React 19 |
| **Language** | TypeScript |
| **Compositions** | `CaseStudyVideo` (1920×1080, 60fps), `CaseStudyVerticalVideo` (1080×1920, 60fps) |
| **Audio Synthesis** | Node.js localized audio generator with frame-level duration calculation |
| **Typography & Palette** | Universal Assistance Brand System (Deep Navy, Corporate Cyan, Signal White) |
| **Output Target** | Hardware-accelerated H.264 / ProRes for broadcast displays |

---

## 03 // QUICK START & RENDERING

```bash
# 1. Install dependencies
npm install

# 2. Launch Remotion interactive preview player
npm run start

# 3. Render 16:9 Theatrical Composition
npx remotion render src/index.ts CaseStudy out/cine_1080p.mp4

# 4. Render 9:16 Vertical Totem Composition
npx remotion render src/index.ts CaseStudyVertical out/totem_1080x1920.mp4
```

---

## 04 // REPOSITORY STRUCTURE

```text
├── src/
│   ├── components/              # Animated kinetic title cards, brand frames, metrics
│   ├── CaseStudyVideo.tsx       # 16:9 Theatrical auditorium sequence
│   ├── CaseStudyVerticalVideo.tsx # 9:16 Vertical totem lobby sequence
│   ├── constants.ts             # Brand colors, durations, aspect ratios
│   ├── Root.tsx                 # Remotion composition registry
│   └── index.ts                 # Video entrypoint
├── generate_rioplatense_audio.js # Regional audio stem synthesis pipeline
├── generate_expanded_voice.js   # Scripted narration timing generator
├── package.json
└── tsconfig.json
```

---

```text
© 2026 LBM STUDIOS // LUCAS BEATHYATE MASCHERINI. ALL RIGHTS RESERVED.
DEVELOPED FOR UNIVERSAL ASSISTANCE (A COMPANY OF ZURICH).
```