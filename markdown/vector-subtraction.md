---
title: "Vector Subtraction Explained | Vectors for Data Science - Lesson 2"
description: "Learn how to subtract vectors to measure differences between customers and track changes over time. Python examples included."
keywords:
  - vector subtraction
  - subtract vectors
  - customer difference
  - distance calculation
  - change measurement
slug: /vectors/vector-subtraction/
---

# Lesson 2: Vector Subtraction

**Breadcrumbs:** [Home](/) > [Vectors for Data Science](index.md) > Vector Subtraction

---

## A) What It Means

Vector subtraction means subtracting matching numbers to find the difference between two vectors. It tells you 'how do I get from one point to another?'

---

## B) How to Picture It

If A is where you start and B is where you end, then B - A is the direction and distance from A to B.

```
    A •--------→ • B
         B - A
    (the arrow from A to B)
```

> **📷 Image Idea (Realistic):** Before and after comparison dashboard showing customer metrics with arrows indicating changes, modern analytics interface
> 
> *Alt text:* Dashboard showing customer metric changes with difference arrows
> 
> *Caption:* Subtraction reveals how customer behavior changed

---

## C) Business Example

**Situation:** Measuring how Alice changed after a marketing campaign.

```
Before campaign: [28, 45, 2, 1, 1, 6]
After campaign:  [28, 45, 7, 4, 3, 8]

Change = After - Before
       = [0, 0, 5, 3, 2, 2]
```

**Interpretation:** Age and income didn't change, but she visited 5 more times, opened 3 more emails, made 2 more purchases, and satisfaction went up by 2!

---

## D) Where It Shows Up in ML

**Plain words:** Subtraction helps you measure "distance" or "difference" between customers. Two customers with a small difference vector are similar.

**In machine learning, this is the first step in calculating "distance" between data points.** K-nearest neighbors (finding similar customers) relies on this to recommend products or segment customers.

> **📊 Image Idea (Infographic):** Two points labeled Alice and Bob with a measuring tape or ruler between them showing the difference vector
> 
> *Alt text:* Visual showing distance between two customer points
> 
> *Caption:* Vector subtraction measures the gap between customers

---

## E) Worked Numeric Example

How different are Alice and Bob?

```
Alice: x_a = [28, 45, 5]  (age, income_k, visits)
Bob:   x_b = [52, 80, 1]

Difference: x_b - x_a = [52-28, 80-45, 1-5]
                      = [24, 35, -4]
```

**Interpretation:** Bob is 24 years older, earns $35k more, but visits 4 fewer times.

---

## F) Python (NumPy) Snippet

```python
import numpy as np

alice = np.array([28, 45, 5])
bob = np.array([52, 80, 1])

# Vector subtraction
difference = bob - alice
print("Difference (Bob - Alice):", difference)

# Calculate distance (how "far apart" they are)
distance = np.sqrt(np.sum(difference**2))
print("Distance:", round(distance, 2))

# Output:
# Difference (Bob - Alice): [24 35 -4]
# Distance: 42.57
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
> - Subtraction gives you the 'arrow' from one point to another
> - It shows what changed or how different two things are
> - B - A points from A toward B

---

## H) Common Mistakes

> ❌ **Avoid These Errors**
> 
> - Confusing direction: A - B is the opposite of B - A
> - Forgetting negative values are meaningful (Bob has -4 visits = fewer visits)
> - Comparing features that aren't on the same scale (we'll address this later)

---

## 📝 Practice Questions

**Question 1:** Subtract: [50, 100, 8] - [30, 60, 5]

<details>
<summary>Show Answer</summary>

[20, 40, 3]

</details>

**Question 2:** If the difference between two customers is [0, 0, 0], what does that mean?

<details>
<summary>Show Answer</summary>

They are identical (at least for these features).

</details>

---

## 📚 Learning Resources

| Type | Resource | Link |
|------|----------|------|
| 🎬 Video | Khan Academy: Subtracting vectors | [Link](https://khanacademy.org/math/precalculus/x9e81a4f98389efdf:vectors) |
| ✏️ Practice | Paul's Online Math Notes: Vector Arithmetic | [Link](https://tutorial.math.lamar.edu/Problems/CalcII/VectorArithmetic.aspx) |
| 🤖 Applied ML | Kaggle: Model Validation | [Link](https://kaggle.com/learn/intro-to-machine-learning) |

---

## Navigation

[← Vector Addition](vector-addition.md) | [Course Home](index.md) | [Scalar Multiplication →](scalar-multiplication.md)

---

*© 2026 Your Website Name*
