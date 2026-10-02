# Routing: which skill or tool for what

## Design and build
| Need | Use |
|---|---|
| Visual direction, layout, type, color, build | `impeccable` (always the lead) |
| Tooling setup at the start of a build | `website-builder-setup` |
| Quick previews or mockup pages to show the user | `artifact-design` |

## Motion: pick one engine per site
Never run GSAP and Framer Motion on the same site.

| Situation | Use |
|---|---|
| React site, component and layout animation | Framer Motion (from website-builder-setup) |
| Scroll-driven sections, pinning, parallax | `gsap-scrolltrigger` (+ `gsap-core`) |
| Choreographed multi-step sequences | `gsap-timeline` |
| Text splitting, Flip, drag, SVG drawing | `gsap-plugins` |
| GSAP inside React or Next.js | `gsap-react` |
| GSAP inside Vue, Nuxt, Svelte | `gsap-frameworks` |
| Smooth 60fps, jank | `gsap-performance` |
| UI details: menus, modals, toasts, toggles, tabs, loaders, hovers | `transitions-dev` (plain CSS; works on any site, alongside either engine) |
| Tuning existing motion timing and easing | `transitions-polish` |
| Overall finish: shadows, radii, type, icons | `make-interfaces-feel-better` |

Default: CSS transitions for UI details; add one JS engine only where the plan has scroll-driven or sequenced moments.

## Visual media: asked at intake
| Choice | Use |
|---|---|
| Video or animated hero, background loops | `flow-motion-director` (Google Flow, Veo 3.1). It writes frame and motion prompts; the user generates clips in Flow; then it processes and embeds them. Raise it at intake when the user has a concept in mind. |
| Still photos | stock-images-mcp |
| Graphics, illustrations | Canva MCP or Gamma image generation |
| None | Typography and layout carry the design |

Do not use generated or stock imagery to fake client work, team photos, results or testimonials.

## Research and reference
| Need | Use |
|---|---|
| Real site screenshots, flows, styles | refero MCP |
| Components, inspiration | 21st-dev-magic MCP |
| Save a reference page as a note | `defuddle` |
| Preview, screenshot, test at mobile width | Browser pane tools |

## Engineering (Superpowers governs)
| Stage | Use |
|---|---|
| Explore the idea | `superpowers:brainstorming` |
| Written plan | `superpowers:writing-plans` |
| Run the plan | `superpowers:executing-plans`, or `superpowers:subagent-driven-development` for big builds |
| Independent parallel tasks | `superpowers:dispatching-parallel-agents` |
| Behavior that can break | `superpowers:test-driven-development` |
| Any bug or failure | `superpowers:systematic-debugging` |
| Review | `superpowers:requesting-code-review`, `superpowers:receiving-code-review`, `/security-review` |
| Finish | `superpowers:verification-before-completion`, then `superpowers:finishing-a-development-branch` if on a branch |

Visual quality cannot be unit-tested. It is judged by `impeccable audit`, `impeccable polish` and screenshots at the verification gate.

## Not used here
Content strategy, offers, email sequences, competitive briefs, research-for-copy. The user provides content.
