# Graph Report - ImDev  (2026-11-12)

## Corpus Check
- 8 files · ~6,605 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 84 nodes · 138 edges · 8 communities
- Extraction: 84% EXTRACTED · 16% INFERRED · 0% AMBIGUOUS · INFERRED: 22 edges (avg confidence: 0.85)
- Token cost: 201,932 input · 0 output

## Community Hubs (Navigation)
- Pages Deploy Workflow
- Hero, Identity & SEO
- Motion, Language & Project Rules
- Theme, Layout & Navigation
- Focus Areas & Featured Projects
- Profile, Education & Experience
- Dinamis Enterprise Platforms
- Favicon Brand Mark

## God Nodes (most connected - your core abstractions)
1. `ImDev single-page site (public/index.html)` - 23 edges
2. `Main site script: theme/language toggles, mobile menu, focus panel activate(), footer year` - 9 edges
3. `motionOK — prefers-reduced-motion gate: disables kinetic type, scramble, ASCII loop and deco animation` - 8 edges
4. `ImDev README — personal site of Devaldi Caliesta Octadiani` - 7 edges
5. `Nara AI chat widget <tanyasaya-chat> — RAG chatbot answering from the Devaldi profile (bot 3k5k34xk3c, api nara.panduarahid.workers.dev); restyled by public/nara-widget.css using the site CSS variables` - 7 edges
6. `Bilingual EN/ID system: [lang] spans hidden via html[data-lang]` - 6 edges
7. `Language toggle button EN/ID [data-lang-toggle]` - 6 edges
8. `Selected Work section #work (featured + enterprise projects)` - 6 edges
9. `Experience section #experience` - 6 edges
10. `ImDev project rules: static site, no build step; bilingual EN/ID text; motion gated by prefers-reduced-motion` - 5 edges

## Surprising Connections (you probably didn't know these)
- `graphify skill trigger (/graphify uses .claude/skills/graphify/SKILL.md)` --conceptually_related_to--> `graphify usage rules: query/path/explain before grep, update after code changes, graph.json diffs expected`  [INFERRED]
  .claude/CLAUDE.md → CLAUDE.md
- `ImDev project rules: static site, no build step; bilingual EN/ID text; motion gated by prefers-reduced-motion` --references--> `graphify skill trigger (/graphify uses .claude/skills/graphify/SKILL.md)`  [EXTRACTED]
  CLAUDE.md → .claude/CLAUDE.md
- `ImDev project rules: static site, no build step; bilingual EN/ID text; motion gated by prefers-reduced-motion` --rationale_for--> `Bilingual EN/ID system: [lang] spans hidden via html[data-lang]`  [INFERRED]
  CLAUDE.md → public/index.html
- `ImDev project rules: static site, no build step; bilingual EN/ID text; motion gated by prefers-reduced-motion` --rationale_for--> `motionOK — prefers-reduced-motion gate: disables kinetic type, scramble, ASCII loop and deco animation`  [INFERRED]
  CLAUDE.md → public/index.html
- `ImDev project rules: static site, no build step; bilingual EN/ID text; motion gated by prefers-reduced-motion` --references--> `ImDev single-page site (public/index.html)`  [EXTRACTED]
  CLAUDE.md → public/index.html

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **Animations gated by prefers-reduced-motion (motionOK + CSS media query)** — public_index_motion_gate, public_index_kinetic_type, public_index_word_scramble, public_index_ascii_field, public_index_contact_ascii, public_index_ticker, public_index_project_illustrations [EXTRACTED 1.00]
- **EN/ID language switch flow (persisted lang, [lang] visibility, chat widget sync, scramble reset)** — public_index_boot_script, public_index_language_toggle, public_index_bilingual_system, public_index_chat_sync, public_index_chat_widget, public_index_word_scramble [EXTRACTED 1.00]
- **Indoor navigation work (PanduArah, Lippo Mall Puri, Focus 01)** — public_index_panduarah, public_index_lippo, public_index_focus_section [INFERRED 0.85]

## Communities (8 total, 0 thin omitted)

### Community 0 - "Pages Deploy Workflow"
Cohesion: 0.11
Nodes (17): permissions, runs-on, steps, jobs, deploy, name, on, push (+9 more)

### Community 1 - "Hero, Identity & SEO"
Cohesion: 0.19
Nodes (15): Hero code card imdev.ts (profile as a TypeScript object), Contact section #contact: email devaldicaliesta@gmail.com, LinkedIn, West Jakarta, Devaldi Caliesta Octadiani (Dev) — site owner, Full Stack Developer & AI-Driven Engineer, Hero / masthead #top: IMDEV title, name, role, tagline, Email & LinkedIn CTAs, Kinetic type: hero IMDEV letter rise + cursor stretch, word-by-word heading reveal on scroll, outline/solid ticker words, ImDev single-page site (public/index.html), Person JSON-LD schema (name, jobTitle, worksFor, alumniOf, sameAs LinkedIn), SEO & Open Graph meta tags (title, description, og:*) (+7 more)

### Community 2 - "Motion, Language & Project Rules"
Cohesion: 0.25
Nodes (12): graphify skill trigger (/graphify uses .claude/skills/graphify/SKILL.md), Animated ASCII field (imdev.ascii): plasma density ramp with the ImDev logo mark dissolving in and out, cursor/tap ripple, pauses off-screen, Bilingual EN/ID system: [lang] spans hidden via html[data-lang], syncChat(l) — keeps the chat widget language in sync with the site EN/ID toggle (tanyasaya:lang + setLang), Nara AI chat widget <tanyasaya-chat> — RAG chatbot answering from the Devaldi profile (bot 3k5k34xk3c, api nara.panduarahid.workers.dev); restyled by public/nara-widget.css using the site CSS variables, Contact deco ASCII loops (| / -  spinner, >>> arrow, [===] bar), Kinetic band .kin: outlined "I build" + scrambling word rotator (Business Systems, Indoor Navigation, Financial Platforms, RAG Chatbots, Real-time Games, Automations) beside the ASCII field, Language toggle button EN/ID [data-lang-toggle] (+4 more)

### Community 3 - "Theme, Layout & Navigation"
Cohesion: 0.20
Nodes (11): Boot script: restores theme/language from localStorage (imdev-theme, imdev-lang) before paint, Dark theme palette (html[data-theme="dark"]), Design tokens: CSS custom properties (cream/olive palette, grid column vars), activate(i) — switches active focus item and panel, Footer (copyright year, back to top), Sticky header & navigation (desktop grid nav + mobile header), ImDev logo mark (.logo-mark clip-path corner bracket), Mobile menu #m-nav with hamburger [data-menu-toggle] (+3 more)

### Community 4 - "Focus Areas & Featured Projects"
Cohesion: 0.43
Nodes (8): Focus Areas section #focus: 6 hover/tap panels (Indoor Navigation, AI Engineering, Business Systems, Financial Apps, Automation, End-to-End), Project Mapping Lippo Mall Puri — indoor mall navigation (freelance), Project Nara / MeetNaraBot — RAG document chatbot on Cloudflare Workers (own project), Project PanduArah — zero-beacon indoor map & navigation PWA (own project), Project PinkPonk — real-time 3D neon ping pong on Durable Objects (own project), Project SVG illustrations (.art classes: floor plan, chat, table, stacked floors), What I Do section #services: 8 numbered service items, Selected Work section #work (featured + enterprise projects)

### Community 5 - "Profile, Education & Experience"
Cohesion: 0.38
Nodes (7): About section #about "Behind The Code" (bio + professional quote), About tiles: GPA 3.79, AI Proficiency (AI-Driven Engineering), Current Role, Education: Ahmad Dahlan University, S.Kom Information Systems, GPA 3.79 Cum Laude, Experience: Full Stack Developer at PT Clipan Finance Indonesia Tbk (Jun 2026 – present, front-end work), Experience: Laboratory Assistant, Information Systems Laboratory UAD (Mar 2022 – Jul 2023), Experience: Internship Full Stack Developer at CV Lumintu Logic (Feb 2022 – Jul 2022), Experience section #experience

### Community 6 - "Dinamis Enterprise Platforms"
Cohesion: 0.47
Nodes (6): Enterprise project Asset Management Platform (ASP.NET Core, Blazor, PostgreSQL, YARP), Enterprise project Branch Information System (operations reporting), Enterprise Platforms grid (ent-card panels with expandable highlights), Experience: Full Stack Developer at PT Dinamis Infomadya (May 2024 – 2026), Enterprise project Fixed Income Platform (bonds workflow, ETL cron, Open API), Enterprise project Visitor Website Revamp & CMS (CodeIgniter 4)

### Community 7 - "Favicon Brand Mark"
Cohesion: 0.50
Nodes (4): ImDev Brand Palette (olive green and cream), Cream Corner Glyph (#fffaf0), ImDev Favicon Mark, Olive Green Rounded Square (#5c7a2b)

## Knowledge Gaps
- **8 isolated node(s):** `Live site https://imdev.pages.dev`, `Responsive breakpoints (860px mobile switch; 1200/1100/640/560px grid steps)`, `Enterprise project Visitor Website Revamp & CMS (CodeIgniter 4)`, `Experience: Internship Full Stack Developer at CV Lumintu Logic (Feb 2022 – Jul 2022)`, `Strengths & Current Interests section` (+3 more)
  These have ≤1 connection - possible missing edges or undocumented components. (Counts symbols only; 19 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `ImDev single-page site (public/index.html)` connect `Hero, Identity & SEO` to `Motion, Language & Project Rules`, `Theme, Layout & Navigation`, `Focus Areas & Featured Projects`, `Profile, Education & Experience`?**
  _High betweenness centrality (0.358) - this node is a cross-community bridge._
- **Are the 2 inferred relationships involving `Nara AI chat widget <tanyasaya-chat> — RAG chatbot answering from the Devaldi profile (bot 3k5k34xk3c, api nara.panduarahid.workers.dev); restyled by public/nara-widget.css using the site CSS variables` (e.g. with `Design tokens: CSS custom properties (cream/olive palette, grid column vars)` and `Project Nara / MeetNaraBot — RAG document chatbot on Cloudflare Workers (own project)`) actually correct?**
  _`Nara AI chat widget <tanyasaya-chat> — RAG chatbot answering from the Devaldi profile (bot 3k5k34xk3c, api nara.panduarahid.workers.dev); restyled by public/nara-widget.css using the site CSS variables` has 2 INFERRED edges - model-reasoned connections that need verification._
- **What connects `Live site https://imdev.pages.dev`, `Responsive breakpoints (860px mobile switch; 1200/1100/640/560px grid steps)`, `Enterprise project Visitor Website Revamp & CMS (CodeIgniter 4)` to the rest of the system?**
  _8 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `Pages Deploy Workflow` be split into smaller, more focused modules?**
  _Cohesion score 0.1111111111111111 - nodes in this community are weakly interconnected._
- **Why does `Selected Work section #work (featured + enterprise projects)` connect `Focus Areas & Featured Projects` to `Hero, Identity & SEO`, `Dinamis Enterprise Platforms`?**
  _High betweenness centrality (0.085) - this node is a cross-community bridge._
- **Why does `Experience section #experience` connect `Profile, Education & Experience` to `Hero, Identity & SEO`, `Dinamis Enterprise Platforms`?**
  _High betweenness centrality (0.083) - this node is a cross-community bridge._