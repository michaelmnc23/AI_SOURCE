# CODEX EXECUTION PROMPT — FULLY INLINED (v1.0)

## ROLE
You are a deterministic renderer.

You DO NOT design.
You DO NOT infer.
You DO NOT improvise.

You EXECUTE exactly what is defined below.

---

## AGENTS.md (MUST CREATE IN PROJECT ROOT)

Create file:
/AGENTS.md

Content:

- This project follows a deterministic UI system
- No design decisions allowed during implementation
- All UI/UX must follow provided execution prompt
- Do not introduce new patterns, layouts, or styles
- Do not fetch external assets
- All assets must use /public paths

---

## SYSTEM OVERVIEW

This is a cinematic wedding invitation.

It is NOT a website.
It is a spatial experience.

User explores memories through orbiting nodes.

---

## CORE PRINCIPLES

- No routing
- Single scene
- Persistent orbit
- Camera illusion using scale/blur
- Emotional pacing over functionality

---

## STATE MODEL

SceneState = "intro" | "orbit" | "memory"

AppState:
- scene
- activeNodeId
- history[]

---

## LAYER ARCHITECTURE

Render order:

1. BackgroundLayer
2. CameraWrapper
   - OrbitSystem (NEVER unmount)
3. MemoryLayer
4. UIOverlay
5. InvitationIntro

---

## POINTER RULES

- Non-interactive: pointer-events none
- Interactive: pointer-events auto

---

## ORBIT SYSTEM

Nodes:
- couple
- story
- gallery
- event
- interaction

Layout:
- radial
- evenly spaced
- mathematically positioned

Rotation:
- extremely slow
- almost static

---

## MOTION SPEC

Entering memory MUST:

1. Node becomes focal
2. Node scales up
3. Camera zooms in
4. Orbit blurs + fades
5. Memory emerges from node direction

Duration: ~800ms

FORBIDDEN:
- instant panels
- modal behavior

---

## VISUAL SYSTEM

Color palette:
- Background: deep brown/black
- Primary glow: warm gold
- Accent: soft champagne

Glow:
- layered radial gradients
- soft bloom effect

---

## CENTER CORE

- circular
- glowing strongest
- displays initials dynamically

Initials:
first letter of each name

---

## DATA CONTRACT

All content must come from data object:

- couple names
- story timeline
- gallery images
- event info
- audio path

Paths:
/images/...
/audio/...

---

## AUDIO

- starts after user interaction
- loops
- persists

---

## OUTPUT STRUCTURE

/app
/components/scene
/lib/data.ts
/styles

---

## VALIDATION

Ensure:

- no hardcoded content
- orbit never unmounts
- motion is directional
- UI matches cinematic behavior

---

## FINAL RULE

Precision over creativity.
