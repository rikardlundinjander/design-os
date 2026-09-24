---
layer: brand
version: 0.3
status: draft
---

# Brand

Layer 6 of the archetype system. The brand layer supplies **the specific assets and voice** of a product: typefaces, colors, logo, imagery, icons, tone, signature motion and other distinctive elements.

Brand is different from the other layers. It is not chosen from a list of archetypes, and it does not arrive in a fixed format. One project starts from a logo and a single color. Another starts from full brand guidelines, a design system in a component library and an existing website. This file describes how to **interpret whatever brand input exists** and connect it to the other layers.

---

## How it relates to other layers

| Layer | Decides | Brand fills in |
|---|---|---|
| Product type | What the product is | Nothing. Structure is brand-independent. |
| Experience model | How the user engages | Nothing. Behavior is brand-independent. |
| Visual language | Character of form, roles of type and color | Which typefaces and hues play those roles |
| Motion language | Timing, easing, choreography | A signature curve and signature moments, within the language |
| Dials | How much of each quality | Specific values, where the dial leaves a choice |

The principle: **the other layers decide how things are used. Brand decides what is used.**

Editorial says "a strong display face paired with a readable text face". Brand says which two typefaces. The color dial says "one to two accent hues, medium chroma". Brand says which hues.

---

## What brand input can be

Brand input can take any form, and often several at once. Common examples:

- A logo file, and nothing else
- A screenshot or image of a color palette
- Brand guidelines as a document or presentation
- A link to a component library, design system documentation or a design file
- An existing website or app to match or evolve from
- Font files or font names
- A tokens file or style definitions from existing code
- Photography, illustrations or other example imagery
- A written description: "we want to feel calm and trustworthy, our color is dark green"

Place files in the `brand/` folder of the project, and mention links and descriptions in the written project description. Nothing needs to be renamed or structured first.

---

## Interpreting brand input

Work through the input in four steps.

1. **Inventory.** List every source: files, links and statements in the description.
2. **Extract.** For each asset in the table below, record what the input defines, and where it came from.
3. **Fill gaps.** Where the input defines nothing, use the fallback. Mark the value as a fallback, so it is visible and can be replaced.
4. **Confirm.** Present what was extracted and what was filled in, and let the user correct it before building.

**What to extract:**

| Asset | Look for | Fallback if missing |
|---|---|---|
| Logo | Logo files, marks in screenshots, the existing product | Logotype set in the chosen typeface, or no logo |
| Typefaces | Font files, names in guidelines, fonts used in the existing product or library | A neutral family that fits the visual language |
| Brand colors | Palettes, guidelines, the logo, the existing product, tokens | One accent derived from the logo; neutral scale from the warmth dial |
| Color scales | Tokens, component library, guidelines | Scales generated from the extracted colors |
| Status colors | Tokens, component library | Neutral defaults that meet contrast requirements |
| Imagery | Example images, guidelines, the existing product | Guided by the visual language; placeholders marked as such |
| Icons | Icon set in library or product | A set that fits the visual language and softness dial |
| Tone of voice | Guidelines, existing copy, the project description | Plain, clear language matching the dials |
| Signature motion | Motion guidelines, the existing product | None; the motion language alone |
| Distinctive assets | Patterns, shapes, graphic devices in any source | None |

**When sources disagree,** for example guidelines and the live product use different colors, prefer the more recent and more authoritative source, and list the disagreement as an open question.

**When extracting from images,** such as a screenshot of a palette, state that values were read from an image and may need exact confirmation.

---

## When brand input includes a design system

A component library or design system carries more than brand. It often already contains decisions that belong to other layers: a type scale, spacing, radius, component behavior and motion.

- **Treat it as a constraint, not as brand only.** Identify which visual language and dial values it corresponds to most closely, and record that in the recipe.
- **Decide whether to follow or evolve it.** Following means the existing system wins where it conflicts with the archetypes. Evolving means the archetypes guide changes. The project description usually says which; if not, ask.
- **Reuse before creating.** Use existing components and tokens where they fit, and only add what is missing.

---

## Brand presence

Brand does not need to be equally loud everywhere. Set a presence level for each surface.

| Level | Description | Typical surfaces |
|---|---|---|
| **Signature** | Brand leads. Distinctive assets, signature motion, brand imagery and voice at full strength. | Marketing, campaigns, onboarding, key moments |
| **Present** | Brand is recognizable but supports the task. Typefaces, colors and voice are used; distinctive assets appear sparingly. | Most product surfaces |
| **Quiet** | Brand steps back. Typefaces and a single accent at most; neutral voice. | Dense tools, settings, error recovery, critical flows |

Rules:
- Critical flows, such as payment, forms and error recovery, are never above **Present**.
- Presence changes how much brand shows, not which brand. Typefaces and core colors stay the same across levels.

---

## Fit with the visual language

Brand assets and the chosen visual language must fit. Check this as soon as the brand input is interpreted.

**Typical conflicts:**

| Visual language | Brand assets that conflict |
|---|---|
| Precision | Rounded or decorative typefaces, a wide saturated palette |
| Refined | Many brand colors, loud patterns, playful illustration |
| Editorial | A single typeface with little range, brand rules that require boxes or badges |
| Warm | A cold, technical palette, sharp geometric marks |
| Playful | A restrained, monochrome brand with strict usage rules |
| Graphic | Soft gradients, photography-only brand expression |
| Brutalist | Strict polish requirements, detailed usage rules |
| Cinematic | No imagery or a brand built only on flat color and type |

**Resolving a conflict,** in order of preference:

1. **Scope the brand asset.** Use the conflicting asset only where it fits, for example a decorative typeface for display only, with a neutral text face.
2. **Adjust the dials.** Move the relevant dial toward the brand, within the language's natural range.
3. **Choose a different visual language** for the affected surface.
4. **Record the tension.** If the conflict is deliberate, write down why.

Never resolve a conflict by breaking a non-negotiable, such as contrast or legibility, because a brand color or typeface demands it.

---

## From brand to tokens

Brand fills in the lowest level of the token system: the raw values. The other layers decide how they are combined.

| Token level | Filled by | Example |
|---|---|---|
| Primitives (raw values) | **Brand** | Font families, brand hue scales, the neutral scale, the icon set |
| Semantic (roles) | Visual language, dials | Text primary, surface raised, accent interactive, display type |
| Component | All layers combined | Button background, card radius, heading size |

Every brand color becomes a full scale, from light to dark, before it is used. If the input only provides single swatches, generate the scales and mark them as generated.

---

## Multiple brands

When the same product serves several brands, such as white label, sub-brands or a group of companies:

- **Fixed across brands:** product type, experience model, visual language, motion language, accessibility floor.
- **Varies per brand:** everything described in this file.
- **Optionally varies:** selected dials, typically color, warmth and softness, within agreed ranges.

Test every brand against the same set of reference views. If a brand breaks a view, adjust how its input is interpreted or add a scoped rule; do not fork the structure.

---

## Kickoff questions

- Which brand material exists, and which parts are fixed versus open to interpretation?
- Should an existing design system or product be followed, or evolved?
- Which typefaces are licensed for digital use on all target platforms?
- Which brand colors meet contrast requirements, and in which combinations?
- Where should the brand be loudest, and where should it step back?
- What must the brand never look or sound like?

---

## Contributing

- Keep structure and behavior out of this layer. If a rule describes navigation, layout or states, it belongs in another layer.
- Add to the extraction table when a new kind of brand input keeps appearing.
- Keep the fallbacks conservative. A fallback should be easy to replace, not a design decision in disguise.
