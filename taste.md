# Taste

What good design is, and how to judge it. The archetypes describe what a product can be; taste describes whether it has been done well. It holds general principles, not a house style. A project's own direction comes from its references and its idea.

---

## Principles

These hold in every visual language. Each can be checked by looking at the result.

1. **Every element has a job.** It helps the user understand, decide or act, or it carries the product's character on purpose. Everything else is removed.
2. **One thing leads.** Each view has a clear first read, and the order in which things are seen matches the order in which they matter.
3. **Space shows relationships first.** Things that belong together sit together, before lines, boxes or color are used.
4. **Few means, used consistently.** A small number of sizes, weights, colors and spacing steps, each with a role. A new variation must mean something new.
5. **Contrast has a purpose.** Differences in size, weight, tone and color create order. Where everything is emphasized, nothing is.
6. **Alignment is deliberate.** Elements share few axes. Breaking the grid is a decision, and it looks like one.
7. **Content is the material.** Design for the real content: the longest name, the empty list, the image that does not fit.
8. **Form tells the truth.** Interactive things look interactive, and similar things behave alike.
9. **Every state is designed.** Loading, empty, error and overflow get the same care as the ideal state.
10. **Correct is not enough.** A product needs at least one decision that makes it specific. A layout can be well built and still be monotonous.
11. **The whole holds together.** Every view belongs to the same product, and the character survives dense views and edge cases.
12. **Accessibility is part of quality.** A design that fails contrast, legibility, focus, target size or reduced motion is not finished.

Where a visual language deliberately does something these principles warn against, the language wins inside its own character. Brutalist rejects polish; Cinematic uses atmosphere. Judge whether it is done with intent.

---

## Signal and noise

**Signal** is everything that helps the user understand, decide or act, and everything that carries the intended character. **Noise** is everything that competes for attention without doing either. Most weak design is not missing signal; it has too much noise around it.

**Common noise:** the same group separated by a card, a border and extra space at once. Labels that repeat the content. Icons that repeat the text beside them. Decoration no one would miss. Equal emphasis on everything. More sizes, weights or colors than there are roles. Badges and counts the user does not need right now.

| Test | How | Signal is strong when |
|---|---|---|
| Removal | Remove an element, in your head or in the product | Something is lost |
| First read | Look for two seconds; note what you saw first, second, third | The order matches what matters |
| Squint | Blur the view | The hierarchy survives as shapes and tones |
| Count | Count the sizes, weights, colors and container styles | Each one has a role you can name |
| One means | Check how each relationship is expressed | By one means: space, a line or a surface, not all three |

Noise is relative to the visual language. Atmosphere is signal in Cinematic; ornament can be signal in Playful.

---

## Anti-patterns

Patterns that make design worse in most contexts. They are judgments, not bans: one is allowed when the genome says why. Without a reason, remove it.

- **Hierarchy:** everything at similar weight; two things competing for the first read; headings barely larger than body text.
- **Structure:** every piece of content in a card; cards in cards; dividers, borders and tints on the same group; uniform spacing everywhere; three-column feature grids as the default.
- **Typography:** sizes and weights without roles; all caps for labels, buttons or navigation; small overlines above every heading; numbered labels (01, 02, 03) on things that are not a sequence; monospace as decoration; long or cramped lines.
- **Color and surface:** gradients, glows, blurred blobs and glass as the main expression; grain or dot grids without a reason; off-white "paper" backgrounds by default; an accent used so often it marks nothing; soft shadows on everything.
- **Components:** icons in tinted rounded squares; badge pills above headlines; arrows after every link; a centered hero with a headline, a subline and two buttons as the default opening; big-number stats without real data.
- **Copy:** slogans and lists of three instead of specific statements; buzzwords; a subline repeating the headline; invented testimonials, logos or numbers; emoji as bullets.

The generic default described in `archetypes/visual-languages.md` and `archetypes/motion-languages.md` is what these add up to.

---

## Judging an idea

An idea is one sentence the whole experience can be built around. It is strong when it passes these tests:

| Test | Passes when |
|---|---|
| Competitor | A competitor could not use it without changing it |
| Image | It suggests specific images, compositions or movements |
| Decision | It can settle a disagreement: one option expresses it better |
| One breath | It can be said aloud to a client in one sentence |
| Ruling out | It makes some common solutions clearly wrong for this product |

| Weak | Why | Stronger |
|---|---|---|
| Modern tech meets human editorial | Adjectives; fits anything | The feeling of tennis, decoded by technology |
| Simple, fast and secure | A feature list | Paying a bill should feel like closing a door |
| Your data, beautifully | A tagline | An instrument panel that only speaks when something changes |

---

## Reading references

References show what words cannot. Read their **form**, not their subject, and separate what a set agrees on from what one reference does alone.

**One reference.** Record observations, not adjectives:

| Look at | Observe |
|---|---|
| First read | What is seen first, second and third |
| Hierarchy | What carries it: size, weight, space, color, position or imagery |
| Typography | Number of sizes, steep or flat scale, weights, case, line length |
| Space and grid | Margins, rhythm, alignment axes, density |
| Color | How much of the surface is colored, how many hues, what the accent does |
| Surface | Containers or open layout, rules, radius, depth |
| Imagery | Role, scale, cropping, relation to type |
| Signature | The one or two details that make it specific |
| Take and leave | What is worth taking, and what belongs to its own brand or content |

**A set.** Compare the readings:

- **Invariants,** found in nearly every reference, are the direction.
- **Variables,** which differ, are open.
- **Outliers** break the pattern: ask whether the outlier is the point.
- **Absences,** things no reference has, are candidate rules. Confirm them first.
- **Contrast pairs,** examples of what not to do, are the strongest signal of all.

**Pitfalls.** The average of many references is generic; the direction lives in the invariants and the signatures. A perfume site says nothing about perfume. A reference's typeface and colors belong to its brand; take the role they play, not the asset. One striking reference can dominate; weigh it against the set. Never copy a layout, a composition, an asset or copy.

**The result** is a short reading: a few statements, each with the references it rests on, the closest visual language, the traits, and two to four signatures. The person corrects it; their corrections outweigh the references.

---

## Reading brand material

Brand material can be anything: a logo, a palette screenshot, guidelines, a component library, a website, a sentence. Extract what exists, fill the gaps, and mark every filled value.

| Asset | Look for | If missing |
|---|---|---|
| Typefaces | Font files, guidelines, the existing product | A neutral family that fits the visual language |
| Colors | Palettes, the logo, tokens, the product | One accent from the logo; neutrals from the warmth trait |
| Logo | Logo files, the product | The name set in the chosen typeface |
| Imagery and icons | Examples, guidelines, the product | Guided by the look; placeholders marked as such |
| Voice | Guidelines, existing copy | Plain, specific language |

- **Values read from an image** are marked, so they can be confirmed.
- **A design system or an existing product** carries more than brand. Name the visual language and traits it is closest to, and ask whether to follow it or evolve it.
- **When brand and look conflict,** for example a playful palette in a Refined look: use the asset only where it fits, lean the traits toward the brand, or choose another language for that surface. Never break accessibility for a brand color.

---

## Critique

Run it on every version before showing it, and whenever the person asks for a review.

1. **Genome fit.** Does the result follow the constraints and the genome? Name deviations, and whether they look deliberate.
2. **Idea.** Does the result express the idea? A result that follows every rule but not the idea has not found its direction.
3. **Principles.** Which are not met?
4. **Signal and noise.** Run the tests. What can be removed?
5. **Anti-patterns.** Which are present without a reason in the genome?
6. **Specificity.** What makes this result specific? Which signatures can be seen? If none, it is correct but generic.

**Report** the single most important problem first. Point at evidence, not impressions: "the headings are only one step larger than the body", not "the typography feels weak". Say what to keep, what feels generic, and the three changes that matter most. Do not praise by default.

---

## Contributing

- Keep the principles general. A preference that only holds for one visual language belongs in that language.
- Add an anti-pattern only when it makes design worse in most contexts, not when it is merely unfashionable.
