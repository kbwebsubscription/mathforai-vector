---
title: "What Is a Vector? | Vectors for Data Science - Lesson 0"
description: "Learn what vectors are and how they represent customer data in machine learning. Beginner-friendly explanation with Python NumPy examples."
keywords:
  - what is a vector
  - feature vector
  - data science vectors
  - NumPy array
  - customer data representation
slug: /vectors/what-is-a-vector/
---

# Lesson 0: What Is a Vector?

**Breadcrumbs:** [Home](/) > [Vectors for Data Science](index.md) > What Is a Vector?

---

## A) What It Means

A vector is simply an ordered list of numbers. When we line up all the features for one customer, we get a vector.

---

## B) How to Picture It

Think of a vector as an arrow pointing somewhere in space. In 2D, it's an arrow on paper. In 6D (like our customer data), it's harder to visualize, but the math works the same.

```
         ↗ (3, 4) = "go right 3, up 4"
        /
       /
      •----→
    origin
```

Each number in the vector tells you how far to go in one direction.

> **📷 Image Idea (Realistic):** A spreadsheet on a computer screen with customer data highlighted, showing one row glowing to represent a single vector
> 
> *Alt text:* Spreadsheet with highlighted customer data row representing a feature vector
> 
> *Caption:* Each row in your customer spreadsheet is a vector

---

## C) Business Example

Alice's feature vector summarizes her entire customer profile:

```
x_alice = [28, 45, 5, 3, 2, 8]
```

This represents: age=28, income=$45k, visits=5, emails_opened=3, prior_purchases=2, satisfaction=8.

Customers with similar vectors probably behave similarly!

---

## D) Where It Shows Up in ML

**Plain words:** When you put all the information about one customer into a single row of your spreadsheet, you've created a vector.

**In machine learning, this is called a "feature vector"** or "input vector." It's the data you feed into your formula to make predictions.

> **📊 Image Idea (Infographic):** Colorful infographic showing a list of numbers [28, 45, 5] transforming into an arrow in 3D space with labeled axes for age, income, and visits
> 
> *Alt text:* Infographic showing numbers becoming a vector arrow in feature space
> 
> *Caption:* A vector is just numbers that can be visualized as a direction

---

## E) Worked Numeric Example

Let's use a simplified 3-feature vector:

```
Customer Carol: x = [35, 60, 9]
Meaning: age=35, income=$60k, satisfaction=9
```

That's a vector! Three numbers in a specific order.

---

## F) Python (NumPy) Snippet

```python
import numpy as np

# Carol's feature vector
x_carol = np.array([35, 60, 9])

print("Carol's vector:", x_carol)
print("Number of features:", len(x_carol))

# Output:
# Carol's vector: [35 60  9]
# Number of features: 3
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
> - A vector is an ordered list of numbers
> - In data science, one customer = one vector
> - The order matters! [28, 45] is different from [45, 28]

---

## H) Common Mistakes

> ❌ **Avoid These Errors**
> 
> - Thinking vectors are only for physics (they're everywhere in data!)
> - Mixing up the order of features (be consistent across all customers)
> - Forgetting that vectors can have any number of dimensions (2, 6, 100, 1000...)

---

## 📝 Practice Questions

**Question 1:** If a customer has age=42, income=$65k, and satisfaction=7, what is their feature vector?

<details>
<summary>Show Answer</summary>

x = [42, 65, 7]

</details>

**Question 2:** Two customers have vectors [30, 50, 8] and [50, 30, 8]. Are they the same?

<details>
<summary>Show Answer</summary>

No! The order matters. The first customer is age 30 with income $50k; the second is age 50 with income $30k.

</details>

---

## 📚 Learning Resources

| Type | Resource | Link |
|------|----------|------|
| 🎬 Video | 3Blue1Brown: Vectors, what even are they? | [Link](https://youtube.com/watch?v=fNk_zzaMoSs) |
| ✏️ Practice | Khan Academy: Vectors unit | [Link](https://khanacademy.org/math/linear-algebra/vectors-and-spaces) |
| 🤖 Applied ML | Kaggle: Intro to Machine Learning | [Link](https://kaggle.com/learn/intro-to-machine-learning) |

---

## Navigation

 | [Course Home](index.md) | [Vector Addition →](vector-addition.md)

---

*© 2026 Your Website Name*
