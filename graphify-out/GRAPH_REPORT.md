# Graph Report - ImDev  (2026-11-04)

## Corpus Check
- Corpus is ~5,603 words - fits in a single context window. You may not need a graph.

## Summary
- 60 nodes · 113 edges · 6 communities
- Extraction: 89% EXTRACTED · 11% INFERRED · 0% AMBIGUOUS · INFERRED: 12 edges (avg confidence: 0.85)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- Theme, Language & Chat Sync
- Page Shell & Deploy Docs
- Hero, Motion & ASCII Art
- Profile, Education & Experience
- Focus Areas & Featured Projects
- Dinamis Enterprise Platforms

## God Nodes (most connected - your core abstractions)
1. `ImDev single-page site (public/index.html)` - 22 edges
2. `Main site script: theme/language toggles, mobile menu, focus panel activate(), footer year` - 11 edges
3. `Nara AI chat widget <tanyasaya-chat> — RAG chatbot answering from the Devaldi profile (bot qw92fe72dp, api nara.panduarahid.workers.dev); restyled by public/nara-widget.css using the site CSS variables` - 7 edges
4. `Selected Work section #work (featured + enterprise projects)` - 6 edges
5. `Experience section #experience` - 6 edges
6. `Design tokens: CSS custom properties (cream/olive palette, grid column vars)` - 5 edges
7. `Sticky header & navigation (desktop grid nav + mobile header)` - 5 edges
8. `Language toggle button EN/ID [data-lang-toggle]` - 5 edges
9. `Focus Areas section #focus: 6 hover/tap panels (Indoor Navigation, AI Engineering, Business Systems, Financial Apps, Automation, End-to-End)` - 5 edges
10. `Project PanduArah — zero-beacon indoor map & navigation PWA (own project)` - 5 edges

## Surprising Connections (you probably didn't know these)
- `Favicon: green rounded square with cream ImDev corner-bracket logo mark` --semantically_similar_to--> `ImDev logo mark (.logo-mark clip-path corner bracket)`  [INFERRED] [semantically similar]
  public/favicon.svg → public/index.html
- `ImDev single-page site (public/index.html)` --references--> `Favicon: green rounded square with cream ImDev corner-bracket logo mark`  [EXTRACTED]
  public/index.html → public/favicon.svg
- `ImDev README — personal site of Devaldi Caliesta Octadiani` --references--> `Devaldi Caliesta Octadiani (Dev) — site owner, Full Stack Developer & AI-Driven Engineer`  [EXTRACTED]
  README.md → public/index.html
- `Run locally: open public/index.html or npx serve public` --references--> `ImDev single-page site (public/index.html)`  [EXTRACTED]
  README.md → public/index.html
- `ImDev README — personal site of Devaldi Caliesta Octadiani` --references--> `ImDev single-page site (public/index.html)`  [EXTRACTED]
  README.md → public/index.html

## Hyperedges (group relationships)
- **Client-side interactions (theme, language, mobile menu, focus panels)** — public_index_site_script, public_index_boot_script, public_index_theme_toggle, public_index_language_toggle, public_index_mobile_menu, public_index_focus_activate, public_index_chat_sync [EXTRACTED 1.00]
- **Kinetic type & ASCII animation system (gated by prefers-reduced-motion)** — public_index_motion_gate, public_index_kinetic_type, public_index_word_scramble, public_index_ascii_field, public_index_contact_ascii [EXTRACTED 1.00]
- **PT Dinamis Infomadya enterprise portfolio** — public_index_exp_dinamis, public_index_asset_management, public_index_fixed_income, public_index_branch_info [EXTRACTED 1.00]

## Communities (6 total, 0 thin omitted)

### Community 0 - "Theme, Language & Chat Sync"
Cohesion: 0.25
Nodes (13): Bilingual EN/ID system: [lang] spans hidden via html[data-lang], Boot script: restores theme/language from localStorage (imdev-theme, imdev-lang) before paint, syncChat(l) — keeps the chat widget language in sync with the site EN/ID toggle (tanyasaya:lang + setLang), Nara AI chat widget <tanyasaya-chat> — RAG chatbot answering from the Devaldi profile (bot qw92fe72dp, api nara.panduarahid.workers.dev); restyled by public/nara-widget.css using the site CSS variables, Dark theme palette (html[data-theme="dark"]), Design tokens: CSS custom properties (cream/olive palette, grid column vars), Sticky header & navigation (desktop grid nav + mobile header), Language toggle button EN/ID [data-lang-toggle] (+5 more)

### Community 1 - "Page Shell & Deploy Docs"
Cohesion: 0.18
Nodes (13): Footer (copyright year, back to top), Kinetic type: hero IMDEV letter rise + cursor stretch, word-by-word heading reveal on scroll, outline/solid ticker words, ImDev single-page site (public/index.html), SEO & Open Graph meta tags (title, description, og:*), Tech stack ticker (Claude Code, TypeScript, C#/.NET, Cloudflare Edge, MapLibre GL...), Technical Toolbox section #toolbox: 6 skill categories, Strengths & Current Interests section, What I Do section #services: 8 numbered service items (+5 more)

### Community 2 - "Hero, Motion & ASCII Art"
Cohesion: 0.24
Nodes (10): Favicon: green rounded square with cream ImDev corner-bracket logo mark, Animated ASCII field (imdev.ascii): plasma density ramp with the ImDev logo mark dissolving in and out, cursor/tap ripple, pauses off-screen, Hero code card imdev.ts (profile as a TypeScript object), Contact section #contact: email devaldicaliesta@gmail.com, LinkedIn, West Jakarta, Contact deco ASCII loops (| / -  spinner, >>> arrow, [===] bar), Devaldi Caliesta Octadiani (Dev) — site owner, Full Stack Developer & AI-Driven Engineer, Hero / masthead #top: IMDEV title, name, role, tagline, Email & LinkedIn CTAs, Kinetic band .kin: outlined "I build" + scrambling word rotator (Business Systems, Indoor Navigation, Financial Platforms, RAG Chatbots, Real-time Games, Automations) beside the ASCII field (+2 more)

### Community 3 - "Profile, Education & Experience"
Cohesion: 0.32
Nodes (8): About section #about "Behind The Code" (bio + professional quote), About tiles: GPA 3.79, AI Proficiency (AI-Driven Engineering), Current Role, Education: Ahmad Dahlan University, S.Kom Information Systems, GPA 3.79 Cum Laude, Experience: Full Stack Developer at PT Clipan Finance Indonesia Tbk (Jun 2026 – present, front-end work), Experience: Laboratory Assistant, Information Systems Laboratory UAD (Mar 2022 – Jul 2023), Experience: Internship Full Stack Developer at CV Lumintu Logic (Feb 2022 – Jul 2022), Experience section #experience, Person JSON-LD schema (name, jobTitle, worksFor, alumniOf, sameAs LinkedIn)

### Community 4 - "Focus Areas & Featured Projects"
Cohesion: 0.46
Nodes (8): activate(i) — switches active focus item and panel, Focus Areas section #focus: 6 hover/tap panels (Indoor Navigation, AI Engineering, Business Systems, Financial Apps, Automation, End-to-End), Project Mapping Lippo Mall Puri — indoor mall navigation (freelance), Project Nara / MeetNaraBot — RAG document chatbot on Cloudflare Workers (own project), Project PanduArah — zero-beacon indoor map & navigation PWA (own project), Project PinkPonk — real-time 3D neon ping pong on Durable Objects (own project), Project SVG illustrations (.art classes: floor plan, chat, table, stacked floors), Selected Work section #work (featured + enterprise projects)

### Community 5 - "Dinamis Enterprise Platforms"
Cohesion: 0.53
Nodes (6): Enterprise project Asset Management Platform (ASP.NET Core, Blazor, PostgreSQL, YARP), Enterprise project Branch Information System (operations reporting), Enterprise Platforms grid (ent-card panels with expandable highlights), Experience: Full Stack Developer at PT Dinamis Infomadya (May 2024 – 2026), Enterprise project Fixed Income Platform (bonds workflow, ETL cron, Open API), Enterprise project Visitor Website Revamp & CMS (CodeIgniter 4)

## Knowledge Gaps
- **8 isolated node(s):** `Live site https://imdev.pages.dev`, `robots.txt — allow all crawlers`, `What I Do section #services: 8 numbered service items`, `Enterprise project Visitor Website Revamp & CMS (CodeIgniter 4)`, `Experience: Laboratory Assistant, Information Systems Laboratory UAD (Mar 2022 – Jul 2023)` (+3 more)
  These have ≤1 connection - possible missing edges or undocumented components. (Counts symbols only; 8 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `ImDev single-page site (public/index.html)` connect `Page Shell & Deploy Docs` to `Theme, Language & Chat Sync`, `Hero, Motion & ASCII Art`, `Profile, Education & Experience`, `Focus Areas & Featured Projects`?**
  _High betweenness centrality (0.658) - this node is a cross-community bridge._
- **Are the 3 inferred relationships involving `Nara AI chat widget <tanyasaya-chat> — RAG chatbot answering from the Devaldi profile (bot qw92fe72dp, api nara.panduarahid.workers.dev); restyled by public/nara-widget.css using the site CSS variables` (e.g. with `Dark theme palette (html[data-theme="dark"])` and `Design tokens: CSS custom properties (cream/olive palette, grid column vars)`) actually correct?**
  _`Nara AI chat widget <tanyasaya-chat> — RAG chatbot answering from the Devaldi profile (bot qw92fe72dp, api nara.panduarahid.workers.dev); restyled by public/nara-widget.css using the site CSS variables` has 3 INFERRED edges - model-reasoned connections that need verification._
- **What connects `Live site https://imdev.pages.dev`, `robots.txt — allow all crawlers`, `What I Do section #services: 8 numbered service items` to the rest of the system?**
  _8 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Why does `Selected Work section #work (featured + enterprise projects)` connect `Focus Areas & Featured Projects` to `Page Shell & Deploy Docs`, `Dinamis Enterprise Platforms`?**
  _High betweenness centrality (0.162) - this node is a cross-community bridge._
- **Why does `Experience section #experience` connect `Profile, Education & Experience` to `Page Shell & Deploy Docs`, `Dinamis Enterprise Platforms`?**
  _High betweenness centrality (0.157) - this node is a cross-community bridge._