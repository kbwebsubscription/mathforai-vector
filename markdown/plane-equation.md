---
title: "Plane Equation & Decision Boundaries | Vectors for ML - Lesson 7"
description: "Learn how plane equations create decision boundaries that separate customer groups. Essential for classification in machine learning."
keywords:
  - plane equation
  - decision boundary
  - classification
  - linear classifier
  - hyperplane
  - SVM
slug: /vectors/plane-equation/
---

# Lesson 7: Equation of a Plane

**Breadcrumbs:** [Home](/) > [Vectors for Data Science](index.md) > Equation of a Plane

---

## A) What It Means

A plane is a flat surface that extends forever. In 3D, it's like an infinite sheet of paper. In math, it's defined by: w · x = b

---

## B) How to Picture It

Imagine a wall. The plane is the wall surface. The normal vector w is an arrow pointing straight OUT from the wall (perpendicular to it).

```
          ↑ normal (w)
          |
    ------+------
   /      |      \
  /   the plane   \
 /   (the wall)    \
```

> **📷 Image Idea (Realistic):** A glass wall dividing a room with people on both sides, some with shopping bags (buyers) and some without
> 
> *Alt text:* Glass wall separating buyers from non-buyers
> 
> *Caption:* A decision boundary separates two groups of customers

---

## C) Business Example

**Situation:** A rule that separates "likely buyers" from "unlikely buyers."

```
Rule: 0.5 × visits + 1.0 × satisfaction = 10

Carol: visits=8, satisfaction=9
Score = 0.5(8) + 1.0(9) = 13
13 > 10 → Carol is on the "likely to buy" side ✓

Bob: visits=1, satisfaction=5
Score = 0.5(1) + 1.0(5) = 5.5
5.5 < 10 → Bob is on the "unlikely" side ✗
```

---

## D) Where It Shows Up in ML

**Plain words:** Many classification models work by finding a plane (or line in 2D) that separates two groups. Customers on one side get one label ("will buy"), customers on the other side get the opposite ("won't buy").

**In machine learning, this is called a "decision boundary."**

The model classifies by checking:
- If w · x > b → predict "yes"
- If w · x < b → predict "no"

Logistic regression and SVMs find the best plane to separate your data.

> **📊 Image Idea (Infographic):** 2D scatter plot with dots in two colors separated by a diagonal line, labeled 'will buy' and 'won't buy'
> 
> *Alt text:* Scatter plot with decision boundary line separating classes
> 
> *Caption:* The plane equation defines the dividing line between groups

---

## E) Worked Numeric Example

Decision boundary: 0.5 × visits + 1.0 × satisfaction = 10

```
Carol: [visits=8, satisfaction=9]
Score = 0.5(8) + 1.0(9) = 4 + 9 = 13
13 > 10 → Likely buyer ✓

Bob: [visits=1, satisfaction=5]  
Score = 0.5(1) + 1.0(5) = 0.5 + 5 = 5.5
5.5 < 10 → Unlikely buyer ✗
```

---

## F) Python (NumPy) Snippet

```python
import numpy as np

# Decision boundary: w · x = b
w = np.array([0.5, 1.0])  # weights for [visits, satisfaction]
b = 10                     # threshold

# Check customers
carol = np.array([8, 9])
bob = np.array([1, 5])

carol_score = np.dot(w, carol)
bob_score = np.dot(w, bob)

print(f"Carol: score = {carol_score}, prediction = {'Buy' if carol_score >= b else 'No buy'}")
print(f"Bob: score = {bob_score}, prediction = {'Buy' if bob_score >= b else 'No buy'}")

# Output:
# Carol: score = 13.0, prediction = Buy
# Bob: score = 5.5, prediction = No buy
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
> - A plane is defined by w · x = b
> - It divides space into two halves (two groups)
> - Decision boundaries in classification are often planes

---

## H) Common Mistakes

> ❌ **Avoid These Errors**
> 
> - Forgetting that in 2D, a 'plane' looks like a line
> - Confusing the normal vector w with points on the plane
> - Thinking all ML uses linear planes (many models use curved boundaries!)

---

## 📝 Practice Questions

**Question 1:** For decision boundary 2x + 3y = 12, classify point (3, 2)

<details>
<summary>Show Answer</summary>

Score = 2(3) + 3(2) = 12. Exactly on boundary! Could go either way.

</details>

**Question 2:** If w · x > b predicts 'yes', what does w · x < b predict?

<details>
<summary>Show Answer</summary>

'No' - the customer is on the opposite side of the decision boundary

</details>

---

## 📚 Learning Resources

| Type | Resource | Link |
|------|----------|------|
| 🎬 Video | StatQuest: Logistic Regression | [Link](https://youtube.com/watch?v=yIYKR4sgzI8) |
| ✏️ Practice | Khan Academy: Equations of planes | [Link](https://khanacademy.org/math/multivariable-calculus) |
| 🤖 Applied ML | Scikit-learn: Support Vector Machines | [Link](https://scikit-learn.org/stable/modules/svm.html) |

---

## Navigation

[← Line Equation](line-equation.md) | [Course Home](index.md) | [Line Intersections →](line-intersections.md)

---

*© 2026 Your Website Name*
