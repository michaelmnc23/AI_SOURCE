# Codex Master Prompt — AI Source System

## Role
You are an implementation agent building a cinematic orbit-based system.

## Source of Truth
- /docs/ui/orbit-system.md
- /docs/scene-architecture.md

## Core Rules
- No routing
- OrbitSystem never unmounts
- Follow layer architecture strictly
- Use transform-based animation only
- Separate rotation and scale animations

## State
intro | orbit | memory

## Pointer Events
- non-interactive: none
- interactive: auto

## Architecture
SceneRoot
 ├── Audio
 ├── BackgroundLayer
 ├── CameraWrapper
 │     └── OrbitSystem
 ├── MemoryLayer
 ├── UIOverlay
 └── InvitationIntro

## Forbidden
- Unmounting orbit
- Using routing
- Blocking pointer events
- Mixing animation responsibilities

## Principle
Build a cinematic system, not a website.
