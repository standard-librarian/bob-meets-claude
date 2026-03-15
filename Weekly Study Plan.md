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
| 1 | Foundations | Intro & naming principles | Course Overview |
| 2 | Functions | What makes a good function | Getting hands on (pt. 1): setup & context |
| 3 | Structure & Form | How code should look and feel | Getting hands on (pt. 2): MCP & GitHub |
| 4 | TDD & Architecture | Testing and big-picture design | Hooks and the SDK |

---

## Week 1 — Foundations

**Theme:** What is clean code and why does naming matter?

### Clean Code Videos
- [ ] [[01 - Introduction]] `#week/1` `#topic/naming` `#source/clean-code`
- [ ] [[02 - Clean Code (Remake)]] `#week/1` `#topic/naming` `#source/clean-code`
- [ ] [[03 - Names++]] `#week/1` `#topic/naming` `#source/clean-code`

### Anthropic: Claude Code in Action — Course Overview
- [ ] [[CC01 - Introduction]] `#week/1` `#topic/claude-code` `#source/anthropic`
- [ ] [[CC02 - What is a coding assistant?]] `#week/1` `#topic/claude-code` `#source/anthropic`
- [ ] [[CC03 - Claude Code in action]] `#week/1` `#topic/claude-code` `#source/anthropic`

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

### Anthropic: Claude Code in Action — Getting hands on (pt. 1)
- [ ] [[CC04 - Claude Code setup]] `#week/2` `#topic/claude-code` `#source/anthropic`
- [ ] [[CC05 - Project setup]] `#week/2` `#topic/claude-code` `#source/anthropic`
- [ ] [[CC06 - Adding context]] `#week/2` `#topic/claude-code` `#source/anthropic`
- [ ] [[CC07 - Making changes]] `#week/2` `#topic/claude-code` `#source/anthropic`
- [ ] [[CC08 - Course satisfaction survey]] `#week/2` `#topic/claude-code` `#source/anthropic`
- [ ] [[CC09 - Controlling context]] `#week/2` `#topic/claude-code` `#source/anthropic`
- [ ] [[CC10 - Custom commands]] `#week/2` `#topic/claude-code` `#source/anthropic`

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

### Anthropic: Claude Code in Action — Getting hands on (pt. 2)
- [ ] [[CC11 - MCP servers with Claude Code]] `#week/3` `#topic/claude-code` `#source/anthropic`
- [ ] [[CC12 - Github integration]] `#week/3` `#topic/claude-code` `#source/anthropic`

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

### Anthropic: Claude Code in Action — Hooks and the SDK
- [ ] [[CC13 - Introducing hooks]] `#week/4` `#topic/claude-code` `#source/anthropic`
- [ ] [[CC14 - Defining hooks]] `#week/4` `#topic/claude-code` `#source/anthropic`
- [ ] [[CC15 - Implementing a hook]] `#week/4` `#topic/claude-code` `#source/anthropic`
- [ ] [[CC16 - Gotchas around hooks]] `#week/4` `#topic/claude-code` `#source/anthropic`
- [ ] [[CC17 - Useful hooks!]] `#week/4` `#topic/claude-code` `#source/anthropic`
- [ ] [[CC18 - Another useful hook]] `#week/4` `#topic/claude-code` `#source/anthropic`
- [ ] [[CC19 - The Claude Code SDK]] `#week/4` `#topic/claude-code` `#source/anthropic`

### Anthropic: Claude Code in Action — Wrapping up
- [ ] [[CC20 - Quiz on Claude Code]] `#week/4` `#topic/claude-code` `#source/anthropic`
- [ ] [[CC21 - Summary and next steps]] `#week/4` `#topic/claude-code` `#source/anthropic`

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

## 🌍 Multi-Language Exercises

> These are alternative exercises for each week, covering Go, Java, Python, and Rust. Pick the language you know (or want to learn) — the clean code lessons apply identically across all of them. You can do one language or all of them. Contribute your write-up as `Exercises/Exercise - Week N - Lang - [your name].md`.

---

### Week 1 (Naming) — Go: `cobra`

**Codebase:** [`spf13/cobra`](https://github.com/spf13/cobra)

Cobra is the CLI framework behind Kubernetes, Hugo, and GitHub CLI. The Go standard library is famous for terse but precise naming — cobra exemplifies this at the library level.

**Tasks:**
1. Clone: `git clone https://github.com/spf13/cobra.git`
2. Open `command.go`. Go naming avoids redundant context — e.g. a method on `Command` is never named `CommandRun`, just `Run`. Find 5 names that follow this rule and 1 that you think breaks it.
3. Compare Go's naming style (short, no underscores, context-from-type) to the JS style in lodash. Write a paragraph on the trade-offs.
4. Ask Claude Code: `"What are the naming conventions in this Go codebase and how do they compare to Uncle Bob's rules?"` — Go idioms sometimes conflict with Uncle Bob; document where and why.

---

### Week 1 (Naming) — Java: `guava`

**Codebase:** [`google/guava`](https://github.com/google/guava)

Google Guava is the gold standard of Java library design. It's also a study in how verbose Java naming can become — and when that verbosity is actually helpful.

**Tasks:**
1. Clone: `git clone https://github.com/google/guava.git`
2. Open `guava/src/com/google/common/collect/` and pick any 3 classes. Java names tend to be long and fully qualified — does the length add clarity or noise?
3. Find a method whose name you think is too long. Propose a shorter alternative and argue whether it would be better or worse in context.
4. Ask Claude Code: `"Identify any naming inconsistencies across the classes in this package"`.

---

### Week 2 (Functions) — Go: `gin`

**Codebase:** [`gin-gonic/gin`](https://github.com/gin-gonic/gin)

Gin is the most popular Go web framework. Go encourages small functions and explicit error returns — gin shows what this looks like at scale.

**Tasks:**
1. Clone: `git clone https://github.com/gin-gonic/gin.git`
2. Open `context.go`. This is gin's core file. How long are the functions? Go convention favours shorter functions than Uncle Bob even — does gin follow that?
3. Find a function that takes more than 3 parameters. In Go, this is often a sign something is wrong. Use Claude Code: `"Suggest how to reduce the parameter count of this function using idiomatic Go"`.
4. Compare gin's error-handling pattern (multiple return values) to JavaScript's try/catch. How does the language shape function design?

---

### Week 2 (Functions) — Python: `requests`

**Codebase:** [`psf/requests`](https://github.com/psf/requests)

Requests is the most downloaded Python package ever and is famous for being "HTTP for Humans." Its source is a case study in making complex behaviour feel simple through function design.

**Tasks:**
1. Clone: `git clone https://github.com/psf/requests.git`
2. Open `requests/api.py` — the public-facing API. It's very short. Why? Where does the actual work happen?
3. Trace the call chain from `requests.get()` all the way down to the socket. Count how many functions are involved. Does each one do exactly one thing?
4. Ask Claude Code: `"Draw the call chain from requests.get() to the underlying urllib3 connection and label each function's single responsibility"`.

---

### Week 3 (Structure & Form) — Rust: `ripgrep`

**Codebase:** [`BurntSushi/ripgrep`](https://github.com/BurntSushi/ripgrep)

Ripgrep is one of the most respected Rust codebases in existence. It's fast, correct, and beautifully structured. Rust's module system enforces clean boundaries in a way no other language does.

**Tasks:**
1. Clone: `git clone https://github.com/BurntSushi/ripgrep.git`
2. Open the `crates/` directory. Each crate is a hard architectural boundary — map out what each one is responsible for. This is Uncle Bob's "use cases and layers" made concrete by the compiler.
3. Open `crates/core/src/search.rs`. Read the file from top to bottom. Does it read like prose? Where does it break down?
4. Use Claude Code with MCP: `"Map the architectural layers in this Rust workspace and identify which crates correspond to Uncle Bob's entities, use cases, and interface adapters"`.

---

### Week 3 (Structure & Form) — Java: `spring-framework`

**Codebase:** [`spring-projects/spring-framework`](https://github.com/spring-projects/spring-framework)

Spring is one of the most architecturally deliberate Java projects ever built. It's also famously complex — which makes it a perfect case study in how structure can help or hurt readability.

**Tasks:**
1. Clone: `git clone https://github.com/spring-projects/spring-framework.git`
2. Pick one module (e.g. `spring-core` or `spring-web`). Open its `src/main/java/` tree. Notice how deeply packages are nested. Does the depth help or hurt navigation?
3. Find a class that has grown too large (over 500 lines). Use Claude Code: `"Identify the responsibilities of this class and suggest how to split it following the single responsibility principle"`.
4. Write a note: *What does Java's verbosity do to form? Is it always noise, or sometimes signal?*

---

### Week 4 (TDD & Architecture) — Go: `testify`

**Codebase:** [`stretchr/testify`](https://github.com/stretchr/testify)

Testify is Go's most popular testing library — the direct equivalent of Jest. Reading its source while studying TDD gives you the same meta-insight as studying jest in JavaScript.

**Tasks:**
1. Clone: `git clone https://github.com/stretchr/testify.git`
2. Open `assert/assertions.go`. Every assertion is a small, single-purpose function. Count how many there are. How is the file structured so it doesn't become unreadable at that length?
3. Open `assert/assertions_test.go`. The tests test the testing library — read 10 of them before reading the corresponding implementation. Were you able to predict the code?
4. Ask Claude Code: `"Identify the architectural layers of the testify library and explain how the suite, assert, require, and mock packages relate to each other"`.

---

### Week 4 (TDD & Architecture) — Java: `junit5`

**Codebase:** [`junit-team/junit5`](https://github.com/junit-team/junit5)

JUnit 5 is the ground-up rewrite of Java's oldest testing framework. The rewrite was explicitly guided by clean architecture principles — which makes reading it alongside Uncle Bob's architecture lecture particularly rewarding.

**Tasks:**
1. Clone: `git clone https://github.com/junit-team/junit5.git`
2. Open the `junit-platform-engine/` module. This is the core abstraction layer. Notice it has no dependencies on any specific test runner — it's a pure use-case layer. How does this map to Uncle Bob's dependency rule?
3. Find a test inside `junit-jupiter-engine/src/test/` and read it before reading the source it's testing. Could you have written the implementation from the test alone?
4. Ask Claude Code: `"Show how junit5's module structure maps to the Clean Architecture dependency rule — which modules are the core, which are the adapters?"`.

---

### Week 4 (TDD & Architecture) — Python: `pytest`

**Codebase:** [`pytest-dev/pytest`](https://github.com/pytest-dev/pytest)

Pytest is Python's dominant test framework and has a beautifully plugin-based architecture. Its internals are a lesson in designing for extensibility without sacrificing clarity.

**Tasks:**
1. Clone: `git clone https://github.com/pytest-dev/pytest.git`
2. Open `src/_pytest/` and read `hookspec.py`. Pytest's whole architecture is driven by a hook system — every extension point is declared here. How does this shape the rest of the codebase?
3. Pick any plugin in `src/_pytest/` (e.g. `capture.py` or `tmpdir.py`). Read its tests in `testing/` first.
4. Ask Claude Code: `"Explain pytest's plugin architecture and identify which files represent the core domain vs. the plugin boundary vs. the built-in adapters"`.

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
