# Graph Report - ImDev  (2026-11-20)

## Corpus Check
- 1 files · ~7,687 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 130 nodes · 350 edges · 7 communities
- Extraction: 76% EXTRACTED · 24% INFERRED · 0% AMBIGUOUS · INFERRED: 83 edges (avg confidence: 0.91)
- Token cost: 310,403 input · 0 output

## Community Hubs (Navigation)
- Motion, Hero & Layout Engine
- Work, Stack & What I Build
- Project Rules & Language
- Pages Deploy Workflow
- Contact, Experience & Navigation
- Identity, Images & Footer
- Favicon Brand Mark

## God Nodes (most connected - your core abstractions)
1. `ImDev single-page site (public/index.html)` - 27 edges
2. `Main inline site script (IIFE): helpers ($, $$, save, clamp, lerp, lang, pad, rnd), feature flags (motionOK, hasIO, fine, sda) and all page behavior` - 24 edges
3. `public/index.html: markup, inline CSS and inline JS (theme/language toggles, nav menu, kinetic type: headline scramble and cursor stretch, "I build" word rotator, ASCII field, ticker, flying portrait card, folder dialogs, wave timeline, contact form, footer band), all motion gated by prefers-reduced-motion` - 19 edges
4. `motionOK — prefers-reduced-motion gate (with the boot script's js-motion class and the CSS override): no scramble, cursor stretch, word rotation, ASCII animation, scroll-driven ticker, flying portrait, parallax, reveals, band motion or View Transition under reduced motion` - 19 edges
5. `Site layout (dark monochrome portfolio): floating nav pill, < FULL STACK DEVELOPER /> hero whose portrait card flips into About on scroll, kinetic "I build ___" band next to an animated ASCII field, scroll-driven tech ticker, staggered tech stack, project folders with case-study dialogs, wave experience timeline (oldest left, current role right), email-draft contact form, white footer band with ink illustration before a giant name` - 18 edges
6. `Flying portrait card (.fly): two-faced clone of img/portrait.webp (.fly-f / .fly-b with backface-visibility hidden) that travels from slot a (hero) into slot b (About), flipping once on the way; driven by a CSS scroll-driven animation (.fly.sda) where supported, by renderFly on mouse/trackpad browsers without it, while touch browsers without it keep the two static cards` - 14 edges
7. `Hero section #top: < FULL STACK / DEVELOPER /> headline, portrait card (slot a), ImDev label and {{ AI-Driven Engineering }} tag over a film-grain layer` - 13 edges
8. `Case-study dialog #case: 01 / 08 counter, close button, eight hidden .cs articles (badge, title, summary, highlights, [data-art] slot, stack chips, optional site link), Previous / Next` - 12 edges
9. `Kinetic I build band section #build [data-kin]: // what i build label, outlined I build (Saya membangun) lead that wraps only between words, rotating focus word, six dots with a 01 / 06 index, cursor or tap hint, and a dark ASCII terminal card (imdev.ascii · cols×rows header)` - 12 edges
10. `ImDev README: personal site of Devaldi Caliesta Octadiani (Full Stack Developer & AI-Driven Engineer), one static page, no build step, bilingual EN/ID, dark by default with a light theme` - 11 edges

## Surprising Connections (you probably didn't know these)
- `Manual deploy: npx wrangler pages deploy public --project-name imdev --branch main` --semantically_similar_to--> `command`  [INFERRED] [semantically similar]
  README.md → .github/workflows/deploy.yml
- `Deploy to Cloudflare Pages: every push to main deploys through .github/workflows/deploy.yml, or start it by hand from the Actions tab (Run workflow)` --references--> `workflow_dispatch`  [INFERRED]
  README.md → .github/workflows/deploy.yml
- `Deploy to Cloudflare Pages: every push to main deploys through .github/workflows/deploy.yml, or start it by hand from the Actions tab (Run workflow)` --references--> `push`  [INFERRED]
  README.md → .github/workflows/deploy.yml
- `Repository secrets CLOUDFLARE_API_TOKEN and CLOUDFLARE_ACCOUNT_ID (required by the deploy workflow)` --shares_data_with--> `accountId`  [INFERRED]
  README.md → .github/workflows/deploy.yml
- `Repository secrets CLOUDFLARE_API_TOKEN and CLOUDFLARE_ACCOUNT_ID (required by the deploy workflow)` --shares_data_with--> `apiToken`  [INFERRED]
  README.md → .github/workflows/deploy.yml

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **ImDev site-editing rules (CLAUDE.md ## ImDev)** — claude_imdev_project_rules, claude_index_html_graph_rebuild_rule, claude_bilingual_text_rule, claude_reduced_motion_rule [EXTRACTED 1.00]
- **Cloudflare Pages deploy flow (push to main or manual wrangler run, repository secrets, live site)** — readme_deploy_cloudflare_pages, readme_cloudflare_secrets, readme_manual_deploy, readme_live_site, github_workflows_deploy [EXTRACTED 1.00]
- **Reduced-motion gating: the CLAUDE.md rule and its three layers in index.html (boot script js-motion class, prefers-reduced-motion CSS override, motionOK JS gate)** — claude_reduced_motion_rule, public_index_boot_script, public_index_reduced_motion_css, public_index_motion_gate [INFERRED 0.85]
- **Portrait fly-and-flip scroll transition: the same portrait travels from the hero card (slot A) to the About card (slot B), flipping once, only when motionOK (prefers-reduced-motion) allows it** — public_index_hero, public_img_portrait, public_index_about, public_index_motion_gate [INFERRED 0.95]
- **EN/ID language switch flow: persisted imdev-lang, [lang] visibility, attribute swap, chat widget sync, clock suffix, rotating I build word reset and relayout** — public_index_boot_script, public_index_language_toggle, public_index_bilingual_system, public_index_sync_attrs, public_index_sync_theme, public_index_chat_sync, public_index_chat_widget, public_index_jakarta_clock, public_index_word_rotator, public_index_relayout [EXTRACTED 1.00]
- **Enterprise reporting pattern: live browser preview with Excel and PDF export on the ASP.NET Core / Blazor stack (PT Dinamis Infomadya platforms)** — public_index_asset_management, public_index_fixed_income, public_index_branch_info, public_index_dotnet_stack, public_index_exp_dinamis [INFERRED 0.85]
- **Split-text staggered reveal pattern: hero headline letters (--d), [data-words] heading words (--i), footer DEVALDI letters (--i)** — public_index_headline_scramble, public_index_scramble_in, public_index_scroll_reveals, public_index_band_motion [INFERRED 0.85]

## Communities (7 total, 0 thin omitted)

### Community 0 - "Motion, Hero & Layout Engine"
Cohesion: 0.19
Nodes (28): Animated ASCII field [data-ascii]: two stacked pre layers draw plasma noise through a density ramp ( .:-=+*#%@) at about 24 fps with a mouse and 15 fps on touch, with the ImDev mark dissolving in and out on the bright layer and a cursor or tap ripple; sized to the card (cols×rows in the header), held still while the page scrolls, paused off-screen or in a hidden tab, one static frame under reduced motion, Font and image preloads: Google Fonts Plus Jakarta Sans (wght 300-800) + Inter (wght 400-700), img/portrait.webp, Back-to-top replay: #top links arm a flag past half a viewport; once the hero is 70% visible again, scrambleIn() and the fly card intro replay, Footer band motion: DEVALDI letters rise in on view, the illustration steps up, and word and illustration drift with the pointer (--mx / --my) on fine pointers, Cursor-stretch kinetic type stretch(zone, letters, amp): letters near the mouse stretch vertically through --sy (CSS scale on .ht-c and .kc), batched in requestAnimationFrame; applied to the hero headline letters (amp .2) and the I build letters (.kc, grouped per word in no-wrap .kn boxes; amp .24); fine pointers and motionOK only, Design tokens: :root CSS custom properties (dark default palette, Plus Jakarta Sans display and Inter sans fonts, mono stack, --px gutter, --maxw, --ease), drawWave(): cubic Bezier path through the timeline node centres, sets the SVG viewBox and --len for the stroke-draw animation, skipped while the wave is hidden, Flying portrait card (.fly): two-faced clone of img/portrait.webp (.fly-f / .fly-b with backface-visibility hidden) that travels from slot a (hero) into slot b (About), flipping once on the way; driven by a CSS scroll-driven animation (.fly.sda) where supported, by renderFly on mouse/trackpad browsers without it, while touch browsers without it keep the two static cards (+20 more)

### Community 1 - "Work, Stack & What I Build"
Cohesion: 0.16
Nodes (27): About section #about: Hi, I'm Dev; role; currently at PT Clipan Finance Indonesia Tbk since Jun 2026; West Jakarta; portrait slot b; lead copy; Explore projects button, Asset Management Platform — legacy-to-web modernization (greenfield structure, reporting with web preview + Excel/PDF, portfolio and accounting modules, YARP gateway; enterprise); case study cs4, folder data-case=4, Branch Information System — centralized branch operations and executive monitoring (multi-metric reporting, scheduled Excel/PDF export; enterprise); case study cs6, folder data-case=6, Case-study dialog #case: 01 / 08 counter, close button, eight hidden .cs articles (badge, title, summary, highlights, [data-art] slot, stack chips, optional site link), Previous / Next, Case-study dialog controller: show(i) wraps the index, shows one article, sets aria-labelledby, clones the folder SVG into [data-art] once, updates the counter; showModal + modal-open scroll lock; close button and backdrop; focus back to the folder; Prev / Next and arrow keys, Cloudflare edge platform (Workers, Durable Objects, D1 SQLite FTS5, Vectorize, Workers AI), ASP.NET Core / C# / Blazor enterprise stack (with PostgreSQL or SQL Server, Redis, IIS), Project group: Enterprise platforms (Asset Management, Fixed Income, Branch Information, Visitor Website & CMS) (+19 more)

### Community 2 - "Project Rules & Language"
Cohesion: 0.21
Nodes (14): graphify skill trigger: /graphify runs the installed skill (.claude/skills/graphify/SKILL.md, any input to knowledge graph) before anything else, Boot script: restores theme (imdev-theme-v2) and language (imdev-lang, navigator.language fallback) before paint, adds js-motion when reduced motion is off, syncChat(l, tries): keeps the Nara chat widget language in sync with the site EN/ID toggle (tanyasaya:lang, waits for the custom element, retries while busy, setLang / fetchInfo), Nara AI chat widget <tanyasaya-chat> embed (bot ns29ieww7m, api-base nara.panduarahid.workers.dev, css nara-widget.css) loaded by the deferred widget.js, Language toggle button EN/ID [data-lang-toggle]: flips html data-lang, saves imdev-lang, then runs syncAttrs, syncChat, tickClock, kinReset and relayout, ImDev single-page site (public/index.html), syncAttrs(): applies language-specific placeholders (data-ph-*), aria-labels (data-al-*) and alt text (data-alt-*), then syncTheme(), robots.txt: User-agent * Allow / (every crawler may index the whole site) (+6 more)

### Community 3 - "Pages Deploy Workflow"
Cohesion: 0.11
Nodes (19): permissions, runs-on, steps, jobs, deploy, name, on, push (+11 more)

### Community 4 - "Contact, Experience & Navigation"
Cohesion: 0.20
Nodes (15): Contact section #contact: Let's talk, mailto link, copy-email button, LinkedIn, West Jakarta GMT+7, email-draft form, Copy email button [data-copy]: Clipboard API with execCommand fallback and a bilingual aria-live status, Education: Bachelor of Information Systems (S.Kom), Ahmad Dahlan University, 2019-2023, GPA 3.79 Cum Laude, GDSC core member and head lab assistant, Email address devaldicaliesta@gmail.com (JSON-LD, menu CTA, contact link and copy button, footer, mailto draft), Contact email-draft form [data-draft]: validates name, email and message, then opens a prefilled mailto draft with a bilingual subject (no backend), Current role: Full Stack Developer, PT Clipan Finance Indonesia Tbk (Jun 2026 - present): Multipurpose Ticketing front end in a Scrum team (Jira, Azure), Laboratory Assistant, Information Systems Laboratory UAD (Mar 2022 - Jul 2023): programming, algorithms and data mining practicums, Internship Full Stack Developer, CV Lumintu Logic (Feb-Jul 2022): LMS front end, relational database design, SQL, payment gateway module (+7 more)

### Community 5 - "Identity, Images & Footer"
Cohesion: 0.22
Nodes (11): figure.webp - full-length ink illustration of Devaldi taking a mirror selfie (glasses, open black shirt over white tee, backpack, wide black trousers, white sneakers), used as the footer band figure, Monochrome pen-and-ink hatching style with transparent cut-out background, portrait.webp - black-and-white chest-up photo of Devaldi smiling (dark wavy hair, black rectangular glasses, light crew-neck tee) on a flat white background, used as the hero and About portrait card, Monochrome photo-card style (grayscale photo on an opaque flat white background, no transparency), Devaldi Caliesta Octadiani (Dev) — site owner, Full Stack Developer & AI-Driven Engineer in West Jakarta, Footer: ImDev. logo and role, Explore links, Get in touch (email, LinkedIn), See you around, Back to top, white name band, Footer band [data-band]: giant DEVALDI word, ink mirror-selfie illustration (img/figure.webp), © year and West Jakarta clock notes, tickClock(): Jakarta local time (Asia/Jakarta, 24h) with a WIB / GMT+7 suffix, refreshed every 30s and on language change (+3 more)

### Community 6 - "Favicon Brand Mark"
Cohesion: 0.67
Nodes (3): ImDev Favicon Mark, Near-Black Rounded Square (#141414), Off-White Corner Bracket Glyph (#f1f1ee)

## Ambiguous Edges - Review These
- `Full Stack Developer, PT Dinamis Infomadya (May 2024 - 2026): enterprise back-office, financial modules, reporting engines, cron ETL, API integrations` → `Visitor Website Revamp & CMS — legacy PHP migrated to CodeIgniter 4 MVC with a faster responsive frontend and refactored CMS (enterprise); case study cs7, folder data-case=7`  [AMBIGUOUS]
  public/index.html · relation: conceptually_related_to

## Knowledge Gaps
- **3 isolated node(s):** `Near-Black Rounded Square (#141414)`, `Off-White Corner Bracket Glyph (#f1f1ee)`, `Internship Full Stack Developer, CV Lumintu Logic (Feb-Jul 2022): LMS front end, relational database design, SQL, payment gateway module`
  These have ≤1 connection - possible missing edges or undocumented components. (Counts symbols only; 9 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `ImDev single-page site (public/index.html)` connect `Project Rules & Language` to `Motion, Hero & Layout Engine`, `Work, Stack & What I Build`, `Contact, Experience & Navigation`, `Identity, Images & Footer`?**
  _High betweenness centrality (0.303) - this node is a cross-community bridge._
- **Are the 2 inferred relationships involving `ImDev single-page site (public/index.html)` (e.g. with `robots.txt: User-agent * Allow / (every crawler may index the whole site)` and `README rebuild note: the site is HTML (a graphify document), so rebuild the graph through an agent with the graphify skill (/graphify . --update) after editing`) actually correct?**
  _`ImDev single-page site (public/index.html)` has 2 INFERRED edges - model-reasoned connections that need verification._
- **What connects `Near-Black Rounded Square (#141414)`, `Off-White Corner Bracket Glyph (#f1f1ee)`, `Internship Full Stack Developer, CV Lumintu Logic (Feb-Jul 2022): LMS front end, relational database design, SQL, payment gateway module` to the rest of the system?**
  _3 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `Pages Deploy Workflow` be split into smaller, more focused modules?**
  _Cohesion score 0.10526315789473684 - nodes in this community are weakly interconnected._
- **Why does `Deploy to Cloudflare Pages: every push to main deploys through .github/workflows/deploy.yml, or start it by hand from the Actions tab (Run workflow)` connect `Project Rules & Language` to `Pages Deploy Workflow`?**
  _High betweenness centrality (0.267) - this node is a cross-community bridge._
- **Are the 17 inferred relationships involving `public/index.html: markup, inline CSS and inline JS (theme/language toggles, nav menu, kinetic type: headline scramble and cursor stretch, "I build" word rotator, ASCII field, ticker, flying portrait card, folder dialogs, wave timeline, contact form, footer band), all motion gated by prefers-reduced-motion` (e.g. with `Reduced-motion rule: keep all motion gated by prefers-reduced-motion` and `Animated ASCII field [data-ascii]: two stacked pre layers draw plasma noise through a density ramp ( .:-=+*#%@) at about 24 fps with a mouse and 15 fps on touch, with the ImDev mark dissolving in and out on the bright layer and a cursor or tap ripple; sized to the card (cols×rows in the header), held still while the page scrolls, paused off-screen or in a hidden tab, one static frame under reduced motion`) actually correct?**
  _`public/index.html: markup, inline CSS and inline JS (theme/language toggles, nav menu, kinetic type: headline scramble and cursor stretch, "I build" word rotator, ASCII field, ticker, flying portrait card, folder dialogs, wave timeline, contact form, footer band), all motion gated by prefers-reduced-motion` has 17 INFERRED edges - model-reasoned connections that need verification._

### Low-confidence Hints
_AMBIGUOUS edges — the extractor was unsure. Verify before acting on these._

- **What is the exact relationship between `Full Stack Developer, PT Dinamis Infomadya (May 2024 - 2026): enterprise back-office, financial modules, reporting engines, cron ETL, API integrations` and `Visitor Website Revamp & CMS — legacy PHP migrated to CodeIgniter 4 MVC with a faster responsive frontend and refactored CMS (enterprise); case study cs7, folder data-case=7`?**
  _Edge tagged AMBIGUOUS (relation: conceptually_related_to) - confidence is low._