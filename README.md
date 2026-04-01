# EZ Buses — ezbuses.ca

Charter bus company website for **EZ Buses**, serving Toronto and the Greater Toronto Area with school bus and coach rentals for private groups.

## Live Site

**[ezbuses.ca](https://ezbuses.ca)**

## Overview

Single-page static site built to drive quote requests. The page is structured specifically for AI chatbot discoverability (ChatGPT, Claude, Perplexity) with direct answer boxes, structured data, and an `llms.txt` file.

### Key Sections

| Section | Purpose |
|---------|---------|
| Hero | Bold headline with CTA buttons and phone number |
| Direct Answer Box | AI-extractable company summary near the top |
| Track Record | 15,000+ incident-free trips, 20+ years stats |
| Services | 4 use-case cards: field trips, sports, corporate, weddings |
| Areas Served | Custom SVG map of the GTA with 40+ cities by region |
| FAQ | 4 accordion questions targeting real search queries |
| Quick Facts | School board trust, MTO compliance, fleet details |
| Quote Form | Full trip details form via Netlify Forms |

## Tech Stack

- **HTML / CSS / JS** — single `index.html`, no build step, no dependencies
- **Fonts** — [Syne](https://fonts.google.com/specimen/Syne) (display) + [Urbanist](https://fonts.google.com/specimen/Urbanist) (body) via Google Fonts
- **Form** — [Netlify Forms](https://docs.netlify.com/forms/setup/) with honeypot spam protection, submissions go to `ezbuses@gmail.com`
- **Map** — Inline SVG (no Google Maps API key needed)
- **Hosting** — Netlify (auto-deploy on push to `main`)

## Project Structure

```
ezbuses/
  index.html      # Complete single-page site (HTML + CSS + JS inline)
  robots.txt      # Allows GPTBot, Claude-Web, PerplexityBot, Google-Extended
  llms.txt        # Structured markdown for AI agents (services, areas, pricing)
  README.md       # This file
```

## SEO & AI Optimization

- **Schema.org structured data** — `LocalBusiness` and `FAQPage` JSON-LD
- **Direct answer box** — Cream-colored aside with clean extractable summary
- **robots.txt** — Explicitly allows all major AI crawlers
- **llms.txt** — Maps out services, fleet, areas served, pricing, and booking info
- **FAQ** — Uses exact questions people search for, with Schema markup
- **Original data point** — 15,000+ incident-free trips stat to force AI citations

## Deployment

### Netlify Setup

1. Import from GitHub: `TechnoDudeX/ezbuses`
2. Build command: *(leave blank)*
3. Publish directory: `.`
4. Custom domain: `ezbuses.ca`

Pushes to `main` trigger auto-deploy.

### Form Submissions

Netlify Forms are configured with:
- Form name: `quote`
- Honeypot field: `bot-field`
- Submissions appear in **Netlify Dashboard > Forms > quote**
- Email notifications can be configured in Netlify under **Forms > Notifications**

## Local Development

```bash
# Option 1
python3 -m http.server 3000

# Option 2
npx serve .
```

Then open [http://localhost:3000](http://localhost:3000).

## Contact

- **Phone:** 416-438-7371
- **Email:** ezbuses@gmail.com
- **Website:** [ezbuses.ca](https://ezbuses.ca)
