---
type: recipe
project: example-monitoring-terminal
version: 0.1
status: example
---

# Example: Monitoring terminal

A fictional example showing how a recipe is filled in. Not a real project.

---

## Summary

A monitoring tool for operators who watch many live systems at once and must react to changes within seconds. Speed of reading and acting matters more than first impressions.

```text
Product:    Data (primary) + Tool
Experience: Dashboard (dominant) + Command (experienced users) + Object (incident detail)
Visual:     Precision
Motion:     Responsive
Dials:      density 90, contrast 80, softness 5, depth 5, color 30, warmth 25, expressivity 10, motion 15, novelty 15
Brand:      provisional minimum viable brand, presence quiet (product)
```

---

## Context

- **Users:** Trained operators, using the product for full shifts, every day
- **Core job:** Notice abnormal behavior, find the cause and act
- **Success looks like:** Shorter time from anomaly to action; fewer missed alerts
- **Constraints:** Large and multiple screens; keyboard-heavy use; long sessions

---

## 1. Product type

- **Primary:** Data
- **Secondary:** Tool
- **Why:** The core is monitoring and understanding live data; operators also create and manage incidents
- **Key views in scope:** Overview dashboard, system detail, incident list, incident detail, alert configuration
- **Key flows in scope:** Scan, spot change, drill down, find cause; create incident, assign, resolve; set up and tune alerts
- **Required states:** Partial or delayed data, data errors, no results for a filter, very large result sets, conflicting edits on an incident
- **Differs from the archetype:** Data must be live; stale data is a critical state, not an edge case

---

## 2. Experience model

- **Dominant:** Dashboard
- **Supporting:** Command for experienced users across all views; Object for incidents
- **Why:** Operators need an overview first, then fast drill-down; experts navigate by keyboard
- **What motion must communicate:** Which values changed, where a drilled-down view came from, when data is stale
- **Differs from the archetype:** The overview is never left for long; detail opens beside it, not instead of it

---

## 3. Visual language

- **Dominant:** Precision
- **Why:** High density, exact values and functional color are the core needs
- **Additional avoid rules for this project:** No color used for decoration anywhere, because color is reserved for status
- **Differs from the archetype:** None

---

## 4. Motion language

- **Language:** Responsive
- **Why:** Actions must feel immediate; motion is used to signal change, not to decorate
- **Reduced motion approach:** Value changes are signaled by a brief highlight in place, with no movement

---

## 5. Dials

| Dial | Preset | Value | Scope | Why |
|---|---|---|---|---|
| Density | 80 | 90 | All | Many systems must fit on one screen |
| Contrast | 70 | 80 | All | Status must be readable at a glance, across a room |
| Softness | 10 | 5 | All | |
| Depth | 10 | 5 | All | Overlays are rare; everything sits on one plane |
| Color | 20 | 30 | All | Several status levels need distinct colors |
| Warmth | 35 | 25 | All | |
| Expressivity | 15 | 10 | All | |
| Motion | 25 | 15 | All | Motion only for change and feedback |
| Novelty | 15 | 15 | All | |

---

## 6. Brand

- **Profile:** Minimum viable brand
- **Status:** provisional

| Surface | Presence |
|---|---|
| Product | quiet |

---

## Project principles

1. Status is always readable without interaction.
2. Color means status, and nothing else.
3. Every view can be operated by keyboard alone.
4. Stale data is shown as stale, never as current.

---

## Open questions

- How many status levels do operators actually distinguish in practice?
