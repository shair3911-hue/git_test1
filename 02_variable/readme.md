# Python Slicing Cheat Sheet

## Overview

This guide explains Python slicing using the format:

`sequence[start:stop:step]`

* **start**: index where slicing begins
* **stop**: index where slicing ends (**not included**)
* **step**: number of positions to move

---

## Example Data

```python
lst = (10, 20, 40, 50, 60, 70, 80, 90)
```

| Value          | 10 | 20 | 40 | 50 | 60 | 70 | 80 | 90 |
| -------------- | -- | -- | -- | -- | -- | -- | -- | -- |
| Index          | 0  | 1  | 2  | 3  | 4  | 5  | 6  | 7  |
| Negative Index | -8 | -7 | -6 | -5 | -4 | -3 | -2 | -1 |

---

## Rule 1: Stop is Excluded

```python
lst[2:5]
# Output: (40, 50, 60)
```

---

## Rule 2: Step Controls Direction

* `step > 0` → forward (left to right)
* `step < 0` → backward (right to left)

---

## Positive Step (step > 0)

Condition: `start < stop`

```python
lst[2:6:1]
# Output: (40, 50, 60, 70)

lst[0:8:2]
# Output: (10, 40, 60, 80)
```

### Invalid Case

```python
lst[6:2:1]
# Output: ()
```

---

## Negative Step (step < 0)

Condition: `start > stop`

```python
lst[6:2:-1]
# Output: (80, 70, 60, 50)

lst[::-1]
# Output: (90, 80, 70, 60, 50, 40, 20, 10)
```

### Invalid Case

```python
lst[2:6:-1]
# Output: ()
```

---

## Step Meaning

| Step | Meaning             |
| ---- | ------------------- |
| 1    | Every element       |
| 2    | Skip one element    |
| 3    | Every third element |
| -1   | Reverse order       |

---

## Negative Indexing

```python
lst[-1]  # Output: 90
lst[-3]  # Output: 70
```

---

## Mixed Slicing

```python
lst[2:-2]
# Output: (40, 50, 60, 70)

lst[2:-2:2]
# Output: (40, 60)
```

---

## Common Mistakes

```python
lst[6:2:1]    # ()
lst[2:6:-1]   # ()
lst[-1:4:1]   # ()
```

---

## Practice Examples

```python
lst[2:-2:1]
# Output: (40, 50, 60, 70)

lst[2:-2:2]
# Output: (40, 60)

lst[-1:4:-1]
# Output: (90, 80, 70)

lst[::-2]
# Output: (90, 70, 50, 20)
```

---

## Summary

* Format: `start:stop:step`
* Stop index is always excluded
* `step > 0` → `start < stop`
* `step < 0` → `start > stop`

---

