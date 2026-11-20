# ImDev

Personal site of **Devaldi Caliesta Octadiani** — Full Stack Developer & AI-Driven Engineer.

A single static page (`public/index.html`) with no build step, bilingual (EN / ID), dark by default with a light theme.

The layout is a dark monochrome portfolio: a floating nav pill, a `< FULL STACK DEVELOPER />` hero whose portrait card flips into the About section as you scroll, a kinetic "I build ___" band next to an animated ASCII field, a scroll-driven tech ticker, a staggered tech stack, project folders that open case-study dialogs, a wave-shaped experience timeline (oldest on the left, current role on the right), an email-draft contact form, and a white footer band with the ink illustration standing in front of a giant name.

- `public/index.html` holds the markup, inline CSS and inline JS (theme / language toggles, nav menu, kinetic type: headline scramble and cursor stretch, the "I build" word rotator, the ASCII field, the ticker, the flying portrait card, folder dialogs, wave timeline, contact form, footer band). All motion is gated by `prefers-reduced-motion`.
- `public/img/` holds the portrait (`portrait.webp`) and the footer illustration (`figure.webp`, background cut out to transparency).
- `public/nara-widget.css` restyles the embedded Nara chat widget (`<tanyasaya-chat>`) to match the site; it reads the page CSS variables, so the light theme follows automatically.

## Project map for AI agents (graphify)

A [graphify](https://github.com/safishamsi/graphify) knowledge graph of the repo lives in `graphify-out/`:

- `GRAPH_REPORT.md` lists the communities, hub nodes and every section / script with its line number. Use it for a broad review; for a specific question, query the graph first (below).
- `graph.json` is the raw graph; each node carries `source_file` and `source_location`.
- `graph.html` is an interactive view that opens in any browser.

```bash
graphify query "where is the chat widget language synced?"
graphify explain "Animated ASCII field"
graphify explain "Flying portrait card"
graphify path "Language toggle button EN/ID [data-lang-toggle]" "Nara AI chat widget"
```

The site is HTML (a document for graphify), so after editing it, rebuild the graph through an agent with the graphify skill (`/graphify . --update`).

## Run locally

Open `public/index.html` in a browser, or serve the folder:

```bash
npx serve public
```

## Deploy (Cloudflare Pages)

Every push to `main` deploys automatically through `.github/workflows/deploy.yml` (needs the `CLOUDFLARE_API_TOKEN` and `CLOUDFLARE_ACCOUNT_ID` repository secrets). You can also start it by hand from the Actions tab ("Run workflow"). Manual deploy from a computer:

```bash
npx wrangler pages deploy public --project-name imdev --branch main
```

Live at https://imdev.pages.dev
