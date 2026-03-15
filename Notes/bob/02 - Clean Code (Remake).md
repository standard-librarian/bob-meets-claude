---
title: "Clean Code (Remake)"
date: 2026-03-15
source: "clean-code"
week: 1
topic: "foundations"
status: watched
tags:
  - study
  - "week/1"
  - "source/clean-code"
  - "topic/foundations"
---

# 02 - Clean Code (Remake)

> **Source:** [[Weekly Study Plan]] · **Week 1** · 2026-03-15

---

This is the remake of episode 1 — the actual business case episode. Uncle Bob makes the argument for why clean code matters, defines what it smells like when it doesn't exist, and ends with expert definitions of what it does.

---

## 🎯 Key Takeaways

- **The Sword Inc. story**: A company with a great C debugger rushed the C++ port, made an unworkable mess, and went bankrupt. The developer's postmortem: *"The reason we failed was because we rushed in the first place."* Bad code killed the company — not management, not competition.
- **Making a mess is not how you go fast. It is how you go slow.** And not just in the long run — rushing slows you down even in the short term. You already know this, because you've raised your hand when asked if bad code has significantly impeded you.
- **The four code smells**: rigidity, fragility, inseparability, opacity. These are the specific ways code becomes painful to work with.
- **The Boy Scout Rule**: leave every module you touch a little cleaner than you found it. Never check in worse than you checked out.

## 🔗 Connections

- Relates to: [[01 - Introduction]], [[03 - Names++]]
- The Sword story maps directly to the productivity-decay curve: fast start → mess builds → slowdown → gap → failed redesign
- Brooks' Law shows up here — adding programmers to a late project makes it later, and new programmers learn bad habits from bad code

## 🛠️ Practical Application

> The "we'll clean it up later" lie. Deadline pressure never gets less. Customers never get more patient. The moment you say "I'll go back and fix this", you're not going back. The only way to go fast is to stay clean — the sushi chef's workspace is spotless throughout, because that's the only way he can be fast.

## ❓ Open Questions

- The inseparability smell is about reuse — but when does "reuse" become the wrong goal? There's a version of this where forcing reuse creates its own coupling problems.
- "Clean code reads like well-written prose" (Grady Booch) — is this actually achievable, or is it always an approximation?

## 📎 Example

The four smells, defined:

```
Rigidity     — fixing one bug requires changes in many places
Fragility    — a simple change breaks something unrelated
               (fixing a typo crashed customer systems because
               marketing told them to parse our menus via RS232)
Inseparability — useful parts can't be extracted without bringing
               the whole "trailer" with them
Opacity      — reading the code tells you nothing about what it does
```

Expert definitions of clean code:
- **Stroustrup**: elegant, efficient, does one thing
- **Booch**: simple and direct, reads like well-written prose
- **Feathers**: *"always looks like it was written by someone who cares"*
- **Cunningham**: *"every routine you read is pretty much what you expected"*

---

*Next: [[03 - Names++]] · Back to [[Weekly Study Plan]]*
