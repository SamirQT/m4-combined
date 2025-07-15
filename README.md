## Assignment 1: Caesar Cipher

**Problem Statement**
Write a function

```python
def caesar_cipher(s: str, shift: int) -> str:
    """
    Shift each A–Z/a–z letter in `s` by `shift` positions (wrap around).
    Preserve case; leave other characters unchanged.
    """
```

* **Constraint:** Exactly one loop over `s`.
* Use `ord`/`chr` arithmetic for wrap‑around within `A–Z` or `a–z`.
* Copy any non‑alphabetic character unchanged.

**Evaluation Criteria**

* **Correctness:** All letters shifted correctly, non‑letters left intact.
* **Edge Cases:** Handles empty string, negative or very large `shift` values.
* **Style:** Single clear loop, descriptive variable names, comments explaining wrap logic.

---

## Assignment 2: Interleave Two Sequences

**Problem Statement**
Write a function

```python
def interleave(a, b):
    """
    Given two sequences `a` and `b` of the same length (both `str` or both `list`),
    return a new sequence of the same type by alternating their elements.
    """
```

* **Constraint:** Exactly one loop (no nested loops).
* If inputs are strings, return a `str`; if lists, return a `list`.
* Do **not** use `dict`, `import`, or list comprehensions.

**Evaluation Criteria**

* **Correctness:** Elements from `a` and `b` perfectly interwoven.
* **Type Preservation:** Output type matches input type.
* **Robustness:** Correct behavior for empty inputs and single‑element sequences.

---

## Assignment 3: Circular Shift & Filter

**Problem Statement**
Write a function

```python
def process_list(nums: list[int], k: int) -> list[int]:
    """
    1. Circularly shift `nums` right by `k` positions.
    2. Compute its average.
    3. Return a new list of values ≥ average.
    """
```

* **Constraint:**

  * Perform the shift via slicing: `nums[-k_mod:] + nums[:-k_mod]`.
  * Use one loop to compute the sum and one loop to filter (no nested loops, no comprehensions).
  * No `dict` or `import`.

**Evaluation Criteria**

* **Correctness:** Proper circular shift, accurate average calculation, correct filtering.
* **Edge Cases:** Handles empty list, `k` larger than list length, uniform-value lists.
* **Clarity:** Clear separation (and comments) of shift, sum, and filter steps.

---

## Assignment 4: Character Occurrences & Positions

**Problem Statement**
Write a function

```python
def char_stats(text: str, ch: str) -> tuple[int, list[int]]:
    """
    Count how many times character `ch` appears in `text`,
    and return (count, [all 0‑based positions]).
    """
```

* **Constraint:** Exactly one loop over `text`.
* Use only indexing and `==` to compare characters.
* If `text` is empty or `ch == ""`, return `(0, [])`.

**Evaluation Criteria**

* **Correctness:** Accurate count and complete list of positions.
* **Edge Cases:** Handles empty `text`, `ch` not found, and empty `ch`.
* **Style:** Single clear loop, meaningful variable names, in‑line comments.

---

## Assignment 5: Longest Increasing Run

**Problem Statement**
Write a function

```python
def longest_increasing_run(nums: list[int]) -> tuple[int, int]:
    """
    Find the longest strictly increasing contiguous subsequence (“run”)
    in `nums`. Return (length, start_index). If `nums` is empty, return (0, 0).
    """
```

* **Constraint:** Single pass (one loop) through `nums`.
* Track current run length and best run so far—no nested loops, no `max()`, `dict`, or comprehensions.

**Evaluation Criteria**

* **Correctness:** Identifies the correct run length and starting index.
* **Edge Cases:** Handles empty list, all‑decreasing list, constant list, and fully increasing list.
* **Performance & Style:** Single linear pass; clear updates of “current” vs. “max” run with comments.
