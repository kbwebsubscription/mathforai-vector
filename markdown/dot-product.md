---
title: "Dot Product Explained | The Most Important Vector Operation for ML - Lesson 4"
description: "Master the dot product - the foundation of machine learning predictions. Learn how to calculate scores from features and weights with Python examples."
keywords:
  - dot product
  - inner product
  - linear model
  - prediction score
  - feature weights
  - machine learning basics
slug: /vectors/dot-product/
---

# Lesson 4: Dot Product

**Breadcrumbs:** [Home](/) > [Vectors for Data Science](index.md) > Dot Product

---

## A) What It Means

The dot product takes two vectors and produces a single number. You multiply matching elements, then add everything up.

---

## B) How to Picture It

Formula: a · b = a₁×b₁ + a₂×b₂ + a₃×b₃ + ...

The dot product measures how much two vectors point in the same direction:

```
Same direction:     →  →      dot product: LARGE POSITIVE
Opposite:           →  ←      dot product: NEGATIVE  
Perpendicular:      →  ↑      dot product: ZERO
```

> **📷 Image Idea (Realistic):** A calculator display showing a multiplication and addition sequence, with customer data on sticky notes nearby
> 
> *Alt text:* Calculator showing dot product computation with customer data
> 
> *Caption:* The dot product: multiply and add to get a prediction score

---

## C) Business Example

**This is the BIG one for data science!**

**Situation:** Calculate a "score" for how likely Alice is to buy.

```
Alice's features: x = [28, 45, 5, 3, 2, 8]
Weights:          w = [0.01, 0.02, 0.5, 0.3, 0.8, 0.4]

Score = w · x 
     = (0.01×28) + (0.02×45) + (0.5×5) + (0.3×3) + (0.8×2) + (0.4×8)
     = 0.28 + 0.9 + 2.5 + 0.9 + 1.6 + 3.2
     = 9.38
```

The weights say: "prior purchases (0.8) and visits (0.5) matter a lot; age (0.01) barely matters."

**Higher score → more likely to buy!**

---

## D) Where It Shows Up in ML

**Plain words:** Almost every prediction formula works like this: take the customer's features, multiply each one by how important it is (the weight), and add them up.

**In machine learning, this is the core of "linear models."**

`score = w · x + b`

Where:
- `w` = weight vector (importance of each feature)
- `x` = customer's feature vector
- `b` = "bias" or starting point

Linear regression, logistic regression, and neural networks ALL use dot products!

> **📊 Image Idea (Infographic):** Visual equation showing features × weights = score, with colored boxes showing each multiplication step combining into a final number
> 
> *Alt text:* Step-by-step dot product calculation infographic
> 
> *Caption:* score = features · weights: the heart of ML predictions

---

## E) Worked Numeric Example

```
Customer: x = [30, 50, 7]   (age, income_k, satisfaction)
Weights:  w = [0.1, 0.05, 1.0]

Dot product:
w · x = (0.1 × 30) + (0.05 × 50) + (1.0 × 7)
      = 3 + 2.5 + 7
      = 12.5
```

Score = 12.5. Higher numbers = better match!

---

## F) Python (NumPy) Snippet

```python
import numpy as np

# Customer features
x = np.array([30, 50, 7])

# Learned weights
w = np.array([0.1, 0.05, 1.0])

# Dot product - two equivalent ways
score1 = np.dot(w, x)
score2 = np.sum(w * x)  # element-wise multiply, then sum

print("Score (np.dot):", score1)
print("Score (manual):", score2)

# Output:
# Score (np.dot): 12.5
# Score (manual): 12.5
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
> - Dot product: multiply matching elements, add them up → one number
> - It's the foundation of almost all prediction models
> - score = weights · features is how ML models make guesses

---

## H) Common Mistakes

> ❌ **Avoid These Errors**
> 
> - Forgetting vectors must be the same length
> - Mixing up dot product (gives a number) with scalar multiplication (gives a vector)
> - Not realizing order matters conceptually (w · x means 'weight the features')

---

## 📝 Practice Questions

**Question 1:** Calculate: [2, 3] · [4, 5]

<details>
<summary>Show Answer</summary>

(2×4) + (3×5) = 8 + 15 = 23

</details>

**Question 2:** If weights are [0, 0, 1] and features are [100, 200, 5], what's the score?

<details>
<summary>Show Answer</summary>

Score = 0×100 + 0×200 + 1×5 = 5. Only the third feature matters!

</details>

---

## 📚 Learning Resources

| Type | Resource | Link |
|------|----------|------|
| 🎬 Video | 3Blue1Brown: Dot products and duality | [Link](https://youtube.com/watch?v=LyGKycYT2v0) |
| ✏️ Practice | Khan Academy: Dot product exercises | [Link](https://khanacademy.org/math/linear-algebra/vectors-and-spaces/dot-cross-products) |
| 🤖 Applied ML | StatQuest: Linear Regression Explained | [Link](https://youtube.com/watch?v=nk2CQITm_eo) |

---

## Navigation

[← Scalar Multiplication](scalar-multiplication.md) | [Course Home](index.md) | [Cross Product →](cross-product.md)

---

*© 2026 Your Website Name*
