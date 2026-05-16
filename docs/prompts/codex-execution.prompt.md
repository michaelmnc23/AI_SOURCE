# CODEX EXECUTION PROMPT — v4.1 (CINEMATIC LOCKED MODE)

## ROLE
You are a senior cinematic UI engineer and senior Next.js App Router architect.

You are NOT designing.
You are EXECUTING a locked cinematic experience.

This is NOT:
- dashboard UI
- SaaS UI
- modal system
- rotating orbit menu

This IS:
- cinematic memory traversal
- emotional spatial experience
- immersive wedding memory world

---

# CRITICAL EXECUTION RULES

DO NOT:
- simplify the layout
- redesign composition
- invent UI
- use popup cards
- use modal behavior
- use generic Tailwind cards
- create fast rotating orbit
- make user chase moving nodes
- leave sections empty
- omit navigation controls
- start directly at orbit screen

YOU MUST:
- create intro invitation scene
- create cinematic memory traversal
- create atmospheric layered world
- preserve persistent orbit world
- simulate entering memories physically
- render real visible dummy content
- use directional transitions
- match cinematic mockup composition closely

---

# EXPERIENCE PHILOSOPHY

Orbit is NOT a solar system.

Orbit is:
- floating memories
- emotional navigation
- suspended dreamlike space

The user should feel:
“I am entering memories.”

NOT:
“I opened a popup.”

---

# REQUIRED EXPERIENCE FLOW

1. Invitation Intro
2. Open Invitation Sequence
3. Orbit Memory Field
4. Enter Memory Transition
5. Memory Experience
6. Lateral Memory Navigation
7. Return To Orbit

---

# INTRO INVITATION SCREEN (MANDATORY)

The app MUST start with:
- fullscreen cinematic intro
- NO orbit initially visible

Required content:
- couple names
- subtitle
- ambient particles
- warm cinematic glow
- elegant typography
- Open Invitation button

Button style:
- cinematic
- glowing
- elegant
- animated softly

Background:
- layered particles
- subtle fog
- warm cinematic gradient
- depth atmosphere

---

# OPEN INVITATION TRANSITION

When clicking Open Invitation:

1. intro dissolves softly
2. particles spread outward
3. camera moves through particles
4. orbit world slowly appears
5. center core forms
6. nodes materialize progressively
7. music fades in
8. orbit enters calm idle state

Duration:
2200ms–3500ms

Must feel:
- magical
- cinematic
- emotional
- luxurious

---

# ORBIT MEMORY FIELD

The orbit MUST resemble floating emotional memories.

NOT:
- active spinning menu
- gameplay orbit
- rotating target system

Instead:
- almost static
- drifting softly
- subtle breathing movement
- floating lantern feeling
- underwater dreamlike motion

Allowed motion:
- 1 revolution every 120–180 seconds MAXIMUM
- preferably ambient drift only

User must NEVER chase nodes.

---

# CENTER CORE

Large glowing emotional core.

Contains:
Dynamic initials from data.

Example:
Aurelia + Rory
=> A & R

Visual requirements:
- strongest glow in scene
- layered bloom
- radial aura
- subtle breathing pulse
- atmospheric haze
- warm gold lighting

---

# ORBIT NODES

Nodes are memory bubbles.

Required nodes:
- Couple
- Story
- Gallery
- Event
- RSVP / Wishes

Each node MUST contain:
- image thumbnail
- cinematic glow border
- warm lighting
- subtle hover response
- visible label

DO NOT use generic icons.

Use image thumbnails from:
/public/images/

---

# MEMORY ENTRY TRANSITION (CRITICAL)

FORBIDDEN:
- popup card
- blur + modal
- instant content appearance

REQUIRED SEQUENCE:

1. selected node enlarges
2. glow intensifies
3. surrounding orbit softens
4. camera pushes inward
5. particles trail toward node
6. orbit fades deeper into background
7. node expands into memory world
8. memory content resolves progressively

The user must feel:
traveling INTO the memory.

Duration:
1500ms–2500ms

---

# MEMORY EXPERIENCE

Memory scenes are NOT cards.

They must feel:
- cinematic
- layered
- atmospheric
- spatial
- emotionally framed

FORBIDDEN:
- black floating modals
- centered popup cards
- dashboard panels

Required:
- asymmetrical composition
- cinematic framing
- glow layering
- soft edge blending
- atmospheric depth

---

# STORY MEMORY

Must contain:
- cinematic hero image
- emotional typography
- visible timeline
- descriptive text
- elegant spacing

---

# GALLERY MEMORY

Must contain:
- cinematic gallery
- layered depth
- floating transitions
- visible preview images

---

# EVENT MEMORY

Must contain:
- date
- time
- location
- CTA buttons
- cinematic event framing

---

# RSVP / WISHES MEMORY

Must contain:
- visible tabs
- interaction sections
- elegant forms
- atmospheric styling

---

# UI OVERLAY (MANDATORY)

After intro opens, ALWAYS show:

- previous
- next
- back
- reset orbit
- audio toggle

Style:
- minimal
- glowing
- cinematic
- subtle

---

# AUDIO SYSTEM

Background music REQUIRED.

Behavior:
- starts ONLY after opening invitation
- loops continuously
- fades in smoothly
- persists across all transitions

Audio path:
/public/audio/background.mp3

---

# COLOR SYSTEM

Primary tones:
- #f6c177
- #e0a96d
- #b97a56
- #2b160f
- #140d0a

Background:
- deep warm brown-black

Scene MUST include:
- cinematic fog
- vignette
- bloom illusion
- radial atmosphere
- particle dust
- layered glow

Empty dark background is FORBIDDEN.

---

# DATA CONTRACT

ALL content MUST come from:
/lib/data.ts

NO hardcoded content.

Data MUST include:
- couple names
- initials
- subtitle
- story timeline
- gallery images
- event details
- RSVP content
- wishes content
- audio path

---

# PLACEHOLDER ASSETS

If real assets unavailable:
- create placeholder images
- create placeholder audio
- preserve exact file paths

Paths:
/public/images/
/public/audio/

---

# REQUIRED FILE STRUCTURE

/components/scene
- SceneRoot.tsx
- OrbitSystem.tsx
- OrbitNode.tsx
- MemoryLayer.tsx
- UIOverlay.tsx
- BackgroundLayer.tsx
- InvitationIntro.tsx

/lib
- data.ts

/styles
- globals.css

---

# MOTION RULES

Use:
- Framer Motion
- cinematic easing
- soft acceleration
- slow deceleration
- transform-based animation

FORBIDDEN:
- abrupt transitions
- instant appearance
- mechanical movement
- snappy UI feel

---

# FINAL VALIDATION

Before finishing verify:

- intro invitation exists
- open invitation button exists
- orbit is NOT actively rotating
- nodes use thumbnails
- content is visible
- navigation controls exist
- memory transition feels spatial
- no popup cards exist
- orbit remains persistent
- audio works correctly
- visuals resemble cinematic mockup

If ANY fail:
FIX BEFORE OUTPUT.

---

# FINAL DIRECTIVE

You are rendering a cinematic memory world.

Precision over creativity.
