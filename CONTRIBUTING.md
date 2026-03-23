# Contributing to Claude Code Skills

Thanks for wanting to contribute. This guide covers everything you need to add a new skill or improve an existing one.

---

## Table of Contents

- [What Is a Skill?](#what-is-a-skill)
- [Skill File Structure](#skill-file-structure)
- [Adding a New Skill](#adding-a-new-skill)
- [Improving an Existing Skill](#improving-an-existing-skill)
- [Pull Request Guidelines](#pull-request-guidelines)
- [Skill Quality Bar](#skill-quality-bar)

---

## What Is a Skill?

A Claude Code skill is a directory placed in `~/.claude/skills/<name>/` that contains a `SKILL.md` file. When Claude Code starts, it loads all installed skills and makes them available as slash commands.

Invoking `/skill-name` in a Claude Code session loads the skill's `SKILL.md` as a system-level prompt that shapes Claude's behavior for that interaction.

Skills can also include supporting files (Python scripts, SVGs, config) that the skill references via the `${CLAUDE_SKILL_DIR}` environment variable.

---

## Skill File Structure

Every skill in this repo lives under `skills/<name>/` and must contain:

```
skills/
└── your-skill-name/
    ├── SKILL.md        ← required: skill definition and prompt
    ├── README.md       ← required: user-facing documentation
    └── LICENSE         ← required: MIT license (copy from another skill)
```

Optional files for skills that need them:

```
    ├── *.py            ← Python scripts launched by the skill
    ├── *.svg           ← Banners, demos, or diagrams
    └── config/         ← Any additional config files
```

### SKILL.md Format

Every `SKILL.md` must start with a YAML frontmatter block:

```markdown
---
name: your-skill-name
description: One sentence that explains when this skill should trigger. This text is used by Claude to decide when to invoke it, so be specific about trigger phrases and use cases.
version: 1.0.0
---

# Your Skill Title

[The full skill prompt goes here]
```

**Frontmatter fields:**

| Field | Required | Notes |
|:------|:--------:|:------|
| `name` | Yes | Must match the directory name and the slash command (e.g. `token-surgeon` → `/token-surgeon`) |
| `description` | Yes | Used by Claude to decide when to auto-invoke. Include trigger phrases. |
| `version` | No | Recommended. Semver. |
| `allowed-tools` | No | Restrict which Claude Code tools the skill can use (e.g. `Bash`, `Read`) |
| `disable-model-invocation` | No | Set to `true` for skills that only run shell commands |

### README.md Format

Each skill's README should cover:

1. **What it does** — one paragraph, concrete
2. **How to invoke it** — the exact command and any arguments
3. **What the output looks like** — table, example, or screenshot
4. **Installation** — clone + copy instructions for macOS/Linux and Windows
5. **Requirements** — Claude Code version, Python version if needed, etc.

Look at [`skills/token-surgeon/README.md`](skills/token-surgeon/README.md) for a well-structured example.

---

## Adding a New Skill

### 1. Fork and clone

```bash
git clone https://github.com/natedemoss/claude-code-skills.git
cd claude-code-skills
```

### 2. Create the skill directory

```bash
mkdir skills/your-skill-name
```

### 3. Write `SKILL.md`

Start with the frontmatter, then write the prompt. A good skill prompt:

- Has a clear **trigger** — when should Claude invoke this?
- Has clear **phases** — analysis before action, confirm before irreversible steps
- Has a defined **output format** — tables, code blocks, structured sections
- Does **one thing well** — don't combine unrelated behaviors into one skill

### 4. Write `README.md`

Document the skill for users who find it on GitHub. Reference actual example output. Don't write generic descriptions — show what the skill actually produces.

### 5. Copy the LICENSE

```bash
cp skills/onboarding/LICENSE skills/your-skill-name/LICENSE
```

### 6. Test it locally

```bash
# macOS / Linux
cp -r skills/your-skill-name ~/.claude/skills/your-skill-name

# Windows (PowerShell)
Copy-Item -Recurse skills\your-skill-name "$env:USERPROFILE\.claude\skills\your-skill-name"
```

Open Claude Code and invoke `/your-skill-name`. Verify the output matches your README.

### 7. Update the root README

Add your skill to the skills table and the skill details section in [`README.md`](README.md).

### 8. Open a pull request

---

## Improving an Existing Skill

- **Prompt improvements** — open a PR with a clear description of what the old prompt got wrong and what the new behavior is
- **Bug fixes** — reference any specific input that triggered the wrong output
- **README improvements** — always welcome; clarity and concrete examples are the goal

When editing an existing skill's `SKILL.md`, bump the `version` field in the frontmatter.

---

## Pull Request Guidelines

- **One skill per PR** — don't bundle multiple new skills into one PR
- **Test before submitting** — install the skill locally and verify it works
- **Describe the trigger** — in your PR description, explain what user input invokes the skill and what the expected output looks like
- **Match the existing style** — look at the other skills' `SKILL.md` and `README.md` files for formatting conventions
- **No external dependencies** — skills should work with Claude Code and Python stdlib only (no pip installs required at invocation time)

---

## Skill Quality Bar

A skill is ready to merge when:

- [ ] `SKILL.md` has valid frontmatter with `name` and `description`
- [ ] The skill name matches the directory name
- [ ] `README.md` exists and documents the skill concretely
- [ ] `LICENSE` is present (MIT)
- [ ] The skill has been tested locally and produces the described output
- [ ] The root `README.md` has been updated to include the new skill
- [ ] No external pip dependencies are required at runtime

---

Questions? Open an issue.
