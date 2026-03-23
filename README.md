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

## ✦ &nbsp;Skills

<br>

<table>
<tr>
<td width="33%" align="center">

### 🎁 &nbsp;`/wrapped`

**Claude Code Wrapped**

Spotify Wrapped, but for your AI coding sessions. Interactive slide-by-slide terminal recap with charts, stats, and your developer archetype.

<br>

![Slides](https://img.shields.io/badge/Slides-10-7C3AED?style=flat-square&labelColor=1E293B)
![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=flat-square&labelColor=1E293B)
![Private](https://img.shields.io/badge/100%25-Private-22C55E?style=flat-square&labelColor=1E293B)

<br>

[→ View Skill](skills/wrapped/)

</td>
<td width="33%" align="center">

### 🔪 &nbsp;`/token-surgeon`

**Token Surgeon**

Scan any prompt against 10 named waste patterns. Get an efficiency score, quoted offending lines, and recoverable token count. Rewrites only on demand.

<br>

![Patterns](https://img.shields.io/badge/Waste_Patterns-10-EF4444?style=flat-square&labelColor=1E293B)
![Score](https://img.shields.io/badge/Efficiency_Score-1--10-F59E0B?style=flat-square&labelColor=1E293B)
![Phase](https://img.shields.io/badge/Rewrite-On_Demand-0EA5E9?style=flat-square&labelColor=1E293B)

<br>

[→ View Skill](skills/token-surgeon/)

</td>
<td width="33%" align="center">

### 🗺️ &nbsp;`/onboarding`

**Onboarding Guide Generator**

Deep-analyze any codebase and produce a fully tailored onboarding guide. Architecture, setup, key files, gotchas — all specific to the project.

<br>

![Sections](https://img.shields.io/badge/Sections-10-22C55E?style=flat-square&labelColor=1E293B)
![Languages](https://img.shields.io/badge/Any_Language-Supported-84CC16?style=flat-square&labelColor=1E293B)
![Output](https://img.shields.io/badge/Output-Markdown-6366F1?style=flat-square&labelColor=1E293B)

<br>

[→ View Skill](skills/onboarding/)

</td>
</tr>
</table>

<br>

---

<br>

## ⚡ &nbsp;Quick Install

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
cp -r skills/wrapped      ~/.claude/skills/wrapped
cp -r skills/token-surgeon ~/.claude/skills/token-surgeon
cp -r skills/onboarding   ~/.claude/skills/onboarding
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

## 📖 &nbsp;Skill Details

<br>

### 🎁 &nbsp;`/wrapped` &nbsp;—&nbsp; Claude Code Wrapped

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

### 🔪 &nbsp;`/token-surgeon` &nbsp;—&nbsp; Token Surgeon

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

### 🗺️ &nbsp;`/onboarding` &nbsp;—&nbsp; Onboarding Guide Generator

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

## 🤝 &nbsp;Contributing

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
