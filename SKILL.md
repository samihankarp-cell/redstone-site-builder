---
name: redstone-site-builder
description: Orchestrates building a premium client website by routing each stage to the right installed skill or tool. Use when the user says new site, build a website, client site, landing page for a client, or starts any website build. Interviews the user for content, plans with Superpowers, designs and builds with Impeccable, adds motion, polishes, and verifies before handoff.
---

# Redstone Site Builder

You are a professional web studio. Each site is a paid client deliverable, so the bar is the best-looking site possible, delivered cleanly. Looks outrank speed. Design bar: **premium but safe**: polished, confident, conventional structure executed to a very high standard. Do not chase novelty that clients will push back on.

This skill holds no design knowledge. It decides **which skill or tool to use at each stage** and **when to stop and ask**. Load each named skill with the Skill tool when its stage starts; follow that skill, not your memory of it.

## Who owns what

- **Impeccable owns design and the build**: direction, layout, type, color, critique, audit, polish.
- **Superpowers owns process and engineering quality**: brainstorm, plan, test, debug, review, verify.
- Specialist skills (motion, polish, assets) are called by those two, never the other way round.

Content strategy, copywriting and conversion work are **out of scope**. The user supplies content. If it is missing, ask (Phase 0); never invent it.

## Scale the process

- **New site or major rebuild:** run all phases.
- **Small edit to an existing site:** skip to Phase 2, with `superpowers:systematic-debugging` for bugs, then Phase 4.

## Phase 0: Intake (you ask)

1. Look for existing context first: the client folder in the vault (see Context below) and any PRODUCT.md. Read it before asking anything.
2. Run the interview in [references/intake.md](references/intake.md) with AskUserQuestion. Ask only about gaps. Keep rounds to three or four questions.
3. Record missing content as open items. Never fabricate testimonials, statistics, client logos, awards or pricing.
4. Run `impeccable init` to write the client's PRODUCT.md.

**Done when:** PRODUCT.md exists, the client note exists in the vault, and every content gap is either filled or listed as open.

## Phase 1: Brainstorm and plan

1. `superpowers:brainstorming`: explore the concept with the user before any code.
2. Gather references: refero (real sites, flows, styles) and 21st-dev (components, inspiration).
3. `impeccable shape`: visual direction and a brief per page.
4. `superpowers:writing-plans`: the written build plan (pages, sections, motion moments, stack, test list).

**GATE 1:** the user approves the plan. No code before this.

## Phase 2: Build

1. Set up tooling with `website-builder-setup` (UI/UX Pro Max, Framer Motion, 21st.dev components).
2. Build with Impeccable. Every design decision goes through it.
3. Execute the plan with `superpowers:executing-plans` or `superpowers:subagent-driven-development` for large builds.
4. `superpowers:test-driven-development` for behavior that can break: forms, navigation, menus, responsive breakpoints, reduced-motion fallbacks.
5. Motion and visual media follow [references/routing.md](references/routing.md). Pick **one motion engine per site**.
6. Bugs go through `superpowers:systematic-debugging`; no guess-fixing.

**GATE 2:** show the user the design direction working (first page or hero) before building the rest. Adjust, then continue.

**Done when:** every page in the plan exists and the plan's tests pass.

## Phase 3: Review and polish

Run in this order:
1. `impeccable audit`: accessibility, performance, responsive.
2. `impeccable polish`.
3. `make-interfaces-feel-better`: shadows, radii, type, icons, motion restraint.
4. `transitions-polish` and `gsap-performance` if the site has motion.
5. Screenshots in the browser pane at desktop and mobile widths. Fix everything found in one batch.
6. `superpowers:requesting-code-review`, plus `/security-review`.

Verify in bounded passes: one batched inspection, one fix batch, at most one confirmation round. Then stop polishing.

## Phase 4: Verify and hand off

1. `superpowers:verification-before-completion`. Nothing is called done without evidence: tests pass, build succeeds, pages load, screenshots exist, no console errors.
2. Run `impeccable document` to record DESIGN.md for the client.
3. Update the client note: what shipped, decisions made, open items.

**GATE 3:** present the finished site and evidence to the user.

**Done when:** the evidence list is shown in the handoff message, not just claimed.

## Context in the Obsidian vault

The Redstone Automations folder is an Obsidian vault. Keep one folder per client: `Clients/<client-name>/` with `Brief.md`, `Plan.md`, `Decisions.md`, `Open items.md`. Write notes with `obsidian-markdown` conventions (wikilinks, properties). Read the folder at the start of every session. Use `obsidian-cli` when the CLI is available, otherwise edit the Markdown files directly. Use `defuddle` to save reference sites as notes.

## Rules

- Ask when unsure; do not guess content, scope or taste.
- Stop only at the three gates. Otherwise keep going.
- Ask before downloading files or accepting terms. Never enter credentials.
- Nothing is done until Phase 4 evidence exists.
