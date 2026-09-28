# Genome

An operating system for digital product design, driven by human creativity.

Genome lets an AI work as an expert product designer. It knows the archetypes of digital products, it knows what good visual design is, and it uses that knowledge to realize a person's vision: what the product is, how it looks, how it behaves, and the idea it is built around.

The person brings the vision and makes the decisions. The AI brings knowledge and judgment, proposes, builds and critiques.

---

## The parts

| | File | What it holds |
|---|---|---|
| **Knowledge** | [`archetypes/`](archetypes) | Four sets of archetypes: [product types](archetypes/product-types.md), [experience models](archetypes/experience-models.md), [visual languages](archetypes/visual-languages.md) and [motion languages](archetypes/motion-languages.md) |
| **Vocabulary** | [`traits.md`](traits.md) | How a product leans, in words, and what words like playful or premium mean |
| **Judgment** | [`taste.md`](taste.md) | Principles of good design, signal and noise, anti-patterns, how to read references and brand material, and critique |
| **Method** | [`AGENTS.md`](AGENTS.md) | How the AI works with the person, in a loop of five steps |
| **The vision** | `project/genome.md` | Everything decided for one product, written by the AI and approved by the person |

---

## The genome

Every product gets a genome: one short file that answers four questions.

| | Question | Decided with |
|---|---|---|
| **What** | What is the product, who is it for, what must be true? | Product types, experience models, constraints |
| **Idea** | What is the one idea the whole experience revolves around? | The person's vision, tested with `taste.md` |
| **Look** | How does the idea look? | A visual language, traits, references and the brand |
| **Behavior** | How does it behave and move? | The experience model and a motion language |

```text
Product:    Service + Content
Experience: Workflow (dominant) + Object (case overview)
Visual:     Neutral
Motion:     Quiet
Traits:     spacious (clearly), strong contrast (clearly), conventional (fully)
Idea:       Official matters, as calm as a well-kept archive
```

The archetypes give every product a considered starting point. The idea makes it specific. Without an idea, the result is correct but generic.

---

## The loop

1. **Listen.** The AI reads the person's description and everything in `project/input/`, and asks only what would change a choice.
2. **Write the genome.** What, idea, look, behavior. The person corrects and approves it.
3. **Show alternatives.** When the direction is open: three tracks, the closest, one that stretches and one that challenges. The person chooses.
4. **Build.** With real content and every state.
5. **Critique and refine.** The AI critiques its own work, then the person steers with words, such as "more compact" or "calmer". The AI shows how it reads each request before changing anything.

---

## Starting a project

1. Clone or copy this repository.
2. Put whatever you have in `project/input/`: brand material, references, screenshots, notes. Any form, no templates.
3. Describe what you want to build, in your own words.
4. Let the AI follow [`AGENTS.md`](AGENTS.md).

Keep the system files unchanged. Everything specific to the project lives in `project/`. Keep screenshots of other people's work out of public repositories.

---

## Principles

- **The person decides.** The AI proposes, gives opinions and never chooses on the person's behalf.
- **Structure before style.** Decide what the product is before how it looks.
- **An idea before rules.** Every rule of the look should follow from the idea, the references or the brand.
- **Words, not numbers.** Qualities are described and adjusted in words, and every value is judged in the product.
- **Accessibility is not a setting.** Nothing overrides it.

---

## Contributing

Genome improves through use. When a project shows that an archetype, a trait, a word or a principle is wrong, change the file. Keep every archetype of the same kind in the same format, stay platform-agnostic, and add sparingly.
