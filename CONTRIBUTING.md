# Contributing to the Study Plan

Welcome! This is a collaborative study project. Anyone can contribute notes for videos they've watched, write up an exercise they completed, or improve the plan itself. Everything happens through pull requests.

---

## What You Can Contribute

There are four types of contributions, each with a different process:

**1. Video / lesson notes** — a note for a specific video or Anthropic lesson you watched
**2. Exercise write-ups** — your findings from one of the weekly hands-on exercises
**3. Corrections or improvements** — fixing something wrong or unclear in an existing note
**4. Plan improvements** — suggesting better exercises, resources, or restructuring

---

## Before You Start

1. Fork this repo and clone it locally.
2. Open the vault in [Obsidian](https://obsidian.md) (free) to get the full linked experience, but any text editor works.
3. Check the open issues and existing PRs — someone may already be working on the same note.

---

## How to Add a Video Note

This is the most common type of contribution.

### Step 1 — Copy the template

Duplicate `_Templates/Video Note Template.md` and name the file after the video:

```
01 - Introduction.md
04 - Functions.md
CC03 - Getting Started & Setup.md
```

Use the exact names from the table in `README.md` — this is what makes the Obsidian links work.

### Step 2 — Fill in the frontmatter

At the top of the file, fill in the YAML block:

```yaml
---
title: "Functions"
date: 2026-03-15
source: "clean-code"       # or "anthropic"
week: 2
topic: "functions"         # naming | functions | structure | tdd | architecture | claude-code
status: watched
tags:
  - study
  - week/2
  - source/clean-code
  - topic/functions
---
```

**Valid values for `topic`:** `naming` · `functions` · `structure` · `tdd` · `architecture` · `claude-code`
**Valid values for `source`:** `clean-code` · `anthropic`

### Step 3 — Write the note

Fill in each section of the template honestly. The most valuable parts are:

- **Connections** — link to at least one other note using `[[note name]]`. This is what builds the graph.
- **Open Questions** — don't skip this. Unanswered questions are the most interesting part.
- **Code Snippet** — even a 3-line example is worth including.

### Step 4 — Link back to the Weekly Study Plan

At the very bottom of your note, make sure the link to `[[Weekly Study Plan]]` is there (it's already in the template).

---

## How to Add an Exercise Write-Up

Each week has an exercise against a specific codebase (see the Weekly Study Plan). You can contribute your write-up even if someone else already did — multiple perspectives on the same exercise are encouraged.

### File naming

```
Exercise - Week 2 - [Your GitHub username].md
```

Example: `Exercise - Week 2 - mdht.md`

### What to include

Structure your write-up loosely around the exercise tasks:

- What you found (code examples welcome, keep them short)
- What surprised you
- What Claude Code said vs. what you thought
- What you'd do differently in your own code

There's no strict template for exercise write-ups — write it the way you'd explain it to a friend.

---

## Submitting Your PR

1. Create a branch named after your contribution:
   ```
   git checkout -b note/04-functions
   git checkout -b exercise/week-2-username
   ```

2. Commit with a clear message:
   ```
   git commit -m "Add note: 04 - Functions"
   git commit -m "Add exercise write-up: Week 2 (axios) - username"
   ```

3. Open a PR against `main`. In the PR description, mention:
   - Which video or exercise it covers
   - Anything you're unsure about or want feedback on
   - If you left any sections blank and why

---

## Review Process

PRs for notes are reviewed for:

- **Correct frontmatter** — tags and metadata must match the spec above
- **At least one `[[wikilink]]` connection** — every note should connect to at least one other
- **No spoilers in PR titles** — some contributors haven't watched ahead yet

PRs are merged as-is if the content is honest and the format is correct. There are no wrong opinions about code.

---

## Style Guide

- Write in first person ("I noticed…", "This made me think…") — these are personal study notes, not Wikipedia.
- Keep code snippets under 20 lines. Link to a file in the exercise repo for longer examples.
- Use `[[double brackets]]` for all internal links — never bare filenames.
- Don't edit someone else's note. Open an issue or leave a comment on their PR instead.

---

## Questions

Open a GitHub Discussion or drop a comment in any PR. There are no silly questions.
