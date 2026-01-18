---
title: "Line Intersections | Solving Systems of Equations - Lesson 8"
description: "Learn how to find where two lines cross - essential for solving systems of equations in optimization and machine learning."
keywords:
  - line intersection
  - systems of equations
  - linear systems
  - optimization
  - constraint satisfaction
slug: /vectors/line-intersections/
---

# Lesson 8: Intersection of Lines in 3D

**Breadcrumbs:** [Home](/) > [Vectors for Data Science](index.md) > Intersection of Lines in 3D

---

## A) What It Means

Intersection of lines means finding a point where two lines cross — a point that lies on BOTH lines simultaneously.

---

## B) How to Picture It

In 3D, two lines might:
1. Intersect at exactly one point
2. Be parallel (never touch)
3. Be "skew" (not parallel, but still never touch — like roads at different heights)

```
Line 1:  ─────•─────→
              │
              │ intersection point
Line 2:       ↓
              •
              │
```

> **📷 Image Idea (Realistic):** Aerial view of a traffic intersection with two roads crossing, cars waiting at the crossing point
> 
> *Alt text:* Traffic intersection from above showing two roads meeting
> 
> *Caption:* Lines intersect where they cross - like roads at an intersection

---

## C) Business Example

**Situation:** Finding a customer profile that matches two different criteria paths.

Imagine you're modeling two trends:
- **Trend A:** Customers who respond to email marketing
- **Trend B:** Customers who respond to loyalty programs

```
Trend A: x = [2, 3] + t × [1, 0]  (more emails → more visits)
Trend B: x = [0, 1] + s × [1, 1]  (more loyalty → more of everything)
```

Finding the intersection tells you: "What profile benefits from BOTH strategies?"

---

## D) Where It Shows Up in ML

**Plain words:** Finding intersections means finding solutions that satisfy multiple rules at the same time.

**In machine learning, this relates to "solving linear systems"** and finding feasible regions in constrained optimization.

When you train a model, you're often looking for weights that satisfy many equations at once — one for each training example!

> **📊 Image Idea (Infographic):** Two colored lines on a coordinate grid with their intersection point highlighted and labeled with coordinates
> 
> *Alt text:* Graph showing two lines intersecting at a marked point
> 
> *Caption:* Finding the point that satisfies both equations

---

## E) Worked Numeric Example

Find where these two 2D lines intersect:

```
Line 1: point = [1, 2] + t × [2, 1]
Line 2: point = [0, 0] + s × [1, 3]

For intersection, both must give the same point:
[1 + 2t, 2 + t] = [s, 3s]

This gives two equations:
1 + 2t = s       ... equation 1
2 + t = 3s       ... equation 2

Solving: t = -0.2, s = 0.6

Intersection point = [1 + 2(-0.2), 2 + (-0.2)] = [0.6, 1.8]
```

---

## F) Python (NumPy) Snippet

```python
import numpy as np

# Line 1: [1, 2] + t * [2, 1]
p1 = np.array([1, 2])
d1 = np.array([2, 1])

# Line 2: [0, 0] + s * [1, 3]
p2 = np.array([0, 0])
d2 = np.array([1, 3])

# Set up system: p1 + t*d1 = p2 + s*d2
# Rearrange: t*d1 - s*d2 = p2 - p1
A = np.column_stack([d1, -d2])
b = p2 - p1

# Solve for [t, s]
params = np.linalg.solve(A, b)
t, s = params

print(f"t = {t}, s = {s}")
intersection = p1 + t * d1
print(f"Intersection point: {intersection}")

# Output:
# t = -0.2, s = 0.6
# Intersection point: [0.6 1.8]
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
> - Intersection = point satisfying both line equations
> - In 3D, lines might not intersect at all (skew lines)
> - Solving for intersections = solving systems of equations

---

## H) Common Mistakes

> ❌ **Avoid These Errors**
> 
> - Assuming lines always intersect (they might be parallel or skew)
> - Forgetting to check your answer by plugging back into both equations
> - Mixing up parameters (t for line 1, s for line 2 — they're different!)

---

## 📝 Practice Questions

**Question 1:** If two lines are parallel, how many intersection points do they have?

<details>
<summary>Show Answer</summary>

Zero (unless they're the same line, then infinite)

</details>

**Question 2:** What does it mean when np.linalg.solve fails?

<details>
<summary>Show Answer</summary>

The system has no unique solution - lines might be parallel or there's another issue

</details>

---

## 📚 Learning Resources

| Type | Resource | Link |
|------|----------|------|
| 🎬 Video | Khan Academy: Three-variable linear systems | [Link](https://khanacademy.org/math/algebra2) |
| ✏️ Practice | Paul's Online Math Notes: Lines in 3D | [Link](https://tutorial.math.lamar.edu/Problems/CalcIII/EqnsOfLines.aspx) |
| 🤖 Applied ML | Towards Data Science: Linear Regression Math | [Link](https://towardsdatascience.com) |

---

## Navigation

[← Plane Equation](plane-equation.md) | [Course Home](index.md) | [Plane Intersections →](plane-intersections.md)

---

*© 2026 Your Website Name*
