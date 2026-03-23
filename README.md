<div align="center">

<br>

```
 ██████╗██╗      █████╗ ██╗   ██╗██████╗ ███████╗    ███████╗██╗  ██╗██╗██╗     ██╗     ███████╗
██╔════╝██║     ██╔══██╗██║   ██║██╔══██╗██╔════╝    ██╔════╝██║ ██╔╝██║██║     ██║     ██╔════╝
██║     ██║     ███████║██║   ██║██║  ██║█████╗      ███████╗█████╔╝ ██║██║     ██║     ███████╗
██║     ██║     ██╔══██║██║   ██║██║  ██║██╔══╝      ╚════██║██╔═██╗ ██║██║     ██║     ╚════██║
╚██████╗███████╗██║  ██║╚██████╔╝██████╔╝███████╗    ███████║██║  ██╗██║███████╗███████╗███████║
 ╚═════╝╚══════╝╚═╝  ╚═╝ ╚═════╝ ╚═════╝ ╚══════╝    ╚══════╝╚═╝  ╚═╝╚═╝╚══════╝╚══════╝╚══════╝
```

<br>

**Supercharge your Claude Code workflow with powerful `/skills`**

<br>

![Skills](https://img.shields.io/badge/Skills-3-7C3AED?style=for-the-badge&labelColor=1E293B)
![Claude Code](https://img.shields.io/badge/Claude_Code-Compatible-blueviolet?style=for-the-badge&logo=anthropic&logoColor=white&labelColor=1E293B)
![Platform](https://img.shields.io/badge/Platform-Windows_%7C_macOS_%7C_Linux-0EA5E9?style=for-the-badge&labelColor=1E293B)
![License](https://img.shields.io/badge/License-MIT-22C55E?style=for-the-badge&labelColor=1E293B)

<br>

</div>

---

<br>

## Skills

| Command | Name | Description | Docs |
|:--------|:-----|:------------|:----:|
| `/wrapped` | Claude Code Wrapped | Spotify Wrapped-style interactive terminal recap of your Claude Code usage — charts, stats, and developer archetype | [→](skills/wrapped/) |
| `/token-surgeon` | Token Surgeon | Audit any prompt against 10 named waste patterns, score efficiency 1–10, and cut tokens. Rewrites only on demand | [→](skills/token-surgeon/) |
| `/onboarding` | Onboarding Guide Generator | Deep-analyze any codebase and produce a fully tailored onboarding guide — architecture, setup, gotchas, and more | [→](skills/onboarding/) |

<br>

---

<br>

## Quick Install

<br>

**Clone the repo once, install any skill in seconds.**

<br>

```bash
git clone https://github.com/natedemoss/claude-code-skills.git
cd claude-code-skills
```

<br>

<details>
<summary><b>macOS / Linux</b></summary>

<br>

```bash
# Install all skills
cp -r skills/wrapped       ~/.claude/skills/wrapped
cp -r skills/token-surgeon ~/.claude/skills/token-surgeon
cp -r skills/onboarding    ~/.claude/skills/onboarding
```

</details>

<details>
<summary><b>Windows (PowerShell)</b></summary>

<br>

```powershell
# Install all skills
Copy-Item -Recurse skills\wrapped       "$env:USERPROFILE\.claude\skills\wrapped"
Copy-Item -Recurse skills\token-surgeon "$env:USERPROFILE\.claude\skills\token-surgeon"
Copy-Item -Recurse skills\onboarding    "$env:USERPROFILE\.claude\skills\onboarding"
```

</details>

<br>

> **Restart Claude Code** (or open a new session) after installing. Skills load automatically.

<br>

---

<br>

## Skill Details

<br>

### `/wrapped` — Claude Code Wrapped

Like Spotify Wrapped, but for your AI coding sessions. Reads your local Claude Code data — no uploads, no API calls, 100% private — and turns it into a **slide-by-slide terminal experience**.

<br>

| Slide | What You See |
|:------|:-------------|
| **Year at a Glance** | Total messages, sessions, tool calls, tokens, first session date |
| **Tools You Loved** | Bar chart of every tool ranked by usage |
| **When You Code** | Hour-by-hour heatmap with peak coding time |
| **Legendary Session** | Your longest session: duration + message count |
| **Your AI Fleet** | Model split — Haiku vs Sonnet vs Opus |
| **Your Claude Bill** | Estimated cost with daily / weekly / monthly projections |
| **Files You Couldn't Quit** | Most edited files across all projects |
| **Developer Archetype** | The Marathon Runner? The Automator? Find out. |

<br>

```bash
/wrapped
# SPACE / ENTER → next slide    Q / ESC → quit
```

<br>

→ [Full documentation](skills/wrapped/README.md)

<br>

---

<br>

### `/token-surgeon` — Token Surgeon

Audits any prompt against **10 named waste patterns**. Quotes every offending line, scores efficiency 1–10, and estimates exactly how many tokens you can recover. Never rewrites without your confirmation.

<br>

| # | Pattern | What It Catches |
|:-:|:--------|:----------------|
| 01 | **Hedging Language** | `"if possible"` `"please try to"` `"feel free to"` |
| 02 | **Role Throat-Clearing** | Verbose persona intros that bloat without adding constraint |
| 03 | **Restated Instructions** | The same rule expressed twice in different words |
| 04 | **Politeness Padding** | `"thank you"` `"please note that"` `"I appreciate your help"` |
| 05 | **Filler Affirmations** | `"Remember to always"` `"Make sure that"` `"It's very important"` |
| 06 | **Dead Context** | Background the model doesn't need to complete the task |
| 07 | **Redundant Formatting** | Multiple instructions that say the same thing |
| 08 | **Negation Bloat** | Three `"don't"` clauses where one positive instruction covers all |
| 09 | **Over-Specified Examples** | More examples than the pattern needs to register |
| 10 | **Scope Creep Instructions** | Rules for edge cases that appear 0.1% of the time |

<br>

```bash
/token-surgeon
# Paste any prompt → get analysis → confirm to rewrite
```

<br>

→ [Full documentation](skills/token-surgeon/README.md)

<br>

---

<br>

### `/onboarding` — Onboarding Guide Generator

Points at any codebase and produces a **fully tailored Markdown onboarding guide**. Every line references actual file paths, function names, and commands from the project. No generic boilerplate.

<br>

| Section | What You Get |
|:--------|:-------------|
| **What Is This?** | 1–3 sentence project summary |
| **Tech Stack** | Languages, frameworks, key libraries |
| **Project Structure** | Annotated directory tree |
| **How to Get Started** | Clone → install → configure → run |
| **Architecture Overview** | Data flow and system organization |
| **Key Files to Read First** | Ordered reading list with one-line reasons |
| **Domain Knowledge** | Concepts and patterns a new dev must know |
| **Running Tests** | Test suite commands and strategy notes |
| **Common Gotchas** | Non-obvious things that trip up new developers |
| **Where to Go Next** | Suggested first steps and areas to explore |

<br>

```bash
cd your-project/
/onboarding
# Full guide generated and printed to the conversation
```

<br>

→ [Full documentation](skills/onboarding/README.md)

<br>

---

<br>

## Contributing

Want to add a skill or improve an existing one?

Read the [Contributing Guide](CONTRIBUTING.md) — it covers skill structure, PR guidelines, and how to get your skill added to this collection.

<br>

---

<br>

<div align="center">

Built for [Claude Code](https://claude.ai/claude-code) &nbsp;·&nbsp; MIT License &nbsp;·&nbsp; [Contributing](CONTRIBUTING.md)

<br>

*If this saved you time, consider leaving a star.*

</div>
