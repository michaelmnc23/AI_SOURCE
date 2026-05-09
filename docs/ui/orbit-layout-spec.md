# Orbit Layout Specification — Deterministic System

## 1. Purpose

This document defines **exact spatial, sizing, and proportional rules** for the orbit UI.

It ensures:
- pixel-consistent rendering
- mockup-level fidelity
- no visual guessing

---

## 2. Coordinate System

- Origin: center of viewport
- All orbit calculations are relative to center
- Use transform-based positioning (NOT top/left offsets for layout logic)

---

## 3. Core Layout Metrics

### 3.1 Center Core

- Size: 120px (desktop)
- Shape: perfect circle
- Position: exact center

### Glow:

- Inner glow radius: 60px
- Outer glow radius: 140px
- Opacity falloff: exponential

---

### 3.2 Orbit Rings

Two rings:

#### Inner Ring
- Radius: 160px
- Stroke width: 1.5px
- Opacity: 0.6
- Blur: 2px

#### Outer Ring
- Radius: 220px
- Stroke width: 1px
- Opacity: 0.4
- Blur: 3px

---

### 3.3 Nodes

- Count: 5 (default, must support dynamic)
- Size: 48px
- Shape: circle

### Positioning:

```ts
angle = (index / totalNodes) * 2π
x = cos(angle) * 190px
y = sin(angle) * 190px
```

- Node radius sits BETWEEN inner and outer ring

---

### 3.4 Node Label

- Offset from node: 12px outward (radial direction)
- Font size: 12px
- Opacity: 0.8

---

## 4. Depth System (Exact Values)

### Blur Layers

| Layer       | Blur  |
|------------|------|
| Nodes       | 0px  |
| Rings       | 2–3px |
| Background  | 8–16px |

---

### Scale Layers

| State   | Scale |
|--------|------|
| Idle    | 1.0  |
| Hover   | 1.12 |
| Active  | 1.25 |

---

## 5. Camera Simulation

### Orbit State

- scale: 1
- blur: 0px

### Memory State

- scale: 1.15
- blur: 4px
- opacity: 0.85

---

## 6. Spacing System

### Memory Panel (Desktop)

- Width: 420px
- Right margin: 80px
- Vertical center aligned

### Gap from orbit center → panel:

- ~120px minimum

---

## 7. Z-Index (Locked)

| Layer            | Value |
|------------------|------|
| Background       | 0    |
| Orbit            | 10   |
| Memory           | 20   |
| UI Overlay       | 40   |
| Intro            | 50   |

---

## 8. Motion Timing

### Rotation

- Duration: 40s
- Linear infinite

---

### Node Hover

- Duration: 0.2s
- Ease: easeOut

---

### Orbit → Memory

- Total: 700–800ms

Breakdown:
- 0–300ms: scale + blur
- 300–700ms: panel enters

---

## 9. Glow System (IMPORTANT)

### Node Glow

- Spread: 12px
- Color: gold
- Opacity: 0.6 (idle), 1 (active)

---

### Core Glow

- Strongest in scene
- Must visually dominate nodes

---

## 10. Responsiveness Rules

### Mobile

- Scale entire system: 0.75
- Orbit radius reduces proportionally
- Memory panel becomes centered

---

## 11. Constraints (STRICT)

DO NOT:

- change sizes arbitrarily
- use percentage-based layout for orbit
- break radial positioning math
- let content affect layout size

---

## 12. Deterministic Principle

This system must:

- render IDENTICALLY across sessions
- not depend on content size
- not shift based on text length

---

## 13. Relationship to Other Docs

- orbit-system.md → behavior
- scene-architecture.md → structure
- orbit-visual-spec.md → styling
- THIS FILE → exact layout

---

## 14. Final Rule

If visual output differs from mockup:

→ layout spec is the source of correction
