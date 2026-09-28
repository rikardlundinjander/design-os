---
layer: traits
version: 0.3
status: draft
---

# Traits

Layer 5 of the genome. Traits are **the qualities of the product, described in words**: how compact it is, how strong its contrast is, how soft its forms are, how much it moves. Each trait runs between two poles, such as spacious and compact, and the genome says which way the product leans and how far.

Traits are not set with numbers. They are **adjusted by prompting**: "more compact", "a bit softer", "calmer", "more premium". The words in this file are how a prompt is turned into a change, and how the change is explained back before it is made.

---

## How it relates to other layers

The archetype layers set **character**. Traits say **which way the product leans** within it.

| Layer | Role | Example |
|---|---|---|
| Visual language | Sets the character, and the traits it usually has | Precision: compact, sharp, strong contrast |
| Motion language | Sets the role and character of motion | Quiet: motion that explains without being noticed |
| **Traits** | **Say where this product leans, and how far** | **Sharper than Precision usually is, and fully monochrome** |
| Direction | Turns the idea into concrete rules | Close crops of real play |
| Brand | Supplies specific assets | The typeface, the accent color |

Editorial that leans compact becomes a newspaper. Editorial that leans spacious becomes a magazine. The language is the same; the traits changed.

---

## What this layer owns

| This layer decides | This layer does not decide |
|---|---|
| Which way each quality leans, and how far | The character of the form (visual language) |
| How a prompt about a quality is interpreted | The role and character of motion (motion language) |
| Scoped traits per surface | Which views exist (product type) |
| | Specific colors, typefaces and assets (brand) |

---

## The traits

Nine traits, chosen to be independent of each other and of the language layers.

| Trait | One pole | Other pole |
|---|---|---|
| [Density](#density) | Spacious, few items | Compact, many items |
| [Contrast](#contrast) | Subtle, close tones | Strong, clear separation |
| [Softness](#softness) | Sharp, hard edges | Soft, round forms |
| [Depth](#depth) | Flat, one plane | Layered, elevated |
| [Color](#color) | Monochrome | Saturated, many hues |
| [Warmth](#warmth) | Cool | Warm |
| [Expressivity](#expressivity) | Uniform, templated | Composed, dramatic |
| [Motion](#motion) | Minimal | Rich |
| [Novelty](#novelty) | Conventional patterns | Unconventional patterns |

**How far** is said with three words, used the same way everywhere:

| Word | Means |
|---|---|
| Slightly | A lean that is noticed when looked for |
| Clearly | A lean that is part of the product's character |
| Fully | As far as the trait goes, within the non-negotiables |

A trait with no lean is **balanced**.

---

## Writing traits in the genome

The genome lists the traits that give the product its character. Traits that follow the visual language as usual can be left out.

```text
Traits:     compact (clearly), monochrome (fully), sharp (fully), minimal motion
```

- **Say at least two clear leans.** A product that is balanced on every trait lands on the generic default. Character comes from at least two traits leaning clearly or fully.
- **Lean relative to the product, not to other products.** "Compact" in a trading terminal and "compact" in a public service are different amounts. The words describe this product.
- **Anchor the leans that matter** in something visible: a reference, an earlier version, or a comparison of two options. "Compact, as in this reference" is shared understanding; "compact" alone is not yet.

**Scoped traits.** A product can lean differently on different surfaces, as long as the language stays the same:

```text
Traits:     compact (product), spacious (marketing); composed (marketing only)
```

Keep scoped traits few. More than two or three usually means the product needs two visual languages with scopes.

---

## Tuning by prompt

Traits change when someone asks for a change in words. Every change is relative to the current version.

1. **Read the prompt.** Find the traits it names, and translate other words through the [words table](#words). "More premium" is not a trait; it is a combination of them.
2. **Show the interpretation before changing anything.** Say which traits move, in which direction, how far, and what stays the same:
   *"More premium, read as: less compact (clearly), less color, more space around headings. Typefaces, layout and imagery stay."*
3. **Make the change,** starting from the current version, and keep everything that was not named.
4. **Record it.** Add the prompt, the interpretation and the result to the decision log.

**How far a prompt goes:**

| The prompt says | Move |
|---|---|
| A touch, a bit, slightly | Slightly |
| More, less, without a qualifier | Clearly |
| Much, a lot, all the way | Fully, or as far as the language and the non-negotiables allow |

**When a word has several readings,** such as premium, name them and ask which is meant, or choose one and say so. Record the reading, so the word means the same thing for the rest of the project.

**When a prompt meets a limit,** say so instead of silently stopping. "Less contrast" cannot take text below the contrast requirement; "more novelty" cannot reach the sign-in flow.

---

## Density

**Controls:** How much information and how many elements fit in a view.

**Shows in:** Spacing, text size for body and UI, line height, control height, items per view.

| Lean | Description |
|---|---|
| Spacious | Few elements per view. Large text and generous touch areas. |
| Balanced | Comfortable for most tasks. |
| Compact | Many items in view, small text, tight spacing. For expert, frequent use. |

**Toward compact:**
- Spacing tightens and the steps between spacing values get smaller.
- Body and UI text get smaller, and line height gets tighter.
- Controls get shorter, and more items fit in each view.

**Guardrails:**
- Touch targets stay at or above the platform minimum however compact the product is.
- Body text does not go below a legible size for the reading distance.
- Compactness is applied per surface; detail and reading views can stay more spacious.

---

## Contrast

**Controls:** How strongly elements are separated from each other.

**Shows in:** Tonal distance between surfaces, the lightness of secondary text, visibility of borders, weight contrast in typography, scale contrast in the type scale.

| Lean | Description |
|---|---|
| Subtle | Surfaces and text levels close in tone. Hierarchy is quiet. |
| Balanced | Clear, but calm. |
| Strong | Sharp separation between surfaces, bold weight contrast, high tonal range. |

**Toward strong:**
- The type scale moves toward the steep end of the visual language's range.
- Surfaces move from barely distinguishable tints to clearly separate tones.
- Secondary text moves from close to the primary text toward clearly subdued, never below the accessibility minimum.
- Weights move from one or two close weights toward light and heavy side by side.

**Guardrails:**
- Text contrast never goes below the accessibility minimum, however subtle the product is.
- Subtle contrast applies to surfaces and decoration, not to text or interactive boundaries.

---

## Softness

**Controls:** How rounded and soft the forms are.

**Shows in:** Corner radius, stroke weight, shadow blur, the shape of icons and indicators.

| Lean | Description |
|---|---|
| Sharp | No radius, crisp lines. |
| Balanced | Moderate rounding. |
| Soft | Large radius, pill shapes, soft edges throughout. |

**Toward soft:**
- Controls move from square corners toward fully rounded, within the visual language's range.
- Containers round with them; larger containers get proportionally larger radius.
- Shadows, if the product has depth, move from sharp toward diffuse.

**Guardrails:**
- Nested elements keep a consistent relationship: inner radius equals outer radius minus the padding between them.
- Softness must not make interactive elements indistinguishable from decorative shapes.

---

## Depth

**Controls:** How layered the interface feels.

**Shows in:** Number of elevation levels, shadow strength, use of overlays and translucency, separation between layers.

| Lean | Description |
|---|---|
| Flat | One plane. Separation through tone and lines only. Overlays are the only exception. |
| Balanced | A few levels: base, raised, overlay. Shadows on raised elements and overlays. |
| Layered | Several levels, pronounced shadows or translucency, visible stacking. |

**Toward layered:**
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

| Lean | Description |
|---|---|
| Monochrome | Color only for status. |
| Balanced | Neutral base with one or two accent hues. |
| Saturated | Several hues, color used for structure and mood. |

**Toward saturated:**
- More hues come into use, beyond status colors.
- Accent chroma moves from low to high.
- The colored share of the surface grows from minimal to large.

**Guardrails:**
- Status colors (success, warning, error) stay distinguishable however monochrome the product is.
- Color never carries information alone.
- Saturated color on text is checked for contrast.

---

## Warmth

**Controls:** The temperature of the product: neutrals, tints and the tone of imagery.

**Shows in:** Hue shift of grays and surfaces, the undertone of backgrounds, tone and grading of imagery.

| Lean | Description |
|---|---|
| Cool | Blue-leaning neutrals, crisp tones. |
| Neutral | True grays. |
| Warm | Yellow or red-leaning neutrals, softer tones. |

**Away from neutral:**
- Neutrals shift slightly toward cool or warm, more the further the lean goes.
- Surface tints stay subtle; warmth changes temperature, not saturation. Saturation belongs to the color trait.
- Imagery is graded toward the same temperature.

**Guardrails:**
- Warmth is independent of color. A monochrome product can be warm; a saturated product can be cool.
- Status colors keep their meaning regardless of warmth.

---

## Expressivity

**Controls:** How composed and dramatic each view is, versus uniform and templated.

**Shows in:** Scale contrast of display type, variation in layout between views, size and prominence of imagery, frequency of signature elements.

| Lean | Description |
|---|---|
| Uniform | Every view follows the same template. Nothing draws special attention. |
| Balanced | Mostly consistent, with emphasis on key views. |
| Composed | Each view is composed. Large type, dramatic imagery, layouts that change with content. |

**Toward composed:**
- Display type moves toward the top of the visual language's scale.
- Layouts move from one shared template toward view-specific compositions.
- Imagery moves from supporting and contained toward dominant and full-bleed.
- Signature elements move from none toward recurring and prominent.

**Guardrails:**
- Composition applies to key views first; repeated task views stay consistent.
- Navigation and controls stay predictable however composed the product is.

---

## Motion

**Controls:** How much motion the product uses, within its motion language.

**Shows in:** Which moments move, how noticeable the movement is, how far things travel.

| Lean | Description |
|---|---|
| Minimal | Only essential motion: feedback and the state changes that would be confusing without it. |
| Balanced | Motion on the moments the language normally uses. |
| Rich | Motion on every moment the language allows, and more noticeable where it appears. |

**Toward rich:**
- Moments are added in order: feedback, state and continuity first, then attention, hierarchy and character.
- Movement becomes more noticeable and travels further, within the character of the motion language.

**Guardrails:**
- The motion language sets the role and character. This trait cannot turn Quiet into Expressive; it only says how much Quiet motion there is.
- Reduced motion preferences override this trait completely.
- Frequently repeated actions stay close to instant however rich the motion is.

---

## Novelty

**Controls:** How far the product departs from conventional patterns.

**Shows in:** Use of standard versus custom components, navigation patterns, layout conventions, interaction patterns.

| Lean | Description |
|---|---|
| Conventional | Platform and industry standards everywhere. |
| Balanced | Standard foundations with a few distinctive patterns. |
| Unconventional | Custom patterns, unexpected layouts and interactions. |

**Toward unconventional:**
- Components move from standard to custom.
- Navigation moves from conventional placement to custom structures.
- Distinctive moments move from none, to a few, to many.

**Guardrails:**
- Critical flows stay conventional regardless of this trait: sign-in, payment, forms, error recovery and settings.
- Every unconventional pattern must be learnable without instructions, or have a conventional fallback.

---

## Words

Briefs, clients and prompts rarely name traits. They say playful, premium or modern tech. This table translates common words into traits, and names what each word is often confused with. It is a starting point; every project records what its words mean, and repeated corrections change the table.

| Word | Reads as | Not the same as |
|---|---|---|
| Playful | Saturated, soft, composed, richer motion | Childish: everything soft and saturated at once, with no hierarchy |
| Premium, quiet | Spacious, little color, controlled contrast, a high finish | Empty: space without content strong enough to hold it |
| Premium, dramatic | Layered, composed, dramatic imagery; often a Cinematic language | Glossy: effects standing in for a point of view |
| Luxury | Fully spacious, monochrome, very few elements | Black and gold, thin serif type everywhere |
| Minimal | Spacious, little color, flat, uniform | Unfinished: missing states and hierarchy |
| Clean | Flat, little color, few means used consistently | The generic default |
| Calm | Subtle contrast, little color, spacious, minimal motion | Dull: nothing leads |
| Bold | Strong contrast, composed, saturated or large in scale | Loud: everything at full volume |
| Friendly | Soft, slightly warm, some color | Childish |
| Human | Warm, slightly soft, imagery of real people and situations | Stock photos of smiling people |
| Precise | Compact, strong contrast, sharp, flat | Cold: precise with no point of view |
| Technical | Compact, cool, sharp, uniform | Monospace and grids as decoration |
| Modern tech | Sharp, strong contrast, little color or one vivid accent, flat | Purple and blue gradients, glow, glass, dark by default |
| Restrained | Uniform, minimal motion, little color | Timid: no decision stands out |
| Elegant | Spacious, subtle contrast, sharp, few type sizes | Fragile: text too light or small to read |
| Energetic | Strong contrast, composed, rich motion, saturated | Noisy: motion and color without hierarchy |
| Trustworthy | Conventional, strong contrast in text, restrained | Blue everything |
| Physical | Layered, a Physical motion language, richer motion | Skeuomorphic decoration |

Words such as editorial or industrial are not traits. They describe a character, and belong to the visual language.

**Growing the words.** A word means most when it is anchored in images. References for a word can be collected in `taste/words/<word>/`, with examples of what it does not mean beside them, and read with the method in `taste.md`. The reading replaces the row in this table for that project, and repeated readings update the table.

---

## Language character

What each visual language usually leans toward. A genome only lists traits that differ from this, or that define the product.

| Visual language | Usual traits |
|---|---|
| Neutral | Balanced density and contrast, slightly soft, mostly flat, little color, uniform, fully conventional |
| Editorial | Slightly spacious, strong contrast, sharp, flat, little color, clearly composed, slightly unconventional |
| Precision | Clearly compact, strong contrast, sharp, flat, little color, slightly cool, uniform, conventional |
| Warm | Clearly spacious, slightly subtle contrast, clearly soft, some depth, some color, clearly warm |
| Refined | Fully spacious, subtle contrast, sharp, flat, monochrome, slightly composed |
| Playful | Strong contrast, clearly soft, fully saturated, fully composed, rich motion, unconventional |
| Graphic | Fully strong contrast, fully sharp, fully flat, clearly saturated, clearly composed |
| Brutalist | Slightly compact, fully strong contrast, fully sharp, fully flat, clearly composed, fully unconventional, minimal motion |
| Cinematic | Clearly spacious, fully layered, fully composed, rich motion |

**Where a language stops being itself.** Leaning far from the usual traits is allowed, but some leans make the language into something else. Treat them as a deliberate tension and record why:

| Visual language | Becomes something else when it leans |
|---|---|
| Refined | Compact, or colorful |
| Precision | Spacious, or soft |
| Editorial | Soft, or layered |
| Warm | Sharp, or strongly contrasted |
| Playful | Monochrome, or uniform |
| Graphic | Subtle, or layered |
| Brutalist | Soft, or conventional |
| Cinematic | Compact, or flat |

---

## From traits to values

Traits do not calculate values. When a concrete value is needed, such as a spacing step, a radius or a text size, decide it in this order:

1. **Language character.** The visual or motion language says what kind of value fits.
2. **Traits.** They say which way to lean within that character, and how far.
3. **Direction.** The art direction may set the value directly, for a reason tied to the idea.
4. **Brand.** Supplies specific assets where a choice remains.
5. **Accessibility floor.** Clamps anything that would break contrast, legibility, target size or reduced motion. It always wins.

Then look at the result. If it does not read as the intended lean, change the value, not the trait. The trait records intent; the product shows whether the intent was met.

---

## Examples

Generic examples of how traits describe very different products.

**A trading or monitoring terminal**

```text
Visual:     Precision
Motion:     Responsive
Traits:     compact (fully), strong contrast (clearly), cool (clearly), minimal motion
```

**A public self-service for citizens**

```text
Visual:     Neutral
Motion:     Quiet
Traits:     spacious (clearly), strong contrast (clearly), conventional (fully)
```

**A learning app for young children**

```text
Visual:     Playful
Motion:     Expressive
Traits:     spacious (fully), soft (fully), saturated (fully), rich motion
```

---

## Contributing

- Add a new trait only when it is independent of the existing traits and of the language layers. If it can be expressed as a combination, add it to the words table instead.
- Every trait needs two poles, a description of each lean, the direction of change, and guardrails.
- Do not add numbers. Traits are words, and values are decided in the product.
- Add a word to the words table when it keeps appearing in briefs or prompts, and update a row when projects keep correcting it.
- Keep descriptions platform-agnostic.
