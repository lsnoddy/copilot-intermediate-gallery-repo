# Architecture Overview

## Application summary

The repository is a Next.js 15 photo gallery and portfolio application built with TypeScript, React 19, Tailwind CSS 4, and a small set of UI-focused libraries.

## Stack

- **Framework:** Next.js 15.4.4 with the App Router
- **Language:** TypeScript 5
- **UI:** React 19, Tailwind CSS 4
- **Animation:** Framer Motion
- **Icons:** Lucide React
- **Upload UX:** React Dropzone
- **Image processing dependency:** Sharp

## Route structure

- `/` — homepage with hero, feature cards, quick upload, and gallery preview
- `/gallery` — searchable and filterable gallery view
- `/upload` — upload flow with supporting feature explanations
- `/admin` — dashboard with stats, quick actions, and recent galleries

## Component composition

The root layout in `src/app/layout.tsx` provides shared metadata, navigation, and global styles. Individual pages compose reusable UI building blocks from `src/components/ui`, while feature-specific interactions live in gallery and upload components.

## Data model today

The application is currently frontend-driven and reads from mock data modules in `src/lib`, including photo records, feature-card content, tags, and admin dashboard stats.
