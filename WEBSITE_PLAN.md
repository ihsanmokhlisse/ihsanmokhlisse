# Personal Website Plan

## Current State
- Profile README renders on GitHub profile page
- Repo: github.com/ihsanmokhlisse/ihsanmokhlisse

## Future: Full Personal Website

### Recommended Stack

**Framework: [Astro](https://astro.build/)**
- Static-first, ships zero JS by default (fastest possible)
- Markdown/MDX for blog posts (write content in .md files)
- Component islands for interactive parts (can use React/Vue/Svelte)
- Built-in content collections for blog, projects, CV sections
- SEO-friendly out of the box

**Why Astro over alternatives:**
- Hugo: faster build but Go templates are painful, less ecosystem
- Next.js: overkill for a portfolio (SSR, hydration overhead)
- Jekyll: outdated, slow, limited
- Astro: best of all worlds — fast, modern, markdown-first, component-flexible

### Recommended Theme
- [Astro Nano](https://github.com/markhorn-dev/astro-nano) — minimal, dark, blog + projects
- [Astro Portfolio](https://astro.build/themes/details/astro-portfolio/) — official, clean
- [Brutal](https://github.com/eliancodes/brutal) — bold, standout design

### Hosting: Cloudflare Pages (FREE)

**Why Cloudflare Pages over alternatives:**

| Feature | GitHub Pages | Cloudflare Pages | Vercel | Netlify |
|---------|-------------|------------------|--------|---------|
| Cost | Free | Free | Free (non-commercial) | Free |
| CDN | Limited | 300+ global PoPs | Edge | Edge |
| Bandwidth | Soft 100GB | Unlimited | 100GB/mo | 100GB/mo |
| Custom domain | Yes | Yes + free SSL | Yes | Yes |
| Build minutes | 10/hr | 500/mo | 6000/mo | 300/mo |
| Speed | Good | Fastest | Fast | Fast |
| DDoS protection | No | Yes (built-in) | No | No |
| Analytics | No | Free (privacy-first) | Paid | Paid |

**Winner: Cloudflare Pages** — unlimited bandwidth, fastest CDN, free analytics, free DDoS protection, zero cost.

### Domain Options
- Free: `ihsanmokhlisse.pages.dev` (Cloudflare) or `ihsanmokhlisse.github.io` (GitHub Pages)
- Cheap: `ihsanmokhlisse.dev` (~$12/year from Cloudflare Registrar, at-cost pricing)
- Alternative: `mokhlisse.dev`, `ihsan.dev` (check availability)

### Content Structure
```
/                    — Home (hero + summary)
/about               — Extended bio, career timeline
/cv                  — Interactive CV / downloadable PDF
/projects            — Open source contributions + personal projects
/blog                — Technical articles (Markdown/MDX)
/blog/supply-chain-security-openclaw  — Example article
/contact             — Links + contact form (Cloudflare Workers for form backend)
```

### Migration Path
1. Current: Profile README (done)
2. Next: `npx create-astro@latest` with a portfolio theme
3. Deploy to Cloudflare Pages (connect GitHub repo)
4. Optional: buy `ihsanmokhlisse.dev` domain ($12/year)
5. Write first blog post about OpenClaw security contributions
