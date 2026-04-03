# Project Guidelines

## Project Overview
- Astro 5 application using `@astrojs/node` in standalone mode with server-side rendering enabled.
- Primary app routes live in `src/pages/`; API routes live under `src/pages/api/`.
- Treat `src/pages/api/contributions/[username].ts` as the main server-side data endpoint for contribution lookups.
- Ignore `workshop/` for product behavior; it is tutorial material, not app source.

## Build and Run
- `npm install` to install dependencies.
- `npm run dev` to start the local Astro dev server.
- `npm run build` to create a production build.
- `npm run preview` to preview the built output.
- `npm run astro` to access the Astro CLI directly.

## Code Style
- TypeScript is strict via `astro/tsconfigs/strict`; keep types explicit where route params, handlers, or responses matter.
- Match nearby file style and avoid unnecessary formatting churn.
- Prefer Astro components and pages for UI, and keep plain `.ts` files focused on API or utility logic.

## Astro Conventions
- Keep request-driven or data-driven routes unprerendered when needed with `export const prerender = false`.
- Use `APIRoute` for API handlers and return `Response` objects with explicit JSON headers when sending JSON.
- Put static assets in `public/` and reference them with root-relative paths.
- Preserve the existing SSR setup in `astro.config.mjs` when adding routes or server logic.