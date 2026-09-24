# Instructions for AI agents

This file tells AI agents how to use Design OS. It applies to any tool or model working in this repository or in a project started from it. If your tool expects a different file name for instructions, point it to this file.

---

## How a project starts

1. The user clones or copies this repository.
2. The user adds any brand material they have to the `brand/` folder. This can be anything: a logo, a screenshot of a palette, guidelines, font files, or nothing at all. Optionally, they add references to the `taste/` folder: a direction chosen with a client, their own references, screenshots, UI elements, or examples of what to avoid.
3. The user describes in written text what they want to build. The description may also contain links, such as a component library, an existing website or a design file.
4. **You** turn the description, the brand material and any references into a recipe, and write it to `recipe.md` at the project root.
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

The taste model in `archetypes/taste.md` is not a layer. It is the quality bar that applies to every project: principles of good design, signal and noise, anti-patterns and critique. It also describes how to read the references in `taste/`. It never changes structure or brand.

---

## Creating the recipe

### 1. Read the input

- The written project description
- Everything in `brand/`, and every link mentioned in the description
- Everything in `taste/`, if the folder has content
- An existing `recipe.md`, if the project already has one; update it rather than starting over

### 2. Choose each layer, in order

Work from structure to style: product type, experience model, visual language, motion language, dials, brand.

For each layer, read its "How to use this file" section and the sections listed under [Reading the layers](#reading-the-layers). Then:

- Pick the choice that fits the description best, following the layer's rules: one primary or dominant choice, and supporting choices only with a scope.
- Write down why, referring to what the description said.
- Note where the project differs from the archetype. That is usually where the interesting design work is.

### 3. Set the dials

Start from the preset for the chosen visual language. If there are project references, shift the starting positions toward the dial directions in their reading, within the language's natural range. Then move only the dials the description gives a reason to move. Push at least two dials clearly away from the middle, as the dials file requires.

### 4. Interpret the brand

Follow the four steps in `archetypes/brand.md`: inventory, extract, fill gaps, confirm. Mark every value that was read from an image, generated or filled in as a fallback. If the brand input includes a design system or an existing product, identify the closest visual language and dial values, and decide with the user whether to follow or evolve it.

### 5. Read the references

If `taste/` has content, analyze it with the method in `archetypes/taste.md`: read each reference, then the set, and summarize it as a reading. References yield to the description and the brand. Use the reading to choose languages where the description leaves them open, to shift dial starting positions, and to add confirmed absences to the avoid lists. Present the reading with the recipe so the user can correct it. Skip this step when there are no references.

### 6. Ask only what changes the choices

Do not ask the user to answer every kickoff question. Ask only when the answer would change a choice in the recipe, and ask all such questions at once. Everything else becomes an assumption, stated in the recipe.

### 7. Write the recipe

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
Taste:      <reference sources, or none>, applied to <choices, dials, avoid lists>
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

## Taste

<Omit this section when there are no project references.>

- **Sources:** <references, links and notes used>
- **Reading:** <five to ten statements, each with the references it rests on and a confidence level>
- **Applied:** <choices, dial shifts and added avoid rules, and what they came from>
- **Yielded:** <where the references gave way to the description or the brand>

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
| Motion language | What this layer owns, Non-negotiables, The generic default, Vocabulary, Timing grows in the product | Role and character, Principles, Avoid, Reduced motion, the column in the Moments table |
| Dials | From direction to values, Anchoring the dials | The descriptions and guardrails for every dial the recipe sets, and the presets table |
| Brand | The whole file | Not applicable |
| Taste | Principles of good design, Signal and noise, Anti-patterns, Critique | Analyzing references and References in a project, when `taste/` has content |

For secondary or supporting choices, read the same sections and apply them only within their stated scope.

---

## Rules

### Respect layer ownership

Each layer owns specific decisions, listed in its "What this layer owns" section. Never let one layer make a decision that belongs to another.

- Product type and experience model decide structure and behavior. Brand never changes them.
- Visual language decides the character of form. Dials decide the amount. Brand decides the specific assets.
- The taste model judges how well the layers are carried out. Project references fill only what the description and the brand leave open. Neither changes structure, behavior or brand assets.
- The experience model states what motion must communicate. The motion language decides how.

### Decide values in order

Dials are an internal direction, not a measurement. They never calculate a value. For every concrete value, such as a radius, a text size, a spacing step or a duration:

1. Start from the character of the visual or motion language.
2. Lean in the direction the dial describes.
3. Fill in specific assets from the interpreted brand.
4. Clamp to the accessibility floor.

Then look at the result in the product. If it does not read as the intended direction, change the value. Anchor dial positions in references or in an earlier version, as described in `archetypes/density-and-personality.md`. When a dial is outside the language's natural range, apply it and note the tension.

### Treat avoid lists as constraints

The avoid lists and anti-patterns in each chosen archetype are hard constraints, not suggestions. Check work against them before delivering it.

### Apply the taste model

The principles, the signal and noise tests and the anti-patterns in `archetypes/taste.md` apply to every project. Anti-patterns are judgments rather than bans: one is allowed only when the recipe states why it is used. Where a chosen visual language deliberately does something the taste model warns against, the language wins inside its own character.

### Check against the generic default

`visual-languages.md` and `motion-languages.md` each describe a generic default look and motion. If your output shows it, and the recipe did not ask for it, revise the output before delivering.

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
7. Critique the result as described in `archetypes/taste.md`, and revise before delivering.
8. Run the self-check below.

When generating tokens, structure them in three levels: primitives from the brand, semantic roles from the visual language and dials, and component values from all layers combined. Report every value clamped by the accessibility floor.

When the user changes direction during the project, update `recipe.md` and add a line to the decision log.

---

## Reviewing work

When asked to review work, run the critique in `archetypes/taste.md`. It starts with recipe fit: report findings by layer, and for each layer state what matches, what deviates, and whether each deviation looks deliberate or accidental. Then judge the result against the principles, the signal and noise tests, the anti-patterns and the non-negotiables, and lead with the single most important problem.

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
- [ ] Values follow the language character and the dial directions, and read as intended in the product
- [ ] Nothing in the chosen avoid lists appears in the output
- [ ] The output does not drift toward the generic default
- [ ] All non-negotiables are met
- [ ] Required states are handled, not only the ideal state
- [ ] Brand fallbacks and generated values are marked
- [ ] The result passes the signal and noise tests, and every anti-pattern present has a stated reason
- [ ] The result has at least one decision that makes it specific
- [ ] Project references were used only where the description and the brand left room, and every use is recorded
- [ ] Assumptions and tensions are listed
