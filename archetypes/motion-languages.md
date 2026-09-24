---
layer: motion
version: 0.2
status: draft
---

# Motion languages

Layer 4 of the archetype system. A motion language describes **the role and character of motion**: what motion is used for, how it feels, and where it is deliberately absent.

Motion is not decoration. It explains what happened, where things went, what caused what and what matters now. A motion language decides how much of that explanation is carried by movement, and with what character.

A motion language does not set durations or curves. Specific timing and behavior grow in the actual product, where motion can be seen and felt, and are recorded there once they settle (see [Timing grows in the product](#timing-grows-in-the-product)).

---

## How it relates to other layers

| Layer | Contributes to motion |
|---|---|
| Product type | Which states and transitions exist |
| Experience model | **What** motion must communicate, such as "show where the object went" |
| Visual language | The character motion must fit, such as restrained or expressive |
| **Motion language** | **How** it is communicated: the role motion plays and its character |
| Density and personality | How much motion, via the motion dial |
| Brand | Signature moments, such as a logo animation or a characteristic curve |

The experience model hands over requirements. The motion language fulfills them. Two products with the same requirement, "show that the item was saved", can answer it with a quick color change or a choreographed confirmation. Both are correct within their language.

---

## How to use this file

1. **Pick one motion language.** Unlike other layers, motion rarely benefits from a secondary language. If needed, scope it tightly, for example "Cinematic on the landing experience only".
2. **List the motion requirements from the experience model.** Each dominant and supporting model states what motion must communicate.
3. **Use the moments table** to see how the chosen language handles common moments.
4. **Write the role and character into the recipe,** not values. Durations and curves are found in the product.
5. **Define reduced motion behavior** before anything else is animated.

If you cannot decide, answer this: *when the user does something, should they feel the product respond, or just see the result?* Feeling points toward Responsive, Physical or Expressive. Seeing points toward Still or Quiet.

---

## What this layer owns

| This layer decides | This layer does not decide |
|---|---|
| Role: which purposes motion serves | What must be communicated (experience model) |
| Character: tempo, easing, distance and choreography, described in words | Visual style of what moves (visual language) |
| Interruptibility and gesture continuity | Amount of motion overall (motion dial) |
| Reduced motion behavior | Signature brand animations (brand) |
| Where motion is deliberately absent | Which states exist (product type) |
| | Specific durations and curves (the product) |

---

## Purposes of motion

Every animation should serve at least one purpose. If it serves none, remove it.

| Purpose | What it does | Example |
|---|---|---|
| **Feedback** | Confirms that input was received | A button responds when pressed |
| **Continuity** | Shows where something came from and went | A list item expands into its detail view |
| **Causality** | Shows what caused a change | A filter is applied and the results reorder |
| **State** | Makes a change of state visible | A toggle moves from off to on |
| **Attention** | Draws the eye to what matters now | A new message arrives |
| **Hierarchy** | Reveals order of importance through sequence | The primary element arrives first |
| **Character** | Expresses the personality of the product | A distinctive way a panel settles |

Motion languages differ mostly in which purposes they use, and how strongly.

---

## Vocabulary

Shared terms used throughout this file.

**Tempo:** words for how quickly motion completes, relative to each other.

| Tempo | Feels like | Typical use |
|---|---|---|
| Instant | No perceptible wait | Feedback on press, hover, focus |
| Fast | Noticed, but never waited for | Small state changes, toggles, small elements |
| Moderate | A clear, unhurried movement | Overlays, panels, list changes |
| Slow | A deliberate transition | View transitions, large elements |
| Extended | A moment in itself | Narrative moments, orchestrated sequences |

Larger elements and longer distances need more time. Frequently repeated motion needs less.

**Easing:**
- **Decelerate:** starts fast, ends gently. For elements entering.
- **Accelerate:** starts gently, ends fast. For elements leaving.
- **Standard:** gentle at both ends. For elements moving within the view.
- **Linear:** constant speed. Only for continuous motion such as progress or rotation.
- **Spring:** defined by stiffness and damping instead of duration. Can overshoot and settle. Handles interruption naturally.

**Choreography:**
- **Simultaneous:** everything moves together.
- **Sequenced:** one element after another.
- **Staggered:** a group moves with small, even offsets.
- **Led:** one element moves first and the rest follow its path.

**Physicality:**
- **Interruptible:** a new input can take over a running animation without waiting.
- **Gesture continuity:** motion follows the finger or pointer, and continues with its momentum on release.
- **Momentum:** movement carries speed and slows naturally.

---

## Non-negotiables

No motion language overrides these.

- Respect the user's reduced motion preference. Replace movement with fades or instant changes; never remove the information motion carried.
- Motion never blocks input. The user can act before an animation finishes.
- No information is conveyed by motion alone.
- Nothing flashes more than three times per second.
- Large movements across the view, parallax and zooming backgrounds are reduced or removed under reduced motion.
- Looping or autoplaying motion can be paused.
- Motion never delays the user in a repeated task. If an animation is seen a hundred times a day, it must be nearly instant.

---

## The generic default

Without direction, generated interfaces tend toward the same motion. Name it, so it becomes a choice rather than an accident.

**Signs of the generic default:**
- Every element fades and slides up when scrolled into view
- One duration and one ease used for everything
- Cards that scale up on hover
- Staggered entrance of every list on every page load
- Bouncy springs on elements that should feel stable
- Shimmering skeletons for content that loads in a few hundred milliseconds
- Motion added because it is possible, not because it explains anything

Each motion language below includes an avoid list that moves away from this default in its own direction.

---

## Schema

Every motion language uses the same sections. Role says what motion is for; tempo, easing, distance and choreography describe its character, in words rather than values.

- **Definition:** one sentence.
- **Feels like:** three words.
- **Role:** which purposes of motion it relies on.
- **Tempo:** how quickly motion completes, from the tempo vocabulary.
- **Easing:** the kind of acceleration or physical behavior.
- **Distance and scale:** how far and how much things move.
- **Choreography:** how multiple movements relate.
- **Where motion appears:** and where it is deliberately absent.
- **Principles:** rules that can be followed by people and AI.
- **Avoid:** what breaks the language.
- **Reduced motion:** how the language degrades.
- **Fits well with:** visual languages and experience models.
- **Risks:** where the language fails.

---

## Overview

| Language | Role | Tempo | Physicality | Character |
|---|---|---|---|---|
| [Still](#still) | State | Instant | None | Absent |
| [Quiet](#quiet) | Feedback, state, continuity | Fast | Low | Subtle |
| [Responsive](#responsive) | Feedback, causality | Instant to fast | Medium | Direct |
| [Physical](#physical) | Continuity, feedback | Spring-based | High | Tactile |
| [Expressive](#expressive) | Character, hierarchy, attention | Moderate | Medium | Signature |
| [Cinematic](#cinematic) | Continuity, hierarchy, character | Slow to extended | Low to medium | Atmospheric |

---

## Still

**Definition:** Motion is almost entirely absent. Changes happen instantly, and state is carried by form and color.

**Feels like:** Immediate, stable, uncompromising.

**Role:** State, carried visually rather than through movement.

**Tempo:** Instant. Where transitions exist, they are very short fades.

**Easing:** Not relevant for most elements. Short linear or standard fades where needed.

**Distance and scale:** None. Elements do not travel.

**Choreography:** Simultaneous. Everything changes at once.

**Where motion appears:** Only where the absence of motion would cause confusion, such as progress indicators and loading states. Nowhere else.

**Principles:**
- A change should be visible in the result, not in the transition.
- If orientation is lost without motion, fix the layout, not the timing.
- Progress and loading are the only continuous motion allowed.

**Avoid:**
- Hover and entrance effects
- Transitions added to soften abrupt changes that are better solved by layout
- Loading animations that call attention to themselves

**Reduced motion:** Already compliant. No change needed.

**Fits well with:** Brutalist, Precision, Neutral. Command, Document, Dashboard.

**Risks:** Spatial relationships can be lost when views change. Can feel abrupt or unfinished if the visual language relies on softness.

---

## Quiet

**Definition:** Subtle, functional motion that supports understanding without being noticed.

**Feels like:** Calm, smooth, unobtrusive.

**Role:** Feedback, state and continuity.

**Tempo:** Fast for most changes; moderate for overlays and panels.

**Easing:** Standard, decelerate for entering, accelerate for leaving. No overshoot.

**Distance and scale:** Short distances. Small offsets, small scale changes.

**Choreography:** Mostly simultaneous. Light sequencing only when order matters.

**Where motion appears:** State changes, overlays, list changes, view transitions. Absent from scroll, decorative elements and repeated micro-interactions.

**Principles:**
- The user should notice what changed, not that it moved.
- Use short distances; elements move just enough to show direction.
- Entering is slightly slower than leaving.

**Avoid:**
- Overshoot and bounce
- Scroll-triggered entrances
- Motion on elements the user did not interact with
- Long durations on frequently repeated actions

**Reduced motion:** Replace movement with fades of the same duration.

**Fits well with:** Neutral, Refined, Editorial, Warm. Object, Workflow, Document, Service.

**Risks:** Can become invisible to the point of losing continuity in complex transitions. Easily drifts into the generic default if one duration is applied to everything.

---

## Responsive

**Definition:** Fast, direct motion that makes the product feel immediate and in the user's hands.

**Feels like:** Snappy, precise, alive.

**Role:** Feedback and causality.

**Tempo:** Instant for feedback, fast for everything else. Nothing slow.

**Easing:** Sharp decelerate. Short, stiff springs with little or no overshoot.

**Distance and scale:** Short and precise. Small scale changes on press.

**Choreography:** Simultaneous or tightly led. Cause first, effect immediately after.

**Where motion appears:** Every direct interaction: press, drag, select, toggle, reorder. Absent from ambient or decorative contexts.

**Principles:**
- Response begins within the first frame of input.
- Every action has a visible, immediate reaction.
- The cause always moves first; the effect follows.
- Everything can be interrupted.

**Avoid:**
- A slow tempo on anything
- Waiting for an animation to finish before accepting new input
- Soft, floaty easing
- Motion that happens without user input

**Reduced motion:** Keep instant feedback such as color and opacity; remove travel and scale.

**Fits well with:** Precision, Neutral, Graphic. Command, Object, Canvas, Utility.

**Risks:** Can feel nervous if too many elements react at once. Needs careful performance work; any lag breaks the language.

---

## Physical

**Definition:** Motion that behaves like material objects, with springs, momentum and continuity with the user's gestures.

**Feels like:** Tactile, weighty, natural.

**Role:** Continuity and feedback.

**Tempo:** Defined by springs rather than fixed durations. Fast to settle, with natural variation.

**Easing:** Springs with moderate stiffness and damping. Slight overshoot allowed where it matches the material.

**Distance and scale:** Follows the gesture. Distance is whatever the user moved plus momentum.

**Choreography:** Led by the element the user touches. Related elements follow with slight delay, as if connected.

**Where motion appears:** Gestures, drag, swipe, pull, dismiss, scroll edges, sheets and panels. Absent from purely informational changes.

**Principles:**
- Motion follows input directly; nothing moves on its own path during a gesture.
- Release carries momentum.
- Every movement can be caught and reversed mid-flight.
- Objects have consistent weight: heavy things move slower than light things.

**Avoid:**
- Fixed-duration animations on gesture-driven elements
- Overshoot on elements that should feel stable, such as text and navigation
- Physics that differs between similar objects
- Gestures without a non-gesture alternative

**Reduced motion:** Keep gesture following, since it is input, not animation. Remove overshoot and momentum on release; settle directly.

**Fits well with:** Warm, Playful, Cinematic, Neutral. Manipulation, Canvas, Feed.

**Risks:** Hard to implement consistently across platforms. Springs can feel sluggish if tuned too soft. Poor fit for dense, keyboard-driven work.

---

## Expressive

**Definition:** Motion as part of the identity, with signature movements and choreography that make the product recognizable.

**Feels like:** Distinctive, confident, memorable.

**Role:** Character, hierarchy and attention.

**Tempo:** Moderate, with contrast between fast and slow for emphasis.

**Easing:** Custom curves used consistently as a signature. Overshoot and anticipation allowed where they fit the character.

**Distance and scale:** Medium to large for key moments; small for routine interactions.

**Choreography:** Sequenced and staggered. The order of arrival expresses hierarchy.

**Where motion appears:** Key moments: first run, success, empty states, transitions between major sections, brand moments. Routine, repeated interactions stay quiet.

**Principles:**
- Choose a small set of signature movements and use them consistently.
- Expression is concentrated in key moments, not spread across everything.
- Sequence expresses importance: what matters arrives first.
- Repeated interactions stay fast, even in an expressive product.

**Avoid:**
- Expressive motion on actions repeated many times a day
- A different effect for every element
- Choreography that delays access to content
- Borrowed effects that do not belong to the product's character

**Reduced motion:** Keep the sequence and timing as fades; remove travel, scale and overshoot. Signature moments may become still compositions.

**Fits well with:** Playful, Graphic, Warm, Editorial. Feed, Narrative, Conversation.

**Risks:** Tiring if overused. Easily delays the user. Signature motion becomes generic if it is not specific to the product.

---

## Cinematic

**Definition:** Motion that creates atmosphere and narrative, with long transitions, depth and camera-like movement.

**Feels like:** Immersive, dramatic, deliberate.

**Role:** Continuity, hierarchy and character.

**Tempo:** Slow to extended. Pacing matters as much as speed.

**Easing:** Long, smooth decelerate. Camera-like ease in and out. Rarely overshoot.

**Distance and scale:** Large. Full-view transitions, zoom, depth, parallax.

**Choreography:** Directed like a scene. One lead movement, supporting layers moving at different speeds.

**Where motion appears:** Transitions between scenes, chapters or major views; scroll-driven storytelling; imagery and background layers. Interface controls stay stable and fast.

**Principles:**
- Motion tells the story; every transition has a narrative reason.
- One lead movement per moment.
- Controls never move with the scene; the user always has a stable way to act.
- Pacing is designed, including stillness between movements.

**Avoid:**
- Long transitions on repeated tasks
- Scroll hijacking that fights the user's input
- Parallax and depth without reduced motion alternatives
- Atmosphere that hides content or the way forward

**Reduced motion:** Replace scene transitions with crossfades. Remove parallax, zoom and depth movement. Keep pacing through sequence rather than travel.

**Fits well with:** Cinematic, Refined, Editorial, Graphic. Narrative, Manipulation, Immersive.

**Risks:** Slow for anyone with a task. Performance-heavy. High risk of motion sickness without reduced motion handling.

---

## Moments

How each language typically handles common moments. Use this as a starting point, then adjust per project.

| Moment | Still | Quiet | Responsive | Physical | Expressive | Cinematic |
|---|---|---|---|---|---|---|
| Press / hover | Color change | Subtle color or opacity | Immediate press response | Press follows input | Signature response | Controls stay responsive and simple |
| Toggle / select | Instant switch | Short slide | Snappy slide | Spring into place | Characterful switch | Simple, fast |
| Open overlay | Appears | Fade and short rise | Quick scale from origin | Sheet follows gesture | Choreographed entry | Scene-like reveal |
| View transition | Instant | Short crossfade | Quick directional slide | Continuous from gesture | Sequenced arrival | Camera-like move |
| Item added / removed | Instant | Short height and fade | Immediate reflow | Items make room physically | Staggered reflow | Rarely used |
| Loading | Static indicator | Subtle progress | Minimal progress | Progress with weight | Branded loading moment | Atmospheric hold |
| Success | Static confirmation | Quiet confirmation | Immediate check | Settling confirmation | Celebratory moment | Narrative beat |
| Error | Static message | Message appears | Short shake or highlight | Resistance, pull back | Clear, characterful signal | Stable message, no drama |
| Scroll | Native | Native | Native | Native with momentum | Occasional reveal on key sections | Scroll-linked scenes |

---

## Pairings

**With visual languages:**

| Visual language | Common motion languages |
|---|---|
| Neutral | Quiet, Responsive, Still |
| Editorial | Quiet, Still, Cinematic |
| Precision | Responsive, Still |
| Warm | Quiet, Physical, Expressive |
| Refined | Quiet, Cinematic |
| Playful | Expressive, Physical |
| Graphic | Expressive, Responsive |
| Brutalist | Still, Responsive |
| Cinematic | Cinematic, Physical |

**With experience models:**

| Experience model | Common motion languages |
|---|---|
| Object | Quiet, Responsive |
| Workflow | Quiet |
| Document | Still, Quiet |
| Canvas | Responsive, Physical |
| Manipulation | Physical, Responsive |
| Command | Responsive, Still |
| Conversation | Quiet, Expressive |
| Feed | Physical, Quiet |
| Dashboard | Quiet, Still |
| Narrative | Cinematic, Expressive |
| Ambient | Quiet, Still |

---

## Combining and scoping

- **One motion language governs the product.** Motion that changes character between views feels inconsistent faster than any other layer.
- **Scope exceptions tightly.** A Cinematic onboarding in an otherwise Quiet product is fine if it is clearly a separate moment.
- **Frequency beats language.** Whatever the language, motion on actions repeated many times a day is shortened toward instant.
- **Controls stay stable.** In every language, the elements the user acts with respond quickly, even when content or scenes move slowly.

Written as a line in a project definition:

```text
Motion: Quiet (product) + Cinematic (onboarding only)
```

---

## Timing grows in the product

The motion language describes what motion is for and how it should feel. The specific durations, curves and springs are found by building and trying them.

1. **Start from the character.** Build the first version from the language's tempo, easing and choreography, and from the moments table.
2. **Judge it in use.** Motion can only be evaluated in the running product: repeated, interrupted, on real content and on slower devices.
3. **Record what settles.** When a duration or a curve holds up across several moments, record it in the project, as part of its design system or in the recipe. Those values belong to the product, not to the archetype.
4. **Keep the words as the test.** A settled value is right when the motion still reads as the language describes it. If it does not, change the value, not the language.

---

## Contributing

- Keep every language in the schema above.
- Describe role and character in words. Do not add durations, curves or other values; they belong to each product.
- Never refer to a specific animation library or platform API.
- Every language needs an avoid list and a reduced motion section.
- Add a new language only when a direction cannot be described as an existing language with a different motion dial or a brand signature.
