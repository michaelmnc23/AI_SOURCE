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

## 2. Data-Driven Design (CRITICAL)

This system is NOT static.

All visible content MUST be dynamically driven by data.

### Dynamic Elements

- Couple names
- Center initials
- Node labels
- Story text
- Images (gallery, thumbnails)
- Event details

### Rules

- NEVER hardcode text like "A & R"
- NEVER hardcode images
- ALWAYS derive from props / data source

---

## 3. Color System

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

## 4. Lighting Model

- Central light source from orbit core
- All elements subtly affected by this light
- Use radial gradients for glow

---

## 5. Center Core

- Circular glowing element
- Strongest brightness in scene
- Radial gradient outward

### Content (Dynamic)

- Displays initials derived from couple names

Example:
- Aurelia & Rory → A & R
- Michael & Nathaniel → M & N

### Rules

- MUST be computed dynamically
- MUST NOT be hardcoded
- Typography style remains constant

---

## 6. Orbit Composition

- Two orbit rings (inner + outer)
- Thin glowing strokes
- Soft blur applied
- Small light particles distributed along path

---

## 7. Node Design

Each node:
- Circular image thumbnail (dynamic)
- Gold glowing border
- Soft bloom (outer glow)
- Label text outside node (dynamic)

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

## 8. Depth System

Layer separation is REQUIRED:

Foreground:
- nodes (sharp)

Midground:
- orbit rings (slightly blurred)

Background:
- particles (heavily blurred)

---

## 9. Particle System

- slow floating motion
- subtle randomness
- varying opacity
- no sudden movement

---

## 10. Memory Transition Visuals

When entering memory:

- selected node emits particle trail
- camera zooms inward
- background blur increases
- orbit fades but remains visible

---

## 11. Memory UI

### Story View (Bottom-left of mockup)
- large rounded image (dynamic)
- soft glow border
- text on right (dynamic)
- timeline below (dynamic)

### Gallery View (Bottom-middle of mockup)
- centered main image (dynamic)
- side images blurred (dynamic)
- navigation arrows

---

## 12. UI Elements

- minimal
- gold outlined buttons
- subtle hover glow

---

## 13. Motion Tone

- slow
- smooth
- easeInOut
- no abrupt transitions

---

## 14. Anti-Patterns

DO NOT:
- use flat colors
- use harsh shadows
- use sharp edges everywhere
- create static feeling UI
- hardcode user content

---

## 15. Guiding Principle

This is not UI.

This is:
> a glowing, living memory space powered by dynamic data
