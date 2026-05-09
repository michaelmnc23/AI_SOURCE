# Color System — Cinematic Orbit UI

## 1. Purpose

This document defines ALL color values used in the system.

NO color may be invented outside this file.

---

## 2. Core Palette

### Gold (Primary Accent)

- Gold Base: #F5C27A
- Gold Bright: #FFD89C
- Gold Dim: #C89B5A

Usage:
- node borders
- glow effects
- center core
- highlights

---

### Background Gradient

- Top: #1A120B
- Middle: #0F0A07
- Bottom: #050303

MUST be radial or layered gradient.
NO flat background allowed.

---

### Text Colors

- Primary Text: #F3E9DC
- Secondary Text: #D6C6B8
- Muted Text: #A89B8F

---

## 3. Glow System (STRICT)

### Core Glow

Use MULTIPLE layers:

- Inner: rgba(255, 216, 156, 0.9)
- Mid: rgba(245, 194, 122, 0.6)
- Outer: rgba(245, 194, 122, 0.2)

---

### Node Glow

- Default: rgba(245, 194, 122, 0.5)
- Hover: rgba(255, 216, 156, 0.8)
- Active: rgba(255, 216, 156, 1)

---

## 4. Ring Colors

- Inner Ring: rgba(245, 194, 122, 0.6)
- Outer Ring: rgba(245, 194, 122, 0.3)

---

## 5. Blur + Transparency

- Background particles: opacity 0.1–0.3
- Orbit fade (memory state): opacity 0.85

---

## 6. Constraints

DO NOT:

- use pure white (#FFFFFF)
- use pure black (#000000)
- introduce new colors
- replace gold with yellow/orange
- use flat shadows instead of glow

---

## 7. Principle

Color must feel:

- warm
- cinematic
- glowing
- layered

NOT flat, NOT modern-minimal.
