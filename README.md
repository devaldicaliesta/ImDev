# ImDev

Personal site of **Devaldi Caliesta Octadiani** — Full Stack Developer & AI-Driven Engineer.

A single static page (`public/index.html`) with no build step, bilingual (EN / ID) and light / dark themes.

- `public/index.html` holds the markup, inline CSS and inline JS (theme / language toggles, kinetic type, ASCII field, focus panels).
- `public/nara-widget.css` restyles the embedded Nara chat widget (`<tanyasaya-chat>`) to match the site; it reads the page CSS variables, so dark mode follows automatically.

## Project map for AI agents (graphify)

A [graphify](https://github.com/safishamsi/graphify) knowledge graph of the repo lives in `graphify-out/`:

- `GRAPH_REPORT.md` lists the communities, hub nodes and every section / script with its line number. Read this first.
- `graph.json` is the raw graph; each node carries `source_file` and `source_location`.
- `graph.html` is an interactive view that opens in any browser.

```bash
graphify query "where is the chat widget language synced?"
graphify explain "Animated ASCII field"
graphify path "Language toggle button EN/ID [data-lang-toggle]" "Nara AI chat widget"
```

The site is HTML (a document for graphify), so after editing it, rebuild the graph through an agent with the graphify skill (`/graphify . --update`).

## Run locally

Open `public/index.html` in a browser, or serve the folder:

```bash
npx serve public
```

## Deploy (Cloudflare Pages)

```bash
npx wrangler pages deploy public --project-name imdev --branch main
```

Live at https://imdev.pages.dev
