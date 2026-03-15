---
title: "Names++"
date: 2026-03-15
source: "clean-code"
week: 1
topic: "naming"
status: watched
tags:
  - study
  - "week/1"
  - "source/clean-code"
  - "topic/naming"
---

# 03 - Names++

> **Source:** [[Weekly Study Plan]] · **Week 1** · 2026-03-15

---

The naming episode. Longest and most concrete of the ones watched so far. Most of the ideas trace back to Tim Ottinger's 1997 paper *Ottinger's Variable and Class Naming Rules* — the most-downloaded paper on the Object Mentor site, and the direct source for the Names chapter in the Clean Code book.

---

## 🎯 Key Takeaways

- **Names exist to communicate intent, not for your convenience.** If you need a comment to explain the name, the name failed. Variable names are "compilable comments" — they should document intent by themselves.
- **Avoid disinformation.** A name that doesn't mean what it says is one of the worst things a programmer can do. `SerialDate` is wrong because the class is abstract — the name implies a concrete implementation detail that subclasses could override entirely. Names must not drift as code changes; if the meaning changes, so does the name.
- **Names must be pronounceable.** Uncle Bob and Bullet Bob's war story: they worked with a codebase that used `gwd` everywhere and didn't know how to pronounce it, so one called it "good-aay" and the other "good-bee." People need to *say* names in conversations. Abbreviations that nobody can pronounce are a tax on every code review and pairing session.
- **Drop the encodings.** Hungarian Notation was invented by Charles Simonyi (Hungarian-born chief architect at Microsoft during the DOS era) when IDEs didn't exist and you couldn't hover to see a type. That world is gone. `I` prefix for interfaces, `m_` for members, `C` for classes — these distract, obfuscate, and cost more in reading friction than they ever saved in type-tracking. Let the IDE, compiler, and tests do that job.
- **Parts of speech matter.** Classes and variables are nouns. Methods are verbs. Booleans — whether variables or methods — are predicates (`isEmpty`, `isTerminated`, `IsPostable`). Noise words like Manager, Processor, Data, Info are synonyms for "I don't know what to call this." The goal is code that reads like well-written prose.
- **The scope rule — and it runs opposite for variables vs. functions.** Variable name length should be *proportional* to scope: one-letter variables are fine when they're used in three lines; a variable spanning 20+ lines needs a real name (`d` for document doesn't work when you have to scroll up to figure out what `d` is). Function and class name length should be *inversely proportional* to scope: public functions with wide visibility get short, convenient names (`serve`, `open`); private functions called from one place can — and should — be long and descriptive (`tryProcessInstructions`).

## 🔗 Connections

- Relates to: [[02 - Clean Code (Remake)]], [[04 - Function Structure]]
- Builds on: Grady Booch's definition from Episode 02 — "clean code reads like well-written prose" — this episode is the how
- The `SerialDate` disinformation example connects directly to the opacity smell from Episode 02: if you have to read the code to understand a name, the name failed

## 🛠️ Practical Application

> The scope rule is the one I'll actually change behavior around. I've defaulted to making all names "medium length" regardless of scope, which is wrong in both directions — over-explaining short-lived locals and under-explaining widely-used ones. The fix is deliberate: ask "how far does this name travel?" and size accordingly.
>
> The `Boolean`-returning `set` method trap is also real. `IF Set(userName, "UncleBob")` — is that testing whether it's already set, or setting and checking success? There's no way to know without reading the implementation. The fix (void `set` + exception on failure, separate `isSet` predicate) makes both intent and behavior unambiguous.

## ❓ Open Questions

- The scope rule for derived classes is flagged as an exception — longer scopes but longer names because you add adjectives (`Account` → `SavingsAccount`). Where does this break down with deep inheritance hierarchies?
- "Names should be as abstract as the class" (re: `SerialDate`) — how do you name a *genuinely* abstract domain concept without defaulting to the noise words he just said to avoid?

## 📎 Example

The `include` range constants before and after:

```
// Before — mysterious
INCLUDE_BOTH   // useful constant
INCLUDE_FIRST  // useful constant
INCLUDE_SECOND // useful constant

// After — uses the mathematical concept directly
enum DateInterval {
  OPEN,             // excludes both bounds
  CLOSED,           // includes both bounds
  OPEN_LEFT,        // includes only upper bound
  OPEN_RIGHT        // includes only lower bound
}
```

The scope rule in action:

```
// Public method — short scope visibility, short name
public void serve(Socket s) {
    // Private method — narrow scope, long descriptive name
    tryProcessInstructions(s);
}
```

---

*Next: [[04 - Function Structure]] · Back to [[Weekly Study Plan]]*
