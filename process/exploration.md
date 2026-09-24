---
process: exploration
version: 0.1
status: draft
---

# Exploration

Exploration turns one recipe into **several directions that can be compared and chosen between**. Each direction is a track: a thesis about what the product could be, a set of differences from the recipe, and a few built views that show it.

The recipe says what the product is and which character it should have. Exploration shows that the same intention can be expressed in more than one way, before the product commits to one of them.

---

## When to explore

- **After the first recipe, before building the product.** The recipe gives the tracks a shared base; exploration tests its open choices.
- **Before a workshop or review with a client,** when the direction should be chosen together.
- **When a direction has stalled,** and iterating on it no longer improves it.
- **For one surface,** such as onboarding or a marketing page, when that surface needs its own direction within an existing product.

Do not explore without a recipe. Without a shared base, the tracks differ in everything and cannot be compared.

---

## What is locked and what is open

By default, exploration varies the **form** of the product and keeps its **structure**.

| Locked by default | Open in every track |
|---|---|
| Product type | Visual language |
| Experience model | Motion language |
| Content and key tasks | Dials |
| Brand assets | Brand presence per surface |
| Non-negotiables | Composition and typographic hierarchy |
| The taste model | |

**Exploring structure.** When the user asks for it, tracks may also differ in experience model, for example a Dashboard track and a Command track for the same data product. Product type stays locked. Structural tracks are compared on the key tasks first: every track must let the user complete the same tasks, and the comparison starts with how well each does that, before how it looks.

---

## Tracks

Three tracks is the default. Each has a role.

| Track | Role | Thesis |
|---|---|---|
| **A: Closest** | The strongest version of the recipe as written | "This is what the recipe asks for, done well." |
| **B: Stretch** | Pushes the recipe further in a direction it already points | "What if we go further on what makes this product specific?" |
| **C: Challenge** | Questions one choice in the recipe, and records it as a deliberate tension | "What if the recipe is wrong about this one thing?" |

The challenge track is a serious proposal, not a contrast to make the others look good. If it would never be chosen, it is not a challenge; replace its thesis.

More tracks are possible when the user asks for them. Each extra track needs its own thesis. Five tracks is the useful maximum; beyond that, the comparison becomes the work.

**Naming.** Tracks are named by letter and a short name, such as `B: Editorial scale`. The letters stay fixed for the whole project, so later work can refer to them: "the navigation from C".

---

## How different is different enough

Tracks must offer a real choice. Every pair of tracks differs in at least two of these:

- The dominant visual language
- The motion language
- Two or more dials, clearly apart
- The principle of composition, for example type-led versus image-led, or one column versus a strict grid
- Brand presence on the key views

**These do not count as a difference on their own:** a different accent color, a different typeface in the same role, different imagery, or the same layout with different spacing.

**The glance test.** With the same view from each track side by side, a person should be able to tell them apart at a glance, and say in one sentence what each one is betting on. If two tracks need explaining, merge them and write a new thesis.

---

## The track file

Each track has a short file at `explorations/<letter>-<name>/track.md` in the project.

````markdown
# B: Editorial scale

**Role:** Stretch
**Thesis:** <one sentence: what this direction bets on>
**Status:** open | chosen | parked

## Differs from the recipe

```text
Visual:     Editorial (was Neutral)
Dials:      contrast 85 (was 60), expressivity 70 (was 30)
```

## Why it could work

<Two or three sentences, tied to the project description.>

## What it risks

<Two or three sentences: where this direction could fail.>

## Key views

<The views built for this track, and where to see them.>

## Critique

<Written after building, following the critique in archetypes/taste.md.>
````

List only what differs from the recipe. Everything not listed is the recipe.

---

## Key views

Every track builds the same views, with the same content. Choose one to three views that put the most pressure on a direction:

1. **The first impression.** The view most users see first, or the view that carries the product's character.
2. **The working view.** The densest or most repeated view, where a direction shows whether it holds up in daily use.
3. **An edge.** An empty, error or overflow state, or the longest real content, where weak directions break.

Use real content. Placeholder text makes every direction look better than it is.

---

## Building tracks

- **Build enough to judge, not a product.** The key views, responsive, in their ideal state and one edge state. Skip full flows.
- **Build every track to the same level.** A polished track next to rough ones wins by finish, not by direction.
- **Share scaffolding, not style.** Tracks can share code structure, data and components, but nothing that decides the form, beyond the locked brand assets.
- **Make them viewable side by side.** Every key view of every track has a preview that can be opened next to the others, on desktop and on mobile.
- **Critique each track** with the taste model before comparing them.

---

## Comparing and choosing

Present the tracks together, with one comparison:

| | A: Closest | B: Stretch | C: Challenge |
|---|---|---|---|
| Thesis | | | |
| Fit with the description | | | |
| Fit with the brand | | | |
| Hierarchy and clarity | | | |
| What makes it specific | | | |
| Main risk | | | |

An opinion on which track is strongest is welcome, but label it as an opinion and give the reason. The choice belongs to the designer, or to the designer and the client together.

A choice can take three forms:

- **One track.** It becomes the direction.
- **One track, with qualities from another.** For example B, with the navigation from C. Record exactly what is borrowed and from where.
- **None.** Write down what the tracks taught, adjust the recipe, and explore again with new theses.

---

## After the choice

1. **Update the recipe.** Apply the chosen track's differences, and any borrowed qualities, to `recipe.md`.
2. **Log the decision.** Add a line to the decision log: which track was chosen, over which, and why.
3. **Park the others.** Set their status to parked. Keep the files and the previews; they are the history of the direction and can be borrowed from later.
4. **Keep the reactions.** What the client or the team reacted to, for or against, is a strong reference. Add notes to `taste/`, so the next reading of the references includes them.

---

## Pitfalls

- **Three versions of one idea.** Tracks that pass the glance test only when explained.
- **A challenge track built to lose.**
- **Uneven finish,** so the choice is decided by polish.
- **Different content per track,** so the comparison is unfair.
- **Exploring details before direction.** Button styles and icon sets are not directions.
- **Choosing silently.** The AI never picks a track on its own; it presents, compares and gives an opinion.

---

## Contributing

- Keep the track roles few and distinct. Add a role only when projects repeatedly need a kind of track the three roles cannot express.
- Refine the difference rules when projects show that tracks still end up too similar, or too far apart to compare.
