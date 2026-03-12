---
tags:
  - study
  - meta
  - index
---

# 📚 Weekly Study Plan

> **Goal:** Work through the Clean Code video series and the Anthropic [Claude Code in Action](https://anthropic.skilljar.com/claude-code-in-action) course at a steady, sustainable pace — and build a rich linked knowledge graph of notes along the way.
>
> **How notes work:** After each video or lesson, create a new note using the [[_Templates/Video Note Template]] and save it inside `Notes/`. Fill in the connections section — even one `[[link]]` makes a visible difference in the graph. See the [[_Graph/Graph Legend]] for how the tags and links work.

---

## 🗓️ Overview

| Week | Theme | Clean Code Focus | Anthropic Course |
|------|-------|-----------------|-----------------|
| 1 | Foundations | Intro & naming principles | Basics: architecture & setup |
| 2 | Functions | What makes a good function | Intermediate: context & custom commands |
| 3 | Structure & Form | How code should look and feel | Advanced: MCP & GitHub workflows |
| 4 | TDD & Architecture | Testing and big-picture design | Expert: Hooks and the SDK |

---

## Week 1 — Foundations

**Theme:** What is clean code and why does naming matter?

### Clean Code Videos
- [ ] [[01 - Introduction]] `#week/1` `#topic/naming` `#source/clean-code`
- [ ] [[02 - Clean Code (Remake)]] `#week/1` `#topic/naming` `#source/clean-code`
- [ ] [[03 - Names++]] `#week/1` `#topic/naming` `#source/clean-code`

### Anthropic: Claude Code in Action — Part 1: Basics
- [ ] [[CC01 - Welcome & Course Overview]] `#week/1` `#topic/claude-code` `#source/anthropic`
- [ ] [[CC02 - What Is Claude Code]] `#week/1` `#topic/claude-code` `#source/anthropic`
- [ ] [[CC03 - Getting Started & Setup]] `#week/1` `#topic/claude-code` `#source/anthropic`

### 🧪 Exercise — Week 1

**Codebase:** [`lodash`](https://github.com/lodash/lodash)

Lodash is one of the most widely-used JavaScript utility libraries and has excellent naming conventions. It's small enough to navigate but rich enough to study.

**Tasks:**
1. Clone the repo: `git clone https://github.com/lodash/lodash.git`
2. Open `src/` and pick 5 functions. For each one, answer: *Does the name tell you exactly what it does without reading the body?*
3. Find one function whose name you think could be better. Write a short note explaining why and what you'd rename it to.
4. Try Claude Code: open the repo and ask `"Explain the naming conventions used in this codebase"`. Compare its analysis to your own.
5. Save your write-up as `Exercises/Exercise - Week 1 - [your name].md`

---

## Week 2 — Functions

**Theme:** Functions are the basic unit of clean code — learn to write them well.

### Clean Code Videos
- [ ] [[04 - Functions]] `#week/2` `#topic/functions` `#source/clean-code`
- [ ] [[05 - Functions Screencast — Testable HTML]] `#week/2` `#topic/functions` `#source/clean-code`
- [ ] [[06 - Functions Screencast — Prime Generator]] `#week/2` `#topic/functions` `#source/clean-code`
- [ ] [[07 - Functions Screencast — Video Store]] `#week/2` `#topic/functions` `#source/clean-code`

### Anthropic: Claude Code in Action — Part 2: Intermediate
- [ ] [[CC04 - Context Management]] `#week/2` `#topic/claude-code` `#source/anthropic`
- [ ] [[CC05 - Custom Commands]] `#week/2` `#topic/claude-code` `#source/anthropic`
- [ ] [[CC06 - Practical Refactoring with Claude Code]] `#week/2` `#topic/claude-code` `#source/anthropic`

### 🧪 Exercise — Week 2

**Codebase:** [`axios`](https://github.com/axios/axios)

Axios is the most popular HTTP client for JavaScript. Its source code (~2,000 lines) is a masterclass in small, single-purpose functions.

**Tasks:**
1. Clone the repo: `git clone https://github.com/axios/axios.git`
2. Open `lib/core/Axios.js`. Count the number of functions. How many do more than one thing?
3. Find a function longer than 20 lines. Use Claude Code to refactor it: `"Refactor this function to follow the single responsibility principle"`. Review and critique the output.
4. Write a note: *What patterns from this week's videos did you actually see in the axios source?*
5. **Bonus:** Submit a real PR to axios if you find a genuine improvement (their CONTRIBUTING guide is beginner-friendly).
6. Save your write-up as `Exercises/Exercise - Week 2 - [your name].md`

---

## Week 3 — Structure & Form

**Theme:** Good code has a visual and structural rhythm.

### Clean Code Videos
- [ ] [[08 - Function Structure]] `#week/3` `#topic/structure` `#source/clean-code`
- [ ] [[09 - Function Structure Screencast — Stack]] `#week/3` `#topic/structure` `#source/clean-code`
- [ ] [[10 - Form]] `#week/3` `#topic/structure` `#source/clean-code`
- [ ] [[11 - Form Screencast — Lychrel]] `#week/3` `#topic/structure` `#source/clean-code`

### Anthropic: Claude Code in Action — Part 3: Advanced
- [ ] [[CC07 - MCP Server Integration]] `#week/3` `#topic/claude-code` `#source/anthropic`
- [ ] [[CC08 - GitHub Workflows with Claude Code]] `#week/3` `#topic/claude-code` `#source/anthropic`

### 🧪 Exercise — Week 3

**Codebase:** [`express`](https://github.com/expressjs/express)

Express.js is the gold standard of clean, readable Node.js code. The entire framework is under 5,000 lines — intentionally minimal and beautifully structured.

**Tasks:**
1. Clone the repo: `git clone https://github.com/expressjs/express.git`
2. Read `lib/application.js` top to bottom. Note: the file reads almost like a prose document. Why?
3. Pick any file in `lib/` and draw (or describe) its vertical structure: how much is at the top level? How deeply nested does it go?
4. Use Claude Code with MCP integration (from this week's Anthropic module): connect Claude Code to GitHub and ask it to `"Review the structure of lib/router/index.js and suggest improvements based on clean code principles"`.
5. Save your write-up as `Exercises/Exercise - Week 3 - [your name].md`

---

## Week 4 — TDD & Architecture

**Theme:** Tests drive better design; architecture shapes the whole system.

### Clean Code Videos
- [ ] [[12 - TDD — Part 1]] `#week/4` `#topic/tdd` `#source/clean-code`
- [ ] [[13 - TDD — Part 2]] `#week/4` `#topic/tdd` `#source/clean-code`
- [ ] [[14 - Architecture, Use Cases and High Level Design]] `#week/4` `#topic/architecture` `#source/clean-code`

### Anthropic: Claude Code in Action — Part 4: Expert
- [ ] [[CC09 - Hooks in Claude Code]] `#week/4` `#topic/claude-code` `#source/anthropic`
- [ ] [[CC10 - The Claude Code SDK]] `#week/4` `#topic/claude-code` `#source/anthropic`

### 🧪 Exercise — Week 4

**Codebase:** [`jest`](https://github.com/jestjs/jest)

What better way to study TDD than to read the source of the testing framework itself? Jest's packages folder contains real TDD in action.

**Tasks:**
1. Clone the repo: `git clone https://github.com/jestjs/jest.git`
2. Open `packages/jest-each/src/` — a self-contained package. Read the tests in `__tests__/` *before* reading the source. Try to guess the implementation from the tests alone.
3. Pick one package. Use Claude Code's SDK to write a small script that asks Claude Code to `"Identify the architectural boundaries in this package and explain which layer each file belongs to"`.
4. Reflect: *Did the tests you read actually drive a better design? What evidence do you see in the code?*
5. **Bonus:** Write one new test for any jest package and submit it as a PR.
6. Save your write-up as `Exercises/Exercise - Week 4 - [your name].md`

---

## 📝 Notes & Takeaways

### Key Concepts
-

### Things to Try in My Own Code
-

### Questions to Explore
-

---

## 🔗 Resources

- **Clean Code videos:** `/Users/admin/Study/`
- **Anthropic — Claude Code in Action:** [https://anthropic.skilljar.com/claude-code-in-action](https://anthropic.skilljar.com/claude-code-in-action)
- **Note template:** [[_Templates/Video Note Template]]
- **Graph guide:** [[_Graph/Graph Legend]]

---

*Created: 2026-03-12 · See [CONTRIBUTING.md](CONTRIBUTING.md) on GitHub for how to add your notes*
