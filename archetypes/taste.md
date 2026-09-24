---
layer: taste
version: 0.1
status: draft
---

# Taste

An optional modifier for the archetype system. Taste describes **the preferences of the people designing the product**: what they are drawn to, what they refuse, and the references that show what they mean.

Taste is not a layer and it is not a style. The archetypes stay neutral, and taste never becomes part of them. Like brand, taste is input that the system interprets: a person, a team or a studio places it in the `taste/` folder, and the system takes it into account where the project leaves room for it.

---

## How it relates to other layers

| Layer | Decides | Taste can |
|---|---|---|
| Product type | What the product is | Nothing. Structure follows the product, not the designer. |
| Experience model | How the user engages | Nothing. Behavior follows the user, not the designer. |
| Visual language | Character of form | Favor a language when the description leaves the choice open |
| Motion language | How it moves | Favor a language when the description leaves the choice open |
| Dials | How much of each quality | Shift starting positions, within the language's natural range |
| Brand | Which assets are used | Nothing. Brand belongs to the product, taste to the designer. |

The principle: **brand is what the product must look like. Taste is what the designer would choose when nothing else decides.**

Taste also adds constraints. Everything a taste refuses is added to the avoid lists of the chosen archetypes for the project.

---

## What taste input can be

Taste input can take any form. Common examples:

- A written profile: principles, preferences and things the designer never does
- A list of websites, products or designers they admire, with or without notes
- Screenshots or images of references
- Earlier work by the designer or the studio
- Corrections repeated across projects: "we always end up removing the shadows"

Place files in the `taste/` folder, and mention links in the written project description. Nothing needs to be renamed or structured first.

**Annotated references are worth more than many references.** A reference with a note on what to take from it and what not to take is useful. A folder of unannotated screenshots mostly shows what is popular. When the input is a large unannotated collection, look for what the references have in common, and confirm the reading with the user.

**Images of other people's work stay private.** Keep screenshots out of public repositories. Links and written notes can be shared.

---

## Interpreting taste input

Work through the input in four steps.

1. **Inventory.** List every source: files, links and statements.
2. **Extract.** For each item in the table below, record what the input shows, and where it came from.
3. **Weigh.** Compare the extracted taste with the project description and the brand. Taste yields to both. Note where it had to yield.
4. **Confirm.** Present the reading of the taste together with the recipe, so the user can correct it.

**What to extract:**

| Item | Look for | Used for |
|---|---|---|
| Refusals | "Never" statements, repeated corrections, patterns absent from every reference | Added to the avoid lists for the project |
| Principles | Written rules, what the references consistently do | Project principles in the recipe |
| Language affinities | Visual and motion languages the references belong to | Choosing a language when the description leaves it open |
| Dial tendencies | Density, contrast, color and other qualities shared by the references | Shifting dial starting positions |
| References per language | Which references show which visual or motion language | Calibration while building |
| Typography and color habits | Recurring kinds of typefaces, scales and palettes | Fallbacks where brand defines nothing |

---

## Precedence

When sources disagree, resolve in this order. Earlier wins.

1. **Non-negotiables.** Accessibility is never traded for taste.
2. **The project description.** What the user asks for in this project wins over what the designer usually prefers.
3. **Brand.** The product's assets and rules win over the designer's habits.
4. **Taste.** Fills the choices that are still open.
5. **Archetype defaults.** Presets and fallbacks apply where taste says nothing.

Refusals are the exception. A refusal still applies when the description and the brand say nothing about it. If a refusal conflicts with the description or the brand, follow them and list the conflict in the recipe.

Taste can tighten the rules but never loosen them. It cannot allow a pattern from the avoid lists, the generic default or the AI slop list in `AGENTS.md`. Only the recipe or the brand can allow those, with a stated reason.

---

## Using references while building

- **Read the references for the chosen languages,** two or three of them, preferably from different domains.
- **Take principles, not surfaces.** Extract how hierarchy, space, type and color work, and apply that to the product's own content and brand.
- **Never copy** a layout, a composition, an asset or copy text from a reference.
- **Structure does not come from taste references.** How other products solve a checkout or a settings view is research, not taste. Keep it separate.

---

## Dial tendencies

Taste shifts where the dials start, not where they end.

1. Start from the preset for the chosen visual language.
2. Move each dial toward the taste tendency, but stay inside the language's natural range.
3. Then move dials the description gives a reason to move.

Record every shift in the dials table of the recipe, with taste as the reason. If taste pulls a dial outside the natural range, stop at the edge and note the tension rather than crossing it.

---

## Several tastes

When a team shares a project, several people may have taste profiles.

- **Refusals combine.** Anything one person refuses is avoided, unless the team decides otherwise.
- **Preferences are merged where they agree.** Where they disagree, taste gives no direction, and the archetype defaults apply.
- **A studio taste and a personal taste** can both be present. The studio taste comes first, and the personal taste fills what it leaves open.

---

## Kickoff questions

- Whose taste should this project follow: a person, the team or the studio?
- Which references show what you mean, and what should be taken from each?
- What do you never do, regardless of project?
- Where should taste give way: to the brand, to the users, to the conventions of the platform?

---

## Contributing

- Keep style out of this file. It describes how taste is interpreted, never what good taste is.
- Keep structure out of taste. If a preference describes navigation, flows or states, it belongs in the project description.
- Add to the extraction table when a new kind of taste input keeps appearing.
