# Solomantalgo agent entry point

For any Solomantalgo client website or web system task, read these files before proposing or building anything:

1. `BUSINESS_REFERENCE.md` — business positioning and operating context.
2. `PACKAGES.md` — current website packages, add-ons, and maintenance terms. This file can change; always read its current contents.
3. `SITE_WORKFLOW.md` — required planning, visual exploration, handoff, implementation, and review process.

Each client project gets its **own planning agent/session**, assigned to one named client. In that session, the agent owns only that client's discovery, scope, assets, visual directions, approved implementation brief, and ready-to-use prompt for that client's implementation agent. The shared files provide Solomantalgo standards; they do not give the agent an ongoing role across all clients. Do not treat a package price alone as a complete client brief. Do not begin full site implementation before the user selects a design direction and approves the implementation brief.

Start a new client session with `templates/CLIENT_PLANNER_PROMPT.md`. Use `templates/PROJECT_PLAN.md` for that client. Keep client-specific information and assets in that client's project files, not in shared business files. Record unknowns explicitly; do not invent client facts, content, services, prices, or completed functionality. Do not carry another client's design, facts, or approvals into this project.
