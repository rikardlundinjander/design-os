---
layer: experience
version: 0.1
status: draft
---

# Experience models

Layer 2 of the archetype system. An experience model describes **how the user engages with the product**: where their attention lives, how they move through it, who is in control and how they express intent.

Two products of the same product type can feel completely different depending on their experience model. A task manager built around a list, a board, a command bar or a conversation is the same product type with four different experiences.

---

## How it relates to product type

| Product type answers | Experience model answers |
|---|---|
| What is the product about? | Where does the user's attention live? |
| Which objects, views and flows exist? | How does the user move between them? |
| Which states must be handled? | How does the system respond to the user? |
| What is the core job? | Who drives: the user, the system, or both? |

Product type defines the parts. Experience model defines the center of gravity and how the parts are reached.

---

## How to use this file

1. **Pick one dominant model.** It decides the primary surface, the navigation structure and what the user sees most of the time.
2. **Add supporting models where needed.** Supporting models are scoped: they apply to a specific view, flow or user group. Example: an object-first tool with a command layer for experienced users and a workflow for onboarding.
3. **Check the fit against the product type.** Use the pairing table at the end of this file. Unusual pairings are allowed, and can be the source of an original product, but they should be deliberate.
4. **Answer the kickoff questions** for the dominant model.

If you cannot decide on a dominant model, answer this: *what is on screen when the user is doing the thing they came to do?* That surface is the center of gravity.

---

## What this layer owns

| This layer decides | This layer does not decide |
|---|---|
| The primary surface and center of gravity | Which objects and views exist (product type) |
| Navigation structure and wayfinding | Visual style of navigation (visual language) |
| Locus of control (user, system, shared) | Typography, color, spacing |
| Primary input and interaction patterns | How motion looks and feels (motion language) |
| Selection, focus and feedback model | Density values (density and personality) |
| What motion must communicate | Brand expression |

This layer may state *what* must be communicated, such as "the user must see where an item went". The motion and visual layers decide *how*.

---

## Schema

Every model uses the same sections.

- **Definition:** one sentence.
- **Center of gravity:** the surface where the user spends most time.
- **Mental model:** how the user thinks about the product.
- **Who drives:** user-driven, system-driven or shared.
- **Structure:** spatial, linear, hierarchical, stream or ambient.
- **Primary input:** how intent is expressed.
- **Navigation:** how the user moves and stays oriented.
- **Selection and feedback:** how focus, selection and system response work.
- **Implications for other layers:** requirements handed to visual, motion and density.
- **Works well when:** conditions where the model shines.
- **Breaks when:** conditions where it fails.
- **Anti-patterns:** common mistakes.
- **Kickoff questions:** what to ask at the start of a project.

---

## Overview

| Model | Center of gravity | Who drives | Structure |
|---|---|---|---|
| [Object](#object) | Collections and detail views | User | Hierarchical |
| [Workflow](#workflow) | The current step or stage | Shared | Linear |
| [Document](#document) | A flowing, authored surface | User | Linear |
| [Canvas](#canvas) | A freeform space | User | Spatial |
| [Manipulation](#manipulation) | One continuous thing being handled | User | Spatial |
| [Command](#command) | An input for intent | User | None (flat) |
| [Conversation](#conversation) | An ongoing exchange | Shared | Linear |
| [Feed](#feed) | A ranked stream | System | Stream |
| [Dashboard](#dashboard) | An overview of signals | System, then user | Hierarchical |
| [Narrative](#narrative) | An authored sequence | System | Linear |
| [Ambient](#ambient) | Outside the product | System | Ambient |

---

## Object

**Definition:** The experience revolves around things, collected in lists or grids, opened into detail views, and related to each other.

**Center of gravity:** A collection view and a detail view, often side by side.

**Mental model:** "I have a set of things. I find one, open it, and work on it."

**Who drives:** User.

**Structure:** Hierarchical. Collections contain objects; objects relate to other objects.

**Primary input:** Pointer or touch for browsing and selection, keyboard for navigation and editing.

**Navigation:**
- Global navigation between object types or collections
- Breadcrumbs or back paths from detail to collection
- Links between related objects

**Selection and feedback:**
- Clear single and multiple selection
- The selected object is always obvious
- Changes are reflected in the collection immediately

**Implications for other layers:**
- Visual: collection and detail must be distinguishable at a glance
- Motion: must show where an object comes from when opened and where it goes when closed, moved or deleted
- Density: collection views often need higher density than detail views

**Works well when:** There are many objects of a few types and users return to them repeatedly.

**Breaks when:** The value lies in the relationships or arrangement between objects, rather than the objects themselves.

**Anti-patterns:**
- Every object type gets its own navigation item, so the structure mirrors the database
- Detail views that lose the user's place in the collection
- Relationships that exist in data but are invisible in the interface

**Kickoff questions:**
- What are the three most important object types?
- Does the user work on one object at a time or many?
- Which relationships between objects matter to the user?

---

## Workflow

**Definition:** The experience is organized around stages, steps and progression toward completion.

**Center of gravity:** The current step, stage or task.

**Mental model:** "I am somewhere in a process, and I know what comes next."

**Who drives:** Shared. The process sets the order; the user moves it forward.

**Structure:** Linear, sometimes branching.

**Primary input:** Forms, decisions, approvals; pointer, touch and keyboard.

**Navigation:**
- Progress indicator showing where the user is and what remains
- Forward and back within the process
- Overview of all items and their stage (for multi-item workflows, such as a pipeline or a case queue)

**Selection and feedback:**
- Every action confirms what changed and what happens next
- Blocking issues are shown where they occur, not at the end
- Status is explicit: not started, in progress, waiting, done, rejected

**Implications for other layers:**
- Visual: progress and status must be readable without text
- Motion: must communicate progression and transitions between stages
- Density: individual steps are often low density; overviews of many items are high density

**Works well when:** The task has a known order, dependencies or approvals, or users are unfamiliar with the process.

**Breaks when:** Experienced users need to jump around, or the real process is less linear than the designed one.

**Anti-patterns:**
- A rigid step flow for a task that experts do in any order
- Progress indicators that lie about how much remains
- No way to save and return mid-process

**Kickoff questions:**
- Is the order required, or just recommended?
- Who else takes part in the process, and when?
- What happens if the user stops halfway?

---

## Document

**Definition:** The experience is a flowing surface where content is read or authored in sequence.

**Center of gravity:** A single, scrollable document.

**Mental model:** "I am writing or reading something from top to bottom."

**Who drives:** User.

**Structure:** Linear, with nested blocks or sections.

**Primary input:** Keyboard for writing, pointer or touch for selection and structure.

**Navigation:**
- Scroll as the primary movement
- Outline or table of contents for long documents
- Links and references between documents

**Selection and feedback:**
- Text and block selection behave predictably
- Formatting and structure are visible while writing
- Save state is always visible or automatic

**Implications for other layers:**
- Visual: typography carries the hierarchy; chrome stays out of the way
- Motion: minimal; must not interrupt writing or reading
- Density: governed by reading comfort, not by information volume

**Works well when:** The content is primarily text, or text with embedded elements, and has a natural order.

**Breaks when:** Content is better understood spatially, or consists of many small independent items.

**Anti-patterns:**
- Toolbars that take more attention than the text
- Structure (headings, blocks) that is hard to see or change
- A document model forced onto content that is really a set of records

**Kickoff questions:**
- Is the user mostly reading or mostly writing?
- How long do documents get?
- What gets embedded in the document besides text?

---

## Canvas

**Definition:** The experience is a freeform space where the user composes, arranges and connects elements.

**Center of gravity:** An open, often infinite, surface.

**Mental model:** "This is my space. Where I put things means something."

**Who drives:** User.

**Structure:** Spatial.

**Primary input:** Pointer, touch, pen and gestures; keyboard shortcuts for tools.

**Navigation:**
- Pan and zoom
- Overview or minimap for large spaces
- Jump to selection, frame or bookmark
- Layers or outline as an alternative, non-spatial way in

**Selection and feedback:**
- Direct selection, marquee selection, multi-select
- Handles and guides during manipulation
- Snapping, alignment and spacing feedback

**Implications for other layers:**
- Visual: interface chrome recedes; the canvas content dominates
- Motion: must preserve spatial continuity when zooming and navigating
- Density: chrome is compact; the canvas has no fixed density

**Works well when:** Arrangement, proximity and grouping carry meaning, and users create rather than consume.

**Breaks when:** Content has a natural order or structure that the canvas hides, or when users need to find things fast.

**Anti-patterns:**
- A canvas where a list would do
- No non-spatial way to find or reach content
- Tool panels that cover the work

**Kickoff questions:**
- Does the position of an element mean something?
- How big does a typical space get?
- How do people find things in a space they did not create?

---

## Manipulation

**Definition:** The experience centers on handling one continuous thing directly, such as a timeline, a map, a model or a configurator.

**Center of gravity:** The thing itself, with controls close to it.

**Mental model:** "I am holding it and shaping it."

**Who drives:** User.

**Structure:** Spatial or continuous (time, geography, three dimensions).

**Primary input:** Drag, scrub, pinch, rotate, resize; precise keyboard or numeric input as a complement.

**Navigation:**
- Movement within the continuous dimension (scrub time, pan a map, rotate a model)
- Zoom between overview and detail
- Reset to a known position

**Selection and feedback:**
- Immediate, continuous feedback during the gesture
- The result is visible before the gesture ends
- Precise values available when needed

**Implications for other layers:**
- Visual: the handled object dominates; controls are close to what they affect
- Motion: must feel physical and direct; latency is failure
- Density: controls can be dense; the object needs room

**Works well when:** The thing has a continuous dimension and small adjustments matter.

**Breaks when:** Tasks require exact values primarily, or users have limited motor precision and no alternative input.

**Anti-patterns:**
- Gestures without a precise, accessible alternative
- Feedback that only appears after release
- No way to undo a gesture step by step

**Kickoff questions:**
- What is the continuous dimension: time, space, value?
- How precise does the user need to be?
- What is the alternative for users who cannot drag or pinch?

---

## Command

**Definition:** The experience centers on expressing intent directly, through search, commands and keyboard.

**Center of gravity:** An input field or command palette, often available everywhere.

**Mental model:** "I say what I want, and it happens."

**Who drives:** User.

**Structure:** Flat. Everything is reachable from one place.

**Primary input:** Keyboard and typed text.

**Navigation:**
- Search and commands replace navigation hierarchies
- Recent items and suggestions reduce typing
- Visible navigation exists as a fallback, not the main path

**Selection and feedback:**
- Results update as the user types
- The selected result is obvious and actionable with one key
- Every command confirms what it did

**Implications for other layers:**
- Visual: results must be scannable at high speed
- Motion: fast and minimal; nothing may slow down input
- Density: high; experienced users expect many results in view

**Works well when:** Users are frequent, experienced and know what they want.

**Breaks when:** Users do not know what is possible, or do not know the words for it.

**Anti-patterns:**
- Commands as the only way to discover features
- Search that requires exact names
- Shortcuts that conflict with platform or assistive technology conventions

**Kickoff questions:**
- How experienced are the users, and how often do they use the product?
- Which actions are repeated most?
- How does a new user learn what they can type?

---

## Conversation

**Definition:** The experience is an ongoing exchange, between the user and an AI or between people.

**Center of gravity:** A thread of messages and an input.

**Mental model:** "I am talking to someone who understands context."

**Who drives:** Shared. The user asks; the other party responds, suggests or asks back.

**Structure:** Linear, in time.

**Primary input:** Text, voice, attachments; pointer or touch for actions on messages.

**Navigation:**
- Scrolling through the thread
- A list of threads or sessions
- Search across history
- Jumping from a message to the object it refers to

**Selection and feedback:**
- Clear indication of who is speaking and when
- Visible state while the other party is responding
- Messages can contain actions, not just text

**Implications for other layers:**
- Visual: the difference between parties must be clear; generated content must be distinguishable from user content
- Motion: must communicate waiting and arrival without distraction
- Density: governed by reading comfort

**Works well when:** The task is open-ended, context builds over time, or the user cannot easily express intent through controls.

**Breaks when:** The output is a structured object that needs editing, or the task is repeated and better served by a direct control.

**Anti-patterns:**
- A conversation as the whole interface, whatever the task
- Important results buried in scroll history
- No way to act on or edit what was produced

**Kickoff questions:**
- What does the conversation produce, and where does that output live?
- When is a control faster than a sentence?
- How does the user return to something from earlier?

---

## Feed

**Definition:** The experience is a continuous stream of items, ordered by time or by relevance.

**Center of gravity:** A scrolling stream.

**Mental model:** "I check in and see what is new."

**Who drives:** System. The product decides what comes next.

**Structure:** Stream.

**Primary input:** Scroll and swipe; tap or click to open or react.

**Navigation:**
- Scroll as the primary movement
- Tabs or filters for different streams
- Open an item and return to the same place in the stream

**Selection and feedback:**
- Reactions are immediate and reversible
- New items are signaled without moving what the user is reading
- The user can influence what they see

**Implications for other layers:**
- Visual: items must be recognizable and scannable in isolation
- Motion: must never shift content under the user's attention
- Density: consistent item rhythm matters more than absolute density

**Works well when:** Content is abundant, frequently updated and consumed in short sessions.

**Breaks when:** Users need to find a specific item, finish something, or trust that they have seen everything important.

**Anti-patterns:**
- Losing the user's position when they return
- No end, no summary, no sense of being done
- Ranking the user cannot understand or influence

**Kickoff questions:**
- What makes an item worth showing now?
- Should the user be able to reach the end?
- How does the user control what they see?

---

## Dashboard

**Definition:** The experience starts with an overview of signals, then lets the user drill into detail.

**Center of gravity:** An overview of key indicators.

**Mental model:** "Show me what matters, then let me dig in."

**Who drives:** System first (what to highlight), then user (where to dig).

**Structure:** Hierarchical: overview, segment, detail.

**Primary input:** Pointer or touch for filtering and drilling down; keyboard for power users.

**Navigation:**
- Overview as home
- Drill-down from any signal to its detail
- Filters and time ranges that persist across views
- A clear path back to the overview

**Selection and feedback:**
- Hover or tap reveals exact values
- Filters show clearly what is currently applied
- Changes and anomalies are signaled, not just displayed

**Implications for other layers:**
- Visual: hierarchy between primary and secondary signals must be strong
- Motion: must connect overview and detail; data updates must not distract
- Density: high in detail views; overview density depends on how many signals truly matter

**Works well when:** Users monitor something regularly and need to spot change fast.

**Breaks when:** There is no clear answer to what matters most, so the overview shows everything.

**Anti-patterns:**
- Every metric given equal weight
- Drill-down that loses the filter context
- Overviews that look informative but support no decision

**Kickoff questions:**
- What should the user notice within five seconds?
- What do they do after noticing it?
- Which filters are global and which are local?

---

## Narrative

**Definition:** The experience is an authored sequence that the user moves through, with the product setting the order and pace.

**Center of gravity:** The current moment in the story.

**Mental model:** "I am being taken through something."

**Who drives:** System. The user controls pace, not order.

**Structure:** Linear, sometimes with chapters or branches.

**Primary input:** Scroll, swipe, tap to continue; sometimes sound or gesture.

**Navigation:**
- Forward movement as the default
- Chapter overview or progress for orientation
- A way to skip, return or leave at any time

**Selection and feedback:**
- The user always knows how to continue
- Progress is visible
- Interactive moments are clearly signaled

**Implications for other layers:**
- Visual: composition changes with the story; each moment has one focus
- Motion: carries the story; transitions are part of the content
- Density: low; one idea at a time

**Works well when:** The goal is understanding, persuasion or emotional impact, and the order matters.

**Breaks when:** Users arrive with a specific question, or return to find one piece of information.

**Anti-patterns:**
- Forcing a sequence on content people want to scan
- Scroll behavior that fights the user's input
- No way to see the whole or skip ahead

**Kickoff questions:**
- What must the user understand or feel at the end?
- What happens when someone arrives in the middle?
- How long is the whole sequence?

---

## Ambient

**Definition:** The experience happens mostly outside the product, through notifications, widgets, glances, background tasks or other surfaces.

**Center of gravity:** Wherever the user already is.

**Mental model:** "It takes care of things and tells me when it matters."

**Who drives:** System. The user sets rules and responds.

**Structure:** Ambient. Brief touchpoints rather than sessions.

**Primary input:** Glance, tap, quick reply, voice; configuration in a traditional interface.

**Navigation:**
- From a touchpoint directly to the relevant detail
- A home or log where the user can review what happened
- Settings for what the product should handle and when to interrupt

**Selection and feedback:**
- Every interruption must earn its place
- Actions can be completed from the touchpoint
- The user can always see what the product did on their behalf

**Implications for other layers:**
- Visual: must work in very small, foreign contexts (lock screens, widgets, other apps)
- Motion: minimal and recognizable
- Density: extreme compression; one message per touchpoint

**Works well when:** The product monitors or acts on the user's behalf, and the best experience is not having to open it.

**Breaks when:** The user does not trust what happens in the background, or interruptions outweigh the value.

**Anti-patterns:**
- Notifications used for engagement rather than value
- Background actions without a log or undo
- No way to tune how often the product interrupts

**Kickoff questions:**
- When is it worth interrupting the user?
- What can the user do without opening the product?
- How does the user review and correct what the product did?

---

## Pairings with product types

Typical dominant models per product type. Bold marks the most common dominant model. Other combinations are possible and can be deliberate sources of originality.

| Product type | Common dominant models | Common supporting models |
|---|---|---|
| Tool | **Object**, Document, Canvas, Workflow | Command, Conversation |
| Content | **Document**, Narrative, Feed | Command (search) |
| Commerce | **Object**, Feed | Workflow (checkout), Conversation |
| Service | **Workflow** | Object (cases), Conversation (help) |
| Community | **Feed**, Conversation | Object (profiles, groups) |
| Data | **Dashboard**, Object | Command, Conversation |
| AI-native | **Conversation**, Document, Canvas | Workflow (approvals), Ambient |
| Utility | **Command**, Manipulation | Ambient |
| Immersive | **Narrative**, Manipulation, Canvas | Ambient (sound, presence) |

---

## Combining models

- **One model dominates.** It owns the primary surface and the default navigation.
- **Supporting models are scoped.** State where each applies: a view, a flow or a user group.
- **Models may change with experience.** A product can start in Workflow for new users and settle into Object or Command for experienced ones. Design the transition, do not leave it to chance.
- **Avoid two competing dominant models.** If two surfaces both claim to be home, the user has no stable place to return to.

Written as a line in a project definition:

```text
Experience: Object (dominant) + Command (experienced users) + Workflow (onboarding)
```

---

## Contributing

- Keep every model in the schema above.
- Describe behavior and structure, never visual style or platform.
- Add a new model only when a product cannot be described as a dominant model with supporting ones.
- When a model hands requirements to another layer, write what must be communicated, not how it should look or move.
