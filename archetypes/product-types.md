---
layer: product
version: 0.1
status: draft
---

# Product types

Layer 1 of the archetype system. A product type describes **what the product is**: its core job, its objects, its views, its flows and the states it must handle. It says nothing about how the product looks, moves or sounds. Those decisions belong to other layers.

Use this file at the start of a project, before any visual work, to establish the structural needs of the product.

---

## How to use this file

1. **Pick one primary type.** Every product has exactly one. It decides the information architecture and what the default view is.
2. **Add up to two secondary types.** Most real products are hybrids. Secondary types add objects, views or flows, but they do not change the core structure.
3. **Copy the relevant sections into the project.** Views, flows and required states become the first checklist for the project scope.
4. **Answer the kickoff questions.** They expose where the project differs from the archetype. Those differences are usually where the interesting design work is.

If you cannot decide on a primary type, answer this: *what does the user do in the first ten seconds of a typical session?* The answer usually points to the primary type.

---

## What this layer owns

| This layer decides | This layer does not decide |
|---|---|
| Core objects and their relationships | Layout style, grid, spacing |
| Which views exist | Typography, color, radius |
| Primary and secondary flows | Navigation pattern (see interaction layer) |
| Required states (empty, loading, error, etc.) | Motion and transitions |
| Structural needs (search, permissions, history) | Brand expression |
| What success means for the user | Density and personality |

Keep this boundary strict. If a line in a product type starts describing appearance, move it to another layer.

---

## Schema

Every product type uses the same sections, so types can be compared and combined.

- **Definition:** one sentence.
- **Core job:** what the user is trying to get done.
- **Recognize it by:** signals that a product belongs to this type.
- **Core objects:** the things the product is about.
- **Key views:** the views almost every product of this type needs.
- **Key flows:** the paths users take through those views.
- **Required states:** states that must be designed, not left to chance.
- **Structural needs:** capabilities the architecture must support.
- **What good looks like:** how to judge whether the structure works.
- **Common failure modes:** what typically goes wrong.
- **Kickoff questions:** what to ask at the start of a project.
- **Often combined with:** typical secondary types.

---

## Overview

| Type | Core job | Session shape |
|---|---|---|
| [Tool](#tool) | Get work done | Long, repeated, focused |
| [Content](#content) | Understand or be inspired | Linear, reading or viewing |
| [Commerce](#commerce) | Find and buy | Funnel, decision-driven |
| [Service](#service) | Complete a task with an organization | Short, goal-driven, infrequent |
| [Community](#community) | Connect and participate | Frequent, social, open-ended |
| [Data](#data) | Monitor and understand | Scan, then drill down |
| [AI-native](#ai-native) | Delegate or co-create with AI | Iterative, conversational |
| [Utility](#utility) | Do one thing quickly | Very short, single-purpose |
| [Immersive](#immersive) | Experience something | Nonlinear, exploratory |

---

## Tool

**Definition:** A product people use to create, manage or process their own work.

**Core job:** Get a recurring task done efficiently, with control and confidence.

**Recognize it by:**
- Users return daily or weekly and build habits in it
- Users create, edit and organize their own objects
- Efficiency for experienced users matters as much as ease for new ones

**Core objects:** Workspaces, projects, documents or records, items within them, users, teams, settings.

**Key views:**
- Home or overview of the user's work
- List or collection view (with sorting and filtering)
- Object detail and editor
- Settings (personal, workspace, billing)
- Onboarding and first-run

**Key flows:**
- Create, edit, save, delete an object
- Find an existing object (search, browse, recent)
- Organize (group, tag, move, archive)
- Collaborate (invite, share, comment, assign)
- Import and export

**Required states:**
- First-run empty state (no content yet)
- Filtered empty state (no results)
- Unsaved changes, saving, saved, save failed
- Conflict (two people editing the same thing)
- Permission denied, read-only
- Bulk selection

**Structural needs:** Search, undo, permissions and roles, keyboard access, history or versioning, notifications, bulk actions.

**What good looks like:** Common tasks take few steps. Experienced users get faster over time. The user always knows whether their work is saved.

**Common failure modes:**
- Designed for the demo, not for the hundredth use
- Settings become a dumping ground for unresolved decisions
- Empty states treated as an afterthought, so onboarding fails
- No clear model for what is shared and what is private

**Kickoff questions:**
- What is the single most repeated task?
- How does a new user differ from a user in their sixth month?
- Who else sees or touches the user's work?
- What happens when something goes wrong: can it be undone?

**Often combined with:** AI-native, Data, Community.

---

## Content

**Definition:** A product whose main value is content that people read, watch or listen to.

**Core job:** Understand something, be inspired, or be convinced.

**Recognize it by:**
- Most users consume rather than create
- The content is authored and curated, not user-generated
- Storytelling, sequence and hierarchy matter

**Core objects:** Articles, stories, pages, media, authors, topics, collections.

**Key views:**
- Front page or landing
- Article or story view
- Topic, category or collection view
- Search results
- Author or source view

**Key flows:**
- Arrive (often from outside, via search or a shared link), read, continue to related content
- Browse by topic
- Search for something specific
- Share or save for later
- Convert (subscribe, sign up, contact, apply)

**Required states:**
- Arrival on a deep page without context
- Long-form reading progress
- Paywalled or gated content
- Missing or broken media
- Outdated content

**Structural needs:** Content model and CMS structure, search, metadata for sharing and search engines, related content logic, accessibility of media (captions, alt text).

**What good looks like:** Every page works as an entry point. The next step is always clear. The content model supports how editors actually publish.

**Common failure modes:**
- Front page designed, but article pages neglected (where most traffic lands)
- Content model too rigid for editors, or too loose to stay consistent
- Conversion goals crowd out the content itself

**Kickoff questions:**
- Where do most visitors arrive, and from where?
- Who produces the content, how often, and with what tools?
- What should a visitor do after reading?
- How long must content stay relevant?

**Often combined with:** Commerce, Community, Immersive.

---

## Commerce

**Definition:** A product where users discover, evaluate and buy products or services.

**Core job:** Find the right thing and buy it with confidence.

**Recognize it by:**
- There is a catalog and a checkout
- Decisions depend on comparison, trust and price
- Conversion is the primary business metric

**Core objects:** Products, variants, categories, prices, cart, orders, customers, reviews, inventory.

**Key views:**
- Start or campaign page
- Category or listing page
- Product detail page
- Cart
- Checkout
- Order confirmation and order history
- Account

**Key flows:**
- Browse or search, filter, compare, choose
- Choose variant, add to cart, check out, pay
- Track order, return, get support
- Return and reorder

**Required states:**
- Out of stock, low stock, back in stock
- Price changes, discounts, invalid codes
- Payment failed, address invalid
- Empty cart, abandoned cart
- Guest versus signed-in

**Structural needs:** Search and faceted filtering, product data model with variants, payment integration, inventory, localization of price, tax and shipping, order management.

**What good looks like:** The path from intent to purchase is short. Product pages answer the questions that block a decision. Checkout never surprises the user.

**Common failure modes:**
- Filtering that reflects the internal catalog rather than how customers think
- Checkout surprises (shipping cost, forced account creation)
- Product detail pages that lack the information needed to decide

**Kickoff questions:**
- How do customers decide: by browsing, by searching, or by recommendation?
- What blocks a purchase today?
- How many products and variants, and how often do they change?
- What happens after the purchase?

**Often combined with:** Content, Community (marketplaces, reviews).

---

## Service

**Definition:** A product that lets people complete a task with an organization, such as applying, booking, reporting, managing an account or checking a status.

**Core job:** Get something done with the organization, without calling or visiting.

**Recognize it by:**
- Usage is infrequent and goal-driven
- There are processes behind the interface (case handling, approvals, systems of record)
- Users are often stressed, uncertain or unfamiliar with terminology

**Core objects:** Cases, applications, bookings, accounts, documents, messages, deadlines.

**Key views:**
- Start page organized by user need, not by organization structure
- Form or step-by-step flow
- Status or case overview
- Messages and notifications
- Account and personal details
- Help and contact

**Key flows:**
- Find the right service, check eligibility, start, complete, submit
- Save progress and continue later
- Follow status, respond to requests, receive decision
- Change or cancel an existing booking or case

**Required states:**
- Not eligible
- Missing documents or information
- Session timeout
- Submitted, in progress, waiting for user, completed, rejected
- System unavailable

**Structural needs:** Identity and authentication, form logic with validation and branching, save and resume, integration with back-office systems, accessibility at a high standard, plain language.

**What good looks like:** Users understand what is needed before they start. They always know where their case stands. Few users need to contact support to finish.

**Common failure modes:**
- Structure mirrors the organization chart instead of user needs
- Long forms without progress or save
- Status that says "in progress" and nothing else
- Legal or internal terminology exposed to users

**Kickoff questions:**
- What makes users contact support today?
- Which back-office steps affect what the user sees?
- What must the user have ready before starting?
- Who is excluded by the current solution?

**Often combined with:** Content, Tool (for internal case handlers).

---

## Community

**Definition:** A product where the main value is created by users interacting with each other.

**Core job:** Connect, share, participate and belong.

**Recognize it by:**
- Most content is user-generated
- The product gets better as more people use it
- Identity, reputation and relationships matter

**Core objects:** Users, profiles, posts, comments, reactions, groups, messages, notifications.

**Key views:**
- Feed or activity stream
- Post or thread view
- Profile
- Group or space
- Messages
- Notifications
- Create or compose

**Key flows:**
- Sign up, set up profile, find people or groups to follow
- Consume, react, comment, share
- Create and publish
- Message privately
- Report, block, moderate

**Required states:**
- New user with an empty network
- Deleted or removed content
- Blocked or muted users
- Private versus public content
- Moderation pending

**Structural needs:** Identity and profiles, social graph, ranking or ordering logic, notifications, moderation tools, privacy settings, reporting.

**What good looks like:** New users find value before they have a network. Contributing feels safe. Moderation scales with growth.

**Common failure modes:**
- The empty network problem is not solved, so new users leave
- Moderation and safety designed after launch
- Notification systems that optimize for engagement over value

**Kickoff questions:**
- Why would the first hundred users come, before there is a community?
- What behavior do we want to encourage, and what must we prevent?
- What is public, what is private, and who decides?
- Who moderates, and with what tools?

**Often combined with:** Content, Commerce, Tool.

---

## Data

**Definition:** A product where users monitor, analyze and act on data.

**Core job:** Understand what is happening, why, and what to do about it.

**Recognize it by:**
- The main content is numbers, metrics and records
- Users compare across time, segments or entities
- The product supports decisions rather than creation

**Core objects:** Metrics, data sources, dimensions, filters, reports, dashboards, alerts, entities (customers, assets, transactions).

**Key views:**
- Overview dashboard
- Detailed report or exploration view
- Entity detail (one customer, one asset)
- Table view with filtering and sorting
- Alerts and notifications
- Configuration of sources and metrics

**Key flows:**
- Scan the overview, spot a change, drill down, find the cause
- Filter and segment, compare periods
- Save, share or export a view
- Set up an alert and respond to it

**Required states:**
- No data yet, or data still loading
- Partial or delayed data
- Data errors and anomalies
- No results for a filter
- Very large result sets

**Structural needs:** Filter and query model, time handling, aggregation, export, permissions on data, performance with large data sets, clear definitions of metrics.

**What good looks like:** The most important signal is visible without interaction. Every number can be traced to its definition and source. Going from overview to detail is fast.

**Common failure modes:**
- Dashboards showing everything, so nothing stands out
- Metrics without definitions, so users stop trusting them
- No path from insight to action

**Kickoff questions:**
- Which decisions should this product support?
- What does a user look at first, every time?
- How fresh does the data need to be?
- Who defines the metrics, and how are they explained?

**Often combined with:** Tool, AI-native.

---

## AI-native

**Definition:** A product where the core value is produced by AI together with the user, through generation, analysis or autonomous work.

**Core job:** Delegate work to AI, or create something with it, while keeping control over the outcome.

**Recognize it by:**
- Output is generated, not retrieved
- Results vary and need review
- The user steers through intent (prompts, instructions, examples) rather than direct operation

**Core objects:** Prompts or requests, outputs, sessions or threads, context (files, sources, memory), agents or tasks, versions.

**Key views:**
- Input or request view
- Output or result view, with editing
- History of sessions or threads
- Context and source management
- Task or agent progress view
- Settings for model behavior and permissions

**Key flows:**
- Ask, receive, review, refine, accept
- Compare alternatives and choose
- Add context, rerun
- Delegate a longer task, follow progress, approve steps
- Edit output directly and continue from there

**Required states:**
- Generating, streaming, long-running tasks
- Uncertain or low-confidence output
- Refusal or failure to generate
- Output that needs approval before action
- Output that differs from what the user expected

**Structural needs:** History and versioning, source attribution, editable output, cancellation, permission model for actions the AI takes, feedback mechanisms, cost or usage visibility.

**What good looks like:** Users understand what the AI can and cannot do. Output is easy to verify, edit and reuse. The user stays in control of consequential actions.

**Common failure modes:**
- A chat box as the whole product, whatever the task
- Output that cannot be edited, only regenerated
- No way to see what the AI based its answer on
- Autonomous actions without clear approval points

**Kickoff questions:**
- Which parts of the task should AI do, and which should the user own?
- How does the user verify that the output is right?
- What happens when the AI is wrong?
- Which actions need explicit approval?

**Often combined with:** Tool, Data, Content.

---

## Utility

**Definition:** A focused product that does one thing well.

**Core job:** Complete a single, narrow task as fast as possible.

**Recognize it by:**
- One primary action
- Very short sessions
- Little or no account or setup needed

**Core objects:** The input, the output, and possibly a small history.

**Key views:**
- The main view with the primary action
- The result
- Minimal settings

**Key flows:**
- Open, act, get result, leave
- Repeat with small variations

**Required states:**
- Invalid input
- Processing
- Result ready, copied, exported
- Offline or failed

**Structural needs:** Fast startup, sensible defaults, minimal navigation, clear output handling (copy, save, share).

**What good looks like:** The primary action is available immediately. Nothing stands between the user and the result.

**Common failure modes:**
- Feature creep that turns the utility into a mediocre tool
- Setup or sign-up before first value
- Too many options on the main view

**Kickoff questions:**
- What is the one thing this product does?
- What would we remove if we could only keep one screen?
- What does the user do with the result?

**Often combined with:** AI-native.

---

## Immersive

**Definition:** An experience where the value is in the experience itself: spatial, nonlinear, gesture-based, sound-led or highly expressive.

**Core job:** Explore, feel, play or be moved.

**Recognize it by:**
- There is no efficient path, and there should not be
- Exploration and discovery are part of the value
- The medium itself (space, sound, motion, touch) carries meaning

**Core objects:** Scenes, spaces, moments, interactive elements, narrative chapters, media.

**Key views:**
- Entry or threshold that sets expectations
- The experience itself (scenes or spaces)
- Orientation aid (map, progress, chapter overview)
- Exit or conclusion

**Key flows:**
- Enter, orient, explore, discover
- Move between scenes or chapters
- Pause, resume, leave and return
- Share a moment

**Required states:**
- Loading heavy assets
- Unsupported device or input method
- Sound off or unavailable
- Reduced motion preferences
- User lost or inactive

**Structural needs:** Asset loading strategy, performance budgets, fallback experiences, accessibility alternatives, input handling across devices.

**What good looks like:** Users know how to interact without instructions. The experience holds together on weaker devices. There is always a way out.

**Common failure modes:**
- Spectacle without purpose
- Performance that breaks the experience
- No accessible alternative
- Users getting lost with no way to orient

**Kickoff questions:**
- What should a user feel, and remember, afterwards?
- What is the minimum device the experience must work on?
- How does someone who cannot use the primary input take part?
- How long is a typical visit?

**Often combined with:** Content, Commerce (brand experiences).

---

## Common hybrids

Most products are combinations. These are frequent patterns, written as primary + secondary.

| Hybrid | Example of what it becomes |
|---|---|
| Commerce + Community | Marketplace, peer-to-peer selling |
| Commerce + Content | Brand site with shop, editorial commerce |
| Tool + AI-native | Editor or workspace with AI assistance |
| Tool + Data | Operational system with reporting |
| Content + Community | Publication with discussion, knowledge base with contributions |
| Service + Content | Public sector site with self-service |
| Data + AI-native | Analytics with natural language questions and generated insights |
| Content + Immersive | Campaign, storytelling experience, digital exhibition |

When combining, the **primary type decides the default view and the navigation structure**. Secondary types add objects, views and flows inside that structure.

---

## Contributing

- Keep every type in the schema above, so types stay comparable.
- Write in terms of objects, views, flows and states. Never platform, framework or visual style.
- Add a new type only when a product cannot be described as a hybrid of existing ones.
- Prefer sharper failure modes and kickoff questions over longer lists.
