# CODEX EXECUTION PROMPT — v2 (PIXEL + MOTION LOCKED, SELF-CONTAINED)

## ROLE
You are a deterministic renderer.

You DO NOT design.
You DO NOT infer.
You DO NOT improvise.

You EXECUTE exactly what is defined.

---

## AGENTS.md (MUST CREATE)

Create `/AGENTS.md` with the following content:

# AGENTS.md

## Rules
- No design decisions allowed
- No layout changes
- No spacing changes
- No color changes
- No asset invention beyond defined placeholders
- No external fetching

## System
- Single scene only
- OrbitSystem NEVER unmounts
- Audio MUST persist

## Motion
- Must feel spatial, not UI
- No modal / popup behavior
- No instant transitions

## Data
- All content must come from local data module (see DATA MODULE below)
- Assets must use /public paths

Precision over creativity.

---

## SYSTEM TYPE

Cinematic spatial experience.
NOT a website.
NOT a dashboard.

User explores memories in space.

---

## STATE MODEL

type SceneState = "intro" | "orbit" | "memory"

type AppState = {
  scene: SceneState
  activeNodeId: string | null
  history: string[]
}

---

## RENDER TREE (LOCKED)

SceneRoot
 ├── Audio (persistent)
 ├── BackgroundLayer
 ├── CameraWrapper (controls scale/blur)
 │     └── OrbitSystem (NEVER unmount)
 ├── MemoryLayer
 ├── UIOverlay
 └── InvitationIntro (conditional)

---

## ORBIT LAYOUT (PIXEL LOCKED)

- Total nodes: 5
- Radius: 220px (desktop), 160px (mobile)
- Center: exact viewport center

Angles (degrees):
- couple: 270°
- story: 342°
- gallery: 54°
- event: 126°
- interaction: 198°

Position formula:
x = cos(angle) * radius
y = sin(angle) * radius

MUST be mathematically correct.
NO visual approximation.

---

## CENTER CORE (LOCKED)

- Size: 140px
- Perfect circle
- Strongest glow in entire scene

Glow layers:
1. inner: solid warm gold
2. mid: radial gradient (gold → transparent)
3. outer: blurred bloom

Dynamic initials:
const initials = `${personA[0]} & ${personB[0]}`

---

## NODE DESIGN (LOCKED)

- Size: 64px
- Shape: circle
- Glow intensity: medium

Idle:
- scale: 1
- subtle breathing (1 → 1.03)

Hover / Tap:
- scale: 1.08
- glow increases

---

## COLOR SYSTEM (LOCKED)

Background:
- #0F0E0D (base)
- gradient to #1A1715

Primary Glow:
- #D6A85A

Secondary:
- #F2D7A1

Text:
- #FFFFFF (primary)
- #CFCFCF (secondary)

NO deviation allowed.

---

## ORBIT BEHAVIOR (LOCKED)

- rotation duration: 120s per full rotation
- linear easing
- MUST feel almost static

User must NOT chase nodes.

---

## CAMERA SYSTEM (CRITICAL)

CameraWrapper controls:

- scale
- blur
- opacity (optional)

OrbitSystem MUST NOT contain camera logic.

---

## MEMORY TRANSITION (MOTION LOCKED)

Total duration: 800ms

Phase 1 (0–150ms):
- clicked node scale: 1 → 1.1
- other nodes dim

Phase 2 (150–600ms):
- CameraWrapper scale: 1 → 1.15
- Orbit blur: 0px → 12px
- Orbit opacity: 1 → 0.3

Phase 3 (600–800ms):
- MemoryLayer enters FROM node direction
- translate: 20–40px from node vector
- fade + scale in

---

## MEMORY STATE

- Orbit still visible (blurred)
- Depth layering required:
  - Memory: sharp
  - Orbit: soft

---

## DATA MODULE (INLINE, NO EXTERNAL REFERENCE)

You MUST create a local file:

/lib/data.ts

Use THIS EXACT structure and placeholder data:

export const data = {
  couple: {
    personA: "Aurelia",
    personB: "Rory"
  },
  story: [
    { title: "First Meet", description: "We met unexpectedly." },
    { title: "Falling in Love", description: "Moments became memories." }
  ],
  gallery: [
    "/images/gallery1.jpg",
    "/images/gallery2.jpg",
    "/images/gallery3.jpg"
  ],
  event: {
    date: "2026-12-12",
    location: "Jakarta"
  },
  audio: "/audio/bg-music.mp3"
}

---

## ASSETS (PLACEHOLDER RULE)

You MUST create placeholder assets in:

/public/images/
/public/audio/

Examples:
- /public/images/gallery1.jpg
- /public/audio/bg-music.mp3

These can be empty or dummy files.

DO NOT fetch external assets.

---

## AUDIO

- starts ONLY after user interaction
- auto loop
- persists across state changes
- controlled via useRef

---

## OUTPUT STRUCTURE

/app
/components/scene
/lib/data.ts
/styles/globals.css
/public/images
/public/audio

---

## VALIDATION (MUST PASS ALL)

- Pixel layout matches spec
- Orbit perfectly radial
- No hardcoded content outside data module
- Motion is directional
- Memory emerges from node
- Orbit never unmounts
- Audio persists

IF ANY FAILS → FIX BEFORE OUTPUT

---

## FINAL DIRECTIVE

You are rendering a system, not building UI.

Precision over creativity.
