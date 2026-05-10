# Codex Final Prompt — Cinematic Orbit System

## Purpose

This prompt is the SINGLE executable instruction used with Codex.
It references all system specs and behavior rules.

---

## Prompt

Repository:
https://github.com/michaelmnc23/AI_SOURCE

Use this repository as the single source of truth.

---

## REQUIRED FILES

### System Behavior (HOW to behave)
- /docs/system/codex-behavior.md

### Architecture + System
- /docs/ui/orbit-system.md
- /docs/scene-architecture.md

### Visual + Layout
- /docs/ui/orbit-visual-spec.md
- /docs/ui/orbit-layout-spec.md
- /docs/ui/color-system.md

### Data
- /docs/data/data-contract.md

---

## CRITICAL RULE

You MUST follow /docs/system/codex-behavior.md strictly.

No guessing.
No approximation.
No deviation.

---

## DATA RULE

- All UI content MUST come from data-contract.md
- Initials MUST be computed dynamically:

const initials = `${personA[0]} & ${personB[0]}`

---

## TASK

Generate full Next.js (App Router) + React + Framer Motion implementation.

---

## VALIDATION

Before output, ensure:

- Layout matches orbit-layout-spec EXACTLY
- Colors match color-system EXACTLY
- Glow is layered correctly
- Orbit is perfectly radial
- Depth is clearly visible
- Data is fully dynamic (no hardcoding)

If ANY fails:
→ fix before output

---

## OUTPUT

Return full working code only.
No explanation.
