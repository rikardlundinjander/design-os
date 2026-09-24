---
layer: brand
version: 0.2
status: draft
---

# Brand

Layer 6 of the archetype system. The brand layer supplies **the specific assets and voice** of a product: typefaces, colors, logo, imagery, icons, tone, signature motion and other distinctive elements.

Unlike the other layers, brand is not a set of archetypes to choose from. Every brand is unique. This file therefore contains two things:

1. **The rules** for how brand connects to the other layers.
2. **A template** for capturing a brand as a brand profile.

Brand profiles are stored separately, one file per brand, in `brands/<brand-name>.md`, using the template in `templates/brand-profile.md`.

---

## How it relates to other layers

| Layer | Decides | Brand fills in |
|---|---|---|
| Product type | What the product is | Nothing. Structure is brand-independent. |
| Experience model | How the user engages | Nothing. Behavior is brand-independent. |
| Visual language | Character of form, roles of type and color | Which typefaces and hues play those roles |
| Motion language | Timing, easing, choreography | A signature curve and signature moments, within the language |
| Dials | How much of each quality | Which specific values, where the dial leaves a choice |

The principle: **the other layers decide how things are used. Brand decides what is used.**

Editorial says "a strong display face paired with a readable text face". Brand says which two typefaces. The color dial says "one to two accent hues, medium chroma". Brand says which hues.

The same product structure can therefore carry different brands and still behave consistently. And the same brand can be expressed through different visual languages on different surfaces.

---

## What this layer owns

| This layer decides | This layer does not decide |
|---|---|
| Typefaces and their availability | Type scale and hierarchy (visual language, dials) |
| Color values: brand hues, neutral base, accents | How much color is used (color dial) |
| Logo, marks and their rules | Navigation and structure (experience model) |
| Imagery style and subjects | Where imagery is used and how large (visual language, expressivity) |
| Icon set or icon style | Icon roles and density (visual language) |
| Tone of voice and vocabulary | Content structure (product type) |
| Signature motion: curve, moments, logo animation | Motion timing and amount (motion language, motion dial) |
| Sound and haptics | |
| Distinctive assets: patterns, shapes, textures | |
| Brand presence per surface | |

---

## Brand presence

Brand does not need to be equally loud everywhere. Set a presence level for each surface.

| Level | Description | Typical surfaces |
|---|---|---|
| **Signature** | Brand leads. Distinctive assets, signature motion, brand imagery and voice at full strength. | Marketing, campaigns, onboarding, key moments |
| **Present** | Brand is recognizable but supports the task. Typefaces, colors and voice are used; distinctive assets appear sparingly. | Most product surfaces |
| **Quiet** | Brand steps back. Typefaces and a single accent at most; neutral voice. | Dense tools, settings, error recovery, critical flows |

Written in a project definition:

```text
Brand: <brand-name>, presence signature (marketing), present (product), quiet (settings, payment)
```

Rules:
- Critical flows, such as payment, forms and error recovery, are never above **Present**.
- Presence changes how much brand shows, not which brand. Typefaces and core colors stay the same across levels.

---

## Fit with the visual language

Brand assets and the chosen visual language must fit. Check this early, before any detailed design.

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
2. **Adjust the dials.** Move the relevant dial toward the brand, for example softness up for a rounded typeface, within the language's natural range.
3. **Choose a different visual language** for the affected surface.
4. **Record the tension.** If the conflict is deliberate, write down why.

Never resolve a conflict by breaking a non-negotiable, such as contrast or legibility, because a brand color or typeface demands it.

---

## From brand to tokens

Brand fills in the lowest level of the token system: the raw values. The other layers decide how they are combined.

| Token level | Filled by | Example |
|---|---|---|
| Primitives (raw values) | **Brand** | Font families, the brand hue scale, the neutral scale, the icon set |
| Semantic (roles) | Visual language, dials | Text primary, surface raised, accent interactive, display type |
| Component | All layers combined | Button background, card radius, heading size |

**What brand must provide for tokens to resolve:**

- Font families for each role the visual language needs (display, text, UI, and mono where relevant), with the weights available
- A neutral scale, with its temperature (see the warmth dial)
- One or more brand hues, each as a full scale from light to dark, not a single swatch
- Status colors, or confirmation that neutral defaults may be used
- An icon set, or a description precise enough to choose one
- Optionally: a signature easing curve, a signature moment, sound and haptics

If a brand only provides single swatches, build scales from them and have them approved as part of the brand profile.

---

## Minimum viable brand

Early products and internal tools often have no brand yet. Do not wait for one. Define the smallest brand that lets the other layers resolve:

- **One typeface family** with enough weights for text and headings
- **One neutral scale** with a chosen temperature
- **One accent hue** as a scale
- **Three words** for tone of voice
- **A logotype** set in the chosen typeface, or no logo at all

Mark the profile as `status: provisional`. Replace it when a real brand exists; because structure and behavior live in other layers, the product survives the swap.

---

## Multiple brands

When the same product serves several brands (white label, sub-brands, a group of companies):

- **Fixed across brands:** product type, experience model, visual language (or a small set of allowed languages), motion language, accessibility floor.
- **Varies per brand:** everything in the brand profile.
- **Optionally varies:** selected dials, typically color, warmth and softness. Decide which dials a brand may change, and within what range.

Test every brand profile against the same set of reference views. If a brand breaks a view, fix the profile or add a scoped rule; do not fork the structure.

---

## Kickoff questions

- Which brand guidelines exist, and which parts are fixed versus open to interpretation?
- Were the guidelines made for digital products, or mainly for print and marketing?
- Which typefaces are licensed for digital and for all target platforms?
- Which brand colors meet contrast requirements, and in which combinations?
- Where should the brand be loudest, and where should it step back?
- What is the brand never allowed to look or sound like?
- Who approves brand decisions, and how fast?

---

## Brand profile template

The template for brand profiles is [`templates/brand-profile.md`](../templates/brand-profile.md). Copy it to `brands/<brand-name>.md` and fill it in. Leave a section empty rather than guessing; empty sections fall back to the visual language and dial defaults. See [`brands/README.md`](../brands/README.md) for naming and status.

---

## Contributing

- Keep structure and behavior out of brand profiles. If a rule describes navigation, layout or states, it belongs in another layer.
- Every brand hue is a scale, not a swatch.
- Record known tensions with the visual language in the profile, not in this file.
- Update the template when the same missing field appears in more than one brand profile.
