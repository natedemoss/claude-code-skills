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
