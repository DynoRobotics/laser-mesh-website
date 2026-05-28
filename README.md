---
maturity-stage: exploration
operator-reviewed: pending
authored: 2026-05-28
purpose: FMV-evaluator-facing pitch site for the laser-mesh deliverable (svarsbilaga deadline 2026-06-03).
authoritative-substrate:
  - ../../README.md
  - ../architecture-prototype-triage/00-current-family-character-proposal.md (v0.2)
  - ../architecture-prototype-triage/04-architecture-spine.md
  - ../architecture-prototype-triage/05-role-contracts-and-cast.md
  - ../../raw-input/fmv-liten-robot.md
  - ../../../workspaces-tooling/weavermesh/weaver/prompts/styles/laser-mesh-nordic-product-photo.mdx
---

# laser-mesh website — operator notes

Single-page Tailwind site for sharing with FMV evaluators, dyno colleagues,
and prospective co-applicants. Civilian-engineering register, Nordic-product-
photo visual language, logo-free aesthetic.

## How to view

```
open index.html
```

The site loads Tailwind from CDN and IBM Plex (Sans + Mono) from Google
Fonts. No build step. Works in any modern browser; no local server
required (`file://` works because there are no module imports).

Tested viewports during authoring: 375 px, 768 px, 1280 px, 1920 px.

## Files

```
website/
├── PROMPT.md          # original brief
├── README.md          # this file
├── index.html         # main FMV-evaluator-facing pitch (Tailwind CDN, inline palette)
├── for-vantor.html    # executive brief for Vantor leadership (links back to index.html)
├── styles.css         # supplementary CSS (anchor offsets, hairline borders)
└── assets/
    └── images/        # copies of the operator-validated renders from ../images/i0/
```

## Two pages, two audiences

| Page | Audience | Opener | Length |
|---|---|---|---|
| `index.html` | FMV procurement evaluator (svarsbilaga reader) | The two load-bearing FMV pains (forward human risk + operator cognitive load) | ~2630 words, 809 lines |
| `for-vantor.html` | Vantor CEO + leadership | "Vantor on the ground" — opportunity framing, ground-tier gap, three paths for involvement, six-day FMV deadline | ~1620 words, 609 lines |

The two pages share the palette, the Tailwind config, the `styles.css`, and the rendered images. `for-vantor.html` links back to `index.html` for the full FMV-facing pitch; `index.html` does NOT link to `for-vantor.html` (the FMV reader should not be routed to an internal executive brief).

`for-vantor.html` carries the same banned-vocabulary discipline as `index.html` — no defense-marketing register, no marketing-emotional vocabulary. The opener pivots from FMV pain framing to Vantor opportunity framing while preserving the civilian-engineering register throughout the body.

## Where to iterate

| Operator wants to change… | Edit this |
|---|---|
| Palette hex codes | `<script>` block inside `<head>` of `index.html` (search "tailwind.config") |
| Section copy | `index.html` — sections are commented with their anchor IDs |
| Hero image | `<img src="assets/images/chassis-platform-v04-solo.png">` — swap filename or replace file in `assets/images/` |
| Module captions | The `<figcaption>` inside each `<article id="module-…">` |
| Contact link | Search `OPERATOR TUNE` in `index.html` |
| Header navigation | `<header>` element near the top of `index.html` |
| Footer text | `<footer>` element at the bottom |

If a newer render lands in `../images/i0/` (e.g. a v0.5 Relay with
Lantern beacon head, or the multi-character field deployment shot the
PROMPT.md hero-question flagged), drop the file into `assets/images/`
and update the matching `<img src=…>` in `index.html`.

## Anchors (for direct linking)

- `#top` — hero
- `#problems` — FMV pain section
  - `#pain-forward-risk` — Pain #1
  - `#pain-cognitive-load` — Pain #3
- `#modules` — demo cast
  - `#module-mule`, `#module-relay`, `#module-scout`, `#module-hand`, `#module-sparrow`, `#module-lantern`
- `#platform` — Built on the Vantor Spatial Intelligence Platform (Forge, Raptor, Sentry)
- `#architecture` — role-contract spine + universal rail dock
- `#innovations` — six laser-mesh-specific primitives
- `#future` — Phase-3 named configurations
- `#context` — Swedish-made + CTA

## Vantor product integration (2026-05-28)

The site is now pitched as **a Vantor ground product line**, extending Vantor&rsquo;s space-to-air spatial-intelligence stack to the ground. Three Vantor products are cited by name:

| Vantor product | Where it shows up | Source |
|---|---|---|
| **Forge™** | Platform section card; spatial-intelligence fusion substrate. Co-registers laser-mesh ground sensor feeds onto Vivid Terrain at the edge. | `vantor.com/product/platform/forge` |
| **Raptor™** | Scout module card (Raptor-class visual-terrain matching); Sparrow module card (Raptor Guide on drone camera, Raptor Sync on aerial frames, Raptor Ace for ground coordinates); Platform section card. | `vantor.com/product/mission-solutions/raptor` |
| **Sentry™** | Phase-3 Sentry block (laser-mesh chassis Sentry = local-scale ground tier of Vantor Sentry global ISR); Platform section card. | `vantor.com/product/mission-solutions/sentry` |

The four-altitude space-to-ground loop is rendered as a small CSS diagram inside the Platform section: Space (Sentry, WorldView) → Air (Sparrow drone, Raptor Guide) → Ground (chassis + cast) → Anchor (Lantern posts). Forge fuses all four onto Vivid Terrain.

Audience pivot for this revision: Vantor CEO (Swedish) presentation 2026-05-28 / 2026-05-29, in addition to the original FMV-evaluator audience for svarsbilaga submission 2026-06-03. The civilian-engineering register is preserved for FMV; Vantor product positioning sits in the Platform section + header + footer + Scout/Sparrow/Sentry citations.

### What did NOT change for the Vantor pivot
- Body register stays civilian-engineering (Husqvarna / Atlas Copco / Volvo CE / Trimble) — no defense-marketing vocabulary leaked into the body copy. Vantor.com uses some defense-marketing register; the laser-mesh PROMPT explicitly bans it. The Vantor CEO reads the site as the FMV-evaluator-facing surface, with Vantor brand explicit but register tuned for procurement.
- Balans v1.0 light-mode palette unchanged (the lineage trace in §Wheel-check still applies).
- Logo-free aesthetic preserved for the laser-mesh side (footer Vantor wordmark is the only brand mark; no symbols imported).
- The six FMV-pain framing + six module cards + six innovations + four Phase-3 configs unchanged.

## Wheel-check trace

Two passes of `/wheel-check` ran during authoring.

### Pass 1 — themes/ + symbols (initial scope check)

`themes/brands/weavermesh/tokens.json` — Tier-1 design tokens. Catppuccin
Mocha base + WeaverMesh Zenoh Purple (`#8b5cf6`) accent. Scope explicitly
declared as **dark-mode only, for Obsidian / IDE / terminal surfaces.**
Light mode + Tier 2 (Tauri, Finder, web) is documented as deferred.

`themes/symbols/` — five WeaverMesh-workspace mythopoetic marks
(`anchor-weaver-mark`, `balance-point`, `the-bridge`, `the-shield`,
`the-spiral`).

**Verdict:** `WORKSPACE-PARTIAL with named divergence` — out-of-scope.
The website is light-mode FMV pitch, not dark-mode dev tooling. No
symbols imported; logo-free aesthetic mirrors Lantern v0.2 (operator
confirmation 2026-05-28).

### Pass 2 — design systems across the workspace (FMV-fit check)

Operator-requested deeper sweep across all design substrate in the
workspace to determine: which design system lands with an FMV evaluator?

| Artifact | Verdict | Notes |
|---|---|---|
| **Balans v1.0** (`compression/1-sources/balans/brand/`) | **WORKSPACE-HAS-IT** | Canonical Swedish-minimalist Tailwind design system (2025-07-05). 10-shade scales, hex codes already ~90% aligned with the laser-mesh-Nordic-product-photo style block. |
| `balans-website/` live implementation | adjacent — informs structure | Vite/React. Title "AI-säkerhet för kritiska system"; tagline references "försvar och industri". Same aesthetic, lighter on archetypal vocabulary in body copy. |
| BirdTurret Dark Mode (`compression/1-sources/birdturret/BIRDTURRET-DARK-MODE-DESIGN-SYSTEM.md`) | **WORKSPACE-HAS-IT but wrong-fit** | "Defense Technology Variant of Balans." Tactical/Ukrainian-defense register. Banned by PROMPT.md "NOT military marketing, NOT defense-industry promo" rule. |
| WeaverMesh tokens (`themes/brands/weavermesh/`) | out-of-scope by own scope-disclaimer | Dark-mode dev-tool only. |
| Saab `lm_graph` (`compression/1-sources/saab/`) | not a design system | Classification/compliance tooling. |
| FMV-specific brand | `WORKSPACE-MISSING` | No Försvarsmakten-specific brand kit exists in the workspace. |

**Aggregate verdict:** `WORKSPACE-HAS-IT` — adopt Balans v1.0 light-mode
as parent palette. **Recommended action:** `iterate-existing` —
import Balans canonical Tailwind scales, with civilian-engineering
token rename (drop archetypal prefixes), and document the laser-mesh
specialization as the layer that sits on top.

### Adopted lineage (current state, after refactor 2026-05-28)

```
Balans v1.0 (Swedish-minimalist parent, operator-canonical 2025-07-05)
  ├── 10-shade scales: swedish-blue, birch-white, birch-wood,
  │                    sage (renamed from sage-green),
  │                    copper (renamed from truth-copper),
  │                    gold (renamed from thread-gold),
  │                    silver (renamed from gentle-silver)
  ├── DROPPED:          alliance-purple #6b5b95
  │                     (mythopoetic; corresponds to WeaverMesh
  │                     Zenoh Purple; out-of-scope)
  └── laser-mesh Nordic specialization (operator-canonical 2026-05-28)
        ├── style block: workspaces-tooling/.../styles/
        │                laser-mesh-nordic-product-photo.mdx v0.1
        ├── additions:   ink #2A2724, ink-soft #4A453F,
        │                hardware #1C1A18, snow #E8EAEB
        ├── aliases:     cream = birch-white DEFAULT
        │                bronze = birch-wood-700
        │                bronze-dark = birch-wood-800
        │                sage-dark = sage-700
        └── register:    civilian-engineering (Husqvarna / Atlas Copco /
                         Volvo CE / Trimble), NOT defense-marketing
                         (BirdTurret is explicitly out-of-scope).
```

| Axis | Balans v1.0 | Laser-mesh Nordic specialization | This website |
|---|---|---|---|
| Mode | light + dark variants | light only (PROMPT.md catalogue register) | light |
| Vocabulary | archetypal (Sacred Alliance, Cosmic Weave) | civilian-engineering | civilian-engineering |
| Primary brand | swedish-blue #2c5aa0 | swedish-blue (glass accents only) | swedish-blue (available, used sparingly) |
| Surface BG | birch-white #f8f6f0 | warm cream — same | birch-white (aliased as `cream`) |
| Accent | truth-copper #b87333 | copper #B87333 — identical | copper |
| Mesh signal | sage-green #8faa8b | sage #8FA68B — ~1pt shift | sage (Balans canonical) |
| Audience | family + AI-collaboration | FMV evaluator | FMV evaluator |

## Content lineage

All site content is **cite-and-extend** of authoritative laser-mesh
substrate. No new architectural claims are introduced. Source map:

| Site section | Source |
|---|---|
| Hero pitch | `00-current-family-character-proposal.md` §1 + style block atmosphere line |
| Pitch paragraph | `04-architecture-spine.md` §1 + §3 L67-79 |
| Pain #1 / #3 framing | `../../README.md` §"Value-criterion" + `raw-input/fmv-liten-robot.md` L18 + L20 |
| Module cards | `05-role-contracts-and-cast.md` §3.1 – §3.6 + character mdx files |
| Anchor-Setter aside | `05-role-contracts-and-cast.md` §3.7 |
| 4-layer DDA diagram | `04-architecture-spine.md` §2 + `00 §5` |
| Universal rail dock visual | `chassis-platform.mdx` Mounting Interface section |
| Innovations | `00 §6` |
| Phase-3 future configs | `00 §3` |
| Bidirectional openness | `00 §6.7` + `16-revision-pass-c8-bidirectional-openness.md` + DR ingest Q-FINAL |
| Visual palette | `workspaces-tooling/.../styles/laser-mesh-nordic-product-photo.mdx` v0.1 |

One small bridge: the line *"a lost UGV is a single-purpose platform
replaced one-for-one"* in the Pain #1 section synthesizes FMV pain #2
("enkelt uppbyggda och utvecklade för att endast lösa enskilda
uppgifter", L20) into the pain #1 framing to make the per-contract-
loss-granularity argument concrete. Flagged here so the operator can
tighten or remove.

## Known gaps / things to fix before share

- **Contact CTA placeholder.** `index.html` has `mailto:contact@example.invalid`
  near the bottom — replace with the operator's actual contact channel
  before sharing externally. Search `OPERATOR TUNE` in `index.html`.
- **Multi-character field deployment hero.** PROMPT.md flagged that if a
  rendered multi-character scene lands, it should be the hero; the current
  draft uses the chassis-platform-solo render. Swap by editing the hero
  `<figure>` block in `index.html` if/when the render lands.
- **Bunker Pro Relay variant.** PROMPT.md noted that if the Bunker Pro
  Relay variant has rendered, it should feature in the architecture
  section. No such render currently exists in `../images/i0/`; the
  architecture section makes the host-agnostic claim narratively for now.
- **Palette tuning.** The hex codes in `index.html` are the canonical
  starting points from the style block. The operator may want to tighten
  shade-by-shade after viewing the site on real hardware.
- **No tracked-undercarriage variant copy.** The chassis-platform v0.5
  mdx switched the canonical chassis from tracked to wheeled; the role-
  contracts doc still describes the Mule as tracked ("treads that chew
  rather than glide"). The site uses neutral language ("moves cargo")
  to avoid the inconsistency. Post-submission, the role-contracts doc
  should be revised to wheeled per the chassis-platform.mdx revision
  history entry.

## Banned vocabulary (style rule)

Per PROMPT.md and the Nordic-product-photo style block, the site does
not use:

- Marketing-promotional: *revolutionary, next-generation, best-in-class,
  cutting-edge, world-class, game-changing, disruptive*
- Military-marketing: *dominate the battlespace, tactical superiority,
  force multiplier, kill chain, weapons platform*
- Sci-fi register: *autonomous swarm, AI brain, intelligent fleet,
  next-gen autonomy*

If reviewing a future revision, grep for these terms before commit.

## Maturity stage

`exploration` per `../../README.md` frontmatter convention. The site
is `operator-reviewed: pending` until explicitly declared otherwise.
The cast it pitches is locked 2026-05-29 EOD; the substrate underneath
this site is canonical as of that date.
