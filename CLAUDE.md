## ImDev

Static personal site, no build step. `public/index.html` holds all markup, inline CSS and inline JS; `public/nara-widget.css` restyles the embedded Nara chat widget. See README.md for run and deploy commands.

- graphify treats `index.html` as a document, not code, so `graphify update .` does not refresh its nodes. After editing the site, rebuild the graph with the graphify skill: `/graphify . --update`.
- Every visible text needs both an English (`lang="en"`) and an Indonesian (`lang="id"`) version.
- Keep all motion gated by `prefers-reduced-motion`.

## graphify

This project has a knowledge graph at graphify-out/ with god nodes, community structure, and cross-file relationships.

Rules:
- When graphify-out/graph.json exists, run `graphify query "<question>"` before your first grep, search or source-file read for a codebase question, and put this rule in every subagent prompt that explores code. Read raw files only for lines the graph or an earlier read already located. Use `graphify path "<A>" "<B>"` for relationships and `graphify explain "<concept>"` for focused concepts. These return a scoped subgraph, usually much smaller than GRAPH_REPORT.md or raw grep output.
- If graphify-out/wiki/index.md exists, use it for broad navigation instead of raw source browsing.
- Read graphify-out/GRAPH_REPORT.md only for broad architecture review or when query/path/explain do not surface enough context.
- After modifying code, run `graphify update .` to keep the graph current (AST-only, no API cost).
- A committed graphify-out/graph.json is rewritten whole on every build, so a large diff to it in a pull request is expected. Do not flag it as churn or suggest skipping the graph rebuild or its hooks.
