# Where SEO lives in common stacks

Pointers to the files and APIs to read first. Framework conventions change between major versions; confirm against the version in the project's package manifest and say which version you assumed.

## Next.js
- App Router: `app/**/layout.*` and `app/**/page.*` exporting `metadata` or `generateMetadata` (title, description, `alternates.canonical`, `alternates.languages`, `robots`); `app/robots.*` and `app/sitemap.*` generators; `app/not-found.*` and the `notFound()` call; `middleware.*` for redirects and locale handling; `next.config.*` for `redirects`, `rewrites`, `trailingSlash`, `i18n`.
- Pages Router: `pages/_app.*`, `pages/_document.*`, `next/head` usage per page; `getStaticProps` or `getServerSideProps` returning `notFound`; `pages/404.*`.
- Watch for: `robots` metadata set from an environment flag; metadata only in client components; `'use client'` pages fetching main content in effects.

## Nuxt
- `nuxt.config.*` (`app.head`, route rules, `ssr: false`), `useHead` and `useSeoMeta` in pages and layouts, `server/routes/sitemap*`, `public/robots.txt`, error page `error.vue`.
- Watch for: `ssr: false` or client-only route rules on pages meant to rank; `createError` with status 200.

## Astro
- Layout components that render `<head>`; `astro.config.*` (site URL, redirects, trailingSlash, integrations such as sitemap); `src/pages/404.*`; `public/robots.txt`.
- Watch for: a missing `site` URL, which breaks absolute canonicals and sitemap URLs; islands that load main content only on the client.

## SvelteKit
- `+layout.svelte` and `+page.svelte` with `<svelte:head>`; `+page.server.*` or `+page.*` load functions and `error()` status; `svelte.config.*` prerender and trailing slash settings; `src/routes/sitemap.xml/+server.*`; `static/robots.txt`.
- Watch for: `ssr = false` on pages meant to rank.

## Remix and React Router framework mode
- `meta` exports per route; `root.*` layout; loaders that throw responses with status codes; `routes/sitemap[.]xml.*` resource routes.
- Watch for: loaders returning empty data with status 200 when a record does not exist.

## Gatsby
- `gatsby-config.*` (siteMetadata, plugins for sitemap and robots), the `Head` export or `gatsby-plugin-react-helmet` usage, `src/pages/404.*`.

## Plain React, Vue or Angular single-page apps
- `index.html` (usually an empty root), the router configuration, any head-management library, the hosting config for fallbacks.
- Watch for: every route served from the same `index.html` with status 200 (soft 404s for unknown paths); no prerendering.

## WordPress themes
- `header.php` and `functions.php` (title support, `wp_head` hooks), SEO plugin settings exported as files if present, `robots.txt` handling, "Discourage search engines" setting (stored in the database; ask the user to check it in Settings, Reading).
- Watch for: noindex added by the theme or a plugin on archives or the whole site.

## Server-rendered frameworks with templates (Django, Rails, Laravel, Express with a view engine)
- Base templates or layouts holding `<head>`; view code that sets title and canonical variables; URL routing files for redirects; the 404 handler and its status code; any sitemap view.

## Static HTML and static-site generators
- Each HTML file's head, `robots.txt`, `sitemap.xml`, `_redirects` or `_headers` files and similar hosting config.

## Hosting and server config
- `vercel.json`, `netlify.toml`, `_redirects`, `_headers`, Nginx or Apache config, CDN rules: redirects, `X-Robots-Tag` headers, trailing slash normalization. These often override framework settings.
