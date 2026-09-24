---
layer: dials
version: 0.2
status: draft
---

# Density and personality

Layer 5 of the archetype system. This layer is a set of **dials** rather than a list of archetypes. Each dial runs from 0 to 100 and describes the direction of one quality of the product: how much fits on screen, how soft the forms are, how strong the contrast is, how much it moves.

Dials replace vague direction such as "make it modern" or "a bit more premium" with positions that people and AI can discuss and compare.

**A dial is an internal direction, not a measurement.** "Density 80" means "clearly toward compact, for this product". It does not convert to a spacing value, and it means little until it is anchored in something visible: a reference, an earlier version or a comparison of two options. Values are decided in the product, where they can be seen and judged.

---

## How it relates to other layers

The archetype layers set **character**. Dials set **direction**.

| Layer | Role | Example |
|---|---|---|
| Visual language | Sets the character and its natural range | Precision: sharp forms, little or no radius |
| Motion language | Sets the role and character of motion | Quiet: motion that explains without being noticed |
| **Dials** | **Say which way the product leans within that character** | **Softness 30: toward the sharp end of what the language allows** |
| Brand | Supplies specific assets | The typeface, the accent color |

Editorial at density 80 becomes a newspaper. Editorial at density 20 becomes a magazine. The language is the same; the direction changed.

---

## How to use this file

1. **Start from the preset** for the chosen visual language (see [Presets](#presets)).
2. **Move the dials that matter** for this product. Most projects adjust three or four dials and leave the rest at the preset.
3. **Push at least two dials away from the middle.** A product with every dial near 50 lands on the generic default. Character comes from clear positions: at least two dials at 25 or below, or 75 or above.
4. **Anchor the positions** in something visible before building on them (see [Anchoring the dials](#anchoring-the-dials)).
5. **Decide values in the product,** guided by the language, the dial and the brand, and checked against the accessibility floor, which always wins.

Written as a line in a project definition:

```text
Dials: density 70, contrast 65, softness 20, depth 10, color 30, warmth 40, expressivity 30, motion 25, novelty 20
```

---

## What this layer owns

| This layer decides | This layer does not decide |
|---|---|
| The direction of each quality, from 0 to 100 | The character of the form (visual language) |
| Which way the product leans within a language | The role and character of motion (motion language) |
| Scoped overrides per surface | Which views exist (product type) |
| | Specific colors, typefaces and assets (brand) |

---

## From direction to values

Dials do not calculate values. When a concrete value is needed, such as a spacing step, a radius or a text size, decide it in this order:

1. **Language character.** The visual or motion language says what kind of value fits. Refined wants few sizes and extreme whitespace; Precision wants a tight grid and small type.
2. **Dial direction.** The dial says which way to lean within that character, and how far.
3. **Brand.** Supplies specific assets where a choice remains, such as which hue is the accent.
4. **Accessibility floor.** Clamps anything that would break contrast, legibility, target size or reduced motion. It always wins.

Then look at the result. If it does not read as the intended direction, change the value, not the dial. The dial records intent; the product shows whether the intent was met.

**When a dial goes outside its language's natural range:** allow it, but record it as a deliberate tension. Refined at density 85 is possible and can be interesting, but it is no longer typical Refined. Write down why.

---

## Anchoring the dials

A position on a dial is only shared understanding when people and AI can point at what it looks like.

- **Anchor in references.** Tie the positions that matter to references that show them: "density 80 means as compact as this reference".
- **Anchor in the product.** Once a version exists, it becomes the anchor. Later positions are read relative to it.
- **Compare pairs.** Build or sketch the same view in two directions, such as density 40 and 70, and choose. The chosen view becomes the anchor for that dial.
- **Compare within the project, not across projects.** Density 70 in a trading terminal and density 70 in a public service are different amounts. The number is an internal direction for this product.

During iteration, dials are used relatively: "more density" or "less contrast" means a move from the current version, not a jump to a new absolute position.

---

## The dials

Nine core dials, chosen to be independent of each other and of the language layers.

| Dial | 0 | 100 |
|---|---|---|
| [Density](#density) | Spacious, few items | Compact, many items |
| [Contrast](#contrast) | Subtle, close tones | Strong, clear separation |
| [Softness](#softness) | Sharp, hard edges | Round, soft forms |
| [Depth](#depth) | Flat, one plane | Layered, elevated |
| [Color](#color) | Monochrome | Saturated, many hues |
| [Warmth](#warmth) | Cool | Warm |
| [Expressivity](#expressivity) | Uniform, templated | Composed, dramatic |
| [Motion](#motion) | Minimal | Rich |
| [Novelty](#novelty) | Conventional patterns | Unconventional patterns |

Each dial below follows the same structure: what it controls, where it shows, what it looks like at 0, 50 and 100, which way things move as it rises, and its guardrails.

---

## Density

**Controls:** How much information and how many elements fit in a view.

**Shows in:** Spacing, text size for body and UI, line height, control height, items per view.

| Position | Description |
|---|---|
| 0 | Very spacious. Few elements per view. Large text and generous touch areas. |
| 50 | Balanced. Comfortable for most tasks. |
| 100 | Very compact. Many items in view, small text, tight spacing. For expert, frequent use. |

**As it rises:**
- Spacing tightens and the steps between spacing values get smaller.
- Body and UI text get smaller, and line height gets tighter.
- Controls get shorter, and more items fit in each view.

**Guardrails:**
- Touch targets stay at or above the platform minimum at any density.
- Body text does not go below a legible size for the reading distance.
- High density is applied per surface; detail and reading views can stay lower.

---

## Contrast

**Controls:** How strongly elements are separated from each other.

**Shows in:** Tonal distance between surfaces, the lightness of secondary text, visibility of borders, weight contrast in typography, scale contrast in the type scale.

| Position | Description |
|---|---|
| 0 | Subtle. Surfaces and text levels close in tone. Hierarchy is quiet. |
| 50 | Clear, but calm. |
| 100 | Strong. Sharp separation between surfaces, bold weight contrast, high tonal range. |

**As it rises:**
- The type scale moves toward the steep end of the visual language's range.
- Surfaces move from barely distinguishable tints to clearly separate tones.
- Secondary text moves from close to the primary text toward clearly subdued, never below the accessibility minimum.
- Weights move from one or two close weights toward light and heavy side by side.

**Guardrails:**
- Text contrast never goes below the accessibility minimum, at any setting.
- Low contrast applies to surfaces and decoration, not to text or interactive boundaries.

---

## Softness

**Controls:** How rounded and soft the forms are.

**Shows in:** Corner radius, stroke weight, shadow blur, the shape of icons and indicators.

| Position | Description |
|---|---|
| 0 | Sharp. No radius, crisp lines. |
| 50 | Moderate rounding. |
| 100 | Very soft. Large radius, pill shapes, soft edges throughout. |

**As it rises:**
- Controls move from square corners toward fully rounded, within the visual language's range.
- Containers round with the same dial; larger containers get proportionally larger radius.
- Shadows, if depth allows them, move from sharp toward diffuse.

**Guardrails:**
- Nested elements keep a consistent relationship: inner radius equals outer radius minus the padding between them.
- High softness must not make interactive elements indistinguishable from decorative shapes.

---

## Depth

**Controls:** How layered the interface feels.

**Shows in:** Number of elevation levels, shadow strength, use of overlays and translucency, separation between layers.

| Position | Description |
|---|---|
| 0 | Flat. One plane. Separation through tone and lines only. Overlays are the only exception. |
| 50 | A few levels: base, raised, overlay. Shadows on raised elements and overlays. |
| 100 | Strongly layered. Several levels, pronounced shadows or translucency, visible stacking. |

**As it rises:**
- More elevation levels are distinguished.
- Shadows spread from overlays to raised elements to most containers.
- Translucency moves from absent, to overlays only, to common.

**Guardrails:**
- Depth never replaces clear boundaries; elevated elements still need visible edges in high contrast settings.
- Translucency respects the user's reduced transparency preference.

---

## Color

**Controls:** How much color is used and how intense it is.

**Shows in:** Chroma of accent and surface colors, share of the surface that is colored, number of hues in use.

| Position | Description |
|---|---|
| 0 | Monochrome. Color only for status. |
| 50 | Neutral base with one or two accent hues. |
| 100 | Saturated, several hues, color used for structure and mood. |

**As it rises:**
- More hues come into use, beyond status colors.
- Accent chroma moves from low to high.
- The colored share of the surface grows from minimal to large.

**Guardrails:**
- Status colors (success, warning, error) stay distinguishable at every setting.
- Color never carries information alone.
- Saturated color on text is checked for contrast.

---

## Warmth

**Controls:** The temperature of the product: neutrals, tints and the tone of imagery.

**Shows in:** Hue shift of grays and surfaces, the undertone of backgrounds, tone and grading of imagery.

| Position | Description |
|---|---|
| 0 | Cool. Blue-leaning neutrals, crisp tones. |
| 50 | Neutral. True grays. |
| 100 | Warm. Yellow or red-leaning neutrals, softer tones. |

**As it moves from the middle:**
- Neutrals shift slightly toward cool or warm, more the further the dial is from 50.
- Surface tints stay subtle; warmth changes temperature, not saturation. Saturation belongs to the color dial.
- Imagery is graded toward the same temperature.

**Guardrails:**
- Warmth is independent of color. A monochrome product can be warm; a saturated product can be cool.
- Status colors keep their meaning regardless of warmth.

---

## Expressivity

**Controls:** How composed and dramatic each view is, versus uniform and templated.

**Shows in:** Scale contrast of display type, variation in layout between views, size and prominence of imagery, frequency of signature elements.

| Position | Description |
|---|---|
| 0 | Uniform. Every view follows the same template. Nothing draws special attention. |
| 50 | Mostly consistent, with emphasis on key views. |
| 100 | Each view is composed. Large type, dramatic imagery, layouts that change with content. |

**As it rises:**
- Display type moves toward the top of the visual language's scale.
- Layouts move from one shared template toward view-specific compositions.
- Imagery moves from supporting and contained toward dominant and full-bleed.
- Signature elements move from none toward recurring and prominent.

**Guardrails:**
- High expressivity applies to key views first; repeated task views stay consistent.
- Navigation and controls stay predictable at every setting.

---

## Motion

**Controls:** How much motion the product uses, within its motion language.

**Shows in:** Which moments move, how noticeable the movement is, how far things travel.

| Position | Description |
|---|---|
| 0 | Only essential motion: feedback and the state changes that would be confusing without it. |
| 50 | Motion on the moments the language normally uses. |
| 100 | Motion on every moment the language allows, and more noticeable where it appears. |

**As it rises:**
- Moments are added in order: feedback, state and continuity first, then attention, hierarchy and character.
- Movement becomes more noticeable and travels further, within the character of the motion language.

**Guardrails:**
- The motion language sets the role and character. The dial cannot turn Quiet into Expressive; it only sets how much Quiet motion there is.
- Reduced motion preferences override the dial completely.
- Frequently repeated actions stay close to instant at any setting.

---

## Novelty

**Controls:** How far the product departs from conventional patterns.

**Shows in:** Use of standard versus custom components, navigation patterns, layout conventions, interaction patterns.

| Position | Description |
|---|---|
| 0 | Conventional. Platform and industry standards everywhere. |
| 50 | Standard foundations with a few distinctive patterns. |
| 100 | Unconventional. Custom patterns, unexpected layouts and interactions. |

**As it rises:**
- Components move from standard to custom.
- Navigation moves from conventional placement to custom structures.
- Distinctive moments move from none, to a few, to many.

**Guardrails:**
- Critical flows stay conventional regardless of the dial: sign-in, payment, forms, error recovery and settings. Keep novelty low on these surfaces.
- Every unconventional pattern must be learnable without instructions, or have a conventional fallback.

---

## Derived traits

Some useful words describe combinations of dials rather than a single quality. Use them to talk about direction, then translate into dial positions.

| Trait | Expressed as |
|---|---|
| Playful | High color, high softness, high expressivity, raised motion |
| Precise | High density, low softness, high contrast, low depth |
| Minimal | Low density, low color, low depth, low expressivity |
| Restrained | Low expressivity, low motion, low color |
| Physical | Raised depth, a Physical motion language, raised motion |
| Premium | Low density, low color, controlled contrast, high finish (a quality, not a dial) |
| Friendly | High softness, raised warmth, medium color |
| Technical | High density, low warmth, low softness, low expressivity |
| Bold | High contrast, high expressivity, high color or high scale contrast |

Qualities such as editorial or industrial are not dials. They are visual languages, and belong in that layer.

---

## Presets

Starting directions for each visual language. They describe the typical form of the language, not the only one.

| Visual language | Density | Contrast | Softness | Depth | Color | Warmth | Expressivity | Motion | Novelty |
|---|---|---|---|---|---|---|---|---|---|
| Neutral | 50 | 50 | 35 | 25 | 25 | 50 | 20 | 30 | 10 |
| Editorial | 35 | 70 | 5 | 5 | 20 | 50 | 65 | 25 | 40 |
| Precision | 80 | 70 | 10 | 10 | 20 | 35 | 15 | 25 | 15 |
| Warm | 35 | 45 | 70 | 35 | 50 | 75 | 40 | 45 | 25 |
| Refined | 15 | 35 | 5 | 5 | 10 | 55 | 45 | 25 | 30 |
| Playful | 40 | 65 | 80 | 30 | 85 | 60 | 85 | 75 | 60 |
| Graphic | 45 | 90 | 0 | 0 | 75 | 50 | 80 | 50 | 55 |
| Brutalist | 60 | 90 | 0 | 0 | 40 | 45 | 70 | 15 | 90 |
| Cinematic | 20 | 60 | 10 | 85 | 50 | 50 | 90 | 80 | 50 |

**Natural ranges.** Moving a dial far from its preset is allowed, but some combinations stop being the same language. Treat these as signals to record a deliberate tension:

| Visual language | Typical range limits |
|---|---|
| Refined | Density above 50, color above 40 |
| Precision | Density below 50, softness above 40 |
| Editorial | Softness above 40, depth above 40 |
| Warm | Softness below 30, contrast above 80 |
| Playful | Color below 40, expressivity below 40 |
| Graphic | Contrast below 60, depth above 30 |
| Brutalist | Softness above 20, novelty below 40 |
| Cinematic | Density above 60, depth below 40 |

---

## Scoped overrides

A product can use different dial positions on different surfaces, as long as the language stays the same.

- **Density** varies most often: collection views more compact than detail views, the product more compact than marketing pages.
- **Expressivity** is often higher on entry points and key moments than on repeated task views.
- **Novelty** stays low on critical flows (see the Novelty guardrails).

Written in a project definition:

```text
Dials: density 70 (product), 30 (marketing); expressivity 25 (product), 70 (marketing)
```

Keep overrides few. More than two or three scoped dials usually means the product needs two visual languages with scopes, not more overrides.

---

## Setting the dials

A few methods that work well, with or without AI:

- **Start from the preset,** then only move a dial when you can say why.
- **Compare pairs.** Generate or sketch the same view in two directions of one dial, such as density 40 and 70, and choose. Repeat for the three dials that matter most.
- **Translate words into directions.** When a stakeholder says "more premium" or "friendlier", use the derived traits table to turn it into dial changes.
- **Avoid the middle.** If every dial sits between 40 and 60, the product will look like everything else. Pick at least two clear positions.
- **Record changes.** When a dial is changed during the project, note the old position, the new position and the reason. Over time, these notes show whether the presets need updating.

---

## Examples

Generic examples to show how dials describe very different products.

**A trading or monitoring terminal**

```text
Visual: Precision
Motion: Responsive
Dials: density 90, contrast 80, softness 5, depth 5, color 30, warmth 25, expressivity 10, motion 15, novelty 15
```

**A public self-service for citizens**

```text
Visual: Neutral
Motion: Quiet
Dials: density 30, contrast 75, softness 40, depth 15, color 25, warmth 55, expressivity 15, motion 20, novelty 5
```

**A learning app for young children**

```text
Visual: Playful
Motion: Expressive
Dials: density 15, contrast 70, softness 90, depth 35, color 90, warmth 70, expressivity 85, motion 80, novelty 55
```

---

## Contributing

- Add a new dial only when it is independent of the existing dials and of the language layers. If it can be expressed as a combination, add it to the derived traits table instead.
- Every dial needs clear descriptions of 0, 50 and 100, a direction of change, and guardrails. A dial without them is a mood word, not a dial.
- Do not add value tables. Dials describe direction; values are decided in the product.
- Update presets when projects show the same correction more than once.
- Keep descriptions platform-agnostic.
