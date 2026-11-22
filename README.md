# Evavind Website

The official website for [Evavind OS](https://github.com/Evan-Windproof/Evavind-OS), built with Astro and TypeScript. The homepage shows the project's early development status and its planned architecture.

## Local development

Use Node.js 24 and npm. From the repository root, run:

```sh
npm ci
npm run dev
```

Run `npm run check` for Astro and TypeScript diagnostics. Run `npm run build` to generate the static site in `dist/` and `npm run preview` to serve that output locally.

The homepage lives in `src/pages/index.astro`. Shared structure lives in `src/layouts/` and `src/components/`, with site styling in `src/styles/global.css`.

## GitHub Pages

1. In **Settings → Pages**, set **Build and deployment → Source** to **GitHub Actions**.
2. On a push to `main`, the Pages workflow installs dependencies, checks and builds the site, and deploys the `dist/` artifact. You can also run it from the Actions tab.
3. For custom domain activation, set `evavind.noxc.uk` in the repository's Pages settings and follow GitHub's instructions to create a DNS CNAME record pointing to `evan-windproof.github.io`. After GitHub verifies the domain and provisions its certificate, enable **Enforce HTTPS**.

Astro's production site URL and `public/CNAME` declare the intended domain. The custom domain must also be configured in GitHub Pages settings for Actions deployments.
