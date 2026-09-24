---
layer: taste
version: 0.3
status: draft
---

# Taste

The taste model is **the quality bar of the system**. The archetype layers describe what a product is and what character it should have. The taste model describes how to judge whether that character has been realized well: the principles of good design, the difference between signal and noise, the patterns that make design worse, and how to critique a result.

It also describes how to read references. References are how a project, a team or a client shows what they mean, and reading them well is how the system picks up a direction without copying it.

The taste model applies to every project. It holds general principles, not a house style. A more specific flavor can grow from references over time.

---

## How it relates to other layers

| Layer | Decides | The taste model adds |
|---|---|---|
| Product type | What the product is | Nothing. Structure follows the product. |
| Experience model | How the user engages | Nothing. Behavior follows the user. |
| Visual language | Character of form | How well that character is carried out |
| Motion language | Role and character of motion | Whether motion earns its place |
| Dials | Direction of each quality | Anchors for the positions, read from references |
| Project references | How the product is expressed, when a project has them | The method for reading them |
| Brand | Which assets are used | Nothing. Brand belongs to the product. |

The principle: **the layers decide what the product should be. The taste model judges how well it is done.**

Where a visual language deliberately does something the taste model warns against, the language wins inside its own character. Brutalist rejects polish; Cinematic uses atmosphere that would be noise in Neutral. The taste model then judges whether the choice is carried out with intent.

---

## Principles of good design

These hold in every visual language. Each can be checked by looking at the result.

1. **Every element has a job.** It helps the user understand, decide or act, or it carries the product's character on purpose. Everything else is removed.
2. **One thing leads.** Each view has a clear first read. The order in which things are seen matches the order in which they matter.
3. **Relationships are shown by space first.** Things that belong together sit together. Distance expresses relationship before lines, boxes or color do.
4. **Few means, used consistently.** A small number of sizes, weights, colors and spacing steps, each with a clear role. A new variation must mean something new.
5. **Contrast has a purpose.** Differences in size, weight, tone and color exist to create order. Where everything is emphasized, nothing is.
6. **Alignment is deliberate.** Elements share a small number of axes. Breaking the grid is a decision, and it is visible as one.
7. **Content is the material.** Design for the real content, including the longest name, the empty list and the one image that does not fit. Placeholder content hides problems.
8. **Form tells the truth.** Interactive things look interactive, static things look static, and similar things behave alike.
9. **Every state is designed.** Loading, empty, error, partial and overflow states get the same care as the ideal state.
10. **Correct is not enough.** A product needs at least one decision that makes it specific: a typographic choice, a composition, a way of using space or motion. A layout can be well structured and still be monotonous.
11. **The whole holds together.** Every view looks like it belongs to the same product, and the character survives dense views and edge cases.
12. **Accessibility is part of quality.** Contrast, legibility, focus, target size and reduced motion are not a separate checklist. A design that fails them is not finished.

---

## Signal and noise

**Signal** is everything that helps the user understand, decide or act, and everything that carries the intended character. **Noise** is everything that competes for attention without doing either.

Most weak design is not missing signal. It has too much noise around the signal.

**Common sources of noise:**
- The same relationship expressed several times: a card with a border, a divider and extra spacing around the same group
- Labels that repeat what the content already says
- Icons that repeat the text next to them
- Decoration that no one would miss
- Equal emphasis on everything, so nothing leads
- More sizes, weights, colors or container styles than there are roles
- Chrome around small amounts of content
- Status, badges and counts that the user does not need at that moment

**Tests:**

| Test | How | Signal is strong when |
|---|---|---|
| Removal | Remove an element in your head, or in the product | Something is lost. If nothing is lost, it was noise. |
| First read | Look for two seconds, then note what you saw first, second and third | The order matches what matters |
| Squint | Blur the view | The hierarchy survives as shapes and tones |
| Count | Count the distinct sizes, weights, colors and container styles in a view | Each one has a role you can name |
| One means | For each relationship, check how it is expressed | It is expressed by one means: space, a line or a surface, not all three |

Noise is relative to the visual language. Atmosphere is signal in Cinematic, ornament can be signal in Playful. Judge noise against what the chosen language says carries hierarchy and character.

---

## Anti-patterns

Patterns that make design worse in most contexts. They are judgments, not universal bans: a pattern is allowed when the recipe states why it is used. Without a stated reason, remove it.

The generic default in `visual-languages.md` and `motion-languages.md` describes the look these patterns add up to. Check both.

**Hierarchy**
- Everything at similar visual weight, so nothing leads
- Two or more elements competing for the first read
- Headings that are barely distinguishable from body text, or much larger than the content needs

**Structure and containers**
- Every piece of content in a card; cards inside cards
- Dividers, borders and background tints all used on the same group
- Uniform spacing everywhere, regardless of relationships
- Three- or four-column feature grids as the default way to present anything

**Typography**
- Many sizes and weights with no clear role for each
- All caps for labels, buttons, navigation or headings
- Small labels above every heading (overlines), especially in caps with wide letter spacing
- Numbered labels such as 01, 02, 03 on things that are not a real sequence
- Monospace used as decoration, to make something feel technical
- Long lines of text, or text set too tight to read

**Color and surface**
- Gradients, glows, blurred color blobs and glass effects as the main expression
- Background textures such as grain, noise and dot grids without a reason
- Beige or off-white "paper" backgrounds as a default rather than a choice
- Accent color used on so many things that it no longer marks anything
- Soft shadows on everything, or depth that does not correspond to layers

**Components**
- Icons in tinted rounded squares on every item
- Badge pills above headlines, such as "New" or "Introducing"
- Arrows after every link
- A centered hero with a headline, a subline and two buttons as the default opening
- Stat rows with large numbers and no real data behind them

**Content and copy**
- Slogans and rhythmic lists of three instead of specific statements
- Buzzwords and vague benefits instead of the actual thing, number or action
- Headline and subline saying the same thing twice
- Invented proof: testimonials, logos, user counts or statistics that are not real
- Emoji as bullets or decoration

**Motion**
- See the generic default and the avoid lists in `motion-languages.md`

---

## Critique

Critique is how the taste model is applied to a result. Run it on every version before delivering, and whenever the user asks for a review.

**Order:**

1. **Recipe fit.** Does the result follow the chosen layers, dials and brand? Report deviations by layer, and whether each looks deliberate.
2. **Principles.** Go through the principles of good design. Name the ones that are not met.
3. **Signal and noise.** Run the tests. List what can be removed.
4. **Anti-patterns.** List every anti-pattern present that the recipe does not justify.
5. **Specificity.** Name what makes this result specific. If nothing does, say so: the result is correct but generic. When the project has references, name the signatures the result translates; if none can be seen, the direction has not come through.

**Dimensions to judge:** hierarchy, composition, typography, rhythm, density, restraint, specificity and coherence.

**How to report:**

- Lead with the single most important problem.
- Point at evidence in the result, not at impressions: "the section headings and the body text are two steps apart in size", not "the typography feels weak".
- Say what works and should be kept, what feels generic, and the three changes that matter most.
- Phrase changes as direction: what to keep, what to strengthen, what to reduce.
- Do not praise by default. A critique with no problems needs a reason.

The designer decides what to change. When a critique leads to a change, record the learning in the recipe's decision log, so the next version starts from it.

---

## Analyzing references

References show what words cannot. Reading them well means extracting **observable qualities of form**, not subject matter, and separating what a set of references agrees on from what only one of them does.

### Reading one reference

For each reference, record observations, not adjectives. Every statement should point at something that can be seen.

| Dimension | What to observe |
|---|---|
| First read | What is seen first, second and third |
| Hierarchy | What carries it: size, weight, space, color, position or imagery |
| Typography | Number of sizes, steep or flat scale, weights, case, line length, families and their roles |
| Space and grid | Margins relative to content, uniform or varied rhythm, alignment axes, density |
| Color | Share of the surface that is colored, number of hues, role of the accent |
| Surface and shape | Containers or open layout, rules, radius, depth |
| Imagery | Role, scale, cropping, relation to type |
| Signal and noise | What carries meaning, what is decoration, how many elements compete |
| Motion | If the reference moves: role and character, from `motion-languages.md` |
| Signature | The one or two details that make it specific rather than generic |
| Reading | Closest visual and motion language, estimated dial directions, and how confident the reading is |
| Take and leave | What is worth taking from it, and what belongs to its own brand or content and should be left |

### Reading a set

Individual readings become useful when they are compared.

- **Invariants** are qualities found in nearly every reference. They are the direction.
- **Variables** are qualities that differ between references. They are open, not part of the direction.
- **Outliers** are single references that break the pattern. Ask whether the outlier is the point or an accident.
- **Absences** are things that appear in none of the references, such as shadows or rounded corners. They are candidate refusals; confirm them before treating them as rules.
- **Contrast pairs** are the strongest signal. When references come with examples of what not to do, the difference between the two sets says more than either set alone.

### Pitfalls

- **Averaging.** The average of many references is generic. The direction lives in the invariants and in the signatures, not in the mean.
- **Subject matter.** A reference from a perfume brand says nothing about perfume. Read its form.
- **Brand as taste.** A reference's specific typeface or blue belongs to its brand. Take the role it plays, not the asset.
- **One loud reference.** A single striking reference can dominate the reading. Weigh it against the set.
- **Surface copying.** Never reproduce a layout, a composition, an asset or copy text.
- **Structure from references.** How another product solves a checkout is research, not taste. Keep it separate.

### The result

Summarize a set as a **reading**: five to ten statements, each with the references it rests on and a confidence level, plus the closest visual and motion language, the dial directions and two to four signatures. Present it to the user and let them correct it. Corrections are stronger evidence than the references themselves.

---

## References in a project

A project can bring its own references in the `taste/` folder. Typical sources:

- A direction chosen with a client, for example in a workshop
- The designer's or the studio's own references and earlier work
- Screenshots, UI elements, links, and notes on what to take from them
- Examples of what to avoid

Place files in the `taste/` folder, and mention links in the written project description. Nothing needs to be renamed or structured first. Notes on what someone reacted to, such as "they liked the calm in B, not the black", are worth more than more images.

**Images of other people's work stay private.** Keep screenshots out of public repositories. Links and written notes can be shared.

Read the references with the method above, and apply the reading as follows.

### References own the expression

When a project has references, they are not a tiebreaker. They decide **how the product is expressed**, and brand decides **what it is expressed with**.

| References decide | Brand decides |
|---|---|
| Visual and motion language | Typefaces |
| Dial directions | Colors and color scales |
| Composition and grid | Logo and distinctive assets |
| Typographic hierarchy: scale, contrast, rhythm | Imagery sources and icon set |
| Treatment of imagery: scale, cropping, placement | Tone of voice |
| Signatures | Signature motion defined by the brand |

The project description wins where it is explicit about expression, for example "it must feel like a public service". Vague words such as "modern" or "premium" do not override the references; the references show what those words mean for this project. The non-negotiables always win.

When the brand comes with rules about expression, such as layout rules in guidelines or an existing design system, weigh them against the references with the follow-or-evolve decision in `brand.md`. Until that is decided, follow the references for expression and list the conflict as an open question.

### How the reading is applied

| From the reading | Applied as |
|---|---|
| Closest visual and motion language | The languages of the recipe, unless the description names others |
| Dial directions | The starting positions of the dials. Presets apply only to dials the reading says nothing about |
| Signatures | Translated into every key view (see below) |
| Invariants | Project principles in the recipe, checked in critique |
| Absences and "not this" examples | Added to the avoid lists for the project, once confirmed |
| References per language | Anchors for the dials and calibration while building |

**Natural ranges do not stop the references.** If the references are denser, softer or more saturated than the chosen language usually is, follow the references and record the tension in the recipe. Those tensions are often where the product's own expression is.

**Anti-patterns can be part of a direction.** If a pattern from the anti-patterns is an invariant or a signature of the reference set, it may be used. Record it in the recipe with the references it comes from. A pattern that appears in only one reference does not qualify.

### Translating signatures

Signatures are what make a direction recognizable. The reading names **two to four signatures**: details that recur across the set, or that the user points out as the reason a reference was chosen.

- **Every key view translates one or two signatures.** A key view with none has not taken the direction.
- **Translate the form, not the surface.** Take what the signature does, such as how a large number sits against small labels, and apply it to this product's content and brand. Never reproduce the reference's layout, assets or copy.
- **Name them.** The recipe lists the signatures, and each built view states which ones it translates and how.
- **Check them in critique.** Under specificity, name the signatures the result translates. If they cannot be seen, the direction has not come through.

### Precedence

When sources disagree about expression, earlier wins:

1. **Non-negotiables.** Accessibility is never traded for taste.
2. **The project description,** where it is explicit.
3. **Project references.** The reading of the references in `taste/`.
4. **The taste model and archetype defaults.** Principles, anti-patterns, presets and fallbacks.

Brand assets are not part of this order. They come from the brand.

---

## Kickoff questions

- Which references show what you mean, and what should be taken from each?
- Are there examples of what this product must not look like?
- Where did the client or the team react most strongly, for or against?
- Where should the references give way: to the brand, to the users, to the conventions of the platform?

---

## Contributing

- Keep the principles general. A preference that only holds for one visual language belongs in that language.
- Add an anti-pattern only when it makes design worse in most contexts, not when it is merely unfashionable.
- Keep structure out of taste. If a rule describes navigation, flows or states, it belongs in another layer.
- Refine the reading method when projects show that a dimension is missing or misleading.
