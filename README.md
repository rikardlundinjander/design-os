# Design OS

A shared starting point for designing digital products. Design OS describes products as combinations of a small number of independent layers, so that every project starts from considered decisions instead of a blank file or a template.

It is platform-agnostic and written for both people and AI. Every file describes principles, structure and behavior in plain language, so that designers, developers and AI tools can read the same definition and arrive at the same product.

---

## The idea

Most products are not unique in their structure. They are unique in how a few decisions are combined. Design OS separates those decisions into layers:

```text
Product type          what the product is
+ Experience model    how the user engages with it
+ Visual language     the character of the form
+ Motion language     how it moves
+ Dials               how much of each quality
+ Brand               the specific assets and voice
= Starting point
```

Each layer answers one question and stays out of the others. That separation is what makes the layers combinable: the same product type can take many experience models, the same visual language can carry many brands, and the same structure can be adjusted with dials instead of redesigned.

The goal is not a library of templates. Templates reproduce sameness. The goal is a set of reusable decisions that can be recombined differently every time, so that the system handles the predictable parts and the designer introduces the unexpected ones.

---

## The layers

| # | Layer | Answers | File |
|---|---|---|---|
| 1 | Product type | What is the product? Which objects, views, flows and states does it need? | [product-types.md](archetypes/product-types.md) |
| 2 | Experience model | Where does the user's attention live, and who drives? | [experience-models.md](archetypes/experience-models.md) |
| 3 | Visual language | What carries hierarchy, and what is the character of the form? | [visual-languages.md](archetypes/visual-languages.md) |
| 4 | Motion language | What is motion for, and how does it behave? | [motion-languages.md](archetypes/motion-languages.md) |
| 5 | Density and personality | Which direction for each quality, from 0 to 100? | [density-and-personality.md](archetypes/density-and-personality.md) |
| 6 | Brand | Which typefaces, colors, imagery, voice and signatures? | [brand.md](archetypes/brand.md) |

Layers 1 to 4 are archetypes: a defined set of options to choose from. Layer 5 is a set of dials. Layer 6 is interpreted from whatever brand material the project has.

**Taste**, described in [taste.md](archetypes/taste.md), is the quality bar of the system rather than a layer. It holds general principles of good design, the difference between signal and noise, anti-patterns and a method for critique, and it applies to every project. It also describes how to read references, so that a project can bring its own direction, such as one chosen with a client, without copying it.

---

## Starting a project

1. **Clone or copy this repository.**
2. **Add brand material, if you have any,** to the `brand/` folder. It can be anything: a logo, a screenshot of a color palette, brand guidelines, font files. Links, such as a component library or an existing website, can go in the description instead. No template to fill in.
3. **Add references, if you have any,** to the `taste/` folder: a direction chosen with a client, screenshots, UI elements, examples of what to avoid, and notes on what to take from them. Keep screenshots of other people's work out of public repositories.
4. **Describe in plain text what you want to build.** Who it is for, what it should do, what it should feel like, and any constraints.
5. **Let the AI write a recipe.** Following [`AGENTS.md`](AGENTS.md), it chooses from each layer, sets the dials, interprets the brand material, reads any references, and writes the result to `recipe.md`. It asks only questions whose answers would change a choice.
6. **Review and adjust the recipe.**
7. **Explore, if the direction is open.** The AI builds a few tracks from the recipe, following [exploration.md](process/exploration.md): the closest version, one that stretches it and one that challenges it, each with the same key views. You choose, and the recipe is updated.
8. **Build from the recipe.**

A recipe looks like this at its core, followed by the reasons for each choice, the interpreted brand, assumptions and open questions:

```text
Product:    Service (primary) + Content
Experience: Workflow (dominant) + Object (case overview)
Visual:     Neutral
Motion:     Quiet
Dials:      density 30, contrast 75, softness 40, depth 15, color 25, warmth 55, expressivity 15, motion 20, novelty 5
Brand:      logo and one color from brand/, presence present (product), quiet (forms and payment)
Taste:      none
```

A recipe is a starting point, not a specification. It gives the project something concrete enough to react to, and open enough to become unique.

---

## How values are decided

Dials are an internal direction, not a measurement. "Density 80" means clearly toward compact for this product, and it is anchored in references or an earlier version, not converted to a number. Every concrete value, such as a radius, a duration or a text size, is decided in the same order:

1. **Language character.** The visual or motion language says what kind of value fits.
2. **Dial direction.** The dial says which way to lean, and how far.
3. **Brand.** Supplies the specific assets where a choice remains.
4. **Accessibility floor.** Clamps anything that would break contrast, legibility, target size or reduced motion. It always wins.

Values are then judged in the product, where they can be seen.

---

## Principles

- **Layers are independent.** Each layer answers one question. If a rule in one layer describes something another layer owns, it is in the wrong place.
- **Structure before style.** Decide what the product is and how it is used before deciding how it looks.
- **One dominant choice per layer.** Supporting choices are allowed, but they need a scope.
- **Avoid lists matter most.** Each archetype names what breaks it. Those lists are what keep AI-generated work from drifting toward the generic default.
- **Accessibility is not a setting.** No archetype, dial or brand overrides the non-negotiables.
- **Deliberate tension is allowed.** Unusual combinations can produce original products. Record why, so the choice is visible.

---

## Repository structure

```text
design-os/
├── README.md                 this file
├── AGENTS.md                 instructions for AI agents
├── process/                  how work moves from recipe to product
│   └── exploration.md
├── archetypes/               the six layers and the taste model
│   ├── product-types.md
│   ├── experience-models.md
│   ├── visual-languages.md
│   ├── motion-languages.md
│   ├── density-and-personality.md
│   ├── brand.md
│   └── taste.md
├── brand/                    brand material for the project, in any form
└── taste/                    optional references for the project, in any form
```

Planned: implementation examples per archetype, such as tokens and reference views, once the text definitions are stable.

---

## Using Design OS in a project

Keep the archetype files unchanged in the project. Project-specific material lives beside them: brand material in `brand/`, references in `taste/`, and the recipe in `recipe.md` at the project root, written by the AI and adjusted by you.

Most AI tools read [`AGENTS.md`](AGENTS.md) automatically. It describes how to turn a written description into a recipe, which sections of each layer to read, how values are decided and how to check the work before delivering it.

---

## Contributing

Design OS improves through use. When a project shows that an archetype, preset or mapping is wrong, update the file.

- **Keep the schema.** Every archetype within a layer uses the same sections, so they stay comparable.
- **Stay platform-agnostic.** Describe principles, structure and behavior, not frameworks, libraries or tools.
- **Add sparingly.** Add a new archetype only when a product cannot be described with the existing ones, their combinations or different dial settings.
- **Update on repetition.** When the same correction appears in more than one project, change the default.
- **Version the files.** Each file has a version and a status in its front matter. Raise the version when the meaning of a file changes.
