# Instructions for AI agents

This file tells AI agents how to use Design OS. It applies to any tool or model working in this repository or in a project started from it. If your tool expects a different file name for instructions, point it to this file.

---

## How a project starts

1. The user clones or copies this repository.
2. The user adds any brand material they have to the `brand/` folder. This can be anything: a logo, a screenshot of a palette, guidelines, font files, or nothing at all.
3. The user describes in written text what they want to build. The description may also contain links, such as a component library, an existing website or a design file.
4. **You** turn the description and the brand material into a recipe, and write it to `recipe.md` at the project root.
5. The user reviews and adjusts the recipe. Only then do you build from it.

The user does not fill in templates. Your job is to interpret free-form input and make the choices explicit.

---

## What this repository contains

Design OS describes digital products as combinations of six independent layers:

| # | Layer | File | Kind |
|---|---|---|---|
| 1 | Product type | `archetypes/product-types.md` | Choose from archetypes |
| 2 | Experience model | `archetypes/experience-models.md` | Choose from archetypes |
| 3 | Visual language | `archetypes/visual-languages.md` | Choose from archetypes |
| 4 | Motion language | `archetypes/motion-languages.md` | Choose from archetypes |
| 5 | Density and personality | `archetypes/density-and-personality.md` | Set dials from 0 to 100 |
| 6 | Brand | `archetypes/brand.md` | Interpret brand input |

---

## Creating the recipe

### 1. Read the input

- The written project description
- Everything in `brand/`, and every link mentioned in the description
- An existing `recipe.md`, if the project already has one; update it rather than starting over

### 2. Choose each layer, in order

Work from structure to style: product type, experience model, visual language, motion language, dials, brand.

For each layer, read its "How to use this file" section and the sections listed under [Reading the layers](#reading-the-layers). Then:

- Pick the choice that fits the description best, following the layer's rules: one primary or dominant choice, and supporting choices only with a scope.
- Write down why, referring to what the description said.
- Note where the project differs from the archetype. That is usually where the interesting design work is.

### 3. Set the dials

Start from the preset for the chosen visual language. Move only the dials the description gives a reason to move. Push at least two dials clearly away from the middle, as the dials file requires.

### 4. Interpret the brand

Follow the four steps in `archetypes/brand.md`: inventory, extract, fill gaps, confirm. Mark every value that was read from an image, generated or filled in as a fallback. If the brand input includes a design system or an existing product, identify the closest visual language and dial values, and decide with the user whether to follow or evolve it.

### 5. Ask only what changes the choices

Do not ask the user to answer every kickoff question. Ask only when the answer would change a choice in the recipe, and ask all such questions at once. Everything else becomes an assumption, stated in the recipe.

### 6. Write the recipe

Write `recipe.md` using the format below, and present it to the user for review.

---

## Recipe format

````markdown
# <Project name>

## Recipe

```text
Product:    <primary> + <secondary>
Experience: <dominant> + <supporting> (<scope>)
Visual:     <dominant> + <secondary> (<scope>)
Motion:     <language> + <exception> (<scope>)
Dials:      density <n>, contrast <n>, softness <n>, depth <n>, color <n>, warmth <n>, expressivity <n>, motion <n>, novelty <n>
Brand:      <short summary of sources>, presence <level> (<surface>), <level> (<surface>)
```

## What we are building

<Your interpretation of the description in a few sentences: users, core job, what success looks like, constraints.>

## Choices

For each layer: the choice, the scope of any supporting choice, why, and how the project differs from the archetype.

## Dials

| Dial | Preset | Value | Scope | Why |
|---|---|---|---|---|

## Brand

- **Sources:** <files, links and statements used>
- **Extracted:** <asset: value, and source>
- **Filled in:** <asset: fallback value, and why>
- **Conflicts and resolutions:** <conflicts with the visual language, and how they are resolved>

## Project principles

<Three to seven rules specific to this project, written so they can be followed and checked.>

## Assumptions

<Everything decided without explicit input from the user.>

## Open questions

<Questions whose answers could change the recipe.>

## Decision log

| Date | Decision | Changed from | Reason |
|---|---|---|---|
````

Keep the recipe short. It is a starting point, not a specification.

---

## Reading the layers

Do not load every file in full for every task. For each layer, read the shared sections and the section for the chosen archetype:

| Layer | Always read | Read for the chosen archetype |
|---|---|---|
| Product type | What this layer owns | Key views, key flows, required states, structural needs, common failure modes |
| Experience model | What this layer owns | Navigation, selection and feedback, implications for other layers, anti-patterns |
| Visual language | What this layer owns, Non-negotiables, The generic default | Principles, Avoid, Tendencies |
| Motion language | What this layer owns, Non-negotiables, The generic default, Vocabulary | Principles, Avoid, Tendencies, Reduced motion, the column in the Moments table |
| Dials | Resolution order | The mapping and guardrails for every dial the recipe sets, and the presets table |
| Brand | The whole file | Not applicable |

For secondary or supporting choices, read the same sections and apply them only within their stated scope.

---

## Rules

### Respect layer ownership

Each layer owns specific decisions, listed in its "What this layer owns" section. Never let one layer make a decision that belongs to another.

- Product type and experience model decide structure and behavior. Brand never changes them.
- Visual language decides the character of form. Dials decide the amount. Brand decides the specific assets.
- The experience model states what motion must communicate. The motion language decides how.

### Resolve values in order

For every concrete value, such as a radius, a text size, a spacing step or a duration:

1. Take the range from the visual or motion language.
2. Place the value within the range using the dial: `value = min + (max - min) × (dial / 100)`.
3. Fill in specific assets from the interpreted brand.
4. Clamp to the accessibility floor.

Round to the project's grid and type scale. When a dial is outside the language's natural range, apply it and note the tension.

### Treat avoid lists as constraints

The avoid lists and anti-patterns in each chosen archetype are hard constraints, not suggestions. Check work against them before delivering it.

### Check against the generic default

`visual-languages.md` and `motion-languages.md` each describe a generic default look and motion. If your output shows several signs of it, and the recipe did not ask for it, revise the output before delivering.

### Never break the non-negotiables

The non-negotiables in the visual and motion layers override every archetype, dial and brand rule. This includes contrast, visible focus, not relying on color alone, legible text sizes, touch target sizes and reduced motion. If the recipe or the brand input would break one, follow the non-negotiable and tell the user.

### Keep scopes

One dominant choice per layer governs everything unless a scope says otherwise. Apply secondary choices only within their scope, and never mix two choices on the same surface without a stated rule.

### Do not invent archetypes

Use only archetypes, dials and presets that exist in the repository. If a project seems to need something that is missing, describe it as a combination of existing ones, or propose a change to the repository.

---

## Building from the recipe

1. Start from the product type: which objects, states and flows does this view need?
2. Apply the experience model: what is the center of gravity, how does navigation work, what must motion communicate?
3. Apply the visual language and dials: hierarchy, composition, shape, surface, color roles, density.
4. Apply the motion language to every state change.
5. Apply the brand at the presence level for the surface.
6. Design the required states, not only the ideal state.
7. Run the self-check below.

When generating tokens, structure them in three levels: primitives from the brand, semantic roles from the visual language and dials, and component values from all layers combined. Report every value clamped by the accessibility floor.

When the user changes direction during the project, update `recipe.md` and add a line to the decision log.

---

## Reviewing work

When asked to review work against the recipe, report findings by layer. For each layer, state what matches, what deviates, and whether each deviation looks deliberate or accidental. Check the avoid lists, the generic default and the non-negotiables explicitly.

---

## Updating this repository

Do not change the archetype files as a side effect of project work. When project work shows that an archetype, preset or mapping is wrong:

1. Describe the problem and the evidence.
2. Propose the specific change.
3. Make the change only when the user agrees, following the Contributing section of the affected file.
4. Raise the version in the file's front matter when the meaning changes.

---

## Self-check before delivering

- [ ] The work follows the recipe, or deviations are stated
- [ ] No layer made a decision owned by another layer
- [ ] Values were resolved in order and fit their language ranges
- [ ] Nothing in the chosen avoid lists appears in the output
- [ ] The output does not drift toward the generic default
- [ ] All non-negotiables are met
- [ ] Required states are handled, not only the ideal state
- [ ] Brand fallbacks and generated values are marked
- [ ] Assumptions and tensions are listed
