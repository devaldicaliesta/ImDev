# Graph Report - ImDev  (2026-11-20)

## Corpus Check
- 10 files · ~6,858 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 128 nodes · 331 edges · 7 communities
- Extraction: 75% EXTRACTED · 25% INFERRED · 0% AMBIGUOUS · INFERRED: 82 edges (avg confidence: 0.91)
- Token cost: 1,279,144 input · 0 output

## Community Hubs (Navigation)
- Project Rules, Theme & Language
- Motion, Kinetic Type & Hero
- Work, Stack & What I Build
- Identity, Contact & Experience
- Pages Deploy Workflow
- Project Folders & Dialog UI
- Favicon Brand Mark

## God Nodes (most connected - your core abstractions)
1. `ImDev single-page site (public/index.html)` - 27 edges
2. `Main inline site script (IIFE): helpers ($, $$, save, clamp, lerp, lang, pad, rnd), feature flags (motionOK, hasIO, fine) and all page behavior` - 22 edges
3. `public/index.html: markup, inline CSS and inline JS (theme/language toggles, nav menu, kinetic type: headline scramble and cursor stretch, "I build" word rotator, ASCII field, ticker, flying portrait card, folder dialogs, wave timeline, contact form, footer band), all motion gated by prefers-reduced-motion` - 19 edges
4. `Site layout (dark monochrome portfolio): floating nav pill, < FULL STACK DEVELOPER /> hero whose portrait card flips into About on scroll, kinetic "I build ___" band next to an animated ASCII field, scroll-driven tech ticker, staggered tech stack, project folders with case-study dialogs, wave experience timeline (oldest left, current role right), email-draft contact form, white footer band with ink illustration before a giant name` - 18 edges
5. `motionOK — prefers-reduced-motion gate (with the boot script's js-motion class and the CSS override): no scramble, cursor stretch, word rotation, ASCII animation, scroll-driven ticker, flying portrait, parallax, reveals, band motion or View Transition under reduced motion` - 16 edges
6. `Flying portrait card (.fly): clone of img/portrait.webp that travels from slot a (hero) into slot b (About), flipping once on the way` - 12 edges
7. `Case-study dialog #case: 01 / 08 counter, close button, eight hidden .cs articles (badge, title, summary, highlights, [data-art] slot, stack chips, optional site link), Previous / Next` - 12 edges
8. `Kinetic I build band section #build [data-kin]: // what i build label, outlined I build (Saya membangun) lead, rotating focus word, six dots with a 01 / 06 index, cursor or tap hint, and a dark ASCII terminal card (imdev.ascii · cols×rows header)` - 12 edges
9. `Language toggle button EN/ID [data-lang-toggle]: flips html data-lang, saves imdev-lang, then runs syncAttrs, syncChat, tickClock, kinReset and relayout` - 11 edges
10. `About section #about: Hi, I'm Dev; role; currently at PT Clipan Finance Indonesia Tbk since Jun 2026; West Jakarta; portrait slot b; lead copy; Explore projects button` - 11 edges

## Surprising Connections (you probably didn't know these)
- `Manual deploy: npx wrangler pages deploy public --project-name imdev --branch main` --semantically_similar_to--> `command`  [INFERRED] [semantically similar]
  README.md → .github/workflows/deploy.yml
- `Deploy to Cloudflare Pages: every push to main deploys through .github/workflows/deploy.yml, or start it by hand from the Actions tab (Run workflow)` --references--> `workflow_dispatch`  [INFERRED]
  README.md → .github/workflows/deploy.yml
- `Deploy to Cloudflare Pages: every push to main deploys through .github/workflows/deploy.yml, or start it by hand from the Actions tab (Run workflow)` --references--> `push`  [INFERRED]
  README.md → .github/workflows/deploy.yml
- `Repository secrets CLOUDFLARE_API_TOKEN and CLOUDFLARE_ACCOUNT_ID (required by the deploy workflow)` --shares_data_with--> `apiToken`  [INFERRED]
  README.md → .github/workflows/deploy.yml
- `Repository secrets CLOUDFLARE_API_TOKEN and CLOUDFLARE_ACCOUNT_ID (required by the deploy workflow)` --shares_data_with--> `accountId`  [INFERRED]
  README.md → .github/workflows/deploy.yml

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **EN/ID language switch flow: persisted imdev-lang, [lang] visibility, attribute swap, chat widget sync, clock suffix, rotating I build word reset and relayout** — public_index_boot_script, public_index_language_toggle, public_index_bilingual_system, public_index_sync_attrs, public_index_sync_theme, public_index_chat_sync, public_index_chat_widget, public_index_jakarta_clock, public_index_word_rotator, public_index_relayout [EXTRACTED 1.00]
- **Split-text staggered reveal pattern: hero headline letters (--d), [data-words] heading words (--i), footer DEVALDI letters (--i)** — public_index_headline_scramble, public_index_scramble_in, public_index_scroll_reveals, public_index_band_motion [INFERRED 0.85]
- **Enterprise reporting pattern: live browser preview with Excel and PDF export on the ASP.NET Core / Blazor stack (PT Dinamis Infomadya platforms)** — public_index_asset_management, public_index_fixed_income, public_index_branch_info, public_index_dotnet_stack, public_index_exp_dinamis [INFERRED 0.85]
- **ImDev site-editing rules (CLAUDE.md ## ImDev)** — claude_imdev_project_rules, claude_index_html_graph_rebuild_rule, claude_bilingual_text_rule, claude_reduced_motion_rule [EXTRACTED 1.00]
- **Cloudflare Pages deploy flow (push to main or manual wrangler run, repository secrets, live site)** — readme_deploy_cloudflare_pages, readme_cloudflare_secrets, readme_manual_deploy, readme_live_site, github_workflows_deploy [EXTRACTED 1.00]
- **Reduced-motion gating: the CLAUDE.md rule and its three layers in index.html (boot script js-motion class, prefers-reduced-motion CSS override, motionOK JS gate)** — claude_reduced_motion_rule, public_index_boot_script, public_index_reduced_motion_css, public_index_motion_gate [INFERRED 0.85]
- **Portrait fly-and-flip scroll transition: the same portrait travels from the hero card (slot A) to the About card (slot B), flipping once, only when motionOK (prefers-reduced-motion) allows it** — public_index_hero, public_img_portrait, public_index_about, public_index_motion_gate [INFERRED 0.95]

## Communities (7 total, 0 thin omitted)

### Community 0 - "Project Rules, Theme & Language"
Cohesion: 0.14
Nodes (22): graphify skill trigger: /graphify runs the installed skill (.claude/skills/graphify/SKILL.md, any input to knowledge graph) before anything else, Font and image preloads: Google Fonts Archivo + Space Grotesk, img/portrait.webp, Boot script: restores theme (imdev-theme-v2) and language (imdev-lang, navigator.language fallback) before paint, adds js-motion when reduced motion is off, syncChat(l, tries): keeps the Nara chat widget language in sync with the site EN/ID toggle (tanyasaya:lang, waits for the custom element, retries while busy, setLang / fetchInfo), Nara AI chat widget <tanyasaya-chat> embed (bot ns29ieww7m, api-base nara.panduarahid.workers.dev, css nara-widget.css) loaded by the deferred widget.js, Design tokens: :root CSS custom properties (dark default palette, Archivo display and Space Grotesk sans fonts, mono stack, --px gutter, --maxw, --ease), tickClock(): Jakarta local time (Asia/Jakarta, 24h) with a WIB / GMT+7 suffix, refreshed every 30s and on language change, Language toggle button EN/ID [data-lang-toggle]: flips html data-lang, saves imdev-lang, then runs syncAttrs, syncChat, tickClock, kinReset and relayout (+14 more)

### Community 1 - "Motion, Kinetic Type & Hero"
Cohesion: 0.21
Nodes (23): Animated ASCII field [data-ascii]: two stacked pre layers draw plasma noise through a density ramp ( .:-=+*#%@) at about 24 fps, with the ImDev mark dissolving in and out on the bright layer and a cursor or tap ripple; sized to the card (cols×rows in the header), paused off-screen or in a hidden tab, one static frame under reduced motion, Back-to-top replay: #top links arm a flag past half a viewport; once the hero is 70% visible again, scrambleIn() and the fly card intro replay, Footer band motion: DEVALDI letters rise in on view, the illustration steps up, and word and illustration drift with the pointer (--mx / --my) on fine pointers, Cursor-stretch kinetic type stretch(zone, letters, amp): letters near the mouse stretch vertically through --sy (CSS scale on .ht-c and .kc), batched in requestAnimationFrame; applied to the hero headline letters (amp .2) and the I build letters (amp .24); fine pointers and motionOK only, drawWave(): cubic Bezier path through the timeline node centres, sets the SVG viewBox and --len for the stroke-draw animation, skipped while the wave is hidden, Flying portrait card (.fly): clone of img/portrait.webp that travels from slot a (hero) into slot b (About), flipping once on the way, Hero headline letter split [data-title] with hover scramble on fine pointers (motionOK only, .ready reveal with a 2.5s CSS failsafe), Hero section #top: < FULL STACK / DEVELOPER /> headline, portrait card (slot a), ImDev label and {{ AI-Driven Engineering }} tag over a film-grain layer (+15 more)

### Community 2 - "Work, Stack & What I Build"
Cohesion: 0.18
Nodes (22): About section #about: Hi, I'm Dev; role; currently at PT Clipan Finance Indonesia Tbk since Jun 2026; West Jakarta; portrait slot b; lead copy; Explore projects button, Asset Management Platform — legacy-to-web modernization (greenfield structure, reporting with web preview + Excel/PDF, portfolio and accounting modules, YARP gateway; enterprise); case study cs4, folder data-case=4, Branch Information System — centralized branch operations and executive monitoring (multi-metric reporting, scheduled Excel/PDF export; enterprise); case study cs6, folder data-case=6, Case-study dialog #case: 01 / 08 counter, close button, eight hidden .cs articles (badge, title, summary, highlights, [data-art] slot, stack chips, optional site link), Previous / Next, Cloudflare edge platform (Workers, Durable Objects, D1 SQLite FTS5, Vectorize, Workers AI), ASP.NET Core / C# / Blazor enterprise stack (with PostgreSQL or SQL Server, Redis, IIS), Project group: Enterprise platforms (Asset Management, Fixed Income, Branch Information, Visitor Website & CMS), Full Stack Developer, PT Dinamis Infomadya (May 2024 - 2026): enterprise back-office, financial modules, reporting engines, cron ETL, API integrations (+14 more)

### Community 3 - "Identity, Contact & Experience"
Cohesion: 0.16
Nodes (22): figure.webp - full-length ink illustration of Devaldi taking a mirror selfie (glasses, open black shirt over white tee, backpack, wide black trousers, white sneakers), used as the footer band figure, Monochrome pen-and-ink hatching style with transparent cut-out background, portrait.webp - black-and-white chest-up photo of Devaldi smiling (dark wavy hair, black rectangular glasses, light crew-neck tee) on a flat white background, used as the hero and About portrait card, Monochrome photo-card style (grayscale photo on an opaque flat white background, no transparency), Contact section #contact: Let's talk, mailto link, copy-email button, LinkedIn, West Jakarta GMT+7, email-draft form, Devaldi Caliesta Octadiani (Dev) — site owner, Full Stack Developer & AI-Driven Engineer in West Jakarta, Education: Bachelor of Information Systems (S.Kom), Ahmad Dahlan University, 2019-2023, GPA 3.79 Cum Laude, GDSC core member and head lab assistant, Email address devaldicaliesta@gmail.com (JSON-LD, menu CTA, contact link and copy button, footer, mailto draft) (+14 more)

### Community 4 - "Pages Deploy Workflow"
Cohesion: 0.11
Nodes (19): permissions, runs-on, steps, jobs, deploy, name, on, push (+11 more)

### Community 5 - "Project Folders & Dialog UI"
Cohesion: 0.40
Nodes (5): Case-study dialog controller: show(i) wraps the index, shows one article, sets aria-labelledby, clones the folder SVG into [data-art] once, updates the counter; showModal + modal-open scroll lock; close button and backdrop; focus back to the folder; Prev / Next and arrow keys, Copy email button [data-copy]: Clipboard API with execCommand fallback and a bilingual aria-live status, Project folder cards (.folder button[data-case]): back panel, three fanned docs holding an SVG illustration, front flap that tilts open on hover or focus, Project line-art SVG illustrations (.art, dark .art.dk variant; dashed .route paths march on hover and in the case dialog), Featured Projects section #projects: 08 case studies as folder cards in two groups

### Community 6 - "Favicon Brand Mark"
Cohesion: 0.67
Nodes (3): ImDev Favicon Mark, Near-Black Rounded Square (#141414), Off-White Corner Bracket Glyph (#f1f1ee)

## Ambiguous Edges - Review These
- `Visitor Website Revamp & CMS — legacy PHP migrated to CodeIgniter 4 MVC with a faster responsive frontend and refactored CMS (enterprise); case study cs7, folder data-case=7` → `Full Stack Developer, PT Dinamis Infomadya (May 2024 - 2026): enterprise back-office, financial modules, reporting engines, cron ETL, API integrations`  [AMBIGUOUS]
  public/index.html · relation: conceptually_related_to

## Knowledge Gaps
- **3 isolated node(s):** `Internship Full Stack Developer, CV Lumintu Logic (Feb-Jul 2022): LMS front end, relational database design, SQL, payment gateway module`, `Near-Black Rounded Square (#141414)`, `Off-White Corner Bracket Glyph (#f1f1ee)`
  These have ≤1 connection - possible missing edges or undocumented components. (Counts symbols only; 9 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `ImDev single-page site (public/index.html)` connect `Project Rules, Theme & Language` to `Motion, Kinetic Type & Hero`, `Work, Stack & What I Build`, `Identity, Contact & Experience`, `Project Folders & Dialog UI`?**
  _High betweenness centrality (0.310) - this node is a cross-community bridge._
- **Are the 2 inferred relationships involving `ImDev single-page site (public/index.html)` (e.g. with `robots.txt: User-agent * Allow / (every crawler may index the whole site)` and `README rebuild note: the site is HTML (a graphify document), so rebuild the graph through an agent with the graphify skill (/graphify . --update) after editing`) actually correct?**
  _`ImDev single-page site (public/index.html)` has 2 INFERRED edges - model-reasoned connections that need verification._
- **What connects `Internship Full Stack Developer, CV Lumintu Logic (Feb-Jul 2022): LMS front end, relational database design, SQL, payment gateway module`, `Near-Black Rounded Square (#141414)`, `Off-White Corner Bracket Glyph (#f1f1ee)` to the rest of the system?**
  _3 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `Project Rules, Theme & Language` be split into smaller, more focused modules?**
  _Cohesion score 0.14285714285714285 - nodes in this community are weakly interconnected._
- **Why does `Deploy to Cloudflare Pages: every push to main deploys through .github/workflows/deploy.yml, or start it by hand from the Actions tab (Run workflow)` connect `Project Rules, Theme & Language` to `Pages Deploy Workflow`?**
  _High betweenness centrality (0.271) - this node is a cross-community bridge._
- **Are the 17 inferred relationships involving `public/index.html: markup, inline CSS and inline JS (theme/language toggles, nav menu, kinetic type: headline scramble and cursor stretch, "I build" word rotator, ASCII field, ticker, flying portrait card, folder dialogs, wave timeline, contact form, footer band), all motion gated by prefers-reduced-motion` (e.g. with `Reduced-motion rule: keep all motion gated by prefers-reduced-motion` and `Animated ASCII field [data-ascii]: two stacked pre layers draw plasma noise through a density ramp ( .:-=+*#%@) at about 24 fps, with the ImDev mark dissolving in and out on the bright layer and a cursor or tap ripple; sized to the card (cols×rows in the header), paused off-screen or in a hidden tab, one static frame under reduced motion`) actually correct?**
  _`public/index.html: markup, inline CSS and inline JS (theme/language toggles, nav menu, kinetic type: headline scramble and cursor stretch, "I build" word rotator, ASCII field, ticker, flying portrait card, folder dialogs, wave timeline, contact form, footer band), all motion gated by prefers-reduced-motion` has 17 INFERRED edges - model-reasoned connections that need verification._

### Low-confidence Hints
_AMBIGUOUS edges — the extractor was unsure. Verify before acting on these._

- **What is the exact relationship between `Visitor Website Revamp & CMS — legacy PHP migrated to CodeIgniter 4 MVC with a faster responsive frontend and refactored CMS (enterprise); case study cs7, folder data-case=7` and `Full Stack Developer, PT Dinamis Infomadya (May 2024 - 2026): enterprise back-office, financial modules, reporting engines, cron ETL, API integrations`?**
  _Edge tagged AMBIGUOUS (relation: conceptually_related_to) - confidence is low._