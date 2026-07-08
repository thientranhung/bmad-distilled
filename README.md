# bmad-distilled

A distilled, markdown-first toolkit for turning BMAD into a practical virtual team of AI specialists for software work.

This repository is meant to be dropped into the docs of a project and used as a lightweight operating manual for better AI collaboration. Instead of treating an AI like a generic assistant, you can give it clear specialist roles such as architect, PM, developer, tester, or UX designer.

## Why use it

When a task needs deeper thinking, this kit helps the AI behave more like a real team than a single chatbot.

- Put it in project documentation so the AI can reference it as part of the project context.
- Use it when a prompt needs a specialist role in software development.
- Use it to improve the quality, structure, and accuracy of outputs.
- Use it to spawn a small team of agents and let them collaborate on discovery, planning, design, implementation, and review.

## Common ways to use it

### 1. As project context
Add the folder to your project docs so the AI can work with the same mental model as your team.

### 2. As a role-based expert
Ask the AI to play a role for a specific task:
- Winston for architecture
- John for requirements and planning
- Amelia for implementation
- Murat for testing and quality

### 3. As a multi-agent team
For harder problems, bring several roles into the same conversation:
- Mary for analysis and discovery
- John for planning and requirements
- Winston for architecture
- Amelia for implementation
- Murat for testing and quality

## Quick start

1. Open [distilled/roster.md](distilled/roster.md) and choose the role that fits the task.
2. Ask the AI to play that role and load the matching capability file.
3. For larger work, bring in multiple roles and let them collaborate.

Example prompt:
> "Play the role of Winston in distilled/roster.md, following distilled/capabilities/architecture.md. Design the architecture for this feature."

## Team roles

| Role | Best for | Key capabilities |
|---|---|---|
| 📊 Mary | Research, brainstorming, idea validation | brainstorming, product-brief, market/domain/technical-research |
| 📋 John | Requirements, PRD, story breakdown | prd, create-epics-and-stories |
| 🎨 Sally | UX flows and experience design | ux |
| 🏗️ Winston | Architecture, system design, database decisions | architecture, spec |
| 💻 Amelia | Implementation, coding tasks, reviews | dev-story, quick-dev, code-review |
| 🧪 Murat | Test strategy, edge cases, CI | testarch-* |
| 📚 Paige | Documentation and project context | document-project, generate-project-context |
| 🛠️ Builder | New agents, workflows, modules | builder-agent, workflow-builder, module-builder |

## Structure

```text
distilled/
├── README.md
├── roster.md
└── capabilities/
```

See [distilled/README.md](distilled/README.md) for the full guide and richer usage patterns.
