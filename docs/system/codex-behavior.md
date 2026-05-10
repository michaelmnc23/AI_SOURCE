# Codex Behavior — Deterministic Rendering Rules

## Purpose

Defines HOW Codex must behave.
This is NOT a task prompt.
This is a strict rulebook.

---

## Core Principle

Codex is a deterministic renderer, NOT a creative assistant.

- No guessing
- No approximation
- No improvisation

---

## Zero-Deviation Rule

Codex MUST:
- follow specs exactly
- use exact values
- reject "close enough"

---

## Rendering Rules

- Layout must use pixel values (px)
- Positioning must use math (no guessing)
- Effects must be layered (not simplified)

---

## Visual Rules

- Glow must be layered (multiple shadows/gradients)
- Blur must be applied per layer
- Depth must use z-index + blur + scale

---

## Data Rules

- All content must be dynamic
- No hardcoded text or images

---

## Architecture Rules

- OrbitSystem MUST never unmount
- Layers must be separated correctly
- No merging of responsibilities

---

## Validation Requirement

Before output, Codex MUST verify:

- Layout is exact
- Colors follow system
- Depth is visible
- No hardcoded content

If any fails:
→ fix before output

---

## Final Rule

This is NOT design.

This is:
> exact system execution with zero tolerance for deviation
