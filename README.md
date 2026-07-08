# bmad-distilled

This repository turns BMAD into a lightweight virtual department for software work. Each role is an AI specialist you can call into the conversation when a task needs deeper expertise. It is designed to be dropped into the documentation of a project and used as a practical playbook for better, more structured AI collaboration.

## Why this is useful

This works especially well when you want an AI to behave less like a generic assistant and more like a specialist team.

- Put it inside the docs of a project so the agent can reference it as part of the project context.
- Use it when a prompt needs a role such as architect, PM, developer, tester, or UX designer.
- Use it to make outputs more accurate, more structured, and more aligned with real software delivery practices.
- Use it to spawn a small team of agents and let them play different roles in a discussion, review, or problem-solving session.

## How I use it in practice

### 1. Drop it into project docs

Add this folder to the documentation area of a project so the AI can see the roles and capabilities as part of the project context.

### 2. Use it when a prompt needs a specialist role

Instead of asking a general question, ask the AI to play a specific role such as Winston for architecture or Amelia for implementation.

### 3. Spawn a team of agents

For harder problems, bring multiple roles into the same conversation:
- Mary for analysis and discovery
- John for planning and requirements
- Winston for architecture
- Amelia for implementation
- Murat for testing and quality

## Quick start

1. Open [distilled/roster.md](distilled/roster.md) and pick the role that matches the task.
2. Ask the AI to play that role and load the capability file you need.
3. For larger work, bring in multiple roles and let them collaborate.

Example:
> "Play the role of Winston in distilled/roster.md, following distilled/capabilities/architecture.md. Design the architecture for this feature."

## Who's on the team?

| Role | Use it when you need | Key capabilities |
|---|---|---|
| 📊 Mary | Research, brainstorming, idea validation | brainstorming, product-brief, market/domain/technical-research |
| 📋 John | Requirements, PRD, story breakdown | prd, create-epics-and-stories |
| 🎨 Sally | UX flows and experience design | ux |
| 🏗️ Winston | Architecture, system design, database decisions | architecture, spec |
| 💻 Amelia | Implementation, coding tasks, reviews | dev-story, quick-dev, code-review |
| 🧪 Murat | Test strategy, edge cases, CI | testarch-* |
| 📚 Paige | Documentation and project context | document-project, generate-project-context |
| 🛠️ Builder | New agents, workflows, modules | builder-agent, workflow-builder, module-builder |

## Folder structure

```text
distilled/
├── README.md
├── roster.md
└── capabilities/
```

See [distilled/README.md](distilled/README.md) for the full guide and usage patterns.
