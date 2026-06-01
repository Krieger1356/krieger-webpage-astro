# Krieger's Homepage

Personal website and worldbuilding hub built with [Astro](https://astro.build) and the [Reimu](https://github.com/D-Sketon/astro-theme-reimu) theme.

**[www.kriegerhost.xyz](https://www.kriegerhost.xyz)**

## What's Here

- **Valik'thull** — original fantasy worldbuilding project exploring the Seven Domains
- **Minecraft Servers** — info and install guides for vanilla and modded servers
- **Resources** — collection of useful links and tools
- **About** — who I am and what I do

## Tech Stack

| | |
|---|---|
| Framework | [Astro](https://astro.build) 5 |
| Theme | astro-theme-reimu (customised) |
| Hosting | Cloudflare Workers via Wrangler |
| Domain | kriegerhost.xyz |
| Comments | [Giscus](https://giscus.app) (GitHub Discussions) |
| Analytics | None (privacy-first) |
| Package Manager | pnpm |

## Development

```bash
# Install dependencies
pnpm install

# Start dev server (http://localhost:4321)
pnpm dev

# Build for production
pnpm build

# Preview production build
pnpm preview
```

## Deploy

```bash
pnpm run deploy
```

This runs `astro build` then deploys the `dist/` folder to Cloudflare Workers via Wrangler.

**Note:** Use `pnpm run deploy`, not `pnpm deploy` — pnpm has a built-in `deploy` command that conflicts with the script name.

## Project Structure

```
/
├── public/images/         # Static images served as-is
├── src/
│   ├── components/        # Astro/React components
│   ├── content/blog/      # Blog posts (Valik'thull, MC guides, resources)
│   ├── content.config.ts  # Content collection schema
│   ├── layouts/           # Page layouts (Base, Blog, Markdown)
│   ├── pages/             # Route pages (about, archives, 404)
│   ├── config.ts          # Site configuration
│   └── styles/            # Global CSS and Stylus files
├── astro.config.mjs       # Astro configuration
├── wrangler.jsonc         # Cloudflare Workers config
└── package.json
```

## Config

All site settings live in `src/config.ts` — site info, sidebar, social links, comments, widgets, and feature toggles.

## License

Content and custom code © Krieger. The Reimu theme is MIT-licensed.
