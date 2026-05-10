# Motion Specification — Cinematic Orbit System

## 1. Purpose

Defines HOW the system should FEEL in motion.

This is NOT optional.

Without this, the system becomes a UI instead of an experience.

---

## 2. Core Principle

This is NOT navigation.

This is:

→ Memory exploration in space

User perception must be:

- "I am moving through space"
- NOT "UI is changing"

---

## 3. Orbit Motion

### 3.1 Behavior

- Orbit rotation MUST be extremely subtle
- Speed: barely noticeable
- Purpose: ambient life, NOT interaction

### 3.2 Rule

User must NEVER feel like:
→ chasing a moving target

---

## 4. Node Interaction

### 4.1 Idle State

- Nodes are stable anchors
- Soft glow breathing effect

### 4.2 Hover / Tap

- Slight scale up (1.05–1.1)
- Glow intensifies
- Background dims slightly

---

## 5. Entering Memory (CRITICAL)

### 5.1 Required Illusion

User must feel:
→ being pulled INTO the node

---

### 5.2 Transition Sequence

1. Selected node becomes focal
2. Node scales up slightly
3. CameraWrapper scales IN toward node
4. Orbit fades + blurs progressively
5. Background depth increases
6. Memory content emerges aligned with node position

---

### 5.3 Timing

Total duration: 700–900ms

- Phase 1 (focus): 150ms
- Phase 2 (zoom): 400ms
- Phase 3 (content emerge): 200–300ms

---

## 6. Memory State

### 6.1 Orbit

- Still visible
- Heavily blurred
- Lower opacity

### 6.2 Depth

- Foreground: sharp (memory)
- Background: soft (orbit)

---

## 7. Lateral Navigation

### 7.1 Behavior

- Smooth cross-transition
- No reset to orbit

### 7.2 Motion

- Slight horizontal slide
- Maintain depth illusion

---

## 8. Exit / Reset

### 8.1 Back

- Reverse of enter animation

### 8.2 Reset

- Full zoom OUT
- Orbit returns to clarity
- Rotation resumes

---

## 9. Forbidden Patterns

DO NOT:

- use instant fade-in panels
- use modal-like popups
- snap between states
- break spatial continuity

---

## 10. Validation

System is correct ONLY IF:

- User feels movement in space
- Node feels like entry point
- Transition is directional
- No UI popping behavior exists

---

## 11. Summary

Bad:
→ UI switching

Good:
→ Spatial storytelling
