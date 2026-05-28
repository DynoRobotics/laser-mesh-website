# Painterly scenario prompts for the laser-mesh website

These are **scene-scope** prompts in the canonical `laser-mesh-scandinavian-
field` style (painterly Scandinavian field-concept register — sibling to
the product-photo register we use for chassis + module spec sheets). The
website alternates between the two: product-photo for hardware cards,
painterly for context / deployment / system-overview scenarios.

All scenarios use the **current canonical hardware** (post-iteration):
- Universal rail dock (all modules use the same top-rail interface)
- Side handles + safety-orange battery latches + cooling fins
- Telescoping masts on Scout + Relay + Lantern
- Lantern beacon head = canonical optical hardware (frosted white band
  + 360° aperture ring + antenna) used standalone OR mast-elevated
- X650-class quadcopter in motorized industrial drone-in-a-box case
  (NOT Pelican, fully-motorized lid, no manual latches)
- Matte grey-bronze + copper-bronze + sage-green + deep-Swedish-blue
  palette throughout

Dispatch via NB Pro. Reference images optional — text-only works for
all of these since they're scene compositions where the model has
latitude on per-element rendering. If you want tighter hardware
fidelity on any specific element, attach the corresponding render
(`chassis-platform-v04-solo.png`, `lantern-v02-omnidirectional-beacon.png`,
etc.) as a reference and add a "match Image N exactly" clause.

---

## Scenario 1 — Network topology overview (HERO)

**Use case:** Website hero / above-the-fold. Wide isometric system
overview proving the mesh deploys, chains extend, UAV uplinks,
operator UI surfaces.

```text
STYLE: Painterly Scandinavian field-concept art in the tradition of
sober Nordic engineering systems illustration — like a Vantor /
Ericsson / Volvo CE / Trimble technical diagram, painterly but
precise. Crisp subarctic light, restrained industrial design, readable
silhouettes, matte materials, faint engineering-visualization overlays.
Calm, practical, civilian-engineering register. NOT photoreal product
photography (use the painterly engineering-illustration register).
NOT sci-fi. NOT military. NOT combat. No weapons.

SUBJECT: Wide isometric system overview of a deployed laser-mesh
optical communications network in a remote signal-challenged Nordic
boreal forest area. The network is mid-deployment: a chain of compact
identical wheeled UGV nodes extending from a safe connected area into
the unmapped signal-challenged area, with one new chassis configured
as Relay (mast extended, omnidirectional beacon head active) in the
center as the newest extension to the chain. A small X650-class
quadcopter is overhead providing uplink. Several standalone Lanterns
are placed across the terrain as fixed mesh anchors. Operator-tablet
UI inset visible in one corner.

TERRAIN: Swedish boreal forest viewed from above at a 35-degree
isometric angle. Pine and birch forest, patchy snow, rocky ridges,
one unpaved service road threading through, low hills. Late-afternoon
winter light, blue-grey shadows. Remote infrastructure-sparse area.

NETWORK LAYOUT (the load-bearing visual claim):

- A CHAIN of 3-4 identical chassis-with-mast-module nodes
  (Relay configuration: wheeled chassis + rail-mounted base-plate
  + telescoping mast + omnidirectional beacon head on top)
  extending from the lower-left (safe connected area) into the
  upper-right (signal-challenged area, deeper terrain).
- The newest extension to the chain is the CENTER node, slightly
  highlighted — its telescoping mast is fully extended, beacon
  head visible with the 360° aperture ring catching light.
- BIDIRECTIONAL OPTICAL LINKS between consecutive chain nodes:
  faint, thin, precise blue paired lines with small opposing
  arrowheads near each end. Subtle, engineering-diagram style,
  NOT laser-show beams.
- LOCAL STAR-TOPOLOGY: from the center Relay node, 2-3 thin
  bidirectional optical links branching out to nearby Lanterns
  placed in the terrain (each Lantern visible as a small upright
  post with the omnidirectional beacon head, sage-green LED).
- AERIAL UPLINK: a small X650-class quadcopter (4 rotors, mid-
  size, matte white-grey body, sage-green underbelly markings)
  flying ~50 m above the center Relay, with a bidirectional
  optical link visible between the drone and the Relay's beacon
  head.

GROUND NODES (canonical hardware — must match laser-mesh family):
Each chassis is the same compact four-wheeled UGV — ~75-85 cm long,
matte grey-bronze + copper-bronze powder-coat panels, four chunky
off-road wheels with exposed suspension, side handles visible on
the flanks, swappable battery with safety-orange latches, electronics
cooling fins on the front face. Each chain node has a rail-mounted
base-plate on the top with a telescoping mast (matte grey-bronze,
3-4 nested segments visible) extended to ~70 cm, the omnidirectional
beacon head at the top (cylindrical, frosted-plastic white band +
360° ring of 6-8 deep-Swedish-blue aperture lenses + small stubby
antenna). Same chassis, same mast-module, just deployed at different
positions in the chain. NOT bulky, NOT military, NOT armored — small
civilian-engineering field instruments.

LANTERNS (standalone posts, scattered across the terrain): same
beacon head as the chain-node mast tips, but on small fixed bodies
(thermos-sized cylindrical body with frosted LED panel) bolted to
the ground via steel base plates. 3-5 Lanterns visible at various
positions, sage-green LEDs catching the light.

X650 QUADCOPTER (overhead): mid-size civilian survey/inspection
quadcopter, ~650 mm motor-to-motor diameter unfolded, 4 rotor arms
in X-configuration, matte white-grey upper body, sage-green
underbelly markings, belly optical-link payload visible (small
deep-Swedish-blue glass emitter + larger receive pane). Flying a
calm inspection/surveillance support pattern at moderate altitude.
NOT FPV racing, NOT military drone, NOT hexacopter.

OPERATOR-TABLET UI INSET (corner of the image, ~15% of frame area):
A clean inset showing the SAME terrain as a real-time 3D terrain
model with mesh visualization. UAV icon, ground node icons,
bidirectional link status indicators with directional arrows, mesh-
health summary, small text labels: "resilient optical mesh",
"shared spatial truth", "vision-based positioning", "signal-
challenged area: forward sector". Civilian-industrial UI register
— sage-green for healthy links, amber for aging anchors, NO red
alert overload, NO targeting graphics, NO combat-style UI.

LINK VISUALIZATION VOCABULARY (CRITICAL — engineering-diagram, not
laser-show):
- All optical communication links are FAINT thin precise blue paired
  lines with small opposing arrowheads near each end
- Subtle, like engineering-CAD visualization, NOT glowing laser
  beams, NOT bright energy weapons, NOT sci-fi laser shows
- Each link labeled subtly (small text near one end) when space
  allows: "bidirectional optical link"
- The center Relay can be labeled: "mesh / star relay node — newest
  extension"
- Link lines should be visible but the HARDWARE is the primary
  subject; links are supporting context

COMPOSITION: Wide 16:9 or 21:9 ultrawide isometric view. Network
topology readable first, individual hardware detail second. The
image should prove three claims at once: (1) the chain extends into
unmapped terrain, (2) the mesh has both ground-relay and aerial
uplink, (3) local star-topology branching from the newest node.

LIGHTING: Late-afternoon winter sun, low angle from one side. Warm
golden rim light on chassis edges, mast segments, beacon heads, and
the upper surfaces of the LIDAR/optical apertures. Cool blue ambient
fill from the northern sky. Sage-green LEDs and beacon-head apertures
read warm-and-present against the cool ambient.

ATMOSPHERE: Calm competence at infrastructure scale. The mesh
deployed, the chain extending, the system operating honestly under
partial information. NOT heroic, NOT combat, NOT marketing-spectacle.
A documentary moment of an engineering system doing its job in remote
terrain.

NEGATIVE: weapons, missiles, gun barrels, targeting reticle, military
strike, munitions, combat scene, soldiers, camouflage-heavy styling,
aggressive vehicle posture, sci-fi laser cannon, neon laser show,
explosions, smoke, oversized ground vehicles, tank-like robots,
tracked military vehicles (chassis are wheeled per canon), bulky
turret hardware, large laser hardware, glowing energy weapons,
defense-industry promo render, Hollywood war-movie aesthetic,
drone-warfare aesthetic, surveillance-fantasy framing, photoreal
product-photography register (this is painterly engineering
illustration), bronze-glossy materials (palette is MATTE grey-
bronze + matte copper-bronze, NOT shiny), neon glow on the optical
apertures (must catch winter-sun specular highlights, not glow),
chromatic-aberration lens flares, photography studio backdrop,
trade-show booth backdrop.
```

---

## Scenario 2 — First-kilometer deployment (architecture pitch — honest partial truth)

**Use case:** Architecture-pitch section. The "degraded-mode-as-default"
moment from scene-01 (Call Without Tools) — Mule advancing across
unmapped terrain in the early deployment, Relay holding station, no
fixed Lanterns yet, operator working with partial truth.

```text
STYLE: Painterly Scandinavian field-concept art for near-future
unarmed robotics. Painterly realistic but not photorealistic. Crisp
subarctic weather, low winter light, restrained industrial design,
readable silhouettes, matte materials, snow crust, frost,
condensation, amber/green UI glow, quiet operator tension. Think
high-quality concept art for a serious field prototype, not glossy
sci-fi marketing, not live-action film still, not game cinematic. No
weapons, no explosions, no combat heroism.

SUBJECT: First-kilometer deployment moment in a Swedish subarctic
boreal forest clearing. Civil twilight, ~06:30 local, December. The
laser-mesh team has been on-site for three hours but has not yet
placed any Lanterns into the ground — the mission window opened
early, the Mule is moving cargo before the mesh is fully anchored.
The architecture is doing its job: surfacing honest partial truth,
moving forward under named uncertainty, NOT freezing waiting for
ideal conditions.

SCENE COMPOSITION:

FOREGROUND LEFT: A laser-mesh chassis configured as Mule (cargo deck
mounted on the top rails, one Pelican-style transport case strapped
down to the deck, sage-green nylon restraint straps tensioned), in
the act of moving across the snow toward the upper-right. Faint
tread/wheel marks behind it in the snow. Slightly forward-leaning
visual posture — the Mule is advancing, not parked. A small sage-
green status LED visible on the chassis side.

MID-GROUND RIGHT: A second laser-mesh chassis configured as Relay
(rail-mounted base-plate with telescoping mast fully extended ~1.2 m
above ground, omnidirectional beacon head at the top with the 360°
aperture ring catching the early-twilight light), parked on a slight
rise. The Relay is holding station — stationary, beacon head active,
providing the only link-state-as-mission-geometry surface the mesh
currently has.

BACKGROUND: Sparse boreal forest perimeter — pines and birch in
soft focus, blue-grey twilight sky just beginning to lift, distant
low hills. Heavy snow on the forest floor, more snow in shaded
areas. The forest is the unmapped terrain the Mule is advancing
into.

OPERATOR TENT (frame right edge, partially visible): A small canvas
tent with a propane heater visible glowing warm-orange inside,
casting amber light onto the snow nearby. A rugged tablet on a
wooden ration crate inside the tent, screen visible with the laser-
mesh UI showing partial-truth telemetry (no Lantern dots placed,
Relay holding station, Mule's growing sigma-ring visible on the
tablet map). One human field technician in winter field gear
silhouetted at the tent opening watching the Mule advance — NOT a
soldier, civilian engineering attire, soft-shell jacket, work gloves.

THE LASER-MESH ARCHITECTURAL MOMENT (the visual claim):

This scene proves the laser-mesh degraded-mode-as-default discipline.
The mesh is operating WITHOUT any placed Lanterns yet. The Mule is
moving cargo across terrain whose map confidence is low. The Relay
provides the one stable comms surface. The operator-tablet (visible
in the tent) shows the system being honest about what it does and
does not know. NOT a triumphant deployment, NOT a heroic mission
moment — a routine first-kilometre under named uncertainty.

LIGHTING: Civil twilight, ~06:30 December. Sky just beginning to
lift from full night toward grey-blue dawn. The brightest light
source is the propane heater in the operator tent (warm amber glow
spilling onto the nearby snow). Cool blue ambient from the sky.
The Mule's sage-green status LED reads warm against the cool blue
snow. The Relay's beacon head apertures catch faint specular
highlights from the early light.

ATMOSPHERE: Cold competence. The system moving forward honestly
under partial information. The kind of routine field morning that
happens many times per deployment, captured to show what "deployed
under degraded mode" actually looks like in the subarctic.

COMPOSITION: 16:9 landscape. Mule in foreground left with tracks
behind it, Relay in mid-ground right on the slight rise, operator
tent frame-right edge with warm interior glow, boreal forest
backdrop in soft focus. The composition reads as documentary
field-engineering, not marketing-spectacle.

NEGATIVE: weapons, missiles, gun barrels, ammunition, combat,
soldiers, camouflage, military uniforms, tactical gear, MOLLE
webbing, body armor, defense-industry promo render, Hollywood
war-movie aesthetic, drone-warfare framing, oversized chassis,
tank-like robot, sci-fi laser cannon, neon glow, lens flares,
explosions, smoke, dramatic spotlights, marketing render, glamour
lighting, photography studio backdrop, trade-show booth backdrop,
bronze-glossy materials (palette is MATTE), Pelican brand visible
on the cargo case (generic civilian transport case), missing side
handles or battery latches on the chassis, lanterns visible in
the scene (this is the first-kilometre BEFORE Lanterns are placed
— no Lanterns in this image).
```

---

## Scenario 3 — Disagreement-surface UI close-up (operator's cognitive-load reduction visualized)

**Use case:** Pain-#3 section (operator cognitive load). Close-up of
the operator's rugged tablet showing the disagreement-surface UI in
action — anchor-decay color-coding, link-bending-alert timer, one
fused alert from three converging surfaces.

```text
STYLE: Painterly Scandinavian field-concept art for near-future
unarmed robotics. Painterly realistic but not photorealistic.
Restrained civilian-industrial UI design, sage-green and amber UI
glow against a cool blue ambient. Quiet operator tension, calm
focus. Concept-art register for a serious field prototype. NOT
sci-fi marketing, NOT Hollywood-tactical UI, NOT video-game HUD.

SUBJECT: Close-up of an operator's rugged field tablet showing the
laser-mesh UI in active deployment. The screen shows the
disagreement-surface visualization — the moment when three
converging surfaces (Lantern's PositioningDrift, Mule's
BodyfeelFlag, Scout's PerceptionDisagreementSurfaced) arrive
together and the UI fuses them into ONE alert instead of three
separate notifications. This is what cognitive-load reduction
looks like in software.

SCENE COMPOSITION:

PRIMARY SUBJECT: A rugged civilian-industrial tablet (matte black
casing with green status LED indicators on the edge, IP-rated
construction) held at angle, screen tilted slightly toward the
camera so the UI is clearly readable. The tablet is being held by
a gloved hand (winter glove, brown leather work glove visible
holding the tablet edge from below — the human is implied, not
the subject).

THE UI ON THE SCREEN (the load-bearing visual claim):

Top of screen: a small 3D terrain visualization in soft-grey wireframe
showing the deployment area — boreal forest contours, a few placed
Lanterns as small upright icons, the chassis positions, the active
mesh links as faint blue lines with directional arrows. NOT a
tactical map, NOT a combat HUD — a civilian-engineering terrain
visualization (like a forestry survey UI or a construction-site
monitoring app).

CENTER OF SCREEN: the disagreement-surface visualization made visible.
Three converging signals shown as faint colored vectors pointing
toward a shared "suspect area" in the terrain:
- One AMBER vector labeled "Lantern-3: PositioningDrift (anchor
  aging 3h 14m)"
- One AMBER vector labeled "Mule-1: BodyfeelFlag (slip reason)"
- One AMBER vector labeled "Scout-1: PerceptionDisagreementSurfaced
  (1.2m fusion residual)"
The three vectors converge on a small AMBER-OUTLINED CIRCLE in the
terrain, labeled "convergent disagreement — recommend Anchor-Setter
walk-back to Lantern-3". The amber-circle is the FUSED alert: three
signals become one operational action, not three competing
notifications.

BOTTOM OF SCREEN: a quiet status bar showing system health — mesh-
link health, battery levels across chassis, anchor-decay summary
(small color-coded list of Lanterns with their aging-color status:
green = fresh, amber = aging, red = needs reconfirmation). One
small button labeled "approve-with-review-flag" highlighted softly
(the operator's next action if they accept the recommendation).

NO RED ALERT OVERLOAD. NO targeting reticles. NO combat-UI elements.
The amber callout is the most-saturated color on screen, and it's
muted-amber, not aggressive-red.

ENVIRONMENT (background, soft focus): The interior of the operator
tent — canvas walls in deep shadow, propane heater glow warm-amber
just visible in the lower edge of the frame. Faint breath fog
visible near the tablet from the cold air. Outside the tent (visible
through a small canvas opening), early-winter daylight on snow.

CAMERA: Close-up, lens roughly at tablet level. ~85 mm equivalent
lens or short telephoto. Shallow depth of field — tablet screen
sharp, gloved hand and tent interior soft focus.

LIGHTING: The tablet screen is the brightest element in the frame —
its UI glow (sage-green + amber) provides the primary illumination.
Warm spill from the propane heater visible as soft amber on one
side. Cool blue ambient from outside the tent visible on the other
side. The lighting itself tells the story: warm operator-space,
cold field-truth, the tablet bridging them.

ATMOSPHERE: Quiet decision-making. The moment the operator sees the
fused alert and recognizes what it means — one walk-back to one
Lantern resolves three converging signals. The system has done its
cognitive work. The operator's next move is small and clear.

COMPOSITION: 3:2 landscape. Tablet fills the central 60% of the
frame, angled three-quarter toward camera so the UI is readable.
Gloved hand in the lower 25% of frame holding the tablet edge.
Tent interior in soft focus background occupying 15%.

NEGATIVE: weapons, military UI, tactical HUD, combat HUD, targeting
reticle, red alert overload, video-game UI, Hollywood-tactical
interface, sci-fi holographic display, neon glow on the screen,
chromatic-aberration glitch effects, glowing-text marketing UI,
flat illustration style (must be painterly with realistic lighting),
photoreal product-photography of just the tablet (this is the
painterly scene register, not product-photo), dramatic spotlights,
glamour lighting, military uniforms or insignia on the glove, MOLLE
gear visible, defense-industry promo render, sci-fi font on the UI
(use civilian-engineering sans-serif on screen, like IBM Plex Sans),
oversized tablet (must be rugged-civilian-industrial scale).
```

---

## Scenario 4 — Autonomous Lantern placement (Anchor-Setter → Hand transition moment)

**Use case:** Innovations section, illustrating the named §6
"Anchor-Setter → Hand transition arc" innovation. Hand chassis
reaching toward a Lantern that has frost-heaved out of position,
with the human Anchor-Setter visible in the background watching
but not intervening — the visual moment of human-in-the-loop
maturation.

```text
STYLE: Painterly Scandinavian field-concept art for near-future
unarmed robotics. Painterly realistic but not photorealistic. Crisp
subarctic weather, low winter light, restrained industrial design,
readable silhouettes, matte materials. Quiet operator tension, calm
deliberate motion. Concept art for a serious field prototype, not
sci-fi marketing.

SUBJECT: The Anchor-Setter → Hand transition moment in mid-afternoon
winter light. A laser-mesh chassis configured as Hand (manipulator-
arm-module mounted on the rails, arm extended forward and slightly
downward) is reaching toward a Lantern that has frost-heaved a few
meters out of its original placement position. The human Anchor-
Setter (Sven from the scene docs, but unnamed for this image) stands
nearby with empty hands, visibly ready as fallback but not
intervening. The Hand is doing the work; the human is the witness +
authority.

SCENE COMPOSITION:

CENTER OF FRAME: A laser-mesh chassis (Hand configuration) with the
4-5 DOF manipulator arm extended forward and slightly down. The arm
rises from a rail-mounted base-plate at front-center of the chassis
top, visible articulating joints, matte-black rubber-sheathed cable
routing along the arm (service-visible discipline). The 2-finger
parallel gripper is OPEN, approaching the Lantern at ground level.
Wrist camera visibly angled toward the gripper's target. The chassis
itself: matte grey-bronze + copper-bronze panels, four chunky off-
road wheels with exposed suspension, side handles + safety-orange
battery latches + cooling fins all visible.

LANTERN (lower-right of frame, ground level): A standalone Lantern
that has frost-heaved ~3 meters from its original placement —
visibly tilted slightly, base plate cocked at a small angle in the
snow, but the body still upright, telescoping mast fully extended,
omnidirectional beacon head still active (sage-green LED visible,
360° aperture ring catching the afternoon light). A small survey
nail visible in the snow nearby where the Lantern WAS originally
set (the frost-heave displaced it by ~3m). The Hand is about to
pick it up to re-place it correctly.

HUMAN ANCHOR-SETTER (background left, partially in soft focus): A
human field technician in civilian winter engineering attire (soft-
shell jacket, work gloves, no uniform, no military insignia),
standing ~5 meters back from the action. Posture: hands empty,
relaxed but attentive, watching the Hand do the work but not
moving to intervene. Mid-30s to mid-50s read. Face partially visible,
expression: focused and calm — the human-in-the-loop authority is
present, but the autonomous Hand is the actor in this moment.

ENVIRONMENT: Mid-afternoon winter light in a Swedish boreal forest
clearing — fresh snow over crust, visibility ~200 meters, low
winter sun catching the chassis + Hand-arm + Lantern beacon head
with warm golden rim light. Sparse pines and birch in the background.
Distant low hills in soft focus.

OPERATOR-TABLET (small detail, the human's right hand holds a small
rugged tablet at hip level, screen showing the placement-task UI
with a small "approve-with-review-flag" badge visible — the operator
approves the Hand's autonomy forward, the audit lands later).

THE ARCHITECTURAL MOMENT (the visual claim):

This scene proves the Anchor-Setter → Hand transition arc. The human
is present (still the authority, still the witness, still the audit
holder) but the autonomous Hand is doing the placement work. The
Lantern's frost-heave is a routine operational event, the system
handles it routinely, the human reviews-rather-than-blocks. Early
demos showed human doing all placement; this moment shows the same
capability (`lantern-placement@v1`) answered by a different
implementer (autonomous Hand instead of human hands).

LIGHTING: Mid-afternoon winter sun, low angle from one side. Warm
golden rim light on the chassis edges, the manipulator arm joints,
the Lantern beacon head apertures. Cool blue ambient fill. The
Hand's gripper jaws catch a clean specular highlight. The Lantern's
sage-green LED reads warm against the cool ambient.

ATMOSPHERE: Quiet maturation. NOT a triumph moment, NOT a "robots
replace humans" framing. A routine field moment where the autonomous
hardware is doing what it was designed to do, with the human still
present as authority + witness. The discipline is visible: the
operator-tablet approval flow is happening, the human's posture is
relaxed-attentive (not intervening, not absent), the Hand's motion
is slow and deliberate (not triumphant claw-grab).

COMPOSITION: 16:9 landscape. Hand chassis + extended arm in the
center, Lantern in the lower-right ground-level, Anchor-Setter in
the mid-left background ~5m back, boreal forest backdrop in soft
focus. The composition's emotional center is the SPACE between the
Hand and the human — that space IS the maturation arc.

NEGATIVE: weapons, gun, missile, military scope, threat weapon,
humanoid robot, robot face, android, anthropomorphic, three-finger
or five-finger claw, decorative claw, sci-fi grasping arm,
oversized arm, weapon arm, military Anchor-Setter (must be civilian
engineering attire), military uniform on the human, soldier with
weapon, tactical gear, MOLLE webbing, body armor, helmet, defense-
industry promo render, drone-warfare aesthetic, hollywood war-movie
aesthetic, the human intervening physically (the human must be
hands-empty, NOT touching the Lantern or the Hand), the Hand
triumphantly holding the Lantern up (must be in mid-reach, NOT in
"I lifted it" pose), missing chassis features (handles, battery
latches, cooling fins must be visible), Lantern as a candle/oil
lamp (must be the canonical Lantern beacon-head design with
frosted band + 360° aperture ring), bronze-glossy materials
(palette is MATTE), glamour lighting, dramatic spotlights, lens
flares.
```

---

## Scenario 5 — Loading the kit into civilian transport

**Use case:** Pain-#1 section (forward human risk) + open-architecture
section. The deployment moment — two technicians loading a laser-mesh
chassis + module crates into the back of a civilian utility van,
demonstrating the "deployable by small team from safe pickup point"
claim.

```text
STYLE: Painterly Scandinavian field-concept art for near-future
unarmed robotics. Painterly realistic but not photorealistic. Crisp
subarctic light, restrained civilian-engineering register. Quiet
competence. Concept art for a serious field prototype, NOT marketing
spectacle. NOT military. NOT defense-industry promo. No weapons.

SUBJECT: Two human field technicians in mid-action loading a laser-
mesh chassis (no modules mounted in this shot — chassis in transport
configuration) into the back of a parked civilian utility van or
pickup truck. The chassis is at tailgate height between them, side
handles engaged, mid-lift posture. A small Pelican-style transport
case (containing modules) sits on the ground beside the van, ready
to be loaded next. Captures the deployment moment — kit going from
safe pickup point INTO the operational area.

SCENE COMPOSITION:

CENTER OF FRAME: The two technicians on opposite long sides of the
chassis, each gripping one of the proud matte-black U-loop side
handles with one hand, lifting the chassis up toward the tailgate
height between them. Chassis at about waist height between the two
technicians, about to be slid into the cargo bed. Mid-walk loading
posture — knees slightly bent, backs straight.

THE TWO TECHNICIANS:
- Both in civilian winter engineering attire — soft-shell jackets
  (earth-tone forest-green, NOT camouflage), work gloves, no
  uniforms, no patches, no insignia
- Mid-30s to mid-50s read, professional engineering presence
- NOT soldiers, NOT military operators, NOT defense contractors —
  field technicians deploying the system

THE CHASSIS (canonical, no modules in transport configuration):
- Compact rectangular four-wheeled UGV, ~75-85 cm long, ~25-35 kg
- Matte grey-bronze + copper-bronze powder-coat panels
- Four chunky off-road wheels with exposed suspension
- Proud matte-black U-loop side handles CURRENTLY ENGAGED by both
  technicians' hands
- Swappable battery module with TWO safety-orange or red quick-
  release latches visible on the side
- Electronics cooling module with visible heat-sink fins on the
  chassis front face
- Top mounting rails visible and EMPTY (no module attached — this
  is transport configuration; modules are in the transport case
  on the ground)
- Sage-green status LEDs

THE CIVILIAN UTILITY VAN (rear of vehicle visible, tailgate down):
- A civilian utility van OR pickup truck (NOT a military vehicle in
  this shot — operator wants the "civilian deployable" framing for
  this scenario), matte earth-tone paint, generic civilian
  commercial styling. Could be a Volvo / Mercedes Sprinter / Ford
  Transit / Land Rover Defender utility variant — civilian field-
  service vehicle vocabulary
- Tailgate DOWN, cargo bed visible at waist height
- Cargo bed visible matte ribbed metal lining, mostly empty (ready
  to receive the chassis + module case)
- NO weapons mounted, NO turret, NO military hardware

A small Pelican-style transport case (matte-grey, generic civilian
engineering kit case) sits on the snow-dusted ground at the lower-
left of frame, containing modules (the cargo deck, mast-module
base-plate, sensor-mast assembly, etc., all packed for transport
into the operational area).

ENVIRONMENT: Outdoor parking area at the edge of a Swedish boreal
forest — sparse pines and birch in soft focus background, patchy
snow on dark gravel, distant low hills. Late-afternoon winter sun.
The van is parked on the gravel, the technicians are at the
tailgate, the forest is just behind them.

LIGHTING: Late-afternoon winter sun, low angle from one side. Warm
golden rim light on the chassis edges, the technicians' jacket
shoulders, the tailgate edge, and one face plane of each technician.
Cool blue ambient fill from the northern sky.

ATMOSPHERE: Calm competence. "The kit goes in the van, the van
drives to the deployment site, the team unloads and assembles on-
location." Reads as routine field-engineering deployment, not a
hero scene, not a special-ops mission, not a marketing video. The
chassis is small enough that two civilian technicians load it
together. THAT is the architectural pitch this scenario makes
visible.

COMPOSITION: 3:2 landscape. Both technicians + chassis fill the
center 60% of the frame, in mid-loading action at the van tailgate.
Pelican-style case in lower-left edge. Van/pickup body visible
right edge (cargo bed clearly visible). Boreal forest backdrop in
deeper soft focus.

NEGATIVE: weapons, soldiers, military uniforms, tactical gear,
MOLLE webbing, body armor, helmets, military vehicle (this is the
civilian-deployment scenario — military vehicle goes in a separate
shot), combat scene, defense-industry promo render, Hollywood
war-movie aesthetic, oversized chassis (must match canonical
~75-85 cm scale), three or more technicians (must be exactly two),
single technician carrying the chassis alone (this is two-person
side-handle carry per the canonical spec), modules mounted on the
chassis (this is transport configuration with empty rails),
camouflage on the van (must be civilian utility commercial paint),
glossy marketing render, glamour lighting, dramatic spotlights,
lens flares, photography studio backdrop, bronze-glossy materials
(palette is MATTE).
```

---

## Notes for the website agent

- **Use these in alternation with product-photo renders.** Each
  scenario above is a SCENE; the existing chassis-platform / module
  renders are HARDWARE SPEC SHEETS. The website's visual rhythm
  benefits from alternating between the two registers — painterly
  for context, photoreal for hardware detail.

- **Dispatch order if cost matters:**
  1. Scenario 1 (network topology) — highest hero-impact, best
     ROI for the website's above-the-fold
  2. Scenario 3 (disagreement-surface UI) — illustrates the
     cognitive-load pitch in a way the hardware shots can't
  3. Scenario 5 (loading the kit) — concrete deployment moment,
     reinforces the "two-person liftable" claim
  4. Scenarios 2 + 4 — narrative depth, useful but not first-pass
     critical

- **Reference images optional.** All five scenarios are written as
  text-only prompts (the canonical hardware vocabulary is rich
  enough that NB Pro can render without references). If you want
  tighter hardware fidelity on any specific element, attach the
  relevant render (`chassis-platform-v04-solo.png`,
  `lantern-v02-omnidirectional-beacon.png`,
  `relay-v03-mast-extended.png`, etc.) as a reference and add a
  "match Image N exactly" clause to the prompt.

- **Style consistency across the website.** All five scenarios use
  the same `laser-mesh-scandinavian-field` painterly register —
  they will visually cohere as a set. The hardware-spec renders
  use the `laser-mesh-nordic-product-photo` register; the two
  registers are deliberately distinct so the website's reader
  recognizes context-vs-spec at a glance.

- **Cost estimate:** ~$0.13 per render in NB Pro at 2K, ~$0.24 at
  4K. Five scenarios at 2K = ~$0.65. Worth iterating any that
  drift on first dispatch.
