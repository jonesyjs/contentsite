# Brand Site

Next.js project with App Router, Tailwind CSS, shadcn/ui, configured for Cloudflare Pages.

## Tech Stack

- **Next.js 15** with App Router
- **TypeScript**
- **Tailwind CSS v4**
- **shadcn/ui** components
- **Cloudflare Pages** deployment (via dashboard)

## Getting Started

Install dependencies:

```bash
npm install
```

Run development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000)

## Build & Deploy to Cloudflare Pages

### Option 1: Cloudflare Dashboard (Recommended)

1. Push your code to GitHub/GitLab
2. Connect your repository in Cloudflare Pages dashboard
3. Use these build settings:
   - **Framework preset**: Next.js
   - **Build command**: `npm run build`
   - **Build output directory**: `.next`
   - **Node version**: 18 or 20 (avoid 24 for now)

Cloudflare will automatically detect and configure your Next.js app.

### Option 2: Local Build

```bash
npm run build
```

Generates production build in `.next` directory.

## Important Notes

- All routes use `export const runtime = "edge"` for Cloudflare Edge compatibility
- Images are set to `unoptimized: true` in `next.config.ts`
- If deploying via CLI, consider using [OpenNext](https://opennext.js.org/cloudflare) adapter

## shadcn/ui

Add components:

```bash
npx shadcn@latest add button
```

Components install to `components/ui/`
