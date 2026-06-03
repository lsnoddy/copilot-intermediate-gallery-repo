# Deployment

## Target shape

This application is structured as a standard Next.js 15 app and is suitable for platforms that support Node.js server builds, such as Vercel or other managed hosting providers.

## Deployment checklist

- Install dependencies with `npm ci` or `npm install`.
- Run `npm run lint`.
- Run `npm run build`.
- Configure environment-specific secrets outside the repository.
- Verify the production environment can access any external resources required at build time.

## Operational notes

- The current app uses mock data, so no database provisioning is required yet.
- If `next/font/google` remains in use, ensure the build environment can reach Google Fonts or switch to a bundled font strategy.
