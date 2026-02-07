# Khai Portfolio (Astro)

Minimal personal portfolio built with Astro, with a responsive modern layout and theme switching.

## Tech Stack

- Astro 5
- Astro `Image` component (`astro:assets`) for optimized profile image delivery
- Plain CSS (component-scoped + layout styles)

## Features

- Responsive portfolio sections: Hero, Stack, Experience, Education, Selected Work, Contact
- Dynamic footer component with current year
- Header component with theme switcher (`Auto`, `Light`, `Dark`)
- Theme preference persistence via `localStorage`
- System theme sync when `Auto` is selected
- Rocket favicon in `.ico` format

## Project Structure

```text
/
├── public/
│   ├── favicon.ico
│   └── ...
├── src/
│   ├── assets/
│   │   └── khai.jpg
│   ├── components/
│   │   ├── Footer.astro
│   │   └── Header.astro
│   ├── layouts/
│   │   └── Layout.astro
│   └── pages/
│       └── index.astro
└── package.json
```

## Development

Requirements:

- Node.js `>=18.20.8`
- npm

Install and run:

```sh
npm install
npm run dev
```

Build and preview:

```sh
npm run build
npm run preview
```

## Content Editing

Main content is in:

- `src/pages/index.astro`

Theme variables (light/dark colors) are in:

- `src/layouts/Layout.astro`

Theme toggle behavior/UI is in:

- `src/components/Header.astro`

Footer text and structure are in:

- `src/components/Footer.astro`

## Deployment (Vercel)

This project deploys cleanly on Vercel with default Astro settings.

### Option 1: Vercel Dashboard

1. Push this repo to GitHub/GitLab/Bitbucket
2. Import the repo in Vercel
3. Use these settings if prompted:
   - Framework Preset: `Astro`
   - Build Command: `npm run build`
   - Output Directory: `dist`
4. Deploy

### Option 2: Vercel CLI

```sh
npm i -g vercel
vercel
```

For production deploy:

```sh
vercel --prod
```
