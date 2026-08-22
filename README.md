# Yasins Lowlevel Prison

Personal blog and portfolio, built with [Astro](https://astro.build) and Tailwind CSS. Terminal/hacker-inspired look, focused on low-level programming, OS internals, and security write-ups.

## Stack

- [Astro](https://astro.build) — static site generation, content collections
- [Tailwind CSS v4](https://tailwindcss.com) — styling, theme tokens for the color palette
- JetBrains Mono — site-wide monospace typeface, self-hosted via Astro's Font API

## Project structure

```text
├── public/               # static assets (favicon, cv.pdf, ...)
├── src/
│   ├── assets/           # images, fonts
│   ├── components/       # Header, Footer, TerminalWindow, PostCard, Tag, ...
│   ├── content/blog/     # blog posts (Markdown/MDX)
│   ├── layouts/          # BlogPost.astro
│   └── pages/            # index, blog, projects, about
├── astro.config.mjs
└── src/styles/global.css # Tailwind import + color/theme tokens
```

## Writing a new post

Add a `.md` (or `.mdx`) file under `src/content/blog/`:

```markdown
---
title: 'Post title'
description: 'Short description for meta tags and RSS'
pubDate: 'Aug 22 2026'
tags: ['linux', 'hacking']
---

Post content here.
```

See `src/content.config.ts` for the full frontmatter schema.

## Commands

| Command                   | Action                                       |
| :------------------------ | :-------------------------------------------- |
| `npm install`              | Install dependencies                          |
| `npm run dev`               | Start local dev server at `localhost:4321`   |
| `npm run build`             | Build production site to `./dist/`           |
| `npm run preview`           | Preview the build locally                    |
| `npm run astro ...`         | Run Astro CLI commands (`astro add`, `astro check`) |

## Credit

Originally scaffolded from Astro's official blog starter theme, which is based on [Bear Blog](https://github.com/HermanMartinus/bearblog/).
