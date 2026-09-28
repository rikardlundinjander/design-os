# Instructions for AI agents

This file tells AI agents how to use Genome. It applies to any tool or model working in this repository or in a project started from it. If your tool expects a different file name for instructions, point it to this file.

---

## How a project starts

1. The user clones or copies this repository.
2. The user adds any brand material they have to the `project/brand/` folder. This can be anything: a logo, a screenshot of a palette, guidelines, font files, or nothing at all. Optionally, they add references to the `project/references/` folder: a direction chosen with a client, their own references, screenshots, UI elements, or examples of what to avoid.
3. The user describes in written text what they want to build. The description may also contain links, such as a component library, an existing website or a design file.
4. **You** turn the description, the brand material and any references into a genome and a direction, and write them to `project/genome.md` and `project/direction.md`.
5. The user reviews and adjusts the genome and the direction.
6. If the direction is still open, or the user asks for alternatives, you explore it in tracks, following `process/exploration.md`, and the user chooses.
7. Only then do you build from the genome.

The user does not fill in templates. Your job is to interpret free-form input and make the choices explicit.

---

## What this repository contains

Genome describes a digital product as a genome: four archetypes chosen from a stable foundation, plus traits, brand and an idea.

| Part | File | Kind |
|---|---|---|
| Archetype 1: Product type | `archetypes/product-types.md` | Choose |
| Archetype 2: Experience model | `archetypes/experience-models.md` | Choose |
| Archetype 3: Visual language | `archetypes/visual-languages.md` | Choose |
| Archetype 4: Motion language | `archetypes/motion-languages.md` | Choose |
| Traits | `traits/traits.md`, `traits/words.md` | Describe in words; adjust by prompting |
| Brand | `brand/brand.md` | Interpret the brand material |
| Direction | `process/direction.md` | Find the idea; write the art direction |

Everything specific to a project lives in `project/`: the genome, the direction, the brand material and the references.

The taste model in `taste/taste.md` is not part of the genome. It is the quality bar that applies to every project: principles of good design, signal and noise, anti-patterns and critique. It also describes how to read the references in `project/references/`. It never changes structure or brand.

The `process/` folder describes how work moves from genome to product:

| Process | File | Use when |
|---|---|---|
| Direction | `process/direction.md` | Always: every project gets an idea and an art direction |
| Exploration | `process/exploration.md` | The direction should be compared and chosen between several tracks |

---

## Creating the genome

### 1. Read the input

- The written project description, including every hard requirement in it: these become the constraints
- Everything in `project/brand/`, and every link mentioned in the description
- Everything in `project/references/`, if the folder has content
- An existing `genome.md`, if the project already has one; update it rather than starting over

### 2. Choose each part, in order

Work from structure to style: product type, experience model, visual language, motion language, traits, brand.

For each layer, read its "How to use this file" section and the sections listed under [Reading the parts](#reading-the-parts). Then:

- Pick the choice that fits the description best, following the layer's rules: one primary or dominant choice, and supporting choices only with a scope.
- For the visual and motion language, when the project has references, take the languages from their reading, unless the description names others.
- Write down why, referring to what the description said.
- Note where the project differs from the archetype. That is usually where the interesting design work is.

### 3. Describe the traits

Traits are words, never numbers. When the project has references, take the traits from their reading. Otherwise start from the language character in `traits/traits.md`. Translate the description's words, such as playful or premium, through `traits/words.md`, and record which reading you chose when a word has several. References may lean a trait past where the language stops being itself; record the tension. Write only the traits that give the product its character, with at least two clear leans.

### 4. Interpret the brand

Follow the four steps in `brand/brand.md`: inventory, extract, fill gaps, confirm. Mark every value that was read from an image, generated or filled in as a fallback. If the brand input includes a design system or an existing product, identify the closest visual language and traits, and decide with the user whether to follow or evolve it.

### 5. Read the references

If `project/references/` has content, analyze it with the method in `taste/taste.md`: read each reference, then the set, and summarize it as a reading with two to four signatures. The reading sets the languages and the traits, and it is the main evidence for the art direction. Only an explicit statement in the description overrides it. Present the reading with the genome so the user can correct it. Skip this step when there are no references.

### 6. Write the direction

Follow `process/direction.md`. Find the idea: write three or four candidates from the brief, test them, and keep one; the others are material for exploration. Then write the art direction: concrete rules per area, each with its source, and the signatures. The art direction owns the expression of the product, within the genome and the constraints. Brand owns the assets.

### 7. Ask only what changes the choices

Do not ask the user to answer every kickoff question. Ask only when the answer would change a choice in the genome, and ask all such questions at once. Everything else becomes an assumption, stated in the genome.

### 8. Write the genome and the direction

Write `genome.md` using the format below, and `direction.md` using the format in `process/direction.md`. Present both to the user for review.

---

## Genome format

````markdown
# <Project name>

## Genome

```text
Product:    <primary> + <secondary>
Experience: <dominant> + <supporting> (<scope>)
Visual:     <dominant> + <secondary> (<scope>)
Motion:     <language> + <exception> (<scope>)
Traits:     <trait> (<slightly | clearly | fully>), <trait> (<strength>), <trait> (<scope>)
Brand:      <short summary of sources>, presence <level> (<surface>), <level> (<surface>)
Taste:      <reference sources, or none>, applied to <choices, traits, avoid lists>
Idea:       <the one-sentence idea from direction.md>
```

## What we are building

<Your interpretation of the description in a few sentences: users, core job, what success looks like.>

## Constraints

<Hard requirements from the description and the brand, such as required content, platforms, technical limits or a fixed typeface. They are not interpreted creatively. If a constraint conflicts with a choice, the constraint wins.>

## Choices

For each layer: the choice, the scope of any supporting choice, why, and how the project differs from the archetype.

## Traits

| Trait | Lean | Scope | Why |
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
- **Applied:** <languages, traits, principles and avoid rules taken from the reading>
- **Tensions:** <where the references go outside a language's natural range, or use an anti-pattern, and why>
- **Yielded:** <where the references gave way to an explicit statement in the description>

## Project principles

<Three to seven rules specific to this project, written so they can be followed and checked.>

## Assumptions

<Everything decided without explicit input from the user.>

## Open questions

<Questions whose answers could change the genome.>

## Decision log

| Date | Decision | Changed from | Reason |
|---|---|---|---|
````

Keep the genome short. It is a starting point, not a specification.

---

## Reading the parts

Do not load every file in full for every task. For each part, read the shared sections and the section for the chosen archetype:

| Layer | Always read | Read for the chosen archetype |
|---|---|---|
| Product type | What this layer owns | Key views, key flows, required states, structural needs, common failure modes |
| Experience model | What this layer owns | Navigation, selection and feedback, implications for other layers, anti-patterns |
| Visual language | What this layer owns, Non-negotiables, The generic default | Principles, Avoid, Tendencies |
| Motion language | What this layer owns, Non-negotiables, The generic default, Vocabulary, Timing grows in the product | Role and character, Principles, Avoid, Reduced motion, the column in the Moments table |
| Traits | Writing traits in the genome, Tuning by prompt, From traits to values | The descriptions and guardrails for every trait the genome names, `traits/words.md`, and the language character table |
| Brand | The whole file | Not applicable |
| Taste | Principles of good design, Signal and noise, Anti-patterns, Critique | Analyzing references and References in a project, when `project/references/` has content |

For secondary or supporting choices, read the same sections and apply them only within their stated scope.

---

## Rules

### Respect constraints

The constraints in the genome are mandatory. Never interpret them creatively, and never trade them for a design choice. Only the non-negotiables rank above them.

### Respect layer ownership

Each layer owns specific decisions, listed in its "What this layer owns" section. Never let one layer make a decision that belongs to another.

- Product type and experience model decide structure and behavior. Brand never changes them.
- Visual language decides the character of form. Traits decide which way it leans. Brand decides the specific assets.
- The direction gives the product its idea. The art direction decides the expression, informed by the references; brand decides the assets. The taste model judges how well it is done. None of them change structure or behavior.
- The experience model states what motion must communicate. The motion language decides how.

### Decide values in order

Traits are words, not measurements. They never calculate a value. For every concrete value, such as a radius, a text size, a spacing step or a duration:

1. Start from the character of the visual or motion language.
2. Lean the way the traits describe.
3. Fill in specific assets from the interpreted brand.
4. Clamp to the accessibility floor.

Then look at the result in the product. If it does not read as the intended lean, change the value. Anchor the leans that matter in references or in an earlier version, as described in `traits/traits.md`. When a trait leans past where the language stops being itself, apply it and note the tension.

### Tune by prompt

When the user asks for a change in words, such as "more compact", "calmer" or "more premium", follow *Tuning by prompt* in `traits/traits.md`. Translate the words into traits, show your interpretation before you change anything, change only what was named, starting from the current version, and record the prompt and the interpretation in the decision log. If a word has several readings, name them. If a prompt meets a constraint or a non-negotiable, say so.

### Treat avoid lists as constraints

The avoid lists and anti-patterns in each chosen archetype are hard constraints, not suggestions. Check work against them before delivering it.

### Apply the taste model

The principles, the signal and noise tests and the anti-patterns in `taste/taste.md` apply to every project. Anti-patterns are judgments rather than bans: one is allowed only when the genome states why it is used. Where a chosen visual language deliberately does something the taste model warns against, the language wins inside its own character.

### Check against the generic default

`visual-languages.md` and `motion-languages.md` each describe a generic default look and motion. If your output shows it, and the genome did not ask for it, revise the output before delivering.

### Never break the non-negotiables

The non-negotiables in the visual and motion layers override every archetype, trait and brand rule. This includes contrast, visible focus, not relying on color alone, legible text sizes, touch target sizes and reduced motion. If the genome or the brand input would break one, follow the non-negotiable and tell the user.

### Keep scopes

One dominant choice per layer governs everything unless a scope says otherwise. Apply secondary choices only within their scope, and never mix two choices on the same surface without a stated rule.

### Do not invent archetypes

Use only archetypes and traits that exist in the repository. If a project seems to need something that is missing, describe it as a combination of existing ones, or propose a change to the repository.

---

## Exploring directions

When the user asks for directions, alternatives, options or an exploration, or before a workshop where the direction will be chosen, follow `process/exploration.md`:

- Explore from a genome, never without one.
- Keep product type, experience model, content, brand assets, non-negotiables and the taste model locked, unless the user asks to explore structure. Product type is always locked.
- Build three tracks by default, Closest, Stretch and Challenge, with a thesis each, and check that every pair differs enough.
- Build the same one to three key views with the same real content in every track, to the same level of finish.
- Critique every track, compare them in one table, and give an opinion labeled as such. Never choose on the user's behalf.
- After the choice, update the genome, log the decision and park the other tracks.

---

## Building from the genome

1. Start from the product type: which objects, states and flows does this view need?
2. Apply the experience model: what is the center of gravity, how does navigation work, what must motion communicate?
3. Apply the visual language and traits: hierarchy, composition, shape, surface, color roles, density.
4. Apply the motion language to every state change.
5. Apply the brand at the presence level for the surface.
6. Express the direction: before each view, state in one line how the idea shows in it, and translate one or two signatures from the art direction.
7. Design the required states, not only the ideal state.
8. Critique the result as described in `taste/taste.md`, and revise before delivering.
9. Run the self-check below.

When generating tokens, structure them in three levels: primitives from the brand, semantic roles from the visual language and traits, and component values from all layers combined. Report every value clamped by the accessibility floor.

When the user changes direction during the project, update `genome.md` and add a line to the decision log.

---

## Reviewing work

When asked to review work, run the critique in `taste/taste.md`. It starts with genome fit: report findings by layer, and for each layer state what matches, what deviates, and whether each deviation looks deliberate or accidental. Then judge the result against the principles, the signal and noise tests, the anti-patterns and the non-negotiables, and lead with the single most important problem.

---

## Updating this repository

Do not change the archetype files as a side effect of project work. When project work shows that an archetype, a trait or a word is wrong:

1. Describe the problem and the evidence.
2. Propose the specific change.
3. Make the change only when the user agrees, following the Contributing section of the affected file.
4. Raise the version in the file's front matter when the meaning changes.

---

## Self-check before delivering

- [ ] The work follows the genome, or deviations are stated
- [ ] No layer made a decision owned by another layer
- [ ] Values follow the language character and the traits, and read as intended in the product
- [ ] Nothing in the chosen avoid lists appears in the output
- [ ] The output does not drift toward the generic default
- [ ] All non-negotiables are met
- [ ] Required states are handled, not only the ideal state
- [ ] Brand fallbacks and generated values are marked
- [ ] The result passes the signal and noise tests, and every anti-pattern present has a stated reason
- [ ] The result has at least one decision that makes it specific
- [ ] All constraints are met
- [ ] Each key view expresses the idea and translates one or two named signatures from the art direction
- [ ] Assumptions and tensions are listed
