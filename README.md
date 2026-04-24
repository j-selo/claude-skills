# Claude Code Skills

A collection of custom skills for Claude Code.

## Structure

```
.
├── README.md
└── .claude/
    └── skills/
        ├── devops-plan/
        │   └── SKILL.md
        └── your-skill-name/
            └── SKILL.md
```

Each skill lives in its own folder under `.claude/skills/`. The folder name becomes the slash command name.

## Installation

**Project-scoped** (available in this repo only):

```bash
git clone https://github.com/you/claude-skills
cp -r claude-skills/.claude/skills/your-skill-name .claude/skills/
```

**Global** (available across all your projects):

```bash
cp -r claude-skills/.claude/skills/your-skill-name ~/.claude/skills/
```

## Usage

Once a skill is installed, invoke it in Claude Code with:

```
/skill-name
```

Claude will also pick up skills automatically when your request matches the skill's description — no slash command needed.

## Adding a new skill

1. Create a folder under `.claude/skills/` named after your skill
2. Add a `SKILL.md` file with a frontmatter `name` and `description`
3. Write your instructions in the body of the file

```
.claude/skills/my-skill/SKILL.md
```

See the [Claude Code skills documentation](https://docs.anthropic.com/en/docs/claude-code/skills) for full details on the `SKILL.md` format.
