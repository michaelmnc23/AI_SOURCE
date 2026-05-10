# Data Contract — Cinematic Orbit System

## 1. Purpose

This document defines the COMPLETE data structure for the application.

ALL UI must derive content from this structure.
NO hardcoded content is allowed.

---

## 2. Types

```ts
export type Couple = {
  personA: string
  personB: string
}

export type Node = {
  id: "couple" | "story" | "gallery" | "event" | "interaction"
  label: string
  coverImage: string
}

export type StoryItem = {
  title: string
  date: string
  description: string
  image: string
}

export type EventInfo = {
  title: string
  date: string
  time: string
  location: string
}

export type AudioConfig = {
  src: string
  autoplayAfterIntro: boolean
  loop: boolean
  volume: number
}

export type AppData = {
  couple: Couple
  nodes: Node[]
  story: StoryItem[]
  gallery: string[]
  event: EventInfo
  audio: AudioConfig
}
```

---

## 3. Asset Path Rules (CRITICAL)

All asset paths are served from Next.js `/public` folder.

Mapping:

/public/images/* → "/images/..."
/public/audio/*  → "/audio/..."

Rules:

- NEVER include `/public` in paths
- ALWAYS use root-relative paths ("/... ")
- Codex MUST assume these map to `/public`

---

## 4. Derived Data Rules

Initials MUST be computed dynamically:

```ts
const initials = `${personA[0]} & ${personB[0]}`
```

---

## 5. Dummy Data (Development Only)

```ts
export const data: AppData = {
  couple: {
    personA: "Aurelia",
    personB: "Rory"
  },
  nodes: [
    { id: "couple", label: "Couple", coverImage: "/images/couple.jpg" },
    { id: "story", label: "Story", coverImage: "/images/story.jpg" },
    { id: "gallery", label: "Gallery", coverImage: "/images/gallery.jpg" },
    { id: "event", label: "Event", coverImage: "/images/event.jpg" },
    { id: "interaction", label: "RSVP", coverImage: "/images/rsvp.jpg" }
  ],
  story: [
    {
      title: "First Meeting",
      date: "2020-05-12",
      description: "We met for the first time at a quiet cafe.",
      image: "/images/story1.jpg"
    },
    {
      title: "The Proposal",
      date: "2024-02-14",
      description: "A surprise proposal under the stars.",
      image: "/images/story2.jpg"
    }
  ],
  gallery: [
    "/images/gallery1.jpg",
    "/images/gallery2.jpg",
    "/images/gallery3.jpg"
  ],
  event: {
    title: "Wedding Ceremony",
    date: "2026-12-12",
    time: "10:00 AM",
    location: "Jakarta"
  },
  audio: {
    src: "/audio/bg-music.mp3",
    autoplayAfterIntro: true,
    loop: true,
    volume: 0.6
  }
}
```

---

## 6. Rules

- UI MUST render from this data
- NO placeholder text allowed outside this file
- Audio MUST come from data.audio
- Audio MUST NOT be hardcoded

---

## 7. Future Extension

This structure must support:

- multiple themes
- localization
- CMS integration
