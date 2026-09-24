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
| 5 | Density and personality | How much of each quality, from 0 to 100? | [density-and-personality.md](archetypes/density-and-personality.md) |
| 6 | Brand | Which typefaces, colors, imagery, voice and signatures? | [brand.md](archetypes/brand.md) |

Layers 1 to 4 are archetypes: a defined set of options to choose from. Layer 5 is a set of dials. Layer 6 is a template, filled in once per brand.

---

## Starting a project

Work through the layers in order. Structure comes before style.

1. **Product type.** Pick one primary type and up to two secondary types. Use the views, flows and required states as the first scope checklist.
2. **Experience model.** Pick one dominant model and scope any supporting models to specific views, flows or user groups.
3. **Visual language.** Pick one dominant language. Add a secondary language only with a clear scope.
4. **Motion language.** Pick one. Scope exceptions tightly.
5. **Dials.** Start from the preset for the chosen visual language. Move the three or four dials that matter, and push at least two clearly away from the middle.
6. **Brand.** Fill in a brand profile from the template, or define a minimum viable brand. Set brand presence per surface.
7. **Answer the kickoff questions** in each layer. The places where the project differs from the archetypes are usually where the interesting design work is.

The result is a **recipe**: a short definition that people and AI can build from.

```text
Product:    Service (primary) + Content
Experience: Workflow (dominant) + Object (case overview)
Visual:     Neutral
Motion:     Quiet
Dials:      density 30, contrast 75, softness 40, depth 15, color 25, warmth 55, expressivity 15, motion 20, novelty 5
Brand:      <brand-name>, presence present (product), quiet (forms and payment)
```

A recipe is a starting point, not a specification. It gives the project something concrete enough to react to, and open enough to become unique.

---

## How values are resolved

Every concrete value, such as a radius, a duration or a text size, is resolved in the same order:

1. **Language range.** The visual or motion language sets the allowed range.
2. **Dial position.** The dial picks a point within that range.
3. **Brand.** Supplies the specific assets where a choice remains.
4. **Accessibility floor.** Clamps anything that would break contrast, legibility, target size or reduced motion. It always wins.

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
├── README.md
└── archetypes/
    ├── product-types.md
    ├── experience-models.md
    ├── visual-languages.md
    ├── motion-languages.md
    ├── density-and-personality.md
    └── brand.md
```

Planned:

- `recipe-template.md`: a template for defining a project from the layers
- `AGENTS.md`: instructions for how AI tools should read and apply the repository
- `brands/`: brand profiles, one file per brand
- Implementation examples per archetype, such as tokens and reference views, once the text definitions are stable

---

## Using Design OS in a project

Clone or copy the repository as the starting point for a project. Keep the archetype files unchanged in the project, and add project-specific files beside them: the recipe, the brand profile and any project principles.

When working with AI, give it the recipe and point it to the relevant sections of each layer rather than the whole repository. The most useful parts to include are the principles, the avoid lists and the tendencies.

---

## Contributing

Design OS improves through use. When a project shows that an archetype, preset or mapping is wrong, update the file.

- **Keep the schema.** Every archetype within a layer uses the same sections, so they stay comparable.
- **Stay platform-agnostic.** Describe principles, structure and behavior, not frameworks, libraries or tools.
- **Add sparingly.** Add a new archetype only when a product cannot be described with the existing ones, their combinations or different dial settings.
- **Update on repetition.** When the same correction appears in more than one project, change the default.
- **Version the files.** Each file has a version and a status in its front matter. Raise the version when the meaning of a file changes.
