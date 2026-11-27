# Solomantalgo client site workflow

This workflow separates **planning and design leadership** from implementation. Start a fresh planning agent/session for **one named client project** using `templates/CLIENT_PLANNER_PROMPT.md`. The planning agent remains the owner's sole contact and coordinates the whole project, including the builder. Another client starts with a new planner and project plan. The owner makes key scope and visual decisions using concrete previews rather than needing design vocabulary.

## Core rules

1. Read `BUSINESS_REFERENCE.md` and the current `PACKAGES.md` at the start of every client project.
2. Gather essential requirements, inspect references, identify missing assets, and offer useful recommendations **before creating the client plan or builder prompt**. Then create `PROJECT_PLAN.md` from `templates/PROJECT_PLAN.md` for the assigned client. Put the client's name, project path, scope, verified references, and decisions there; refine it as design decisions are made.
3. Plan the site and its customer journeys **before** visual design. For a new site or requested redesign, no full implementation begins before the owner chooses a direction and approves the implementation handoff. For a focused change to an existing site, use the focused-update path below.
4. Offer at least **three substantially different visual directions** for each new site. A different colour palette on the same layout does not count.
5. Show a **desktop and mobile home-page image for each direction**. Add preview screens for a central ordering, booking, or other interaction when needed to judge the concept.
6. The planning agent inventories supplied assets and creates or sources missing visual assets. Use the Codex imagegen skill for suitable new bitmap imagery. Record exact paths, provenance, usage, and approval in the project plan. Verify that the builder can access each required file before dispatch. Do not invent client branding or factual imagery.
7. Keep package scope, custom additions, exclusions, domain cost, hosting cost, and other recurring costs explicit. Domain is separate. Confirm hosting per project.
8. Design to the assigned client's business and audience. Reuse lessons and patterns, not another client's identity, content, approvals, or page composition.
9. Keep the builder prompt in the **chat**, not only in a `.md` file. Keep plans, decisions, asset manifests, and specifications in Markdown files. The planning agent dispatches and supervises the builder when delegation is available; the owner never has to interact with the builder.
10. Ask the owner only for unresolved decisions that materially affect the work. Use short numbered questions, one decision per item, with the current known value and clear options where possible. Example: `1. Opening hours — the existing site says 10:00–22:00. Keep these, or send the new hours?` Do not send a dense paragraph of unrelated confirmations or re-ask answered questions.

## Continuity across sessions and context resets

The repository files are the durable instructions. Agent memory alone is not a reliable record. The planner keeps a dated decision log in the client's `PROJECT_PLAN.md`, including the owner's answers, approved scope, references, and pending questions. On resuming or after context compaction, reread `AGENTS.md`, this workflow, and the client plan before asking or acting. Check the conversation and project files for an answer before requesting it again. Do not mark an assumption as owner-approved.

## Choosing the right project path

- **New site or requested redesign:** Follow Stages 1–6, including three visual directions and desktop/mobile previews.
- **Focused update to an existing site:** Inspect the live/code state and references; make a short change plan listing exact edits, preserved behavior, assets, and checks. Use the owner's existing authorization; confirm only unresolved material decisions. Skip three design directions and a redesign approval unless the owner asks for redesign. Do not expand a branding update into a new site concept.

## Stage 1 — Discovery and scope

The planning agent gathers: business name and industry; customer types; primary conversion goal; services/products and prices; required content and assets; brand preferences; location/contact details; selected package and budget; required features; target date; domain and hosting arrangements; content ownership; operational details for ordering/booking/payments.

Read the selected package's inclusions and exclusions. Identify any requested feature outside scope. Recommend the smallest practical package or add-on combination, and show any recurring or third-party costs. A price label alone does not authorize assumptions about client content, page count, integrations, or exact workflow behavior.

Before creating the client plan or builder prompt, inspect available client files, URLs, existing code, and references. List confirmed requirements, missing facts, and **optional recommendations** separately. Recommend valuable additions or simpler approaches with cost/scope implications, but do not add them to the approved scope without the owner's decision. Gather essential answers in the planner conversation before writing the plan. The plan may then be refined through direction selection and owner feedback.

**Decision gate:** Owner confirms the project goal, package/custom scope, and outstanding information that materially affects design or cost.

## Stage 2 — Site and experience plan

Create a sitemap or section map; identify the main user journeys; set content priority for mobile; describe each required interaction in plain language; select a proportionate technical approach. Explain what happens when a visitor submits an enquiry, adds items to a cart, books, or pays. For Standard, do not silently introduce stored customer data or automated confirmations.

Plan the actual content structure, not placeholder page furniture. If copy or images are missing, record how they will be obtained. Make mobile connectivity and performance part of the plan.

**Decision gate:** Owner approves the structure and core journeys before visual exploration.

## Stage 3 — Assets and design exploration

Inventory client-supplied logos, photos, copy, and brand elements. Produce missing assets where appropriate and mark generated concepts versus real client facts. Prepare imagegen assets with a coherent art direction for each concept; do not use generated pictures as evidence of a real product, employee, place, or completed project.

If a reference is only attached in the planner conversation, save or copy it into a path accessible to the builder where possible. Record its exact path and role. Open or otherwise verify critical files before handoff. For a specific approved logo or real client asset that is missing, ask the owner **once** through the planner; do not generate a substitute or let the builder discover the gap later.

Develop at least three directions. Each direction needs:

- A distinct concept and why it fits this client and its audience.
- Typography, palette, imagery treatment, layout system, content rhythm, and navigation approach.
- A signature home-page composition rather than a generic hero followed by repetitive cards.
- Planned interactions and purposeful animation, including mobile and reduced-motion behavior.
- **Rendered desktop and mobile home-page previews** as images. Prefer screenshots of small HTML/CSS concept prototypes, so the preview reflects a buildable design. These concept prototypes are design artifacts, not the full site implementation.
- An extra preview of a key flow when the homepage cannot show how ordering, booking, or another central feature works.

Use comparable real or clearly labelled draft content across directions so the owner can judge design differences fairly. Check that the concepts differ in composition and interaction, not only decoration. The owner may choose one, combine specific elements, or request refinements. Record the decision and reasons.

**Decision gate:** Owner selects a direction. Do not proceed by treating silence as approval.

## Stage 4 — Implementation handoff

Refine the selected direction. Update the project plan into a complete handoff with:

- Approved preview images and design rationale.
- Page/section map, content inventory, final copy status, and CTA hierarchy.
- Design tokens and layout rules: type, colours, spacing, widths, grids, imagery, and responsive behavior.
- Components, states, forms, navigation, and exact feature flows.
- Motion specification: trigger, effect, duration/feel, purpose, mobile behavior, and reduced-motion alternative.
- Asset paths, licensing/provenance where applicable, and image generation notes.
- Selected package, included work, custom additions, exclusions, and domain/hosting/third-party cost decisions.
- Acceptance checks and any remaining approved assumptions.

Before handoff, the planner checks that the client plan includes all confirmed requirements, exact accessible paths to references and approved assets, approved changes, exclusions, and acceptance checks. The planner must resolve known missing inputs or clearly mark the affected task as deferred. Do not transfer an incomplete discovery process to the builder.

The planner posts a **client-specific builder prompt directly in chat**. The prompt names the client, exact project and reference paths, approved scope, preserved behavior, checks, and how to report blockers **to the planner**. The prompt does not live only in a Markdown file. The planner then launches and supervises the builder when delegation tools are available. If they are unavailable, the planner continues implementation in its own session and tells the owner that separate delegation was unavailable. The owner is never asked to brief or answer the builder. Avoid broad instructions such as "build client sites" that could make the builder treat other clients as part of this assignment.

**Decision gate:** For a new site or redesign, the owner approves the chosen direction and handoff before full implementation. For a focused update, carry out already authorized changes once essential inputs are available; ask only about unresolved scope or facts.

## Stage 5 — Build and review

The implementation agent builds the approved design and functionality. It checks responsive layouts, navigation, forms and order/booking paths, keyboard use, reduced motion, performance, SEO basics, and broken links or assets. It captures real desktop and mobile screenshots. It reports questions, inaccessible references, and blockers to the planner, not the owner.

The planning agent answers builder questions from the plan or existing evidence. If a genuine owner decision is needed, the planner asks the owner in a numbered, easy-to-scan list and sends the answer back to the builder. The planner compares the finished site with the approved handoff and previews, then lists concrete differences. Fix defects and agreed revisions; surface scope changes with their cost or timeline effect. Verify the site in the actual environment before marking it complete.

## Stage 6 — Reuse learning

After approval, record useful visual and interaction ideas in `DESIGN_LIBRARY.md`: what problem the pattern solved, where it worked, constraints, and how to adapt it. Do not save a whole client site as a default template for unrelated businesses. Record owner feedback such as “too generic” with the exact visual cause and preferred alternative.

## Planner's chat prompt pattern

Post the filled prompt in chat before dispatch. Do not ask the owner to paste it to another agent.

> You are the implementation agent for **[client name]** only. The planning agent is your sole contact. Read `C:\Solomon\Projects\AgentWorkflow\AGENTS.md`, `BUSINESS_REFERENCE.md`, `PACKAGES.md`, and `SITE_WORKFLOW.md` for shared standards, then read `[exact client project path]\PROJECT_PLAN.md` and these verified references: `[exact paths and roles]`. Implement only the approved changes and preserve `[listed existing behavior]`. Use the approved assets at `[exact paths]`. Do not import another client's content or design. Report any missing critical fact, inaccessible file, or scope conflict to the planning agent; do not ask the owner directly. Capture desktop and mobile results, verify the plan's acceptance checks, and report deviations to the planning agent.
