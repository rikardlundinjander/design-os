# Instructions for AI agents

This file tells AI agents how to read and apply Design OS. It applies to any tool or model working in this repository or in a project built from it. If your tool expects a different file name for instructions, point it to this file.

---

## What this repository is

Design OS describes digital products as combinations of six independent layers:

| # | Layer | File |
|---|---|---|
| 1 | Product type | `archetypes/product-types.md` |
| 2 | Experience model | `archetypes/experience-models.md` |
| 3 | Visual language | `archetypes/visual-languages.md` |
| 4 | Motion language | `archetypes/motion-languages.md` |
| 5 | Density and personality (dials) | `archetypes/density-and-personality.md` |
| 6 | Brand | `archetypes/brand.md` and `brands/<brand-name>.md` |

A project is defined by a **recipe**: one choice per layer, with scopes, dial values and a brand profile. The template is `templates/recipe.md`. Example recipes are in `examples/`.

---

## Before doing any design work

1. **Find the recipe.** Look for a recipe file in the project, usually `recipe.md` at the project root. If the user gives a recipe in the conversation, use that.
2. **If there is no recipe,** do not invent one silently. Either help the user create one (see [Creating a recipe](#creating-a-recipe)), or, if the task is small and the user wants you to proceed, choose reasonable values, state them explicitly at the top of your response, and mark them as assumptions.
3. **If a layer is missing from the recipe,** use the defaults described below and say which defaults you used.

**Defaults when a layer is missing:**

| Missing layer | Default |
|---|---|
| Experience model | The most common dominant model for the product type (see the pairing table in `experience-models.md`) |
| Visual language | Neutral |
| Motion language | Quiet |
| Dials | The preset for the visual language |
| Brand | A minimum viable brand, marked as provisional |

---

## Reading the layers

Do not load every file in full for every task. For each layer, read the section for the chosen archetype, and these shared sections:

| Layer | Always read | Read for the chosen archetype |
|---|---|---|
| Product type | What this layer owns | Key views, key flows, required states, structural needs, common failure modes |
| Experience model | What this layer owns | Navigation, selection and feedback, implications for other layers, anti-patterns |
| Visual language | What this layer owns, Non-negotiables, The generic default | Principles, Avoid, Tendencies |
| Motion language | What this layer owns, Non-negotiables, The generic default, Vocabulary | Principles, Avoid, Tendencies, Reduced motion, the column in the Moments table |
| Dials | Resolution order | The mapping and guardrails for every dial the recipe sets, and the presets table |
| Brand | Brand presence, Fit with the visual language, From brand to tokens | The full brand profile |

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
3. Fill in specific assets from the brand profile.
4. Clamp to the accessibility floor.

Round to the project's grid and type scale. When a dial is outside the language's natural range, apply it and note the tension.

### Treat avoid lists as constraints

The avoid lists and anti-patterns in each chosen archetype are hard constraints, not suggestions. Before delivering any visual or interaction work, check it against them.

### Check against the generic default

`visual-languages.md` and `motion-languages.md` each describe a generic default look and motion. If your output shows several signs of it, and the recipe did not ask for it, revise the output before delivering.

### Never break the non-negotiables

The non-negotiables in the visual and motion layers override every archetype, dial and brand rule. This includes contrast, visible focus, not relying on color alone, legible text sizes, touch target sizes and reduced motion. If a recipe or brand rule would break one, follow the non-negotiable and tell the user.

### Keep scopes

One dominant choice per layer governs everything unless a scope says otherwise. Apply secondary choices only within their scope, and never mix two choices on the same surface without a stated rule.

### Do not invent archetypes

Use only archetypes, dials and presets that exist in the repository. If a project seems to need something that is missing, describe it as a combination of existing ones, or propose a change to the repository (see [Updating the repository](#updating-the-repository)).

---

## Common tasks

### Creating a recipe

1. Read the brief or ask the user for it.
2. For each layer in order, from product type to brand, ask or infer the choice. Use the "How to use this file" section and the kickoff questions in each layer.
3. Propose the recipe using `templates/recipe.md`, including a reason for each choice.
4. Push at least two dials clearly away from the middle, as the dials file requires.
5. List open questions rather than filling gaps with guesses.
6. Let the user confirm before building from it.

### Generating tokens

1. Resolve each value using the resolution order.
2. Structure tokens in three levels: primitives from the brand, semantic roles from the visual language and dials, and component values from all layers combined.
3. Report every value that was clamped by the accessibility floor, and every dial that was outside its language's natural range.

### Designing or building a view

1. Start from the product type: which objects, states and flows does this view need?
2. Apply the experience model: what is the center of gravity, how does navigation work, what must motion communicate?
3. Apply the visual language and dials: hierarchy, composition, shape, surface, color roles, density.
4. Apply the motion language to every state change in the view.
5. Apply the brand at the presence level for this surface.
6. Design the required states, not only the ideal state.
7. Run the self-check below.

### Reviewing work against a recipe

Report findings by layer. For each layer, state what matches the recipe, what deviates, and whether each deviation looks deliberate or accidental. Check the avoid lists, the generic default and the non-negotiables explicitly.

### Updating the repository

Do not change archetype files as a side effect of project work. When project work shows that an archetype, preset or mapping is wrong:

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
- [ ] Assumptions and tensions are listed

---

## Output conventions

- Begin with the recipe values you used, in the one-line format, when they are not already confirmed in the conversation.
- List assumptions and tensions separately from the work itself.
- Refer to archetypes by their exact names in the repository, so that choices can be traced.
- Keep the language of the repository: principles, structure and behavior. Mention platforms, frameworks or tools only when the user's project requires them.
