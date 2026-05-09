# Orbit System — Cinematic Interaction Specification

## 1. Overview

The Orbit System is the primary navigation mechanism of the cinematic wedding invitation.

It replaces traditional scrolling with an interactive, spatial exploration model where users navigate content by interacting with orbiting nodes.

This system is designed to feel:
- immersive
- fluid
- emotionally paced
- cinematic rather than functional

---

## 2. Core Principles

### 2.1 Persistent World

- The orbit system MUST NEVER unmount
- It exists as a continuous spatial layer
- Even when entering memory, it remains visible (blurred and de-emphasized)

### 2.2 Camera Illusion (No Real Camera)

All transitions simulate a camera using:
- scale
- blur
- opacity
- slight translation

No actual 3D camera is used.

---

## 3. Node System

### 3.1 Node Definitions

There are exactly 5 primary nodes:
- couple
- story
- gallery
- event
- interaction

### 3.2 Spatial Layout

- Nodes are positioned radially using fixed angles
- Orbit rotates slowly during idle state
- Rotation MUST be visually smooth and continuous

### 3.3 Interaction Model

Each node:
- is individually clickable
- has hover/tap feedback (scale + glow)
- triggers memory transition

---

## 4. Layer Architecture (CRITICAL)

### 4.1 Background Layer
- gradient + particles
- pointer-events: none

### 4.2 Orbit Visual Layer
- handles rotation animation
- pointer-events: none

### 4.3 Orbit Interaction Layer
- contains clickable nodes
- pointer-events: auto

### 4.4 Memory Layer
- floating content panel
- appears above orbit

### 4.5 UI Overlay
- navigation controls (back, reset, arrows, audio)

---

## 5. State Machine

States:
- intro
- orbit
- memory

Rules:
- intro: orbit hidden
- orbit: nodes interactive
- memory: orbit paused + blurred

---

## 6. Transition System

### 6.1 Intro → Orbit
1. User taps invitation
2. Intro dissolves into particles
3. Particles expand outward
4. Orbit nodes form from particles
5. Orbit fades into clarity

### 6.2 Orbit → Memory
1. Rotation pauses
2. Node scales slightly
3. Camera zoom (scale: 1.1–1.2)
4. Background blur increases
5. Memory panel appears LAST

Duration: 700–800ms

### 6.3 Memory Navigation
- Lateral navigation between nodes
- No return to orbit required
- History stack updated

### 6.4 Back Behavior
- Returns to previous node
- If no history → orbit state

### 6.5 Reset
- Clears history
- Returns to orbit
- Camera zooms out
- Rotation resumes

---

## 7. Memory Layer

### Presentation
- Floating panel (right desktop, center mobile)
- Slide + fade animation

### Content Mapping
- couple → intro
- story → timeline
- gallery → media
- event → details
- interaction → RSVP / wishes / gift

---

## 8. Audio Integration

- Starts after user interaction
- Default ON
- Looping
- Smooth fade in/out
- MUST persist across transitions

---

## 9. Mobile Constraints

- Tap-based interaction only
- 60fps target

---

## 10. Anti-Patterns

- Do NOT unmount OrbitSystem
- Do NOT use routing
- Do NOT block pointer events incorrectly
- Do NOT use instant transitions

---

## 11. Extensibility

- Theme swapping
- Dynamic node count
- Reusable content modules
