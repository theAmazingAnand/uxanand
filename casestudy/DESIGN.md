---
version: "1.0-theme-preview"
name: "CarSlot Cinematic Grid"
product: "CarSlot UX Case Study"
status: "awaiting-visual-approval"
scope: "casestudy only"
reference:
  title: "Creative Agency Website – Nguyan | UI/UX Case Study"
  url: "https://www.behance.net/gallery/248473873/Creative-Agency-Website-Nguyan-UIUX-Case-Study"
  usage: "Independent interpretation of publicly visible visual patterns; never copy artwork, brand identity, proprietary imagery, or exact composition."
---

# CarSlot Cinematic Grid

## 1. Intent

Create a memorable, portfolio-grade UX case study that feels cinematic and engineered while remaining easy to read, scan, navigate, and operate. The visual system should support research evidence, UX diagrams, wireframes, interface screens, validation findings, and a separate final-prototype experience.

The signature is **controlled illumination**: a near-black technical canvas, one hot orange action colour, fine grid lines, quiet data labels, large editorial typography, and selective glow. Orange is evidence and action—not decoration everywhere.

## 2. Experience principles

1. **Narrative before decoration** — every visual treatment must clarify the UX story.
2. **One luminous action colour** — orange identifies progress, relationships, emphasis, and primary CTAs.
3. **Quiet reading surfaces** — long-form copy sits on clean, high-contrast surfaces without texture behind it.
4. **Diagrams are first-class content** — IA and flow diagrams use real HTML structure, readable labels, and text equivalents.
5. **Evidence stays traceable** — artifacts, insights, decisions, and outcomes receive distinct labels.
6. **Motion explains state** — transitions reveal hierarchy or navigation state; they never delay reading.
7. **The prototype is a separate destination** — all final-product CTAs open the prototype in a new tab.

## 3. Colour system

```yaml
colors:
  canvas: "#070707"
  canvas-deep: "#030303"
  surface: "#10100f"
  surface-raised: "#171411"
  surface-warm: "#21150f"
  surface-light: "#f3eee8"
  ink: "#fffaf4"
  body: "#d3cbc3"
  muted: "#92877d"
  muted-strong: "#b4aaa1"
  ink-on-light: "#17110e"
  body-on-light: "#5f554e"
  line: "#2b2622"
  line-strong: "#4b3930"
  line-light: "#d8cec5"
  action: "#ff5a1f"
  action-hover: "#ff7345"
  action-active: "#dc3f0d"
  action-soft: "#ffb094"
  action-wash: "rgba(255, 90, 31, 0.10)"
  amber: "#f2a65a"
  success: "#78c99a"
  warning: "#f0bd66"
  danger: "#ff8175"
  focus: "#ffd0bd"
```

### Colour rules

- `action` is the only brand/action colour in navigation, primary CTAs, diagram connectors, and active states.
- Use `surface-light` only for readability resets such as detailed IA, dense tables, or long findings.
- Status colours must always be paired with labels or icons.
- Glow is permitted behind one hero object, one major CTA, or the active diagram path—never around every card.
- Body text must meet WCAG AA contrast against its surface.

## 4. Typography

Use locally available/system fonts; do not depend on a network font request.

```yaml
typography:
  display-family: "Arial Narrow, Roboto Condensed, Inter Tight, Arial, sans-serif"
  text-family: "Inter, Aptos, Segoe UI, Arial, sans-serif"
  mono-family: "IBM Plex Mono, SFMono-Regular, Consolas, monospace"
  display-hero:
    size: "clamp(64px, 11vw, 150px)"
    weight: 700
    line-height: 0.82
    letter-spacing: "-0.065em"
  display-section:
    size: "clamp(44px, 7vw, 92px)"
    weight: 700
    line-height: 0.9
    letter-spacing: "-0.05em"
  heading-lg:
    size: "clamp(30px, 4vw, 54px)"
    weight: 600
    line-height: 1.02
    letter-spacing: "-0.035em"
  heading-md:
    size: "26px"
    weight: 600
    line-height: 1.12
  heading-sm:
    size: "18px"
    weight: 600
    line-height: 1.25
  lead:
    size: "clamp(19px, 2vw, 26px)"
    weight: 400
    line-height: 1.42
  body:
    size: "16px"
    weight: 400
    line-height: 1.65
  body-sm:
    size: "14px"
    weight: 400
    line-height: 1.55
  eyebrow:
    family: "mono-family"
    size: "11px"
    weight: 600
    line-height: 1.4
    letter-spacing: "0.16em"
    transform: "uppercase"
```

### Typography rules

- Hero display can be dramatic; all artifact labels and diagrams remain conventionally readable.
- Avoid centred paragraphs longer than three lines.
- Use mono uppercase labels for phase, evidence type, version, node ID, and metric labels.
- Use sentence case for headings and controls.

## 5. Spacing and layout

```yaml
spacing:
  1: "4px"
  2: "8px"
  3: "12px"
  4: "16px"
  5: "24px"
  6: "32px"
  7: "48px"
  8: "64px"
  9: "96px"
  10: "144px"
layout:
  content-max: "1240px"
  reading-max: "760px"
  wide-diagram-max: "1440px"
  page-gutter: "clamp(20px, 4vw, 56px)"
  section-block: "clamp(88px, 12vw, 170px)"
  grid: "12 columns desktop / 8 tablet / 4 mobile"
```

### Grid texture

- Use a 40px square grid built with subtle CSS gradients.
- Grid opacity stays below 7% on reading areas.
- A stronger grid may appear behind diagrams, never behind dense paragraphs.

## 6. Geometry and depth

```yaml
radii:
  none: "0"
  xs: "4px"
  sm: "8px"
  md: "16px"
  lg: "28px"
  pill: "999px"
elevation:
  flat: "none"
  hairline: "0 0 0 1px rgba(255,255,255,0.09)"
  raised: "0 24px 70px rgba(0,0,0,0.40)"
  action-glow: "0 0 48px rgba(255,90,31,0.26)"
```

- Cards use borders and tonal contrast before shadow.
- Screen/device frames may use `raised`.
- Buttons use `action-glow` only on hover/focus in the final dark CTA chapter.

## 7. Navigation

### Sticky navigation

- Height: 64px desktop, 58px mobile.
- Canvas: translucent near-black with blur.
- Contains project mark, section links, reading progress, and `Explore product` CTA.
- Active section uses an orange dot and brighter text.
- On smaller screens, section links scroll horizontally; the primary CTA remains reachable.

### Reading progress

- 2px fixed bar along the top edge.
- Uses `action` and reflects document scroll progress.
- Must not be the only indication of current location.

## 8. Component system

### Buttons

**Primary**
- Orange fill, black text, 48px minimum height, pill radius.
- Arrow moves no more than 3px on hover.

**Secondary**
- Transparent, ink text, 1px `line-strong`, pill radius.

**Text action**
- Ink text, orange underline on hover/focus.

### Evidence card

- Mono label: `INSIGHT`, `DECISION`, `OUTPUT`, or `OUTCOME`.
- Title, concise explanation, optional metric or artifact link.
- Cards may span different grid widths, but reading order remains logical.

### Phase chapter

- Oversized phase number and title.
- One-sentence objective.
- Inputs, activity, evidence, and outcome summary.
- One orange illuminated divider or path.

### Quote / insight

- 28–44px statement on a quiet surface.
- Orange rule at left or small orange marker; no giant quotation marks.

### Artifact frame

- Dark browser/device frame.
- Caption below with artifact name, phase, takeaway, and optional full-view action.
- Do not place small screenshots in 3-column cards; use large presentation areas.

## 9. Diagram language

### Information architecture

- Light reading surface or high-contrast dark diagram canvas.
- Root node is orange; primary categories are warm raised surfaces; leaf nodes are quiet outlined cards.
- Connector lines are 1px; active branch is 2px orange.
- Node IDs use mono labels.
- On mobile, the tree becomes a horizontally scrollable diagram with a text outline immediately below.

### User flow

- Start/end nodes use pill geometry.
- Screens/actions use rounded rectangles.
- Decisions use diamond-like CSS geometry only when readable; otherwise use labelled decision cards.
- Primary path is orange; alternate is amber; recovery is muted; success is green.
- Every visual flow includes an ordered-list text equivalent.

### Matrices and comparisons

- Use light surfaces for dense tables.
- Strong row labels, thin dividers, orange highlight for the selected priority.
- On mobile, tables convert to labelled stacked cards.

## 10. Motion

```yaml
motion:
  fast: "140ms"
  standard: "260ms"
  reveal: "520ms"
  easing: "cubic-bezier(.2,.8,.2,1)"
```

- Reveal sections with opacity and a maximum 18px vertical movement.
- Do not animate long-form text line by line.
- Diagram paths may illuminate after the diagram enters the viewport.
- Respect `prefers-reduced-motion`; remove transforms and smooth scrolling.

## 11. Responsive behaviour

| Range | Behaviour |
|---|---|
| 0–599px | Four-column layout, single-column narrative, horizontal diagram overflow, 44px touch targets |
| 600–899px | Eight-column layout, two-column evidence cards, stacked narrative/visual pairs |
| 900–1199px | Twelve columns, compact sticky navigation, full diagram labels |
| 1200px+ | Full editorial composition, 1240px content, 1440px wide diagrams |

### Responsive rules

- Never reduce body text below 15px.
- Keep primary CTA visible without covering content.
- Large display type may wrap but must not clip.
- Screens stack vertically below 760px.
- Interactive diagrams must also expose a static accessible reading order.

## 12. Accessibility

- WCAG AA contrast for text and controls.
- Visible 3px `focus` outline with 3px offset.
- Skip link to main content.
- Semantic headings in sequential order.
- Diagrams include text equivalents.
- Minimum pointer target: 44 × 44px.
- No information communicated by colour alone.
- Motion disabled or simplified when reduced motion is requested.
- New-tab prototype links disclose `Opens in a new tab` to assistive technology.

## 13. UX artifact mapping

| Artifact | Preferred presentation |
|---|---|
| Requirements | Scope cards + constraint strip |
| Discovery gaps | Known / unknown / validate map |
| Competitors | Comparison matrix + positioning plot |
| Persona | Full-width editorial profile |
| Pain points | Severity rail + evidence cards |
| Problem framing | Oversized statement + HMW cards |
| Opportunities | Prioritisation matrix |
| Feature definition | Feature stack and dependencies |
| Double Diamond | Illuminated four-phase pathway |
| Information architecture | Hierarchical tree with text outline |
| User flow | Flowchart with primary, alternate, and recovery paths |
| Wireframes | Progressive large-frame gallery |
| Visual design | Full-bleed screen chapters |
| Accessibility | Issue/status scorecard |
| Validation | Severity table + iteration timeline |
| Responsive design | Multi-device comparison |
| Specifications | Annotated screen panels |
| Handoff | Readiness checklist |
| Final product | Cinematic showcase + new-tab CTA |
| Outcomes | Evidence-backed outcome cards |

## 14. Content constraints

- Do not mention agents, orchestration mechanics, prompts, or internal skill structure.
- Do not invent user-testing results, launch metrics, business performance, or research participants.
- Clearly distinguish validated findings, design-review evidence, assumptions, and proposed next steps.
- Keep the full case study grounded in existing CarSlot artifacts.
