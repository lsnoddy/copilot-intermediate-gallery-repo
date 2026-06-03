# Performance

## Current priorities

- Keep the homepage lightweight and easy to scan.
- Limit above-the-fold content to the `Hero` and feature cards.
- Use pagination in gallery views to avoid rendering the entire collection at once.

## Recommended practices

- Prefer optimized image delivery when placeholder blocks are replaced with real assets.
- Reduce client-side work in interactive pages by keeping shared UI components simple.
- Audit large animation or upload flows before adding more client-only logic.
- Monitor bundle impact when introducing new UI or icon libraries.

## Existing considerations

- `GalleryGrid` progressively reveals photos via pagination.
- `UploadZone` is client-side and should stay focused on upload interactions.
- Production builds currently depend on remote font fetching for Geist.
