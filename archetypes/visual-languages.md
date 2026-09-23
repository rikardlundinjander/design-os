---
layer: visual
version: 0.1
status: draft
---

# Visual languages

Layer 3 of the archetype system. A visual language is **art direction expressed as principles**: how hierarchy is created, how space is used, what shapes, surfaces, color and imagery do, and what is deliberately left out.

A visual language is not a theme and not a brand. It says "typography carries the hierarchy and containers are rare", not "use this font in this blue". The same visual language can be applied to many brands, and the same brand can be expressed through different visual languages.

---

## How it relates to other layers

| Layer | Decides | Example |
|---|---|---|
| Product type | What the product is | A commerce product with a catalog and checkout |
| Experience model | How the user engages | Object-first browsing with a workflow checkout |
| **Visual language** | **The character of the form** | **Editorial: type-led hierarchy, few containers, asymmetry** |
| Motion language | How things move | Quiet, functional transitions |
| Density and personality | How much, how strong | Density 40, expressivity 60 |
| Brand | The specific assets | Typefaces, colors, logo, imagery, tone |

Visual language sets the **character**. Density and personality set the **amount**. Brand supplies the **specific assets**.

Editorial at high density becomes a newspaper. Editorial at low density becomes a magazine. Same language, different dial settings.

---

## How to use this file

1. **Pick one dominant visual language.** It governs every surface unless a scope says otherwise.
2. **Optionally add one secondary language, with a scope.** Example: "Editorial for marketing and content pages, Precision for the signed-in product." Never blend two languages on the same surface without a stated rule for which one wins.
3. **Copy the principles and the avoid list into the project.** The avoid list is the most important part when working with AI, because it stops output from drifting toward the generic default.
4. **Calibrate with the tendencies table.** It translates the language into starting ranges for tokens. Density and personality dials then adjust within those ranges.
5. **Let brand fill in the specifics.** Typefaces, color values and imagery come from the brand layer and should fit the chosen language.

If you cannot decide, answer this: *what should carry the hierarchy on a typical screen: type, space, color, containers or imagery?* The answer narrows the choice quickly.

---

## What this layer owns

| This layer decides | This layer does not decide |
|---|---|
| What carries hierarchy (type, space, color, containers, imagery) | Specific typefaces and color values (brand) |
| Typographic character and scale contrast | Content and tone of voice (brand) |
| Composition, grid behavior and use of whitespace | Amount of density (density and personality) |
| Shape language: radius, lines, borders | Navigation structure (experience model) |
| Surfaces, containers and depth | How things move (motion language) |
| The role of color (not the colors) | Which views exist (product type) |
| The role of imagery and iconography | |
| What is deliberately absent | |

---

## Non-negotiables

No visual language overrides these. A language can be quiet, raw or experimental and still meet them.

- Text meets contrast requirements for its size.
- Focus is always visible.
- Color is never the only way information is conveyed.
- Interactive elements are recognizable as interactive.
- Text sizes stay legible for the context and reading distance.
- The language works with user preferences such as larger text, higher contrast and reduced transparency.

---

## The generic default

Without direction, generated interfaces drift toward one look. Name it, so it becomes a choice rather than an accident.

**Signs of the generic default:**
- Every piece of content inside a card with medium radius and a soft shadow
- Cards inside cards
- A centered hero with a large headline, a subline and two buttons
- Feature grids of three or four items, each with an icon in a tinted circle
- Blue or purple gradients as the main expression
- All elements at similar visual weight, so nothing leads
- Decorative badges, pills and dividers everywhere
- Uniform spacing that ignores content relationships

None of these are wrong in isolation. Together, by default, they produce sameness. Every visual language below includes an avoid list that pushes away from this default in its own direction.

---

## Schema

Every visual language uses the same sections.

- **Definition:** one sentence.
- **Feels like:** three words.
- **Hierarchy is carried by:** the primary tools for creating order.
- **Typography:** character, scale contrast and roles.
- **Space and composition:** grid, alignment and whitespace.
- **Shape:** radius, lines and borders.
- **Surface and depth:** containers, layers and elevation.
- **Color:** the role of color, not the values.
- **Imagery and icons:** what images and icons do.
- **Principles:** rules that can be followed by people and AI.
- **Avoid:** what breaks the language.
- **Tendencies:** starting ranges for calibration.
- **Fits well with:** product types and experience models.
- **Risks:** where the language fails.

---

## Overview

| Language | Hierarchy carried by | Expression | Containers | Ornament |
|---|---|---|---|---|
| [Neutral](#neutral) | Conventions, weight, position | Low | Medium | None |
| [Editorial](#editorial) | Typography, space | Medium | Few | Low |
| [Precision](#precision) | Alignment, weight, grid | Low | Structural | None |
| [Warm](#warm) | Space, color, imagery | Medium | Soft, frequent | Low |
| [Refined](#refined) | Space, restraint | Low | Very few | Minimal |
| [Playful](#playful) | Color, shape, scale | High | Shaped, frequent | Medium |
| [Graphic](#graphic) | Color fields, scale, grid | High | Color blocks | Low |
| [Brutalist](#brutalist) | Raw structure, type | High | Exposed | Deliberately none |
| [Cinematic](#cinematic) | Imagery, scale, depth | High | Layers | Atmospheric |

---

## Neutral

**Definition:** A deliberately quiet language that follows platform and interface conventions, so the content and the task are all that stand out.

**Feels like:** Familiar, calm, dependable.

**Hierarchy is carried by:** Font weight, position and established conventions.

**Typography:**
- A single, highly legible family, often a system or neutral sans-serif
- Modest scale contrast
- Weight does most of the work; size changes are small

**Space and composition:**
- Consistent, predictable spacing
- Standard layouts that users recognize
- Alignment to a simple grid

**Shape:** Small to medium radius, consistent everywhere. Thin borders where needed.

**Surface and depth:** Containers used for grouping when needed. Minimal elevation, reserved for overlays.

**Color:** Mostly neutral. One accent reserved for interaction and selection. Semantic colors for status only.

**Imagery and icons:** Functional icons in one consistent style. Imagery only when it is content.

**Principles:**
- Follow conventions unless there is a clear reason to break them.
- One accent color, used only for what the user can act on or has selected.
- Every visual decision should be invisible to the user.

**Avoid:**
- Decoration that does not support a task
- Several accent colors competing for attention
- Custom controls where standard ones work

**Tendencies:**

| Property | Range |
|---|---|
| Type scale ratio | 1.125 to 1.2 |
| Radius | Small to medium, uniform |
| Borders | Thin, used for structure |
| Shadows | Only for overlays |
| Accent share of surface | Very low |
| Whitespace | Moderate, consistent |

**Fits well with:** Tool, Service, Utility. Object, Workflow, Command.

**Risks:** Becomes anonymous if chosen by default rather than on purpose. Can drift into the generic default if containers and accents multiply.

---

## Editorial

**Definition:** A language that borrows from print and publishing, where typography and layout carry meaning and containers are rare.

**Feels like:** Considered, confident, authored.

**Hierarchy is carried by:** Typographic scale and contrast, then whitespace.

**Typography:**
- Strong contrast between display and text sizes
- Often a pairing of two families with different character, such as a serif with a sans-serif
- Careful attention to line length, rhythm and reading comfort
- Type can be the main visual element on a page

**Space and composition:**
- Generous whitespace used actively, not as leftover
- Asymmetric layouts, multi-column grids, deliberate breaks from the grid
- Layout varies between pages to express content

**Shape:** Little or no radius. Lines and rules used sparingly, as typographic elements.

**Surface and depth:** Few containers. Content sits on the page, not in boxes. Flat, with little or no elevation.

**Color:** Restrained, often near-monochrome. Color used as emphasis or as a signature, not as structure.

**Imagery and icons:** Photography and illustration used large and with intent, often full width or cropped deliberately. Icons are minimal and subordinate to type.

**Principles:**
- Prefer typography over containers.
- Use whitespace before dividers.
- Let layout change with content; not every page shares the same template.
- One clear typographic lead on every view.

**Avoid:**
- Cards as the default way to group content
- Many small elements at equal weight
- Centered layouts everywhere
- Icons carrying meaning that words should carry

**Tendencies:**

| Property | Range |
|---|---|
| Type scale ratio | 1.333 to 1.618 |
| Radius | None to very small |
| Borders | Rare, as typographic rules |
| Shadows | None |
| Accent share of surface | Low |
| Whitespace | High, used for rhythm |

**Fits well with:** Content, Commerce, Service (public information). Document, Narrative.

**Risks:** Hard to apply to dense, interactive tools without losing clarity. Requires real content to work; placeholder text hides problems.

---

## Precision

**Definition:** A technical language built on a tight grid, small type and minimal decoration, optimized for clarity at high information density.

**Feels like:** Exact, efficient, engineered.

**Hierarchy is carried by:** Alignment, weight and grid structure.

**Typography:**
- Compact sizes, small scale contrast
- Neutral sans-serif, often with a monospace for data, codes and values
- Tabular numerals for anything that is compared

**Space and composition:**
- Tight, systematic grid
- Strict alignment; edges and baselines line up
- Space is small but precise

**Shape:** Low radius, or none. Thin lines for structure: grids, tables, dividers.

**Surface and depth:** Containers are structural (panels, tables, toolbars), not decorative. Very little elevation.

**Color:** Mostly neutral. Color is functional: status, selection, data encoding. High contrast for text.

**Imagery and icons:** Small, precise, consistent icons. Imagery rare unless it is data.

**Principles:**
- Every element aligns to the grid.
- Color means something, or it is not used.
- Show values precisely; round only when it helps.
- Structure is visible, decoration is not.

**Avoid:**
- Large radius and soft shadows
- Decorative illustration
- Wasted space in data-heavy views
- Several font sizes where weight would do

**Tendencies:**

| Property | Range |
|---|---|
| Type scale ratio | 1.067 to 1.2 |
| Radius | None to small |
| Borders | Frequent, thin, structural |
| Shadows | None or minimal |
| Accent share of surface | Low, functional |
| Whitespace | Low, precise |

**Fits well with:** Tool, Data. Object, Dashboard, Command, Canvas.

**Risks:** Can feel cold or intimidating for new or infrequent users. Needs careful contrast work at small sizes.

---

## Warm

**Definition:** An approachable language with softer forms, warmer color and generous space, designed to feel human and reassuring.

**Feels like:** Friendly, safe, personal.

**Hierarchy is carried by:** Space, color and imagery.

**Typography:**
- Readable, open letterforms; often rounded or humanist
- Moderate scale contrast
- Comfortable sizes and line heights

**Space and composition:**
- Generous spacing
- Simple, balanced layouts
- Content grouped clearly into digestible parts

**Shape:** Medium to large radius. Soft forms. Few hard lines.

**Surface and depth:** Containers are common and soft, often with tinted backgrounds rather than borders. Gentle elevation.

**Color:** Warmer neutrals, tinted backgrounds, a broader palette than neutral languages. Color used to create mood and group content.

**Imagery and icons:** Photography of people and real situations, or illustration with a human touch. Icons friendly and slightly rounded.

**Principles:**
- Every screen should feel calm, even when the task is stressful.
- Group content into small, clear parts.
- Use real people and real situations in imagery.
- Speak plainly, visually and in words.

**Avoid:**
- Cold, high-contrast technical styling
- Dense layouts with many competing parts
- Illustration so generic it could belong to any product
- Softness that makes interactive elements hard to recognize

**Tendencies:**

| Property | Range |
|---|---|
| Type scale ratio | 1.2 to 1.25 |
| Radius | Medium to large |
| Borders | Rare, replaced by tinted surfaces |
| Shadows | Soft, low |
| Accent share of surface | Medium |
| Whitespace | High |

**Fits well with:** Service, Community, Commerce. Workflow, Conversation, Feed.

**Risks:** Easily becomes the generic default if containers multiply. Can feel childish if softness and color are pushed too far.

---

## Refined

**Definition:** A restrained language of few elements, subtle contrast and extreme whitespace, where quality is shown through what is left out.

**Feels like:** Quiet, precise, premium.

**Also known as:** Luxury, minimal.

**Hierarchy is carried by:** Space and restraint. One thing at a time.

**Typography:**
- Few sizes, carefully chosen
- Often light weights, wide tracking for small labels, or a distinctive display face
- Typography treated as the main material

**Space and composition:**
- Extreme whitespace
- Few elements per view
- Precise, often centered or strictly aligned compositions

**Shape:** No radius, or a very consistent small radius. Hairline rules if any.

**Surface and depth:** Almost no containers. Flat or very subtle layering.

**Color:** Very limited palette, often near-monochrome. Subtle contrast between surfaces. Accent used rarely, if ever.

**Imagery and icons:** High-quality photography, often large and still. Icons almost absent; text labels preferred.

**Principles:**
- Remove until removing more would hurt.
- One focal point per view.
- Every detail must be finished; nothing is approximate.
- Interaction effects are subtle and restrained.

**Avoid:**
- Badges, banners and promotional clutter
- Many actions competing on one view
- Loud color or heavy shadows
- Low-quality or inconsistent imagery

**Tendencies:**

| Property | Range |
|---|---|
| Type scale ratio | 1.25 to 1.5, few steps used |
| Radius | None or very small |
| Borders | Hairlines, rare |
| Shadows | None |
| Accent share of surface | Very low |
| Whitespace | Very high |

**Fits well with:** Commerce, Content. Narrative, Object (catalogs).

**Risks:** Low contrast and small type can fail accessibility. Hard to scale to complex tools. Emptiness can read as unfinished when content is weak.

---

## Playful

**Definition:** An expressive language of bold color, large shapes, characterful type and surprise.

**Feels like:** Joyful, energetic, surprising.

**Hierarchy is carried by:** Color, shape and scale.

**Typography:**
- Characterful display faces
- Large scale contrast
- Type can be rotated, stacked, colored or animated

**Space and composition:**
- Dynamic layouts, overlapping elements, unexpected placement
- Rhythm varies to create energy
- Clear structure underneath the play

**Shape:** Large or mixed radius, custom shapes, blobs, pills, stickers. Thick outlines are common.

**Surface and depth:** Colored surfaces and shaped containers. Depth through overlap and offset rather than realistic shadow.

**Color:** Broad, saturated palette. Color used for structure, mood and identity.

**Imagery and icons:** Illustration, characters, stickers, custom icons. Photography often cut out or combined with graphic elements.

**Principles:**
- Surprise in the details, clarity in the structure.
- Every playful element must still support the task.
- Use a small set of signature moves consistently, rather than many one-off effects.

**Avoid:**
- Play that obstructs core tasks
- Random decoration without a system
- Saturated color on text in ways that fail contrast
- Using the same playful treatment on every element, so nothing stands out

**Tendencies:**

| Property | Range |
|---|---|
| Type scale ratio | 1.333 to 1.75 |
| Radius | Large or mixed |
| Borders | Thick outlines common |
| Shadows | Hard offset shadows, or none |
| Accent share of surface | High |
| Whitespace | Medium |

**Fits well with:** Community, Utility, Content, AI-native (consumer). Feed, Conversation, Canvas.

**Risks:** Tiring in daily-use tools. Can undermine trust in serious contexts. Needs strong structure to avoid chaos.

---

## Graphic

**Definition:** A disciplined, bold language rooted in graphic design, with strong grids, color fields and large typography.

**Feels like:** Bold, clear, structured.

**Hierarchy is carried by:** Color fields, scale and a strong grid.

**Typography:**
- Large, confident display type, often a strong grotesque
- High scale contrast
- Type set in blocks that align tightly with the grid

**Space and composition:**
- Strong, visible grid
- Large color fields that divide the page
- Tension between large and small elements

**Shape:** No radius or a consistent geometric shape language. Hard edges.

**Surface and depth:** Surfaces are flat color blocks. No elevation; depth comes from overlap and contrast.

**Color:** A small, strong palette used in large areas. High contrast between fields.

**Imagery and icons:** Imagery cropped to the grid, often duotone or treated. Pictograms rather than decorative icons.

**Principles:**
- The grid is visible and respected.
- Color is used in fields, not in small decorations.
- Scale contrast creates drama; keep supporting elements small.
- Every page is a composition.

**Avoid:**
- Soft shadows and gradients
- Medium radius on everything
- Many small colored details
- Weak, uniform type sizes

**Tendencies:**

| Property | Range |
|---|---|
| Type scale ratio | 1.5 to 2.0 |
| Radius | None |
| Borders | Rare; color fields separate instead |
| Shadows | None |
| Accent share of surface | High, in large fields |
| Whitespace | Medium, structured by grid |

**Fits well with:** Content, Commerce, Community. Narrative, Feed, Object.

**Risks:** Large color fields can overwhelm dense content. Needs strict discipline to avoid becoming poster design applied where it does not fit.

---

## Brutalist

**Definition:** A raw, experimental language that exposes structure, embraces friction and rejects polish.

**Feels like:** Raw, direct, unconventional.

**Hierarchy is carried by:** Raw structure and typography.

**Typography:**
- System fonts, monospace, or aggressive display faces
- Extreme scale contrast or deliberately none
- Type can collide, overflow or break the grid

**Space and composition:**
- Unconventional grids, or visible default layout
- Deliberate misalignment or density
- Structure shown rather than hidden

**Shape:** No radius. Thick borders, visible boxes, default controls.

**Surface and depth:** Exposed boxes and borders. No elevation.

**Color:** Often high contrast: black, white and one loud color. Sometimes raw defaults such as pure primaries.

**Imagery and icons:** Unprocessed images, screenshots, raw media. Icons rare; text labels and symbols preferred.

**Principles:**
- Show how it is built.
- Friction is allowed when it creates meaning or attention, never when it blocks a task.
- Consistency is in the attitude, not in polish.

**Avoid:**
- Polish, softness and decorative gradients
- Hiding structure behind containers
- Friction in critical flows such as payment, forms or error recovery
- Rawness as an excuse for broken accessibility

**Tendencies:**

| Property | Range |
|---|---|
| Type scale ratio | Extreme or flat |
| Radius | None |
| Borders | Thick, visible |
| Shadows | None, or hard |
| Accent share of surface | Varies; often one loud color |
| Whitespace | Low or irregular |

**Fits well with:** Content, Community, Immersive. Feed, Narrative, Document.

**Risks:** Easily becomes unusable. Poorly suited to high-stakes tasks. Requires strong intent to avoid looking unfinished.

---

## Cinematic

**Definition:** An atmospheric language led by imagery, scale, depth and motion, where the interface feels like a film or a place.

**Feels like:** Immersive, dramatic, atmospheric.

**Hierarchy is carried by:** Imagery, scale and depth.

**Typography:**
- Large display type layered over imagery
- Few sizes; text kept short
- Legibility protected by contrast, overlays or placement

**Space and composition:**
- Full bleed; the whole view is the frame
- Strong focal points, often one per view
- Composition changes with scroll or time

**Shape:** Minimal visible shape language; the image defines the space.

**Surface and depth:** Layers, parallax, overlays, translucency. Depth is part of the expression.

**Color:** Driven by imagery. Often dark surfaces to let images glow. Color grading unifies the experience.

**Imagery and icons:** Image-led: large photography, video, 3D or generative visuals. Icons minimal.

**Principles:**
- Every view has one image or moment that leads.
- Text is short and placed where it can be read.
- Atmosphere must never hide the way forward.
- Performance is part of the art direction.

**Avoid:**
- Dense UI layered over imagery
- Text over busy image areas without protection
- Effects that depend on high-end devices with no fallback
- Atmosphere applied to tasks that need speed

**Tendencies:**

| Property | Range |
|---|---|
| Type scale ratio | 1.5 to 2.0 or more |
| Radius | Minimal |
| Borders | None |
| Shadows | Atmospheric, as light and depth |
| Accent share of surface | Driven by imagery |
| Whitespace | Replaced by image space |

**Fits well with:** Immersive, Content, Commerce (brand). Narrative, Manipulation.

**Risks:** Heavy assets and effects harm performance. Low contrast over imagery. Poor fit for repeated, task-driven use.

---

## Pairings

Typical fits. Unusual pairings can be the source of an original product, but they should be deliberate and tested.

**By product type:**

| Product type | Common languages |
|---|---|
| Tool | Neutral, Precision, Editorial |
| Content | Editorial, Graphic, Refined, Cinematic |
| Commerce | Editorial, Refined, Warm, Graphic |
| Service | Neutral, Warm, Editorial |
| Community | Warm, Playful, Graphic |
| Data | Precision, Neutral |
| AI-native | Neutral, Editorial, Warm, Playful |
| Utility | Neutral, Precision, Playful |
| Immersive | Cinematic, Brutalist, Playful |

**By experience model:**

| Experience model | Common languages |
|---|---|
| Object | Neutral, Precision, Editorial |
| Workflow | Neutral, Warm |
| Document | Editorial, Neutral, Refined |
| Canvas | Precision, Neutral, Playful |
| Manipulation | Precision, Cinematic |
| Command | Precision, Neutral |
| Conversation | Neutral, Warm, Editorial |
| Feed | Graphic, Playful, Warm, Editorial |
| Dashboard | Precision, Neutral |
| Narrative | Cinematic, Editorial, Graphic, Brutalist |
| Ambient | Neutral, Refined |

---

## Combining languages

- **One language dominates.** It sets the rules for hierarchy, shape and surface.
- **A secondary language needs a scope.** For example: marketing surfaces versus the signed-in product, or content pages versus tools.
- **Shared foundations bridge the two.** Keep the same typefaces, grid and spacing base across both, and let the secondary language change hierarchy, composition and expression.
- **Never mix on one surface without a rule.** If Editorial and Precision meet on the same view, state which one decides typography and which one decides structure.

Written as a line in a project definition:

```text
Visual: Editorial (dominant) + Precision (signed-in product)
```

---

## Contributing

- Keep every language in the schema above.
- Describe principles and roles, never specific typefaces or color values. Those belong to the brand layer.
- Every language needs an avoid list. It is the most useful part when working with AI.
- Add a new language only when a direction cannot be described as an existing language with different dial settings or a different brand.
- Tendencies are starting ranges, not rules. Change them when a project proves them wrong, and update this file when the same correction happens more than once.
