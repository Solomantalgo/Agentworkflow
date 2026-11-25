# Solomantalgo client site workflow

This workflow separates **planning and design leadership** from full implementation. Start a fresh planning agent/session for **one named client project** using `templates/CLIENT_PLANNER_PROMPT.md`. That agent's responsibility ends with that client's project; another client starts with a new planner and a new project plan. The owner makes key scope and visual decisions using concrete previews rather than needing design vocabulary.

## Core rules

1. Read `BUSINESS_REFERENCE.md` and the current `PACKAGES.md` at the start of every client project.
2. Create a plan for the assigned client using `templates/PROJECT_PLAN.md`. Put the client's name, project path, and scope at the top. Update it as decisions are made. Label unknowns and assumptions.
3. Plan the site and its customer journeys **before** visual design. No full implementation begins before the owner chooses a direction and approves the implementation handoff.
4. Offer at least **three substantially different visual directions** for each new site. A different colour palette on the same layout does not count.
5. Show a **desktop and mobile home-page image for each direction**. Add preview screens for a central ordering, booking, or other interaction when needed to judge the concept.
6. The planning agent inventories supplied assets and creates or sources missing visual assets. Use the Codex imagegen skill for suitable new bitmap imagery. Record provenance, usage, and approval in the project plan. Do not invent client branding or factual imagery.
7. Keep package scope, custom additions, exclusions, domain cost, hosting cost, and other recurring costs explicit. Domain is separate. Confirm hosting per project.
8. Design to the assigned client's business and audience. Reuse lessons and patterns, not another client's identity, content, approvals, or page composition.

## Stage 1 — Discovery and scope

The planning agent gathers: business name and industry; customer types; primary conversion goal; services/products and prices; required content and assets; brand preferences; location/contact details; selected package and budget; required features; target date; domain and hosting arrangements; content ownership; operational details for ordering/booking/payments.

Read the selected package's inclusions and exclusions. Identify any requested feature outside scope. Recommend the smallest practical package or add-on combination, and show any recurring or third-party costs. A price label alone does not authorize assumptions about client content, page count, integrations, or exact workflow behavior.

**Decision gate:** Owner confirms the project goal, package/custom scope, and outstanding information that materially affects design or cost.

## Stage 2 — Site and experience plan

Create a sitemap or section map; identify the main user journeys; set content priority for mobile; describe each required interaction in plain language; select a proportionate technical approach. Explain what happens when a visitor submits an enquiry, adds items to a cart, books, or pays. For Standard, do not silently introduce stored customer data or automated confirmations.

Plan the actual content structure, not placeholder page furniture. If copy or images are missing, record how they will be obtained. Make mobile connectivity and performance part of the plan.

**Decision gate:** Owner approves the structure and core journeys before visual exploration.

## Stage 3 — Assets and design exploration

Inventory client-supplied logos, photos, copy, and brand elements. Produce missing assets where appropriate and mark generated concepts versus real client facts. Prepare imagegen assets with a coherent art direction for each concept; do not use generated pictures as evidence of a real product, employee, place, or completed project.

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

The planning agent provides a **ready-to-paste implementation prompt for this named client only**, pointing to that client's handoff file and assets. The prompt tells the builder to implement the approved direction, report deviations or blockers, and show desktop/mobile results. It does not substitute for the handoff file. Avoid broad instructions such as "build client sites" that could make the implementation agent treat other clients as part of this assignment.

**Decision gate:** Owner approves the handoff before full implementation.

## Stage 5 — Build and review

The implementation agent builds the approved design and functionality. It checks responsive layouts, navigation, forms and order/booking paths, keyboard use, reduced motion, performance, SEO basics, and broken links or assets. It captures real desktop and mobile screenshots.

The planning agent compares the finished site with the approved handoff and previews, then lists concrete differences. Fix defects and agreed revisions; surface scope changes with their cost or timeline effect. Verify the site in the actual environment before marking it complete.

## Stage 6 — Reuse learning

After approval, record useful visual and interaction ideas in `DESIGN_LIBRARY.md`: what problem the pattern solved, where it worked, constraints, and how to adapt it. Do not save a whole client site as a default template for unrelated businesses. Record owner feedback such as “too generic” with the exact visual cause and preferred alternative.

## Planner's implementation prompt pattern

> You are the implementation agent for **[client name]** only. Build the site described in `[exact path]/PROJECT_PLAN.md`. Read `AGENTS.md`, `BUSINESS_REFERENCE.md`, `PACKAGES.md`, and `SITE_WORKFLOW.md` for shared standards, then follow this client's approved handoff and assets. Implement the stated pages, responsive behavior, motion, and feature flows within this client's selected package/custom scope. Do not import another client's content or design. Flag missing critical facts or conflicts before implementing the affected feature. Capture desktop and mobile screenshots, verify the acceptance checks, and report deviations from this client's approved previews.
