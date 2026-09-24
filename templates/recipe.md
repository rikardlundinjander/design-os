---
type: recipe
project: <project-name>
version: 0.1
status: draft | agreed | superseded
design-os: <version or commit of Design OS used>
---

# <Project name>

Copy this file to the project root as `recipe.md` and fill it in. Work through the layers in order: structure before style. Leave a field empty rather than guessing, and add it to open questions instead.

---

## Summary

<One paragraph: what the product is, for whom, and what makes it different.>

```text
Product:    <primary> + <secondary>
Experience: <dominant> + <supporting> (<scope>)
Visual:     <dominant> + <secondary> (<scope>)
Motion:     <language> + <exception> (<scope>)
Dials:      density <n>, contrast <n>, softness <n>, depth <n>, color <n>, warmth <n>, expressivity <n>, motion <n>, novelty <n>
Brand:      <brand-name>, presence <level> (<surface>), <level> (<surface>)
```

---

## Context

- **Users:** <who they are, and how often they use the product>
- **Core job:** <what users are trying to get done>
- **Success looks like:** <how we will know the product works>
- **Constraints:** <platforms, accessibility level, languages, technical or legal constraints>

---

## 1. Product type

- **Primary:** <type>
- **Secondary:** <type, type>
- **Why:** <reason>
- **Key views in scope:** <from the archetype, adjusted for this project>
- **Key flows in scope:** <from the archetype, adjusted>
- **Required states:** <from the archetype, adjusted>
- **Differs from the archetype:** <what is unusual about this product>

---

## 2. Experience model

- **Dominant:** <model>
- **Supporting:** <model> for <view, flow or user group>
- **Why:** <reason>
- **What motion must communicate:** <requirements handed to the motion language>
- **Differs from the archetype:** <what is unusual>

---

## 3. Visual language

- **Dominant:** <language>
- **Secondary:** <language> for <surface>
- **Why:** <reason>
- **Additional avoid rules for this project:** <project-specific additions to the language's avoid list>
- **Differs from the archetype:** <what is unusual>

---

## 4. Motion language

- **Language:** <language>
- **Scoped exceptions:** <language> for <moment or surface>
- **Why:** <reason>
- **Reduced motion approach:** <how the product behaves with reduced motion>

---

## 5. Dials

| Dial | Preset | Value | Scope | Why |
|---|---|---|---|---|
| Density | | | | |
| Contrast | | | | |
| Softness | | | | |
| Depth | | | | |
| Color | | | | |
| Warmth | | | | |
| Expressivity | | | | |
| Motion | | | | |
| Novelty | | | | |

Preset values come from the presets table for the chosen visual language. Fill in "Why" for every dial that differs from the preset.

---

## 6. Brand

- **Profile:** `brands/<brand-name>.md`
- **Status:** approved | provisional

| Surface | Presence |
|---|---|
| <surface> | signature \| present \| quiet |

- **Fit with the visual language:** <conflicts found, and how they are resolved>

---

## Project principles

Three to seven principles specific to this project. They complement the archetypes and guide both people and AI. Write them as rules that can be followed and checked.

1. <Principle>
2. <Principle>
3. <Principle>

---

## Deliberate tensions

| Tension | Why | Revisit when |
|---|---|---|
| <for example: Refined at density 70> | <reason> | <condition> |

---

## Open questions

- <question, and who can answer it>

---

## Decision log

| Date | Decision | Changed from | Reason |
|---|---|---|---|
| | | | |
