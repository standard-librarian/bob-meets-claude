# Clean Code × Claude Code — Study Plan

A 4-week structured study of Robert C. Martin's **Clean Code** video series combined with Anthropic's **[Claude Code in Action](https://anthropic.skilljar.com/claude-code-in-action)** course. This repo is a living knowledge base — every video gets its own note, and every note links to others, building a graph of everything we've learned.

**This is a collaborative project.** You can contribute your own notes for any video or lesson, complete the exercises, and share what you found. See [CONTRIBUTING.md](CONTRIBUTING.md) for how.

---

## What's in This Repo

```
study/
├── Weekly Study Plan.md        ← Start here — the full 4-week schedule
├── README.md                   ← This file
├── CONTRIBUTING.md             ← How to contribute notes and exercises
├── _Templates/
│   └── Video Note Template.md  ← Copy this when taking notes on a video
└── _Graph/
    └── Graph Legend.md         ← How tags and links work for the graph view
```

Each video and lesson gets its own note, created from the template. Notes are tagged and linked to each other — open the vault in [Obsidian](https://obsidian.md) to see the full graph of everything studied.

---

## The Curriculum

### Part A — Clean Code (14 videos, Robert C. Martin)

| # | Video | Week | Topic |
|---|-------|------|-------|
| 01 | Introduction | 1 | Foundations |
| 02 | Clean Code (Remake) | 1 | Foundations |
| 03 | Names++ | 1 | Naming |
| 04 | Functions | 2 | Functions |
| 05 | Functions Screencast — Testable HTML | 2 | Functions |
| 06 | Functions Screencast — Prime Generator | 2 | Functions |
| 07 | Functions Screencast — Video Store | 2 | Functions |
| 08 | Function Structure | 3 | Structure |
| 09 | Function Structure Screencast — Stack | 3 | Structure |
| 10 | Form | 3 | Form |
| 11 | Form Screencast — Lychrel | 3 | Form |
| 12 | TDD — Part 1 | 4 | TDD |
| 13 | TDD — Part 2 | 4 | TDD |
| 14 | Architecture, Use Cases and High Level Design | 4 | Architecture |

### Part B — Claude Code in Action (21 lessons, Anthropic)

| # | Lesson | Week | Section |
|---|--------|------|---------|
| CC01 | Introduction | 1 | Course Overview |
| CC02 | What is a coding assistant? | 1 | Course Overview |
| CC03 | Claude Code in action | 1 | Course Overview |
| CC04 | Claude Code setup | 2 | Getting hands on |
| CC05 | Project setup | 2 | Getting hands on |
| CC06 | Adding context | 2 | Getting hands on |
| CC07 | Making changes | 2 | Getting hands on |
| CC08 | Course satisfaction survey | 2 | Getting hands on |
| CC09 | Controlling context | 2 | Getting hands on |
| CC10 | Custom commands | 2 | Getting hands on |
| CC11 | MCP servers with Claude Code | 3 | Getting hands on |
| CC12 | Github integration | 3 | Getting hands on |
| CC13 | Introducing hooks | 4 | Hooks and the SDK |
| CC14 | Defining hooks | 4 | Hooks and the SDK |
| CC15 | Implementing a hook | 4 | Hooks and the SDK |
| CC16 | Gotchas around hooks | 4 | Hooks and the SDK |
| CC17 | Useful hooks! | 4 | Hooks and the SDK |
| CC18 | Another useful hook | 4 | Hooks and the SDK |
| CC19 | The Claude Code SDK | 4 | Hooks and the SDK |
| CC20 | Quiz on Claude Code | 4 | Wrapping up |
| CC21 | Summary and next steps | 4 | Wrapping up |

---

## Weekly Exercises

Each week has a hands-on exercise applied to a real open-source codebase. **Choose your language** — the clean code principles apply identically across all of them:

| Week | Focus | JavaScript | Go | Java | Python | Rust |
|------|-------|------------|-----|------|--------|------|
| 1 | Naming | [lodash](https://github.com/lodash/lodash) | [cobra](https://github.com/spf13/cobra) | [guava](https://github.com/google/guava) | — | — |
| 2 | Functions | [axios](https://github.com/axios/axios) | [gin](https://github.com/gin-gonic/gin) | — | [requests](https://github.com/psf/requests) | — |
| 3 | Structure & Form | [express](https://github.com/expressjs/express) | — | [spring-framework](https://github.com/spring-projects/spring-framework) | — | [ripgrep](https://github.com/BurntSushi/ripgrep) |
| 4 | TDD & Architecture | [jest](https://github.com/jestjs/jest) | [testify](https://github.com/stretchr/testify) | [junit5](https://github.com/junit-team/junit5) | [pytest](https://github.com/pytest-dev/pytest) | — |

Full exercise instructions for all languages are in the [Weekly Study Plan](study/Weekly%20Study%20Plan.md).

---

## How to Take Notes (and Why)

When you finish a video, create a note from the template. Fill in:

- **Key Takeaways** — 2–3 ideas that stuck
- **Connections** — links to other notes in the vault (this builds the graph)
- **Code snippet** — a short example that illustrates the concept

After all 4 weeks, open the graph view in Obsidian. Topics that are deeply connected will form visible clusters. Isolated notes are prompts to go back and add links.

---

## Get the Certificate

Completing the Anthropic course earns you an **official Anthropic certificate** you can add to your LinkedIn. Enroll free at [anthropic.skilljar.com](https://anthropic.skilljar.com/claude-code-in-action) — you only need a Skilljar account.

---

## Questions?

Open an issue or start a discussion. PRs for notes, exercise write-ups, and improvements to the plan are all welcome.
