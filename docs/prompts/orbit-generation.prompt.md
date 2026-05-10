# Orbit Generation Prompt — Cinematic Orbit System (v3.1 Strict Execution Mode)

## Purpose
Deterministic execution prompt. Codex MUST behave as a renderer, not a designer.

---

Repository:
https://github.com/michaelmnc23/AI_SOURCE

Use this repository as the single source of truth.

---

## ZERO ENVIRONMENT ASSUMPTION (CRITICAL)

All required files exist locally in the repository.

DO NOT:
- fetch external resources
- reconstruct missing specs
- assume missing files

If a file is not found:
→ STOP and do not proceed

---

## REQUIRED FILES

### System Behavior
- /docs/system/codex-behavior.md

### Architecture
- /docs/ui/orbit-system.md
- /docs/scene-architecture.md

### Visual + Layout
- /docs/ui/orbit-visual-spec.md
- /docs/ui/orbit-layout-spec.md
- /docs/ui/color-system.md

### Data
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

## ENVIRONMENT RULES

Do NOT install or modify dependencies.
Assume environment is pre-configured.

Do NOT generate or substitute image/audio assets.
Use ONLY paths defined in data-contract.md

---

## DATA RULE

- All content MUST come from data-contract.md
- NO hardcoded text, images, or audio
- Use root-relative asset paths ("/images/...", "/audio/...")

Compute initials dynamically:

const initials = `${personA[0]} & ${personB[0]}`

---

## ORBIT BEHAVIOR RULE

Orbit is NOT a menu.

It is a passive spatial system.

- rotation: extremely subtle or near-static
- interaction: node-focused
- experience: emotional, not functional

---

## CINEMATIC MOTION REQUIREMENT (CRITICAL)

The system MUST feel like spatial navigation, NOT UI switching.

Orbit behavior:
- rotation must be extremely slow or near-static
- user must NOT feel like chasing moving targets

Memory transition MUST simulate "entering a memory":

Required sequence:

1. Selected node becomes focal point
2. Node slightly scales up
3. CameraWrapper zooms IN toward node (scale increase)
4. Background orbit fades and blurs progressively
5. Node visually anchors the transition
6. Memory content emerges FROM the node direction

FORBIDDEN:
- instant panel appearance
- modal-like behavior
- independent UI popups

The transition must preserve spatial continuity.

---

## REQUIRED OUTPUT STRUCTURE

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

## MOTION VALIDATION (MANDATORY)

Before output, verify:

- User does NOT need to chase nodes
- Transition feels directional (not fade-based)
- Memory appears connected to selected node
- Orbit remains present but de-emphasized

If NOT:
→ Fix before output

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

Precision over creativity.
