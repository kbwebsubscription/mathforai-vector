---
title: "Plane Intersections | Constrained Optimization in ML - Lesson 9"
description: "Learn how plane intersections relate to solving Ax=b and constrained optimization - fundamental concepts in machine learning."
keywords:
  - plane intersection
  - Ax=b
  - constrained optimization
  - linear algebra
  - feasible region
  - numpy linalg solve
slug: /vectors/plane-intersections/
---

# Lesson 9: Intersection of Planes

**Breadcrumbs:** [Home](/) > [Vectors for Data Science](index.md) > Intersection of Planes

---

## A) What It Means

Intersection of planes means finding points that lie on two (or more) planes at the same time.

---

## B) How to Picture It

- Two planes typically intersect in a **line**
- Three planes typically intersect at a **single point**
- Planes can also be parallel (never touch) or identical

```
Two walls meeting → corner line
Three walls meeting → corner point (like a room corner)
```

> **📷 Image Idea (Realistic):** Corner of a room where two walls and the floor meet, with a small dot marking the intersection point
> 
> *Alt text:* Room corner showing three planes meeting at a point
> 
> *Caption:* Three planes meeting at a point - like the corner of a room

---

## C) Business Example

**Situation:** Finding customers who satisfy multiple decision rules.

```
Rule 1 (Budget):      income - 20×purchases ≥ 10  (can afford more)
Rule 2 (Engagement):  visits + emails_opened ≥ 8  (actively engaged)
Rule 3 (Satisfaction): satisfaction ≥ 6           (happy with us)
```

Each rule defines a plane (actually a half-space). The intersection of all three gives you the "sweet spot" — customers who satisfy ALL criteria.

These are your **ideal targets** for a marketing campaign!

---

## D) Where It Shows Up in ML

**Plain words:** Many real problems have multiple constraints or rules. Finding the intersection means finding solutions that satisfy all of them.

**In machine learning, this is called "constrained optimization"** or solving a "system of linear equations" (Ax = b).

The tool `numpy.linalg.solve()` finds the intersection of n planes (equations) in n-dimensional space. This is used everywhere:
- Finding optimal model weights
- Linear programming (business optimization)
- Solving the "normal equations" in linear regression

> **📊 Image Idea (Infographic):** 3D visualization showing three colored planes intersecting at one point, with the point highlighted
> 
> *Alt text:* Three planes intersecting at a single solution point
> 
> *Caption:* Finding the solution that satisfies all constraints

---

## E) Worked Numeric Example

Find the intersection of these two planes (in 2D, so they're lines):

```
Plane 1: 2x + 1y = 8
Plane 2: 1x + 3y = 9

Matrix form:
[2  1] [x]   [8]
[1  3] [y] = [9]

Solving (substitution):
From eq 1: y = 8 - 2x
Substitute: x + 3(8 - 2x) = 9
           x + 24 - 6x = 9
           -5x = -15
           x = 3

Then: y = 8 - 2(3) = 2

Intersection: (3, 2)
```

---

## F) Python (NumPy) Snippet

```python
import numpy as np

# Two planes (as a system of equations)
# 2x + 1y = 8
# 1x + 3y = 9

A = np.array([
    [2, 1],
    [1, 3]
])

b = np.array([8, 9])

# Solve for intersection
solution = np.linalg.solve(A, b)
print(f"Intersection point: x = {solution[0]}, y = {solution[1]}")

# Verify
print(f"Check eq 1: 2({solution[0]}) + 1({solution[1]}) = {2*solution[0] + 1*solution[1]}")
print(f"Check eq 2: 1({solution[0]}) + 3({solution[1]}) = {1*solution[0] + 3*solution[1]}")

# Output:
# Intersection point: x = 3.0, y = 2.0
# Check eq 1: 2(3.0) + 1(2.0) = 8.0
# Check eq 2: 1(3.0) + 3(2.0) = 9.0
```

### 🧪 Try It Yourself

Run this code in [Google Colab](https://colab.research.google.com/) (free, no installation needed):

1. Go to colab.research.google.com
2. Click "New Notebook"
3. Paste the code above into a cell
4. Press Shift+Enter to run

---

## G) Key Takeaways

> ✅ **What to Remember**
> 
> - Two planes usually meet in a line; three planes usually meet at a point
> - This is how you solve systems of equations (Ax = b)
> - Constrained optimization = finding intersections of many rules

---

## H) Common Mistakes

> ❌ **Avoid These Errors**
> 
> - Forgetting that planes might be parallel (no intersection exists)
> - Not checking for 'degenerate' cases (infinite solutions or no solution)
> - Confusing 'intersection point' with 'just any point on a plane'

---

## 📝 Practice Questions

**Question 1:** Solve: x + y = 5 and 2x - y = 1

<details>
<summary>Show Answer</summary>

Add equations: 3x = 6, so x = 2, y = 3. Intersection: (2, 3)

</details>

**Question 2:** What does numpy.linalg.solve(A, b) compute?

<details>
<summary>Show Answer</summary>

The point x where A @ x = b — the intersection of all planes defined by the rows of A

</details>

---

## 📚 Learning Resources

| Type | Resource | Link |
|------|----------|------|
| 🎬 Video | 3Blue1Brown: Inverse matrices, column space | [Link](https://youtube.com/watch?v=uQhTuRlWMxw) |
| ✏️ Practice | Khan Academy: Solving systems with matrices | [Link](https://khanacademy.org/math/algebra-home/alg-matrices) |
| 🤖 Applied ML | Coursera: Andrew Ng's ML Course | [Link](https://coursera.org/learn/machine-learning) |

---

## Navigation

[← Line Intersections](line-intersections.md) | [Course Home](index.md) | 

---

*© 2026 Your Website Name*
