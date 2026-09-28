---
process: direction
version: 0.1
status: draft
---

# Direction

The recipe defines the design space: what kind of product this is and what character it should have. It does not give the product an idea. Without one, the gaps are filled with generic patterns, and the result is correct but visually weak.

Direction adds two things, written to `direction.md` beside the recipe:

- **Creative direction:** the central idea the whole experience revolves around.
- **Art direction:** how that idea looks and behaves, as concrete rules.

The simplest distinction:

> **Creative direction is the idea. Art direction is how the idea looks and behaves.**

---

## How it relates to the rest

| Source | Contributes | Example |
|---|---|---|
| Recipe | The design space: product type, experience model, languages, traits | Content + Narrative, Editorial, spacious |
| Constraints | What must be true, in the recipe | Must include pricing, no WebGL |
| **Creative direction** | **The idea** | "The feeling of tennis, decoded by technology" |
| **Art direction** | **The rules that make the idea visible** | Close crops of real play; data as a thin layer over movement |
| Project references | Evidence for the art direction, and its signatures | The reading of the references in `taste/` |
| Brand | The assets the art direction works with | Typefaces, colors, logo |
| Taste model | Whether the result is good | Principles, signal and noise, critique |

The visual language gives the generic character: Editorial says type and space carry the hierarchy. The art direction makes it specific to this product: which type, at what scale, against which images, for which reason.

**Art direction owns the expression.** References, the visual language and the traits inform it; the brand supplies what it works with. Once the user has confirmed the direction, it wins over the reading of the references and the archetype defaults.

---

## Creative direction

### The idea

The idea is one sentence that the whole experience can be built around. It is not a set of adjectives, a tagline or a feature list.

| Weak | Why it is weak | Stronger |
|---|---|---|
| Modern tech meets human editorial | Adjectives; fits any product | The feeling of tennis, decoded by technology |
| Simple, fast and secure | A feature list | Paying a bill should feel like closing a door |
| Your data, beautifully | A tagline | A quiet instrument panel that only speaks when something changes |

A useful idea often holds a **tension between two things**: feeling and analysis, calm and alarm, the physical and the digital. The tension gives the art direction something to design.

### The thought

Under the idea, write a short paragraph that explains it:

- What leads, and what supports
- What the user should feel first, and understand second
- What the idea rules out

For example: lead with the emotion and physicality of playing tennis. Technology is not the hero by itself; it reveals what happens beneath the experience, such as timing, speed and patterns. The user should first want to play, then understand how the product helps them see their game.

### Finding the idea

Start from the brief, not from style.

- **The truth of the subject.** What is the product's world actually like, physically and emotionally?
- **The user's moment.** When and where does the product meet the user, and what are they feeling then?
- **The tension.** What two things does the product hold together?
- **The difference.** What would a competitor never say about their product?

Write three or four candidate ideas, test them, and keep one. The others are material for exploration.

### Testing the idea

| Test | Passes when |
|---|---|
| Competitor | The idea could not be used by a competitor without changing it |
| Image | It suggests specific images, compositions or movements |
| Decision | It can settle a design disagreement: one option expresses it better |
| One breath | It can be said aloud to a client in one sentence |
| Ruling out | It makes some common solutions clearly wrong for this product |

### Tools and dense products

Products that are used every day need an idea too, but it is about the working experience rather than about marketing. "An instrument panel that only speaks when something changes" shapes a dashboard as much as a campaign idea shapes a landing page. For a single small view in an existing product, the product's idea applies; do not write a new one.

---

## Art direction

Art direction translates the idea into rules that can be followed and checked. Every rule is concrete, and every rule has a source: the idea, the reading of the references, the brand, or the visual language.

### Areas

Write the areas that matter for the product. Most products need the first five.

| Area | Decides |
|---|---|
| Typography | Roles, scale contrast, how type meets images and data |
| Composition | What dominates, grid, cropping and overlap, how views are built |
| Imagery | Subject, cropping, scale, what kind of image is never used |
| Color | The role of each color, what the accent marks, what is never colored |
| Motion | What motion connects or reveals, in the idea's terms |
| Data and UI | How information, numbers and interface elements appear |
| Iconography | Whether icons are used, and in what style |
| Surface and material | Containers, lines, depth, texture |
| Signatures | The two to four recurring details that make the direction recognizable |
| Avoid | What this direction rules out |

### Writing rules

- **Concrete, not atmospheric.** "Close crops of real play: ball impact, court texture, body tension", not "authentic imagery".
- **Tied to the idea.** "A serve can turn into its trajectory" follows from "decoded by technology". A rule that does not follow from the idea, the references or the brand needs a reason.
- **Within the design space.** Art direction works inside the recipe and the constraints. If the direction needs a different visual language or trait, change the recipe and log it.
- **Few and strong.** Five to ten rules per area at most. A long list means the idea is not doing its job.
- **Signatures come from both sides.** Some come from the reading of the references, some from the idea itself. Name where each comes from.

---

## The direction file

Write `direction.md` at the project root, next to `recipe.md`.

````markdown
# Direction

## Creative direction

**Idea:** <one sentence>

<The thought: a short paragraph on what leads, what supports, what the user should feel first and understand second, and what the idea rules out.>

## Art direction

### Typography
- <rule> (<source>)

### Composition
- <rule> (<source>)

### Imagery
- <rule> (<source>)

### Color
- <rule> (<source>)

### Motion
- <rule> (<source>)

### Signatures
- <signature>: <what it does> (<idea or references>)

### Avoid
- <what this direction rules out>
````

Sources are short: `idea`, `references: <files>`, `brand`, or the visual language.

---

## Using the direction

- **Before building a view,** state in one line how the idea shows in it, and which rules and signatures it applies.
- **While building,** when two options are both correct, choose the one that expresses the idea better.
- **In critique,** check the direction first after recipe fit: does the result express the idea, and does it follow the art direction? A result that follows every rule but does not express the idea has not found the direction.
- **When iterating,** change the art direction when a rule proves wrong, and keep the idea unless the user decides otherwise. A change of idea is a change of direction; log it.

In exploration, tracks may differ in idea. That is the largest difference two tracks can have, and often the most useful one (see `exploration.md`).

---

## Pitfalls

- **Adjectives as an idea.** "Bold, human, precise" describes a feeling, not an idea.
- **A tagline as an idea.** Marketing copy can come from the idea later; it is not the idea.
- **Art direction without an idea.** A list of rules with nothing holding them together becomes a style guide for a generic product.
- **An idea that never reaches the product.** If the built views could have been made without the idea, it is decoration.
- **Copying a reference brand.** A brand name carries a whole art direction. Take what it does, never how it looks.

---

## Contributing

- Improve the tests when projects show ideas that passed them but did not work.
- Add an area to the art direction table only when projects repeatedly need it.
