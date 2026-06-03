# Development

## Daily workflow

1. Install dependencies with `npm install`.
2. Start the dev server with `npm run dev`.
3. Make changes under `src/app`, `src/components`, or `src/lib`.
4. Run `npm run lint` before opening a pull request.

## Key directories

- `src/app` — App Router pages and layout
- `src/components/gallery` — gallery display components
- `src/components/upload` — upload experience
- `src/components/ui` — shared UI building blocks
- `src/lib` — mock data and supporting utilities
- `docs` — documentation set for engineering and onboarding

## Current implementation notes

- The homepage in `src/app/page.tsx` combines `Hero`, feature cards, `UploadZone`, and `GalleryGrid`.
- Gallery, upload, and admin experiences are currently powered by mock data in `src/lib`.
- There is no dedicated automated test suite in the repository today.
