# Week 1 Exercise — Naming in lodash

**Codebase:** [lodash](https://github.com/lodash/lodash) · **Focus:** Do function names tell you what they do without reading the body?

---

## 5 Functions: Does the name work on its own?

### `arrayReduce(array, iteratee, accumulator, initAccum)`

Before reading: I wasn't sure what "reduce" meant here — reduce the length? Remove duplicates? The name alone didn't tell me enough.

```js
function arrayReduce(array, iteratee, accumulator, initAccum) {
  var index = -1,
      length = array == null ? 0 : array.length;

  if (initAccum && length) {
    accumulator = array[++index];
  }
  while (++index < length) {
    accumulator = iteratee(accumulator, array[index], index, array);
  }
  return accumulator;
}
```

After reading: "reduce" means collapsing the array into a single accumulated value by applying `iteratee` at each step.

---

### `arraySome(array, predicate)`

Before reading: I assumed `predicate` was another array, and thought it was checking if `array` was a subset of `predicate`.

```js
function arraySome(array, predicate) {
  var index = -1,
      length = array == null ? 0 : array.length;

  while (++index < length) {
    if (predicate(array[index], index, array)) {
      return true;
    }
  }
  return false;
}
```

After reading: `predicate` is a function, not an array. The function returns `true` if any element satisfies the predicate. Once I understood what "predicate" means in functional programming, the name clicked — but it's the same problem as `arrayReduce`: it requires vocabulary the name doesn't teach you.

---

### `asciiToArray(string)`

Before reading: The name says exactly what it does — converts ASCII to an array.

```js
function asciiToArray(string) {
  return string.split('');
}
```

After reading: Mostly right, but there's a subtle issue. The function just splits any string into characters — it's not actually limited to ASCII input. The name implies ASCII-specific behavior that isn't enforced. A more accurate name might be `stringToCharArray`, but I understand why lodash named it this way — it's used internally in a context where the input is known to be ASCII.

---

### `baseFindKey(collection, predicate, eachFunc)`

Before reading: I couldn't tell what this does from the name.

```js
function baseFindKey(collection, predicate, eachFunc) {
  var result;
  eachFunc(collection, function(value, key, collection) {
    if (predicate(value, key, collection)) {
      result = key;
      return false;
    }
  });
  return result;
}
```

After reading: It finds the first key in a collection whose value satisfies `predicate`, using `eachFunc` as the iteration strategy.

---

### `cacheHas(cache, key)`

Before reading: Yes — takes a cache and a key, returns whether the key exists. No ambiguity.

```js
function cacheHas(cache, key) {
  return cache.has(key);
}
```

After reading: Exactly what I expected.

---

## One function I'd rename: `replaceHolders`

```js
function replaceHolders(array, placeholder) {
  var index = -1,
      length = array.length,
      resIndex = 0,
      result = [];

  while (++index < length) {
    var value = array[index];
    if (value === placeholder || value === PLACEHOLDER) {
      array[index] = PLACEHOLDER;
      result[resIndex++] = index;
    }
  }
  return result;
}
```

The name `replaceHolders` doesn't explain that it also *returns the indexes* of where replacements happened — the function does two things: mutates the array and returns an index list. I initially suggested `replacePlaceholdersAndGetIndexes`, but that's too long and a symptom of the real problem: the function has two responsibilities.

A cleaner fix might be to split it into two functions, or rename it `normalizePlaceholders` to signal that it's standardizing the placeholder values (and return the indexes as a side effect of that normalization).

---

## What Claude Code said vs. what I observed

I asked Claude Code: *"Explain the naming conventions used in this codebase."*

Claude gave a systematic breakdown I hadn't noticed on my own:

- **`base*` vs `array*` prefixes** signal the abstraction level — `base*` functions work on any collection, `array*` are optimized for plain arrays only. I had noticed the prefix pattern but didn't understand *why* lodash uses both — Claude's explanation made the layering click.
- **`re*` prefix for regex variables** — I hadn't looked at constants at all, so this was new to me.
- **`*Tag` suffix for type-detection strings** — same, completely missed this.

Where my analysis went further: I caught that `asciiToArray` is slightly misleading (the name implies ASCII-only but the function works on any string). Claude didn't flag this.

The biggest gap in my analysis was the *system*: I was reading functions in isolation, but lodash's naming is a layered taxonomy. Claude saw the taxonomy; I saw individual names.

---

*Back to [[Weekly Study Plan]]*
