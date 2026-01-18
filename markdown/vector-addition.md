---
title: "Vector Addition Explained | Vectors for Data Science - Lesson 1"
description: "Learn how to add vectors together to combine customer profiles and calculate averages. Includes Python NumPy code and real marketing examples."
keywords:
  - vector addition
  - add vectors
  - centroid
  - average customer
  - NumPy vector operations
slug: /vectors/vector-addition/
---

# Lesson 1: Vector Addition

**Breadcrumbs:** [Home](/) > [Vectors for Data Science](index.md) > Vector Addition

---

## A) What It Means

Vector addition means adding two vectors by adding their matching numbers together. If you have two lists, you add the first numbers, add the second numbers, and so on.

---

## B) How to Picture It

Imagine walking: First you walk one direction (vector 1), then you walk another direction (vector 2). Where you end up is the sum!

```
        Vector B
          ↗
         /
    •---→----↗
    Vector A    A + B (where you end up)
```

It's like giving directions: "Go 3 blocks east, then 2 blocks north" = "You're at (3, 2)."

> **📷 Image Idea (Realistic):** Two arrows on graph paper, one red and one blue, with a purple arrow showing their sum, office desk background
> 
> *Alt text:* Two vector arrows being added together on graph paper
> 
> *Caption:* Adding vectors: follow one arrow, then the other

---

## C) Business Example

**Situation:** Finding the "average profile" of a customer segment.

```
Customer 1: x₁ = [25, 35, 4]  (age 25, income $35k, satisfaction 4)
Customer 2: x₂ = [30, 40, 6]  (age 30, income $40k, satisfaction 6)

Sum: x₁ + x₂ = [55, 75, 10]
Average: [27.5, 37.5, 5]
```

The average customer in the "young budget shoppers" segment: age 27.5, income $37.5k, satisfaction 5.

---

## D) Where It Shows Up in ML

**Plain words:** When you want to find the "average customer" in a group, you add up all their vectors and divide by how many there are.

**In machine learning, this is called computing the "centroid" or "mean vector."** It's the center point of a cluster of similar customers. K-means clustering uses this constantly!

> **📊 Image Idea (Infographic):** Split-screen showing customer icons merging into an 'average customer' icon, with numbers showing the calculation
> 
> *Alt text:* Infographic of customer profiles combining into an average
> 
> *Caption:* Finding the centroid: the 'average' customer in a group

---

## E) Worked Numeric Example

```
x₁ = [25, 35, 4]
x₂ = [30, 40, 6]

Step 1: Add matching positions
x₁ + x₂ = [25+30, 35+40, 4+6] = [55, 75, 10]

Step 2: Divide by count to get average
Average = [55/2, 75/2, 10/2] = [27.5, 37.5, 5]
```

---

## F) Python (NumPy) Snippet

```python
import numpy as np

x1 = np.array([25, 35, 4])
x2 = np.array([30, 40, 6])

# Vector addition
total = x1 + x2
print("Sum:", total)

# Average (centroid)
average = total / 2
print("Average customer:", average)

# Output:
# Sum: [55 75 10]
# Average customer: [27.5 37.5  5. ]
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
> - Add vectors by adding matching positions: [a, b] + [c, d] = [a+c, b+d]
> - Vectors must be the same length to add
> - Adding vectors then dividing gives you the average (centroid)

---

## H) Common Mistakes

> ❌ **Avoid These Errors**
> 
> - Trying to add vectors of different lengths (you can't add [1, 2] + [3, 4, 5])
> - Forgetting to divide when finding an average
> - Adding in the wrong order (though order doesn't matter: A + B = B + A)

---

## 📝 Practice Questions

**Question 1:** Add these vectors: [10, 20, 5] + [5, 10, 15]

<details>
<summary>Show Answer</summary>

[15, 30, 20]

</details>

**Question 2:** Find the average of [20, 40] and [30, 60]

<details>
<summary>Show Answer</summary>

Sum = [50, 100], Average = [25, 50]

</details>

---

## 📚 Learning Resources

| Type | Resource | Link |
|------|----------|------|
| 🎬 Video | 3Blue1Brown: Linear combinations, span, basis | [Link](https://youtube.com/watch?v=k7RM-ot2NWY) |
| ✏️ Practice | Khan Academy: Adding & Subtracting Vectors | [Link](https://khanacademy.org/math/precalculus/x9e81a4f98389efdf:vectors) |
| 🤖 Applied ML | Scikit-learn: K-Means Clustering | [Link](https://scikit-learn.org/stable/modules/clustering.html#k-means) |

---

## Navigation

[← What Is a Vector?](what-is-a-vector.md) | [Course Home](index.md) | [Vector Subtraction →](vector-subtraction.md)

---

*© 2026 Your Website Name*
