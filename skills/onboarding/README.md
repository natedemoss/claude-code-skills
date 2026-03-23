[![Claude Code](https://img.shields.io/badge/Claude_Code-Skill-blueviolet?style=flat-square&logo=anthropic&logoColor=white)](https://claude.ai/claude-code)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)

# claude-onboard

A `/onboarding` skill for [Claude Code](https://claude.ai/claude-code) that generates a comprehensive, project-specific onboarding guide for any codebase.

Point it at a repo and get a fully tailored guide covering the tech stack, architecture, setup steps, key files, domain concepts, gotchas, and where to start — in seconds.

---

## What It Does

Runs a deep analysis of your current working directory and produces a structured Markdown onboarding guide with these sections:

| Section | What you get |
|:--------|:-------------|
| **What Is This?** | 1-3 sentence project summary |
| **Tech Stack** | Languages, frameworks, and key libraries |
| **Project Structure** | Annotated directory tree of important files |
| **How to Get Started** | Clone → install → configure → run |
| **Architecture Overview** | How the system is organized and data flows through it |
| **Key Files to Read First** | Ordered reading list with one-line reasons |
| **Important Concepts** | Domain knowledge and patterns a new dev needs |
| **Running Tests** | How to run the test suite and test strategy notes |
| **Common Gotchas** | Non-obvious things that trip up new developers |
| **Where to Go Next** | Suggested first steps and areas to explore |

Every line is tailored to the specific project — no generic boilerplate.

---

## Installation

**1. Clone and copy the skill:**

```bash
git clone https://github.com/natedemoss/claude-onboard.git

# macOS / Linux
cp -r claude-onboard ~/.claude/skills/onboarding

# Windows (PowerShell)
Copy-Item -Recurse claude-onboard "$env:USERPROFILE\.claude\skills\onboarding"
```

**2. That's it.** No dependencies, no API keys, no config.

---

## Usage

Navigate to any project directory and type:

```
/onboarding
```

Claude will explore the codebase and return a full onboarding guide.

---

## Requirements

- [Claude Code](https://claude.ai/claude-code) installed
- A codebase to analyze (works on any language or framework)

---

Made for [Claude Code](https://claude.ai/claude-code). If this was useful, consider giving a star.
