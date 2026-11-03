# commitarium.com

The landing page and the docs for [Commitarium](https://github.com/EinarLogiOskars/commitarium),
built with [Astro](https://astro.build) and [Starlight](https://starlight.astro.build).

```bash
pnpm install
pnpm dev      # http://localhost:4321
pnpm build    # the static site, in dist/
```

- The landing page is `src/pages/index.astro`.
- Docs pages are in `src/content/docs/docs/`, one folder per section; the
  sidebar order is in `astro.config.mjs`.
- Screenshots in `public/screens/` are rendered from the app's real views by
  the main repository, with this repository checked out beside it:

  ```bash
  pnpm --dir ../commitarium/video run render:docs        # every screenshot
  pnpm --dir ../commitarium/video run render:docs -- <id> # one
  ```

  A page shows one with `<Screenshot id="<id>" alt="…" />`.
