---
type: recipe
project: example-learning-app-for-children
version: 0.1
status: example
---

# Example: Learning app for young children

A fictional example showing how a recipe is filled in. Not a real project.

---

## Summary

A learning app where young children practice early reading through short, playful exercises. Parents set it up and follow progress. Children cannot read instructions, so everything must be understood by looking, listening and trying.

```text
Product:    Content (primary) + Tool (parent area)
Experience: Narrative (dominant) + Manipulation (exercises) + Object (parent area)
Visual:     Playful + Neutral (parent area)
Motion:     Expressive
Dials:      density 15, contrast 70, softness 90, depth 35, color 90, warmth 70, expressivity 85, motion 80, novelty 55
Brand:      <app-brand>, presence signature (child experience), quiet (parent area)
```

---

## Context

- **Users:** Children who cannot yet read; parents who set up and follow progress
- **Core job:** Children: play and learn. Parents: see that it helps, and control screen time
- **Success looks like:** Children return voluntarily; parents see progress
- **Constraints:** Touch only for children; sound is central; must work without an account for the child

---

## 1. Product type

- **Primary:** Content
- **Secondary:** Tool, for the parent area
- **Why:** The core value is authored learning content; parents manage profiles and settings
- **Key views in scope:** Journey map, exercise, reward moment, parent overview, progress, settings
- **Key flows in scope:** Choose next exercise, complete, receive reward, continue; parent checks progress and adjusts settings
- **Required states:** Sound off, child stuck or inactive, exercise failed repeatedly, time limit reached
- **Differs from the archetype:** Content is consumed by acting, not by reading

---

## 2. Experience model

- **Dominant:** Narrative
- **Supporting:** Manipulation inside exercises; Object in the parent area
- **Why:** Children follow a guided journey; exercises are hands-on; parents need a conventional overview
- **What motion must communicate:** What can be touched, what happened after a touch, and progress along the journey
- **Differs from the archetype:** The child controls pace and can replay, but cannot skip ahead

---

## 3. Visual language

- **Dominant:** Playful, for the child experience
- **Secondary:** Neutral, for the parent area
- **Why:** Children need energy and clarity; parents need a calm, familiar tool
- **Additional avoid rules for this project:** No text-only instructions in the child experience; no small touch targets
- **Differs from the archetype:** Structure is kept extremely simple under the playful surface

---

## 4. Motion language

- **Language:** Expressive
- **Scoped exceptions:** Quiet in the parent area
- **Why:** Motion carries instruction, feedback and reward for children who cannot read
- **Reduced motion approach:** Instruction and feedback are carried by sound and still illustrations; reward moments become still compositions

---

## 5. Dials

| Dial | Preset | Value | Scope | Why |
|---|---|---|---|---|
| Density | 40 | 15 | Child experience | One thing at a time, large targets |
| Density | 50 | 45 | Parent area | |
| Contrast | 65 | 70 | All | |
| Softness | 80 | 90 | Child experience | |
| Depth | 30 | 35 | Child experience | |
| Color | 85 | 90 | Child experience | |
| Warmth | 60 | 70 | All | |
| Expressivity | 85 | 85 | Child experience | |
| Motion | 75 | 80 | Child experience | Motion replaces written instruction |
| Novelty | 60 | 55 | Child experience | Capped at 30 in the parent area and settings |

---

## 6. Brand

- **Profile:** `brands/<app-brand>.md`
- **Status:** draft

| Surface | Presence |
|---|---|
| Child experience | signature |
| Parent area | quiet |

---

## Project principles

1. Every instruction works without reading.
2. Every touch gets a response.
3. Mistakes are part of play, never punished.
4. The child always knows how to continue.
5. The parent area is calm, and shows what matters in one view.

---

## Deliberate tensions

| Tension | Why | Revisit when |
|---|---|---|
| Two visual languages in one product | Children and parents have opposite needs | If parents start using the app together with the child |

---

## Open questions

- How long can a session be before it stops being helpful?
