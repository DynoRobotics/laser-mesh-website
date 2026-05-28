# Fresh-agent brief — build a Tailwind website for laser-mesh

You are picking up the website-build for the laser-mesh project. The
architectural substrate, the image renders, the human-pain framing, and
the visual design language are all settled. Your job is to assemble
them into a single-page (or small multi-page) Tailwind website that the
operator can share with FMV evaluators, dyno colleagues (Erik, William),
and potential co-applicants.

## Mission

Build a **single-page Tailwind website** (or small 2-3 page site if a
single page becomes unwieldy) that pitches the laser-mesh as: a Swedish-
made modular ground robotics platform with omnidirectional optical mesh,
open architecture for vendor-replaceability, and a focus on solving
named FMV procurement pains (forward human risk + operator cognitive
load).

The site is not a marketing flex. It is a credible engineering pitch —
sober Nordic engineering register, photoreal product photography
aesthetic, civilian-engineering vocabulary throughout. NOT military
marketing, NOT sci-fi, NOT defense-industry promo.

**Audience:**
- Primary: FMV evaluator reading after seeing the svarsbilaga
  submission (deadline 2026-06-03)
- Secondary: Dyno engineering colleagues (Erik Örjehag, William
  Carleson) evaluating the technical pitch
- Tertiary: Potential co-applicants and Swedish defense / civil-
  protection procurement teams

**Tone reference:** Husqvarna, Atlas Copco, Volvo CE, Trimble survey,
Starlink mini — credible field-instrument product pages, not glossy
sci-fi marketing.

## Output spec

**Save to this directory:** `laser-mesh/exploration/website/`
(you're already here — this PROMPT.md lives here)

**File structure:**
```
website/
├── PROMPT.md            # this file (your brief)
├── index.html           # main page
├── styles.css           # any custom CSS not coverable by Tailwind classes
├── tailwind.config.js   # if needed for custom palette (see Visual Design below)
├── assets/
│   └── images/          # copy or symlink the rendered images here
└── README.md            # short note on how to view + iterate
```

**Tech stack:**
- **Tailwind CSS** via CDN (`<script src="https://cdn.tailwindcss.com"></script>`)
  for portability — operator can open `index.html` directly in a
  browser, no build step required
- Vanilla HTML + minimal JS (only if needed for nav toggle or similar)
- NO React, NO Vue, NO build tooling — keep it portable so anyone can
  open it locally and the operator can iterate without a dev env
- If you need custom Tailwind palette colors, use inline config via
  `<script>` block in the HTML head OR a separate `tailwind.config.js`
  if you switch to a local Tailwind build later
- Responsive (mobile + desktop), but desktop-first since the audience
  is reviewing on laptops

## Required reads (in order)

Read these before authoring any HTML. They are the substrate. Do not
re-invent decisions that are already settled.

**1. Orientation:**
- `../../README.md` — laser-mesh folder orientation, current status,
  maturity-stage gradient, value-criterion (FMV pains #1 + #3)
- `../../wheel-check.md` — discipline for wheel-checking before
  inventing new substrate (relevant if you find yourself wanting to
  invent visual elements not in the canonical work)

**2. Architecture canon:**
- `../architecture-prototype-triage/00-current-family-character-proposal.md`
  — the cast (Mule, Relay, Scout, Lantern, Hand, Sparrow + Phase-3
  future configurations Hawk, Hearth, Sentry, Bellows + human role
  Anchor-Setter), §6.7 bidirectional module-chassis openness pitch
- `../architecture-prototype-triage/04-architecture-spine.md` — the
  4-layer DDA architecture (base / reusable specialized / family /
  per-attachment), role-contract as unit of vendor-replaceability,
  capability-discovery runtime
- `../architecture-prototype-triage/05-role-contracts-and-cast.md` —
  per-character sense/command/state/event contracts, "what the
  operator sees" prose per character (these are your visual anchors
  for the per-module sections of the site)

**3. The FMV procurement context:**
- `../../raw-input/fmv-liten-robot.md` — the FMV procurement
  document; the seven named operational pains in §Bakgrund L17-20
  (pains #1 forward human risk + #3 operator cognitive load are
  load-bearing for the pitch)

**4. The visual style canon (mdx files describing each character +
the canonical product-photo style):**
- `../../../workspaces-tooling/weavermesh/weaver/prompts/styles/laser-mesh-nordic-product-photo.mdx`
  — the canonical visual style block (matte grey-bronze + copper-
  bronze + sage-green LEDs + deep-Swedish-blue optical glass)
- `../../../workspaces-tooling/weavermesh/weaver/prompts/characters/chassis-platform.mdx`
  — chassis spec (v0.5: universal rail dock, side handles, swappable
  battery with safety-orange latches, cooling fins)
- `../../../workspaces-tooling/weavermesh/weaver/prompts/characters/cargo-module.mdx`
- `../../../workspaces-tooling/weavermesh/weaver/prompts/characters/mast-module.mdx`
  (v0.5: telescoping mast + Lantern beacon head at tip)
- `../../../workspaces-tooling/weavermesh/weaver/prompts/characters/sensor-mast-module.mdx`
  (v0.3: telescoping perception mast + 3D LIDAR + thermal + cameras)
- `../../../workspaces-tooling/weavermesh/weaver/prompts/characters/manipulator-arm-module.mdx`
- `../../../workspaces-tooling/weavermesh/weaver/prompts/characters/aviary-module.mdx`
  (v0.3: motorized industrial drone-in-a-box case, X650 quadcopter)
- `../../../workspaces-tooling/weavermesh/weaver/prompts/characters/lantern.mdx`
  (v0.3: telescoping mast + omnidirectional 360° aperture ring + no
  logos)
- `../../../workspaces-tooling/weavermesh/weaver/prompts/characters/sparrow-drone.mdx`
  (v0.3: mid-size X650-class quadcopter, NOT hexacopter)

**5. The dispatch pack with all the image prompts (for reference on
what each render shows):**
- `../story-time/i1/image-prompts/laser-mesh-modular-dispatch-pack-2026-05-28.md`

## Image assets to use

All rendered images live in `../images/i0/`. Copy or symlink them
into `website/assets/images/` for the site.

The renders that have landed (operator-validated):

| File | What it shows | Suggested website use |
|---|---|---|
| `chassis-platform-v04-solo.png` | Solo chassis with side handles + battery latches + cooling fins | Architecture section — "the shared chassis" hero |
| `mule-v02-cargo-deck.png` | Chassis + cargo deck + Pelican-class case strapped down | Modules section — Mule card |
| `relay-v03-mast-extended.png` | Chassis + mast-module on rail-mounted base-plate | Modules section — Relay card (NOTE: v0.5 with Lantern beacon head may have re-dispatched and superseded this; check `../images/i0/` for newer Relay renders before authoring) |
| `scout-v01-sensor-mast.png` | Chassis + sensor-mast (cameras + thermal + LIDAR) | Modules section — Scout card (NOTE: v0.3 with telescoping mast + upgraded 3D LIDAR may have re-dispatched; check for newer renders) |
| `hand-v01-arm-extended.png` | Chassis + manipulator-arm extended | Modules section — Hand card |
| `sparrow-chassis-side-v03-drone-in-open-case.png` | Chassis + motorized case open + X650 quadcopter inside | Modules section — Sparrow card |
| `lantern-v02-omnidirectional-beacon.png` | Standalone Lantern with omnidirectional beacon ring | Modules section — Lantern card (NOTE: v0.3 with telescoping mast may have re-dispatched; check for newer renders) |

**Check `../images/i0/` for any newer renders before assuming the
v0.4-v0.3-v0.3-etc. naming above is current.** The operator iterates
fast and there may be `*-v05-*` or `*-v04-*` files you should use
instead.

## Visual design language

This is the most-load-bearing constraint. The site must match the
canonical style block used for all the image renders.

**Color palette (mirror the hardware palette):**
- Primary background: warm off-white / matte cream (matches the
  frosted-plastic Lantern LED panel — `#F5F1EA` or similar)
- Body text: dark warm-grey (`#2A2724` or similar — NOT pure black)
- Accent / brand: matte grey-bronze (`#9C8870`, `#8A7660` range)
- Highlight: copper-bronze (`#B87333`, `#A86420` — used sparingly,
  for callouts and link hovers)
- Mesh signal color: sage-green (`#8FA68B`, `#7A9576` — for status
  indicators, "active" states, accent buttons)
- Optical glass color: deep Swedish-blue (`#1E3A5F`, `#284970` — for
  one or two key visual anchors, not body color)
- Heat-sink / hardware accent: matte black (`#1C1A18`)
- Snow / negative space: cool white-grey (`#E8EAEB` — for section
  dividers, photo backdrops)

**Avoid entirely:**
- Pure white (`#FFFFFF`) — too clinical
- Pure black (`#000000`) — too aggressive
- Saturated red, bright blue, neon green — wrong register
- Gradient marketing backgrounds
- Glossy / shiny visual effects
- Drop shadows that read as 3D depth
- Big bold sans-serif marketing typography (think Inter at 96px)

**Typography:**
- Sans-serif for body — IBM Plex Sans, Inter, or Source Sans Pro
  (commercial-engineering register, not marketing-display)
- Monospace for any code-like elements (capability strings, version
  numbers, contract excerpts) — IBM Plex Mono or JetBrains Mono
- Headings: same family as body, just heavier weight and larger size
  — NOT a separate display font, NOT a serif heading face
- Sizes restrained: hero h1 ~48-56px, h2 ~32-36px, body ~16-18px

**Layout:**
- Generous whitespace
- Grid-based, not centered-narrow-column blog format
- Module cards: image on one side (~60% width), spec text on the
  other (~40% width), alternating left/right for visual rhythm
- Section dividers: thin matte-grey-bronze horizontal lines, NOT
  big graphic dividers
- No hero video, no parallax scrolling, no animated illustrations

**Imagery:**
- Use the rendered images at high resolution
- Frame them in simple matte borders (1-2px grey-bronze) or no
  border at all
- Captions in small monospace beneath each image
- One large hero image at the top (chassis-platform solo OR a
  multi-character composition if it lands)

## Suggested site structure

### Single-page version (recommended for MVP):

**1. Hero (above the fold)**
- One-line pitch: "Modular open-architecture ground robotics for
  subarctic field deployment."
- Sub-line: "Swedish-made base platform + vendor-replaceable modules.
  Designed for the FMV CMIP PCP procurement context."
- Hero image: chassis-platform solo OR multi-character field
  deployment (if rendered)
- Subtle scroll cue

**2. The pitch in one paragraph**
- Two-three sentences of plain prose. Architecture-grounded, not
  marketing-grounded. Something like:
  > "One chassis platform. Modular attachments for cargo, comms,
  > perception, manipulation, and aerial deployment. Open module
  > interface that runs on the consortium reference chassis OR on
  > third-party commercial UGVs (Husky, Bunker Pro, Spot-class). An
  > omnidirectional optical mesh designed to operate honestly under
  > partial information — surfacing what is known, what is not, and
  > what was decided about the gap."

**3. Human problems we solve** (the FMV-pain framing)
- Two load-bearing pains called out as section anchors:
  - **Pain #1 — Forward human risk in hostile terrain** (FMV
    procurement L18)
  - **Pain #3 — Rear operator cognitive load** (FMV procurement
    L20)
- Sub-sections by stakeholder (operator / field tech / procurement)
  with concrete "problem → how laser-mesh solves it" pairs (the
  Slack-format list the operator drafted is the source — paste +
  format)

**4. Modules (the demo cast)**
- One card per module: Mule, Relay, Scout, Hand, Sparrow, Lantern
- Each card: image, name, one-line role, 2-3 bullet capabilities
- Mention the chassis-mounted Lantern variant (mobile mesh anchor)
- Mention Phase-3 future configurations (Hawk, Hearth, Sentry,
  Bellows) as a separate "future modules" block

**5. Architecture / open-interface section**
- One image (Bunker Pro Relay variant if rendered, OR the canonical
  Relay) demonstrating the host-agnostic claim
- 3-4 sentences on the rail-dock universal interface, vendor-
  replaceability, module-first per DR-ingest Q-FINAL
- Optional: a small diagram (CSS-only, no SVG complexity) showing
  the 4 DDA layers OR the chassis + modules + dock relationship

**6. Innovations (the named §6 innovations)**
- Brief callouts for: anchor-decay, disagreement-surface,
  link-state-as-mission-geometry, operator-pause-as-signal,
  approve-with-review-flag, Anchor-Setter → Hand transition
- 1-2 sentences each, no deep dive

**7. About / Swedish-made**
- Brief team / consortium context if the operator wants it (ask if
  unclear)
- Mention: Swedish-built base platform, focus on supply-chain
  resilience, alternative to US/Chinese-dominated UGV market
- Contact / next-step CTA (email link to operator)

**8. Footer**
- Small. Just consortium mark (or none — Lantern is logo-free,
  consider that aesthetic for the site footer too), build date,
  link to the architecture-prototype-triage source docs for
  technical depth.

### Multi-page version (if single-page becomes too long):

Same content split across:
- `index.html` — Hero + pitch + pains + modules summary + CTA
- `modules.html` — Detailed per-module pages with full specs
- `architecture.html` — DDA layers + open-interface + innovations
- `about.html` — Team + contact + procurement context

Single-page is preferred unless content overflow forces split.

## Tone / register

- Engineering-credible, not marketing-promotional
- Direct, specific, dimensional ("~75-85 cm × 45-55 cm chassis,
  ~25-35 kg, two-person side-handle carry" — not "compact and
  portable")
- Swedish-context-aware (mention boreal forest, subarctic conditions,
  Försvarsmakten procurement, Norrbotten deployment scenarios where
  natural)
- Civilian-engineering vocabulary throughout (this is the explicit
  style rule — NOT military marketing, NOT defense-industry promo,
  NOT sci-fi)
- Honest about what's settled vs in-development (the substrate marks
  pre-2026-05-29 as cast-lock; Phase 3 modules are named-but-not-
  yet-engineered)

## Done criteria

The site is done when:

1. **`index.html` opens directly in a browser** (Chrome / Safari /
   Firefox) without a build step or local server
2. **All images render** from `assets/images/`
3. **Tailwind classes render correctly** via the CDN script
4. **Mobile-responsive** (test at 375px / 768px / 1280px / 1920px
   widths)
5. **Each module has its image + spec card** rendered correctly
6. **The two load-bearing FMV pains** (#1 + #3) are clearly called
   out as section anchors
7. **Open-architecture pitch is visible** (chassis + modules
   relationship, vendor-replaceability, Bunker Pro variant if
   rendered)
8. **No marketing-emotional language** ("revolutionary," "next-
   generation," "best-in-class" — all banned)
9. **No military-defense-marketing language** ("dominate the
   battlespace," "tactical superiority," "force multiplier" — all
   banned)
10. **`website/README.md` exists** with one-paragraph notes on how
    to view the site locally and how to iterate

## Out-of-scope (do NOT do)

- Do NOT add interactive 3D viewers (keep it static)
- Do NOT add a CMS, blog system, or dynamic content
- Do NOT add analytics scripts
- Do NOT add fake testimonials or quotes from people who haven't
  approved them
- Do NOT invent specs that aren't in the canonical substrate (if
  you want to make a claim, find it in the mdx files first)
- Do NOT add weapons / tactical / military imagery
- Do NOT generate new images — use only what's in `../images/i0/`

## Ask the operator if unclear about

- Whether to include the consortium / team identity explicitly OR
  keep the site logo-free / consortium-anonymous (Lantern is now
  logo-free per v0.2; the site could mirror that aesthetic OR could
  brand more explicitly if there's a consortium name to use)
- Whether to include contact information (email, phone) OR keep CTA
  abstract ("contact us via the FMV procurement channel")
- Whether the multi-character field deployment shot has rendered
  yet (if so, use it as the hero; if not, use the chassis-platform
  solo as hero and note the gap)
- Whether the Bunker Pro Relay variant has rendered yet (if so,
  feature it in the architecture/open-interface section)
- Color palette tuning — the hex codes above are starting points;
  show the operator a swatch on first dispatch and let them tighten

## Closing

You have the substrate (architecture docs + per-module mdx files),
the visuals (rendered images in `../images/i0/`), the pain framing
(FMV procurement document + the human-problems Slack list), and the
visual design language (matte grey-bronze + sage-green + deep
Swedish-blue, sober Nordic engineering register).

The site is an FMV-evaluator-facing pitch. Build it credibly, build
it civilian-engineering, build it portable (CDN Tailwind, single
HTML file, opens in a browser). Save to `website/` in this folder.

The cast was locked 2026-05-29 EOD. The FMV submission is 2026-06-03.
Build with that timing in mind — done-and-shippable beats perfect-
and-late.
