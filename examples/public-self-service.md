---
type: recipe
project: example-public-self-service
version: 0.1
status: example
---

# Example: Public self-service

A fictional example showing how a recipe is filled in. Not a real project.

---

## Summary

A self-service product where residents apply for a public benefit, follow their case and respond to requests from case handlers. Many users are uncertain, stressed or unfamiliar with the terminology.

```text
Product:    Service (primary) + Content
Experience: Workflow (dominant) + Object (case overview)
Visual:     Neutral
Motion:     Quiet
Dials:      density 30, contrast 75, softness 40, depth 15, color 25, warmth 55, expressivity 15, motion 20, novelty 5
Brand:      <agency-brand>, presence present (information pages), quiet (application and case flows)
```

---

## Context

- **Users:** Residents of all ages and abilities, using the service a few times per year
- **Core job:** Apply, follow the case and get a decision without calling or visiting
- **Success looks like:** More completed applications; fewer support calls about case status
- **Constraints:** High accessibility requirements; several languages; must work on older phones

---

## 1. Product type

- **Primary:** Service
- **Secondary:** Content
- **Why:** The core is completing a task with an organization; users also need clear information before starting
- **Key views in scope:** Start page by need, eligibility check, application flow, case overview, messages, help and contact
- **Key flows in scope:** Check eligibility, start, save and continue later, submit; follow status, respond to requests, receive decision
- **Required states:** Not eligible, missing documents, session timeout, waiting for user, rejected, system unavailable
- **Differs from the archetype:** Many users arrive via search on a deep page, so every information page must work as an entry point

---

## 2. Experience model

- **Dominant:** Workflow
- **Supporting:** Object for the case overview
- **Why:** The process has a required order and users are unfamiliar with it
- **What motion must communicate:** Progress between steps, and what changed in the case since the last visit
- **Differs from the archetype:** None

---

## 3. Visual language

- **Dominant:** Neutral
- **Why:** Familiarity and trust matter more than distinctiveness; the task must stand out
- **Additional avoid rules for this project:** No legal or internal terminology in headings or labels
- **Differs from the archetype:** Slightly larger text and more space than the Neutral preset

---

## 4. Motion language

- **Language:** Quiet
- **Why:** Motion should support orientation without calling attention
- **Reduced motion approach:** Step changes become instant; progress is carried by the progress indicator alone

---

## 5. Dials

| Dial | Preset | Value | Scope | Why |
|---|---|---|---|---|
| Density | 50 | 30 | All | Users are infrequent and often on small screens |
| Contrast | 50 | 75 | All | High accessibility requirements |
| Softness | 35 | 40 | All | |
| Depth | 25 | 15 | All | Fewer layers reduce confusion |
| Color | 25 | 25 | All | |
| Warmth | 50 | 55 | All | Slightly warmer to feel less bureaucratic |
| Expressivity | 20 | 15 | All | |
| Motion | 30 | 20 | All | |
| Novelty | 10 | 5 | All | Conventions help users who are unsure |

---

## 6. Brand

- **Profile:** `brands/<agency-brand>.md`
- **Status:** approved

| Surface | Presence |
|---|---|
| Information pages | present |
| Application and case flows | quiet |

- **Fit with the visual language:** The agency's secondary colors fail contrast on white; they are used only for illustration, never for text or controls

---

## Project principles

1. Users know what they need before they start.
2. Users always know where their case stands, and what happens next.
3. Plain language before precise language; precision in the details, not the headings.
4. Every step can be saved and continued later.
5. Nobody needs to call to finish.

---

## Open questions

- Which documents are most often missing today, and can they be requested earlier?
