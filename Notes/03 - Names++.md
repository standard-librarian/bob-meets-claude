---
title: "Names++"
date: 2026-03-18
source: "Clean Code"
week: One
topic: "naming"
status: watched
tags:
  - study
  - "week/one"
  - "source/clean-code"
  - "topic/naming"
---

# 3 - Names**

> **Source:** [[Weekly Study Plan]] · **Week 1** · 2026-03-18

---

## 🎯 Key Takeaways

Your notes are already quite solid—you captured the core ideas well. I’ll refine them a bit for clarity, correctness, and stronger technical precision, while keeping your structure.

---

### ✅ Refined Version

* **Names are a form of communication**
  Choose them carefully—they’re how other developers understand your code.

* **Names should reveal intent**
  A reader should understand *what something does or represents* without extra comments.

* **Names should be pronounceable**
  If you can’t say it, you can’t discuss it easily with your team.

* **Avoid encoding type information in names**
  Don’t use prefixes/suffixes that describe data types (e.g., `strName`, `iCount`).
  Modern languages and IDEs already handle that.

* **Code should read like well-written prose**

  * Classes → nouns (e.g., `User`, `OrderService`)
  * Variables → nouns (e.g., `totalPrice`)
  * Functions → verbs (e.g., `calculateTotal`)
  * Booleans → predicates (e.g., `isActive`, `hasPermission`)

* **Follow the scope rule**

  * **Variables:**

    * Short scope → short names (`i`, `x`)
    * Long scope → descriptive names (`userAccountBalance`)
    * Global variables → very clear and descriptive

  * **Functions & Classes (inverse rule):**

    * Public / widely used → shorter, simpler names (`getUser`)
    * Private / limited scope → longer, more descriptive (`calculateDiscountForPremiumUsers`)


## 🔗 Connections

*How does this connect to other things I've already studied?*

- Relates to: [[01 - Introduction]], [[02 - Clean Code (Remake)]]


---

*Next: [[04 - Functions]] · Back to [[Weekly Study Plan]]*
