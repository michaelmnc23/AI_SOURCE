# Orbit Generation Prompt — Cinematic Orbit System (v3 Strict Execution Mode)

## Purpose

Deterministic execution prompt. Codex MUST behave as a renderer, not a designer.

---

Repository:
https://github.com/michaelmnc23/AI_SOURCE

Use this repository as the single source of truth.

---

## REQUIRED FILES

### System Behavior (HOW to behave)
- /docs/system/codex-behavior.md

### Architecture (HOW it is built)
- /docs/ui/orbit-system.md
- /docs/scene-architecture.md

### Visual + Layout (HOW it looks)
- /docs/ui/orbit-visual-spec.md
- /docs/ui/orbit-layout-spec.md
- /docs/ui/color-system.md

### Data (WHAT it renders)
- /docs/data/data-contract.md

---

## EXECUTION MODE

You are a deterministic renderer.

DO NOT:
- invent layout values
- change spacing, sizes, or positions
- introduce new components not required by specs
- refactor architecture
- rename variables arbitrarily
- add libraries beyond Next.js + React + Framer Motion

ONLY:
- implement exactly what specs define

---

## DATA RULE

- All content MUST come from data-contract.md
- NO hardcoded text, images, or audio
- Use root-relative asset paths ("/images/...", "/audio/...")
- Compute initials dynamically:

const initials = `${personA[0]} & ${personB[0]}`

---

## REQUIRED OUTPUT STRUCTURE

You MUST generate this structure:

/app
  /page.tsx
  /layout.tsx
/components
  /scene/SceneRoot.tsx
  /scene/BackgroundLayer.tsx
  /scene/OrbitSystem.tsx
  /scene/OrbitNode.tsx
  /scene/MemoryLayer.tsx
  /scene/UIOverlay.tsx
  /scene/InvitationIntro.tsx
/lib
  /data.ts
/styles
  /globals.css

Rules:
- Follow scene-architecture.md exactly
- OrbitSystem MUST NEVER unmount
- Audio MUST live in SceneRoot

---

## ANIMATION RULE

- Use Framer Motion
- Separate transforms (rotation / scale / translate)
- No combined transforms on same element

---

## VALIDATION (MANDATORY)

Before output, verify ALL:

1. Layout is pixel-exact to orbit-layout-spec
2. Colors match color-system
3. Glow uses layered effects
4. Orbit is perfectly radial (math-based)
5. Depth uses blur + scale + z-index
6. Data is fully dynamic
7. Audio uses data.audio and persists

If ANY fails:
→ FIX before output

---

## OUTPUT RULE

- Return FULL working code
- NO explanation
- NO comments unless necessary
- NO partial output

---

## FAILURE CONDITION

If specs are unclear:
→ DO NOT guess
→ choose the most literal interpretation from docs

---

## FINAL DIRECTIVE

This is strict execution.

Precision over creativity.
