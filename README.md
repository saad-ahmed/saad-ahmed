## Saad Ahmed

By day I close enterprise deals at Everlaw. At night I'm agent-pilled, building the
infrastructure my buyers will need in about a year. Both halves make the other one work.

**The day job:** $1.5M closed in my first six months — new business, expansions,
competitive displacements, partner motions. Got complex enterprise customers through
onboarding ahead of schedule by doing the boring necessary work: detailed handoffs,
stakeholder maps, explicit requirements. Built and tested seven agentic legal-workflow
demos for enterprise buyers, then built the v1 GTM playbook around them. The demos
weren't "look, AI can summarize a document." They asked where agentic ediscovery fits an
actual legal workflow, what it replaces, and what has to be governed — then I took the
answers back to Product and Engineering.

**The nights:** everything below. Most repos are private, so the links 404 unless you
have access. Ask and I'll add you, or I'll walk you through any of it live.

### Agents that run for 20+ hours

- **[lorah-app](https://github.com/saad-ahmed/lorah-app)** (private) — a control plane for
  agents working 20+ hours with no human in the loop, without losing task state, context,
  or budget. Planning, isolated worktrees, run logs, and recovery when a run goes
  sideways. Most of what I know about agent reliability came from watching runs fail here.
  [lorah-sandbox](https://github.com/saad-ahmed/lorah-sandbox) holds the experiments that
  weren't ready for it.
  **Stack:** Python 3.11 · Claude Agent SDK · DeepSeek as the executor model · MCP server
  SDK · asyncpg + Postgres · Pydantic + JSON Schema for structured output · Typer + Rich
  CLI · httpx · git worktrees for run isolation · pytest, mypy, ruff.
- **[ecco](https://github.com/saad-ahmed/ecco)** (private) — the coordinator. A
  self-hosted tracker that hands models assignments, context, skills, and constraints, and
  gives them a way to hand work back when they're stuck. The MCP surface mirrors Linear's,
  so an agent plans, files, and closes work through the same interface a person uses.
  **Stack:** FastAPI + uvicorn · asyncpg + Postgres with SQL migrations · MCP server SDK ·
  Clerk auth (PyJWT, Svix webhooks) · Next.js 16 + React 19 · Tailwind · SWR · Framer
  Motion · Playwright with axe-core accessibility checks · Railway.

### Selling systems, because the tools didn't exist

- **[docketsort](https://github.com/saad-ahmed/docketsort)** (private) — territory
  intelligence. It reads a Salesforce territory export, pulls each account's federal
  litigation footprint, predicts the ediscovery data volume sitting behind it, and blends
  that with legal-department headcount and existing footprint into a 0–100 score. A rep
  works the top 50 of 600 accounts instead of guessing. Every score opens to its own
  "why," because a ranking a rep can't interrogate is a ranking a rep ignores.
  **Stack:** Python · FastAPI · MCP connector mounted on the same service · DocketAlarm
  API · pandas + openpyxl for Salesforce exports · an LLM classifier with a deterministic
  rule-based fallback · Postgres · eval suite for the classifier · Docker · semgrep.
- **[docketsort-web](https://github.com/saad-ahmed/docketsort-web)** (private) — the
  marketing site.
  **Stack:** Next.js 15 · React 19 · TypeScript · Tailwind v4 · Sanity (embedded studio,
  next-sanity).

### A content-site factory

- **[atlas](https://github.com/saad-ahmed/atlas)** (private) — CMS experiments: Sanity,
  MCP, and Claude wired together to stand up a beautiful site fast and point it at AEO and
  SEO traffic. Atlas is the platform layer — versioned packages holding the capability
  contract, de-branded renderers, CMS schema, and ops scripts — and four editorial
  properties run on it, so one fix ships to the whole fleet. Built to find out what
  happens when a CMS, search data, analytics, email flows, and the ability to launch a
  site on a whim all sit in one system.
  **Stack:** TypeScript · pnpm workspaces · Changesets for versioned releases · tsup ·
  Vitest · Sanity schema + Portable Text renderers · Next.js 15 + Tailwind v4 on the
  consuming sites · MCP and Claude for content and ops · Railway.

### Products

- **[brunson](https://github.com/saad-ahmed/brunson)** (private) — a talent marketplace
  where the candidate owns the profile and the evidence behind it, instead of a recruiter
  owning the pitch. [brunson-marketing](https://github.com/saad-ahmed/brunson-marketing) is
  the site and studio.
  **Stack:** React 19 + Vite · TypeScript · Mantine · Clerk auth · Postgres with
  node-pg-migrate · S3 with presigned uploads · Anthropic SDK · MCP SDK · pdf.js, mammoth,
  and xlsx for résumé and evidence parsing · Vitest + Playwright · Docker on Railway.
- **[vtt-trader](https://github.com/saad-ahmed/vtt-trader)** (private) — research and
  execution harness for a systematic trading strategy. Backtest, then let it run.
  **Stack:** Python · FastAPI · Postgres · numpy · pandas-market-calendars · Anthropic SDK
  · a local MCP server for base-case research · CSV replay for backtests · Docker on
  Railway.

### Public

- **[thx-boris](https://github.com/saad-ahmed/thx-boris)** — a Claude Code skill packaging
  how Boris Cherny, who created Claude Code, uses it to build Claude Code.
  **Stack:** Claude Code skill format · shell.

---

Functional is cheap now. What's expensive is taste: the judgment and context to turn a
working thing into something useful, usable, joyful, and worth someone's time. That's the
part I'm practicing, twice a day, on both sides of the job.

Washington, D.C.
