# custom-claude-skills

A personal library of reusable custom skills for Claude.

## What are skills?

Skills are `SKILL.md` files that give Claude a specialized playbook for a specific task or workflow. Claude auto-loads relevant skills based on context, or you can invoke them directly with `/skill-name`.

## Structure

```
claude-skills/
├── README.md
└── skills/
    ├── design-interrogator/
    │   └── SKILL.md
    └── your-skill-name/
        ├── SKILL.md
        └── (optional supporting files)
```

Each skill lives in its own subdirectory under `skills/`. The folder name becomes the slash command.

## Using these skills

**Claude.ai (web/desktop)**
1. Zip the skill folder: `zip -r my-skill.zip skills/my-skill/`
2. Go to **Customize > Skills > +** and upload the ZIP
3. Make sure the folder is at the ZIP root, not just its contents

**Claude Code (CLI) — personal (all projects)**
```bash
cp -r skills/my-skill ~/.claude/skills/
```

**Claude Code (CLI) — project-specific**
```bash
cp -r skills/my-skill /path/to/project/.claude/skills/
```

## Adding a new skill

1. Create a folder under `skills/` with a short, descriptive name
2. Add a `SKILL.md` with YAML frontmatter:

```markdown
---
name: skill-name
description: "What this skill does and when Claude should use it. Be specific — this is what drives auto-triggering."
---

# Instructions
...
```

3. Test it, iterate on the description if it's not triggering reliably
4. Commit to this repo

## Skills

| Skill | Description |
|-------|-------------|
| *(none yet)* | |
