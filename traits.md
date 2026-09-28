# Traits

The vocabulary for how a product leans. Traits are qualities described in words, never numbers: how compact the product is, how strong its contrast, how soft its forms, how much it moves. The visual language sets the character; traits say which way this product leans within it, and how far.

Traits are changed by prompting, relative to the current version: "more compact", "a bit softer", "calmer". This file is how those words are read.

---

## The nine traits

| Trait | Leans between | Shows in | Guardrails |
|---|---|---|---|
| **Density** | Spacious, few items ↔ compact, many items | Spacing, text size, line height, control height, items per view | Touch targets and legible text at any density; reading views can stay spacious |
| **Contrast** | Subtle, close tones ↔ strong, clear separation | Tonal distance between surfaces, secondary text, borders, weight and scale contrast | Text never below the contrast requirement; subtle applies to surfaces, not text |
| **Softness** | Sharp, hard edges ↔ soft, round forms | Radius, stroke weight, shadow blur, shape of icons | Inner radius equals outer radius minus padding; soft shapes still read as controls |
| **Depth** | Flat, one plane ↔ layered, elevated | Elevation levels, shadows, overlays, translucency | Elevated things still have visible edges; translucency respects reduced transparency |
| **Color** | Monochrome ↔ saturated, many hues | Chroma, share of colored surface, number of hues | Status colors stay distinct; color never carries meaning alone |
| **Warmth** | Cool ↔ warm | Undertone of neutrals and surfaces, grading of imagery | Independent of color: a monochrome product can be warm |
| **Expressivity** | Uniform, templated ↔ composed, dramatic | Display scale, layout variation between views, size of imagery, signatures | Composition goes to key views first; navigation stays predictable |
| **Motion** | Minimal ↔ rich | Which moments move, how noticeable, how far | The motion language sets the character; reduced motion overrides; repeated actions stay near instant |
| **Novelty** | Conventional ↔ unconventional | Custom versus standard components, navigation, layout, interaction | Sign-in, payment, forms, errors and settings stay conventional |

---

## Writing traits

**How far** is said with three words, the same way everywhere:

| Word | Means | In a prompt |
|---|---|---|
| Slightly | Noticed when looked for | "a touch", "a bit" |
| Clearly | Part of the product's character | "more", "less" |
| Fully | As far as it goes, within accessibility | "much", "all the way" |

A trait with no lean is **balanced**.

```text
Traits:     compact (clearly), monochrome (fully), sharp (fully), minimal motion
```

- **Write only the traits that give the product its character.** The rest follow the visual language as usual.
- **At least two clear leans.** A product balanced on everything lands on the generic default.
- **Lean relative to this product.** "Compact" in a trading terminal and in a public service are different amounts.
- **Anchor the leans that matter** in a reference or an earlier version: "compact, as in this reference".
- **Scope a lean** when surfaces differ: `compact (product), spacious (marketing)`. More than two or three scopes usually means two visual languages.

---

## Words

Briefs and prompts rarely name traits. They say playful, premium or modern tech. Read them like this, and record what a word means for each project.

| Word | Reads as | Not the same as |
|---|---|---|
| Playful | Saturated, soft, composed, richer motion | Childish: everything soft and saturated at once, no hierarchy |
| Premium, quiet | Spacious, little color, controlled contrast, a high finish | Empty: space without content strong enough to hold it |
| Premium, dramatic | Layered, composed, dramatic imagery; often Cinematic | Glossy: effects standing in for a point of view |
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

When a word has several readings, like premium, name them and ask. Words such as editorial or industrial describe a character, and belong to the visual languages.

**Anchoring a word in images.** Collect references for a word in `project/input/words/<word>/`, with examples of what it does not mean beside them, and read them with the method in `taste.md`. The reading replaces the row for that project. When the same correction keeps coming back, update the row.

---

## What each visual language usually leans toward

A genome only writes the traits that differ from this, or that define the product.

| Visual language | Usual traits | Stops being itself when it leans |
|---|---|---|
| Neutral | Balanced density and contrast, slightly soft, mostly flat, little color, uniform, fully conventional | |
| Editorial | Slightly spacious, strong contrast, sharp, flat, little color, clearly composed | Soft, or layered |
| Precision | Clearly compact, strong contrast, sharp, flat, little color, slightly cool, uniform | Spacious, or soft |
| Warm | Clearly spacious, slightly subtle contrast, clearly soft, some color, clearly warm | Sharp, or strongly contrasted |
| Refined | Fully spacious, subtle contrast, sharp, flat, monochrome | Compact, or colorful |
| Playful | Strong contrast, clearly soft, fully saturated, fully composed, rich motion | Monochrome, or uniform |
| Graphic | Fully strong contrast, fully sharp, fully flat, clearly saturated, clearly composed | Subtle, or layered |
| Brutalist | Fully strong contrast, fully sharp, flat, clearly composed, fully unconventional | Soft, or conventional |
| Cinematic | Clearly spacious, fully layered, fully composed, rich motion | Compact, or flat |

Leaning past where a language stops being itself is allowed when the references or the idea ask for it. Write the tension in the genome.

---

## From traits to values

Traits never calculate a value. When a spacing step, a radius or a text size is needed, start from the character of the visual language, lean the way the traits say, apply the look's rules and the brand's assets, and clamp to accessibility. Then look at the result: if it does not read as the intended lean, change the value, not the trait.
