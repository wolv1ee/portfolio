# Saad Mahmud — Portfolio

Built with Astro, Lenis smooth scroll, and GSAP.

## Quick Start

```bash
# 1. Install dependencies
npm install

# 2. Start dev server
npm run dev
# → opens at http://localhost:4321

# 3. Build for production
npm run build

# 4. Preview production build
npm run preview
```

## Deploy to Vercel

```bash
# Option A: Vercel CLI
npm i -g vercel
vercel

# Option B: Push to GitHub → connect repo at vercel.com
# Vercel auto-detects Astro. Zero config needed.
```

## What to Edit

| File | What to change |
|------|----------------|
| `src/pages/index.astro` | Hero bio, about text, skills, featured project |
| `src/pages/projects.astro` | `projects` array at the top — add your real projects |
| `src/pages/blog.astro` | `posts` array at the top — add your real posts |
| `src/pages/contact.astro` | Email, social links, form endpoint |
| `src/layouts/Layout.astro` | Nav logo, footer text, site-wide scripts |
| `astro.config.mjs` | Your Vercel URL / custom domain |

## Add Your Photo

1. Put your photo at `public/images/saad.jpg`
2. In `src/pages/index.astro`, find the `about-img-placeholder` div
3. Replace it with:
   ```html
   <img src="/images/saad.jpg" alt="Saad Mahmud" style="width:100%;height:100%;object-fit:cover;" />
   ```

## Add Project Screenshots

1. Put screenshots in `public/images/projects/`
2. In `src/pages/projects.astro`, add `image: '/images/projects/yourfile.png'` to each project object

## Wire Up the Contact Form (Formspree — free)

1. Sign up at https://formspree.io
2. Create a new form → copy your endpoint ID
3. In `src/pages/contact.astro`, uncomment the fetch block and replace `YOUR_ID`

## Project Structure

```
portfolio/
├── public/
│   ├── favicon.svg
│   └── images/           ← put your photos here
│       └── projects/     ← put project screenshots here
├── src/
│   ├── layouts/
│   │   └── Layout.astro  ← nav, footer, Lenis, GSAP, cursor
│   ├── pages/
│   │   ├── index.astro   ← Home
│   │   ├── projects.astro
│   │   ├── blog.astro
│   │   └── contact.astro
│   └── styles/
│       └── global.css    ← all shared CSS variables + base styles
├── astro.config.mjs
└── package.json
```
