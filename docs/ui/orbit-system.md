# Orbit System (UI Core)

## 1. Concept
The Orbit System is the **primary interaction gateway** of the UI.
It starts as a focused, minimal centerpiece and expands into a split-layout experience upon interaction.

---

## 2. Layout States

### State A — Idle (Initial)
- Orbit position: center (50% x, 50% y)
- Orbit scale: 1
- Background: fully visible (cinematic)
- Main card: not rendered
- User focus: orbit only

---

### State B — Activated (After Click)
- Orbit moves to left side
- Orbit final position: x = 20% viewport width, y = 50%
- Orbit scale: 0.85
- Main card appears on right
- Main card position: x = 65% viewport width

---

## 3. Animation Timeline

### Trigger
- Event: user click on orbit

### Sequence
1. Orbit scale down slightly (1 → 0.9)
   - duration: 150ms
   - easing: ease-out

2. Orbit translate to left
   - duration: 600ms
   - easing: cubic-bezier(0.4, 0, 0.2, 1)

3. Main card fade + slide in
   - delay: 300ms (starts mid orbit movement)
   - duration: 500ms
   - opacity: 0 → 1
   - translateX: +40px → 0

---

## 4. Orbit Behavior

- Orbit consists of multiple nodes rotating around a center
- Rotation must be continuous and smooth
- Speed: slow (non-distracting)

### Constraints
- Nodes must never collide
- Maintain equal spacing between nodes
- Rotation must not break during layout transition

---

## 5. State Machine

States:
- IDLE
- TRANSITIONING
- ACTIVE

Transitions:
- IDLE → TRANSITIONING (on click)
- TRANSITIONING → ACTIVE (after animation complete)

Rules:
- No re-trigger during TRANSITIONING
- Clicking again in ACTIVE state can be defined later

---

## 6. Responsiveness

Desktop:
- Use horizontal split (orbit left, card right)

Mobile:
- Orbit stays top center
- Main card appears below
- Animation becomes vertical (top → center stack)

---

## 7. Visual Rules

- Orbit must remain the visual anchor
- Main card must not overpower orbit
- Maintain cinematic spacing (no cramped layout)

---

## 8. Future Extensions

- Multiple orbit nodes as navigation
- Dynamic content loading per node
- Reverse animation (back to center)

---

## 9. Implementation Notes (for Codex)

- Use transform (translate/scale) instead of absolute positioning when possible
- Avoid layout thrashing
- Prefer CSS transitions or Framer Motion
- Ensure SSR safety (Next.js)

---

## 10. Open Questions

- What happens on second click?
- Should orbit control navigation between cards?
- Should animation be interruptible?
