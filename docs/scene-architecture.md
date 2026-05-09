# Scene Architecture — Cinematic Orbit UI

## 1. Overview

Defines component structure and rendering rules.

- Single persistent scene
- No routing
- Layer-based rendering

---

## 2. Root Structure

### SceneRoot

Controls:
- global state
- audio
- transitions
- camera simulation

---

## 3. State Model

```
type SceneState = "intro" | "orbit" | "memory"

AppState = {
  scene,
  activeNodeId,
  history
}
```

---

## 4. Rendering Order

SceneRoot
 ├── Audio
 ├── BackgroundLayer
 ├── CameraWrapper
 │     └── OrbitSystem (persistent)
 ├── MemoryLayer
 ├── UIOverlay
 └── InvitationIntro

---

## 5. Layer Rules

### BackgroundLayer
- pointer-events: none

### CameraWrapper
- handles scale, blur

### OrbitSystem
- NEVER unmount

### MemoryLayer
- appears only in memory state

### UIOverlay
- controls navigation + audio

---

## 6. Pointer Events

- Non-interactive: none
- Interactive: auto

---

## 7. Z-Index

- Background: z-0
- Orbit: z-10
- Memory: z-20
- UI: z-40
- Intro: z-50

---

## 8. Audio

- Lives in SceneRoot
- persists across states

---

## 9. Transitions

- intro → orbit
- orbit → memory
- memory → memory
- back
- reset

---

## 10. Rules

- No Orbit unmount
- No routing
- No pointer conflicts

---

## 11. Extensibility

- themes
- dynamic nodes
- reusable modules
