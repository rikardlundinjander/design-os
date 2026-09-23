---
layer: dials
version: 0.1
status: draft
---

# Density and personality

Layer 5 of the archetype system. This layer is a set of **dials** rather than a list of archetypes. Each dial runs from 0 to 100 and adjusts one quality of the product: how much fits on screen, how soft the forms are, how strong the contrast is, how much it moves.

Dials replace vague direction such as "make it modern" or "a bit more premium" with values that people and AI can act on and compare.

---

## How it relates to other layers

The archetype layers set **character**. Dials set **amount**.

| Layer | Role | Example |
|---|---|---|
| Visual language | Sets the character and the allowed range | Precision: radius from none to small |
| Motion language | Sets the motion character and its range | Quiet: state changes 120 to 200 ms |
| **Dials** | **Pick a position within those ranges** | **Softness 30 places radius near the low end** |
| Brand | Supplies specific values and assets | The typeface, the accent color |

Editorial at density 80 becomes a newspaper. Editorial at density 20 becomes a magazine. The language is the same; the dial changed.

---

## How to use this file

1. **Start from the preset** for the chosen visual language (see [Presets](#presets)).
2. **Move the dials that matter** for this product. Most projects adjust three or four dials and leave the rest at the preset.
3. **Push at least two dials away from the middle.** A product with every dial near 50 lands on the generic default. Character comes from clear positions: at least two dials at 25 or below, or 75 or above.
4. **Resolve values** using the mapping in each dial, within the range set by the visual and motion language.
5. **Apply the accessibility floor** last. It always wins.

Written as a line in a project definition:

```text
Dials: density 70, contrast 65, softness 20, depth 10, color 30, warmth 40, expressivity 30, motion 25, novelty 20
```

---

## What this layer owns

| This layer decides | This layer does not decide |
|---|---|
| How much of each quality, from 0 to 100 | The character of the form (visual language) |
| Where a value sits within a language's range | The character of motion (motion language) |
| Scoped overrides per surface | Which views exist (product type) |
| | Specific colors, typefaces and assets (brand) |

---

## Resolution order

Every token value is resolved in the same order:

1. **Language range:** the visual or motion language sets a minimum and maximum.
2. **Dial position:** the dial picks a point within that range.
3. **Brand:** supplies specific values where the dial leaves a choice, such as which hue is the accent.
4. **Accessibility floor:** clamps anything that would break contrast, legibility, target size or reduced motion.

As a formula, for any mapped property:

```text
value = language_min + (language_max - language_min) × (dial / 100)
```

Round the result to the project's spacing grid or type scale.

**When a dial goes outside its language's natural range:** allow it, but record it as a deliberate tension. Refined at density 85 is possible and can be interesting, but it is no longer typical Refined. Write down why.

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

Each dial below follows the same structure: what it controls, what it looks like at 0, 50 and 100, how it maps to values, and its guardrails.

---

## Density

**Controls:** How much information and how many elements fit in a view.

**Maps to:** Spacing scale, text size for body and UI, line height, control height, items per view.

| Position | Description |
|---|---|
| 0 | Very spacious. Few elements per view. Large text and generous touch areas. |
| 50 | Balanced. Comfortable for most tasks. |
| 100 | Very compact. Many items in view, small text, tight spacing. For expert, frequent use. |

**Reference mapping** (in px, on a 4 px grid; use as a starting point):

| Property | 0 | 25 | 50 | 75 | 100 |
|---|---|---|---|---|---|
| Base spacing step | 12 | 10 | 8 | 6 | 4 |
| Body text | 18 | 17 | 16 | 15 | 14 |
| UI text (labels, controls) | 16 | 15 | 14 | 13 | 12 |
| Line height, body | 1.65 | 1.55 | 1.5 | 1.45 | 1.35 |
| Control height | 56 | 48 | 40 | 36 | 32 |

**Guardrails:**
- Touch targets stay at or above the platform minimum at any density.
- Body text does not go below a legible size for the reading distance.
- High density is applied per surface; detail and reading views can stay lower.

---

## Contrast

**Controls:** How strongly elements are separated from each other.

**Maps to:** Tonal distance between surfaces, the lightness of secondary text, visibility of borders, weight contrast in typography, position within the language's type scale ratio.

| Position | Description |
|---|---|
| 0 | Subtle. Surfaces and text levels close in tone. Hierarchy is quiet. |
| 50 | Clear, but calm. |
| 100 | Strong. Sharp separation between surfaces, bold weight contrast, high tonal range. |

**Mapping:**
- Type scale ratio: picks a position within the visual language's range.
- Surface steps: from barely distinguishable tints at 0 to clearly separate tones at 100.
- Secondary text: moves from close to primary text at 0 toward clearly subdued at 100, never below the accessibility minimum.
- Weight contrast: from one or two close weights at 0 to light and heavy weights side by side at 100.

**Guardrails:**
- Text contrast never goes below the accessibility minimum, at any setting.
- Low contrast applies to surfaces and decoration, not to text or interactive boundaries.

---

## Softness

**Controls:** How rounded and soft the forms are.

**Maps to:** Corner radius, stroke weight, shadow blur, the shape of icons and indicators.

| Position | Description |
|---|---|
| 0 | Sharp. No radius, crisp lines. |
| 50 | Moderate rounding. |
| 100 | Very soft. Large radius, pill shapes, soft edges throughout. |

**Mapping:**
- Radius for controls, as a fraction of control height: 0 at softness 0, up to 0.5 (fully rounded) at softness 100, within the visual language's range.
- Radius for containers: scales with the same dial, larger containers get proportionally larger radius.
- Shadow blur, if depth allows shadows: sharper at low softness, more diffuse at high softness.

**Guardrails:**
- Nested elements keep a consistent relationship: inner radius equals outer radius minus the padding between them.
- High softness must not make interactive elements indistinguishable from decorative shapes.

---

## Depth

**Controls:** How layered the interface feels.

**Maps to:** Number of elevation levels, shadow strength, use of overlays and translucency, separation between layers.

| Position | Description |
|---|---|
| 0 | Flat. One plane. Separation through tone and lines only. |
| 50 | A few levels: base, raised, overlay. |
| 100 | Strongly layered. Several levels, pronounced shadows or translucency, visible stacking. |

**Mapping:**

| Property | 0 | 50 | 100 |
|---|---|---|---|
| Elevation levels | 1 (plus overlays) | 3 | 5 |
| Shadow use | None | Overlays and raised elements | Most containers |
| Translucency | None | Overlays only | Common |

**Guardrails:**
- Depth never replaces clear boundaries; elevated elements still need visible edges in high contrast settings.
- Translucency respects the user's reduced transparency preference.

---

## Color

**Controls:** How much color is used and how intense it is.

**Maps to:** Chroma of accent and surface colors, share of the surface that is colored, number of hues in use.

| Position | Description |
|---|---|
| 0 | Monochrome. Color only for status. |
| 50 | Neutral base with one or two accent hues. |
| 100 | Saturated, several hues, color used for structure and mood. |

**Mapping:**

| Property | 0 | 50 | 100 |
|---|---|---|---|
| Hues in use (excluding status) | 0 to 1 | 1 to 2 | 3 or more |
| Accent chroma | Low | Medium | High |
| Colored share of surface | Minimal | Small | Large |

**Guardrails:**
- Status colors (success, warning, error) stay distinguishable at every setting.
- Color never carries information alone.
- Saturated color on text is checked for contrast.

---

## Warmth

**Controls:** The temperature of the product: neutrals, tints and the tone of imagery.

**Maps to:** Hue shift of grays and surfaces, the undertone of backgrounds, tone and grading of imagery.

| Position | Description |
|---|---|
| 0 | Cool. Blue-leaning neutrals, crisp tones. |
| 50 | Neutral. True grays. |
| 100 | Warm. Yellow or red-leaning neutrals, softer tones. |

**Mapping:**
- Neutral scale: a small hue shift toward cool or warm, increasing with distance from 50.
- Surface tint: stays subtle; warmth changes temperature, not saturation. Saturation belongs to the color dial.
- Imagery: grading guidance for photography and illustration.

**Guardrails:**
- Warmth is independent of color. A monochrome product can be warm; a saturated product can be cool.
- Status colors keep their meaning regardless of warmth.

---

## Expressivity

**Controls:** How composed and dramatic each view is, versus uniform and templated.

**Maps to:** Scale contrast of display type, variation in layout between views, size and prominence of imagery, frequency of signature elements.

| Position | Description |
|---|---|
| 0 | Uniform. Every view follows the same template. Nothing draws special attention. |
| 50 | Mostly consistent, with emphasis on key views. |
| 100 | Each view is composed. Large type, dramatic imagery, layouts that change with content. |

**Mapping:**
- Display type size: toward the top of the visual language's scale at high expressivity.
- Layout variation: from one shared template at 0 to view-specific compositions at 100.
- Imagery: from supporting and contained at 0 to dominant and full-bleed at 100.
- Signature elements: from none at 0 to recurring and prominent at 100.

**Guardrails:**
- High expressivity applies to key views first; repeated task views stay consistent.
- Navigation and controls stay predictable at every setting.

---

## Motion

**Controls:** How much motion the product uses, within its motion language.

**Maps to:** Which moments are animated, duration within the language's range, distance of movement, use of stagger.

| Position | Description |
|---|---|
| 0 | Only essential motion. Durations at the low end of the language's range. |
| 50 | Motion on the moments the language normally animates. |
| 100 | Motion on all moments the language allows. Durations and distances toward the upper end. |

**Mapping:**
- Duration: position within the motion language's range for each moment.
- Distance: multiplied from small at 0 to the language's maximum at 100.
- Moments: at low settings, only feedback, state and continuity are animated. Attention, hierarchy and character are added as the dial rises.

**Guardrails:**
- The motion language sets the character. The dial cannot turn Quiet into Expressive; it only sets how much Quiet motion there is.
- Reduced motion preferences override the dial completely.
- Frequently repeated actions stay near the instant tier at any setting.

---

## Novelty

**Controls:** How far the product departs from conventional patterns.

**Maps to:** Use of standard versus custom components, navigation patterns, layout conventions, interaction patterns.

| Position | Description |
|---|---|
| 0 | Conventional. Platform and industry standards everywhere. |
| 50 | Standard foundations with a few distinctive patterns. |
| 100 | Unconventional. Custom patterns, unexpected layouts and interactions. |

**Mapping:**
- Components: standard at low novelty, custom at high novelty.
- Navigation: conventional placement at low novelty, custom structures at high novelty.
- Distinctive moments: from none, to a few, to many.

**Guardrails:**
- Critical flows stay conventional regardless of the dial: sign-in, payment, forms, error recovery and settings. Cap novelty at 30 for these.
- Every unconventional pattern must be learnable without instructions, or have a conventional fallback.

---

## Derived traits

Some useful words describe combinations of dials rather than a single quality. Use them to talk about direction, then translate into dial values.

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

Starting positions for each visual language. They describe the typical form of the language, not the only one.

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

A product can use different dial values on different surfaces, as long as the language stays the same.

- **Density** varies most often: collection views higher than detail views, the product higher than marketing pages.
- **Expressivity** is often higher on entry points and key moments than on repeated task views.
- **Novelty** is capped on critical flows (see the Novelty guardrails).

Written in a project definition:

```text
Dials: density 70 (product), 30 (marketing); expressivity 25 (product), 70 (marketing)
```

Keep overrides few. More than two or three scoped dials usually means the product needs two visual languages with scopes, not more overrides.

---

## Setting the dials

A few methods that work well, with or without AI:

- **Start from the preset,** then only move a dial when you can say why.
- **Compare pairs.** Generate or sketch the same view at two positions of one dial, such as density 40 and 70, and choose. Repeat for the three dials that matter most.
- **Translate words into values.** When a stakeholder says "more premium" or "friendlier", use the derived traits table to turn it into dial changes.
- **Avoid the middle.** If every dial sits between 40 and 60, the product will look like everything else. Pick at least two clear positions.
- **Record changes.** When a dial is changed during the project, note the old value, the new value and the reason. Over time, these notes show whether the presets need updating.

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
- Every dial needs a mapping and guardrails. A dial without a mapping is a mood word, not a dial.
- Update presets and reference mappings when projects show the same correction more than once.
- Keep values platform-agnostic: grid units, ratios and relative scales, not platform-specific APIs.
