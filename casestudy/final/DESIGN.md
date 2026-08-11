# CarSlot case-study design direction

## Concept

**Editorial certainty.** A premium long-form case study that contrasts the uncertainty of traditional service booking with a clear, evidence-aware product journey.

The visual language combines a calm editorial foundation with selective cinematic moments. The page is mostly warm white and ink black. Orange marks an active constraint, decision, path, or call to action. Existing product screens are presented through the supplied MacBook Pro, iMac, and iPad SVG mockups without redrawing the interface.

## Experience structure

1. Hero — product promise, gentle motion, scope and evidence boundary.
2. Overview — challenge, role, geography, status, and measurable delivery facts.
3. Discover — requirements, market patterns, persona, pains, and insights.
4. Define — problem statements, opportunity priorities, and concept boundary.
5. Develop — double diamond, IA tree, user flow, wireframe states, visual system, accessibility.
6. Deliver — responsive solution, review gates, handoff, outcomes, and remaining risks.
7. Artifact library — all 27 outputs, filterable by phase.
8. Final prototype CTA — opens the product prototype in a new tab.

## Navigation

- Fixed global header with section links and prototype CTA.
- Sticky vertical phase rail on desktop; compact horizontal phase rail on small screens.
- Intersection-based active state provides orientation without hiding content.
- Every primary section has an anchor and remains available in continuous reading order.

## Motion

- Two soft ambient fields move over 18–24 seconds.
- A journey line shifts slowly behind the original hero screen.
- The frame containing that screen floats by only a few pixels to create depth.
- The progress dot pulses gently.
- `prefers-reduced-motion` disables animation and smooth scrolling.

## Typography and color

- Typeface: system sans-serif stack; no external font dependency.
- Display type: high contrast, tight tracking, fluid sizes.
- Warm white: `#f5f1e8`
- Paper: `#fffdf8`
- Ink: `#10100f`
- Muted ink: `#65635e`
- Path orange: `#ff5a1f`
- Product action blue: `#0066cc`

## Content principles

- Findings are separated from hypotheses.
- No invented participant quotes or post-launch metrics.
- “Approved” refers to phase-review status, not production readiness.
- Unknowns remain visible in the closing risk register.
- Visual summaries link to their full original artifacts.
- Application screens are not recreated; the supplied mockup artwork is used directly and clearly labelled.

## Reusable case-study pattern

Use the following structure when adapting this presentation to another project.

### Narrative sequence

1. **Hero:** one-line product promise, project type, evidence boundary, primary prototype CTA.
2. **Overview:** challenge, scope, geography, method, status, source, and delivery facts.
3. **Discover:** requirements, research method, market patterns, persona, pains, and insights.
4. **Define:** primary problem statement, connected problems, opportunity prioritization, and concept boundary.
5. **Develop:** process model, information architecture, user flow, wireframes, visual system, and accessibility.
6. **Deliver:** approved product screens, responsive behavior, validation, handoff, outcomes, and unresolved risks.
7. **Library:** source artifacts grouped and filterable by phase.
8. **Closing CTA:** open the final output in a new tab or screen.

### Required visual representations

| UX content | Recommended representation |
|---|---|
| Project facts | Editorial metadata list and metric strip |
| Market review | Comparison cards followed by pattern rows |
| Persona | Editorial profile split with goals and evidence label |
| Pain points | Ranked evidence list with confidence markers |
| Problem statement | Full-width high-contrast typographic chapter |
| Opportunities | Two-axis priority matrix plus text legend |
| Scope | In/out boundary comparison |
| Process | Double Diamond diagram |
| Information architecture | Connected tree structure |
| User flow | Directional flowchart with decision nodes and recovery branches |
| Wireframes | Horizontally browsable numbered screen rail |
| Final UI | Existing approved screens inside device mockups; never redraw the product |
| Validation | Phase-gate timeline |
| Outcomes | Delivery facts separated from post-launch impact |
| Risks | Visible closing risk register |

### Device presentation rules

- Use approved application captures inside supplied mockup artwork as the only screen source.
- Place desktop states inside a MacBook or neutral Windows-laptop frame.
- Place tablet states inside an iPad-style frame.
- Place mobile states inside a phone frame.
- Device hardware is presentation framing only; do not modify the UI shown inside it.
- Label the viewport and screen state outside the device.
- Maintain a direct link to the full interactive output.
- Do not claim a viewport is validated unless its responsive behavior exists in the source.

### Layout tokens

| Token | Value | Use |
|---|---|---|
| `--max` | `1240px` | Maximum narrative width |
| Desktop gutter | `24px` minimum | Page breathing room |
| Section spacing | `88px–150px` | Long-form chapter pacing |
| Major grid gap | `40px–110px` | Asymmetric editorial layouts |
| Hairline | `1px solid rgba(16,16,15,.16)` | Structure without heavy cards |
| Corner radius | `0–18px` | Mostly square editorial surfaces; larger only for hardware |
| Shadow | `0 30px 90px rgba(12,12,11,.14)` | Device and focal-object depth |

### Responsive rules

- At approximately `980px`, collapse two-column narrative layouts and convert the phase rail into a sticky horizontal selector.
- At approximately `680px`, use one-column content, shorten device heights, and keep diagrams horizontally scrollable when shrinking would reduce meaning.
- Preserve headings, certainty states, evidence labels, and risk language at every viewport.
- Hide only decorative or duplicated elements.
- Keep all primary CTAs at least 44px high.

### Motion rules

- Animate only the hero framing and ambient background.
- Use translation of approximately 4–10px; avoid large rotation or rapid parallax.
- Recommended duration: 8–24 seconds with ease-in-out timing.
- Do not animate the application interface unless animation already exists in the approved product.
- Disable non-essential motion under `prefers-reduced-motion: reduce`.

### Accessibility checklist

- Provide a skip link and semantic landmarks.
- Keep one logical heading hierarchy.
- Make phase and artifact navigation keyboard accessible.
- Use visible focus states with at least 3:1 component contrast.
- Pair every status color with explicit text.
- Give every embedded screen a descriptive title.
- Keep diagrams understandable through adjacent explanatory copy.
- Make the continuous narrative available even when navigation scripts fail.

### Evidence checklist

- Label hypotheses, assumptions, and unvalidated personas.
- State the source and research limitations near the beginning.
- Do not invent participant quotes, sample sizes, usability metrics, or business impact.
- Separate design-delivery outcomes from post-launch results.
- Keep deployment and production-readiness status explicit.
- End with the research, policy, technology, and operational questions still open.

### Adaptation checklist

Replace the following project-specific values while preserving the pattern:

- Product name and promise
- Problem statement
- Geography and audience
- Evidence boundary
- Phase artifacts and source links
- Persona and pain-point content
- Opportunity priorities
- IA and flow nodes
- Approved application screen sources
- Outcome facts and unresolved risks
- Accent color, while retaining the warm editorial foundation unless the new brand requires otherwise
