# 📖 User Guide — BMAD Roles (distilled)

This kit turns the **BMAD** method into a "virtual department": each role is an AI specialist you *call into the meeting* when needed. Everything is **self-contained** — no BMAD install, no python, just markdown files.

---

## 1. Quick start (3 steps)

1. **Open [`roster.md`](roster.md)** → pick the role that matches the work.
2. **Ask the AI to play that role** and load the capability file you need. Template:
   > *"Play the role of **Winston** in `distilled/roster.md`, following `distilled/capabilities/architecture.md`. Design the architecture for: **[project description]**."*
3. **Hand off** to the next role when done (see the flow in section 3).

> 💡 Load only **1–3 files per session** (persona + 1–2 capabilities) to save tokens. Don't load the whole folder.

---

## 2. Who's on the team? (8 roles)

| Role | Call when you need | Key capabilities |
|---|---|---|
| 📊 **Mary** — Analyst | Research, brainstorming, briefs, idea validation | brainstorming, product-brief, market/domain/technical-research, prfaq, forge-idea |
| 📚 **Paige** — Tech Writer | Documentation, diagrams, editing, project-context | document-project, generate-project-context, editorial-review-* |
| 📋 **John** — PM | Writing the PRD, epic/story breakdown, readiness gate | prd, create-epics-and-stories, check-implementation-readiness |
| 🎨 **Sally** — UX | Experience design, user flows | ux |
| 🏗️ **Winston** — Architect | System design, tech stack, **database**, spec | architecture, spec |
| 💻 **Amelia** — Dev | Coding each story, quick-dev, code-review | dev-story, quick-dev, code-review, create-story |
| 🧪 **Murat** — Test Architect | Test strategy, edge cases, CI, traceability | testarch-* (8 files) |
| 🛠️ **Builder** | Creating new agents/workflows/modules | builder-agent, workflow-builder, module-builder |

There are also **shared capabilities** any role can invoke: `advanced-elicitation`, `party-mode`, `review-adversarial-general`, `review-edge-case-hunter`.

---

## 3. The standard project flow (4 phases)

```
Phase 1 — ANALYSIS      📊 Mary          → brainstorm / research / product-brief
Phase 2 — PLANNING      📋 John + 🎨 Sally → PRD + UX design
Phase 3 — SOLUTIONING   🏗️ Winston        → architecture (incl. database) + epic/story breakdown
Phase 4 — BUILD         💻 Amelia → 🧪 Murat → code each story, then test
                         ↑___ repeat per sprint ___↓
```

Each phase produces an artifact that feeds the next:
`brief → PRD → architecture → story → code → test`

> ⚠️ BMAD principle: **lock the architecture (incl. database) BEFORE breaking work into stories** — because database/API/tech-stack decisions shape how work is split.

---

## 4. Example prompts by situation

**Vague idea, want to explore it:**
> *"Play Mary following `capabilities/brainstorming.md`; brainstorm this idea with me: [X]."*

**Idea is clear, need a requirements doc:**
> *"Play John following `capabilities/prd.md`; write a PRD for: [paste brief]."*

**Need system + database design:**
> *"Play Winston following `capabilities/architecture.md`; design the architecture + database schema for: [paste PRD]."*

**Code a story:**
> *"Play Amelia following `capabilities/dev-story.md`; implement this story: [paste story]."*

**Want multiple perspectives at once (roundtable):**
> *"Use `capabilities/party-mode.md`; have Winston + Amelia + Murat debate whether this schema migration is safe."*

---

## 5. Tips

- **Token-thrift:** don't paste `roster.md` plus many capabilities. Pick exactly one role + the capability you need.
- **Handoff:** at the end of each phase, ask the AI to *"summarize the artifact to hand off to [next role]"*, then open a fresh session with that role.
- **Session memory:** for long work, ask the AI to keep an append-only markdown log so you can resume later.
- **Database:** currently lives under 🏗️ Winston (matching BMAD's original design). To split out a dedicated DBA role, you'd reinstall BMAD + use the Builder, then distill it in.

---

## 6. Folder structure

```
distilled/
├── README.md           ← this file
├── roster.md           ← the 8 roles + links to capabilities
└── capabilities/       ← 44 self-contained capability files (one workflow each)
```

Each `capabilities/*.md` file holds BMAD's **real method** (install machinery stripped), enough for the AI to perform the role correctly — not a shallow summary.
