# Data Flow

## Current state

The app does not yet call live backend endpoints. Instead, pages and client components read from mock data modules and manage UI state in the browser.

## Homepage flow

`src/app/page.tsx` renders the homepage in this order:

1. `Hero` introduces the product.
2. `FeatureCard` items are created from `featureCardsData`.
3. `UploadZone` presents a drag-and-drop upload interaction.
4. `GalleryGrid` shows a recent uploads preview.

## Gallery flow

- `src/app/gallery/page.tsx` stores search text, selected tags, loading state, and pagination in component state.
- Those values are passed into `GalleryGrid`.
- `GalleryGrid` filters `mockPhotos` in memory and progressively shows more results.

## Upload flow

- `UploadZone` accepts files through React Dropzone.
- It creates local preview URLs, simulates upload progress, and updates in-memory status.
- No files are persisted beyond the browser session.

## Admin flow

- `src/app/admin/page.tsx` reads summary data from `mock-admin-data`.
- `StatsGrid` and `FeatureCard` display dashboard metrics and quick actions.
- The recent galleries table renders static mock rows.

## Future API alignment

The OpenAPI contract under `docs/api/openapi.yaml` describes the backend surface that would replace the current mock-data reads and simulated uploads.
