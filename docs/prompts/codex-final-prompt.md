# Codex Final Prompt — Cinematic Orbit System

## Purpose

This prompt is the SINGLE authoritative prompt used to generate the UI.
It MUST be updated whenever any system rule changes.

---

## Prompt

Repository:
https://github.com/michaelmnc23/AI_SOURCE

Use this repository as the single source of truth.

---

### REQUIRED FILES

- /docs/ui/orbit-system.md
- /docs/scene-architecture.md
- /docs/ui/orbit-visual-spec.md
- /docs/ui/orbit-layout-spec.md
- /docs/ui/color-system.md
- /docs/data/data-contract.md
- /docs/codex-master-prompt.md

---

### CRITICAL RULE

Follow codex-master-prompt.md STRICT MODE.

No approximation.
No guessing.

---

### DATA RULE

- Use data structure from data-contract.md
- All UI content MUST come from data
- Initials MUST be computed dynamically:

const initials = `${personA[0]} & ${personB[0]}`

---

### TASK

Generate full Next.js (App Router) + React + Framer Motion implementation.

---

### VALIDATION

Before output:

- Layout matches orbit-layout-spec EXACTLY
- Colors match color-system EXACTLY
- Glow is layered correctly
- Orbit is perfectly radial
- Depth is clearly visible
- Data is fully dynamic (no hardcoding)

If ANY fails:
→ fix before output

---

### OUTPUT

Return full working code only.
No explanation.
