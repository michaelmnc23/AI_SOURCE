# Orbit Visual Specification — Cinematic System

## 0. Reference Mockup

Primary visual reference:

`/public/mockups/orbit-system-overview.png`

All visual decisions MUST align with this image.

Section mapping:
- Top-left → Orbit idle state
- Top-right → Entering memory transition
- Bottom-left → Story memory layout
- Bottom-middle → Gallery memory layout
- Bottom-right → Other nodes / cards

---

## 1. Visual Intent

The UI must feel:
- cinematic
- warm
- romantic
- soft but luminous

Avoid flat UI. Everything should feel layered and glowing.

---

## 2. Color System

### Primary
- Gold glow: #F5C27A (range allowed)

### Background
- Deep brown → near black gradient
- No flat colors

### Text
- Off-white (slightly warm)
- Avoid pure white

### Accents
- Soft orange / amber highlights

---

## 3. Lighting Model

- Central light source from orbit core
- All elements subtly affected by this light
- Use radial gradients for glow

---

## 4. Orbit Composition

- Two orbit rings (inner + outer)
- Thin glowing strokes
- Soft blur applied
- Small light particles distributed along path

---

## 5. Center Core

- Circular glowing element
- Contains initials (A & R equivalent)
- Strongest brightness in scene
- Radial gradient outward

---

## 6. Node Design

Each node:
- Circular image thumbnail
- Gold glowing border
- Soft bloom (outer glow)
- Label text outside node

### States

Idle:
- soft glow
- stable scale

Hover:
- scale up (~1.1–1.15)
- brighter glow

Active:
- strongest glow
- slightly larger scale

---

## 7. Depth System

Layer separation is REQUIRED:

Foreground:
- nodes (sharp)

Midground:
- orbit rings (slightly blurred)

Background:
- particles (heavily blurred)

---

## 8. Particle System

- slow floating motion
- subtle randomness
- varying opacity
- no sudden movement

---

## 9. Memory Transition Visuals

When entering memory:

- selected node emits particle trail
- camera zooms inward
- background blur increases
- orbit fades but remains visible

---

## 10. Memory UI

### Story View (Bottom-left of mockup)
- large rounded image
- soft glow border
- text on right
- timeline below

### Gallery View (Bottom-middle of mockup)
- centered main image
- side images blurred
- navigation arrows

---

## 11. UI Elements

- minimal
- gold outlined buttons
- subtle hover glow

---

## 12. Motion Tone

- slow
- smooth
- easeInOut
- no abrupt transitions

---

## 13. Anti-Patterns

DO NOT:
- use flat colors
- use harsh shadows
- use sharp edges everywhere
- create static feeling UI

---

## 14. Guiding Principle

This is not UI.

This is:
> a glowing, living memory space
