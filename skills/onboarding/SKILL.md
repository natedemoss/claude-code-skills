---
name: onboarding
description: Onboarding Guide Generator
---

# Onboarding Guide Generator

You are an expert software engineer tasked with generating a comprehensive onboarding guide for a developer who is new to this codebase.

## Instructions

Analyze the current repository thoroughly and produce a well-structured onboarding guide in Markdown. Your analysis should cover:

### 1. Explore the Repository
- Read `README.md`, `CLAUDE.md`, `CONTRIBUTING.md`, or any other top-level docs
- Identify the project type (web app, API, CLI, library, monorepo, etc.)
- Detect the language(s) and framework(s) in use
- Read `package.json`, `pyproject.toml`, `Cargo.toml`, `go.mod`, or equivalent dependency manifest
- Scan the top-level directory structure to understand how the project is organized

### 2. Understand the Architecture
- Identify the main entry points (e.g., `main.py`, `index.ts`, `cmd/`, `src/`)
- Trace the high-level data/request flow through the system
- Identify key modules, layers, or domains (e.g., routes, controllers, services, models, utils)
- Note any non-obvious architectural decisions or patterns

### 3. Understand How to Run It
- Find how to install dependencies
- Find how to run the app locally (dev server, CLI, etc.)
- Find how to run tests
- Note any required environment variables or config files (`.env.example`, `config/`, etc.)

### 4. Identify Key Concepts
- What domain knowledge does a new developer need?
- What are the most important files to read first?
- Are there any gotchas, quirks, or non-obvious behaviors worth flagging?

---

## Output Format

Produce the guide in this structure:

```
# Onboarding Guide: [Project Name]

## What Is This?
[1-3 sentence summary of what the project does and who it's for]

## Tech Stack
[Bullet list of languages, frameworks, and key libraries]

## Project Structure
[Annotated directory tree of the most important folders/files]

## How to Get Started
[Step-by-step setup: clone → install → configure → run]

## Architecture Overview
[How the system is organized and how data flows through it]

## Key Files to Read First
[Ordered list of files a new dev should read, with a one-line reason for each]

## Important Concepts & Domain Knowledge
[Any domain-specific terms, patterns, or business logic a new dev needs to understand]

## Running Tests
[How to run the test suite, and any notes on test strategy]

## Common Gotchas
[Non-obvious things that will trip up a new developer]

## Where to Go Next
[Suggested next steps: good first issues, areas to explore, people to ask]
```

Be specific and concrete. Reference actual file paths, function names, and commands from the codebase. Do not write generic advice — every line should be tailored to this specific project.
