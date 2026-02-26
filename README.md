# AI Path

## Prompt Engineering

- https://scrimba.com/prompt-engineering-for-web-developers-c02o
- Overview: [https://www.youtube.com/watch?v=dOxUroR57xs](https://www.youtube.com/watch?v=dOxUroR57xs)
- https://www.promptingguide.ai/
- https://learnprompting.org/docs/introduction
- https://cloud.google.com/discover/what-is-prompt-engineering#what-do-you-need-for-prompt-engineering

### Practical Examples
- Building a Vapi caller for Law Firms - [https://youtu.be/kIyYnhFwaw4?si=r1SMiDyaisqt_h5u](https://youtu.be/kIyYnhFwaw4?si=r1SMiDyaisqt_h5u)
- https://docs.vapi.ai/debugging
- Voice AI agent in minutes - [https://www.youtube.com/watch?v=n64lzhgld8M](https://www.youtube.com/watch?v=n64lzhgld8M)

## Building Agents & Skills

* Rules for Agents usually in .agent/rules folder with any rule as your filename
* Agent Skills - [https://agentskills.io/home](https://agentskills.io/home)
* Creating Custom Skills for Claude - [https://support.claude.com/en/articles/12512198-how-to-create-custom-skills](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills)
* Creating Custom Sub Agents in Claude (Optional) - [https://code.claude.com/docs/en/sub-agents](https://code.claude.com/docs/en/sub-agents)
---

### How Claude Skills Work

A **skill** is a folder containing a `SKILL.md` file (with YAML frontmatter + markdown instructions) and optional bundled resources (scripts, templates, reference docs). Skills are loaded into Claude's context when triggered by a matching user request.

```
skill-name/
├── SKILL.md              # Required: instructions + metadata
├── scripts/              # Optional: reusable automation scripts
├── references/           # Optional: loaded into context as needed
└── assets/               # Optional: templates, checklists, etc.
```

The **SKILL.md frontmatter** has two critical fields:

- `name`: The skill identifier
- `description`: Controls *when* the skill triggers — include specific phrases, contexts, and keywords users would use

The **SKILL.md body** contains the actual instructions Claude follows when the skill is active.
