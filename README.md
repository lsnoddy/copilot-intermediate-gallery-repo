# Photo Gallery & Portfolio

A Next.js 15 photo gallery application for showcasing photography workflows, reusable UI patterns, and GitHub Copilot demos.

## Project overview

This repository contains a component-driven gallery experience built with the Next.js App Router, TypeScript, React 19, and Tailwind CSS. The current implementation uses mock data to demonstrate homepage composition, gallery filtering, uploads, and an admin dashboard.

## Features

- Homepage with hero, feature cards, upload call-to-action, and recent gallery preview
- Searchable and tag-filtered gallery experience
- Drag-and-drop upload flow with simulated progress
- Admin dashboard with stats, quick actions, and recent galleries
- Reusable UI components exported from `src/components/ui`
- Demo content under [`demos/`](demos/)

## Requirements

- Node.js 18.18+ or 20+
- npm 9+

## Quick start

```bash
git clone https://github.com/lsnoddy/copilot-intermediate-gallery-repo.git
cd copilot-intermediate-gallery-repo
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

## Scripts

- `npm run dev` — start the local development server
- `npm run build` — create a production build
- `npm run start` — serve the production build
- `npm run lint` — run the existing lint checks

## Project structure

```text
src/
├── app/                 # Next.js 15 App Router pages and layout
├── components/
│   ├── gallery/         # Gallery-specific components
│   ├── ui/              # Shared UI building blocks
│   └── upload/          # Upload flow components
├── lib/                 # Mock data and supporting utilities
docs/                    # Product, API, architecture, and guide docs
demos/                   # Copilot demo guides and examples
```

## Documentation

Start with [`docs/README.md`](docs/README.md).

- API: [`docs/api/openapi.yaml`](docs/api/openapi.yaml)
- Components: [`docs/components/ui-components.md`](docs/components/ui-components.md)
- Architecture: [`docs/architecture/overview.md`](docs/architecture/overview.md)
- Guides: [`docs/guides/installation.md`](docs/guides/installation.md)
- ADRs: [`docs/adr/0001-use-nextjs-15-typescript.md`](docs/adr/0001-use-nextjs-15-typescript.md)

## Demos

All demo guides and examples are in the [`demos/`](demos/) folder. For demo-specific walkthroughs, start with [`demos/README.md`](demos/README.md).

## Contributing

See [`CONTRIBUTING.md`](CONTRIBUTING.md) for setup, pull request expectations, and documentation contribution guidance.
