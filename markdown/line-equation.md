---
title: "Vector Line Equation | Understanding Gradient Descent - Lesson 6"
description: "Learn the vector equation of a line and how it connects to gradient descent - the algorithm that trains machine learning models."
keywords:
  - vector equation line
  - parametric line
  - gradient descent
  - optimization
  - learning rate
slug: /vectors/line-equation/
---

# Lesson 6: Vector Equation of a Line

**Breadcrumbs:** [Home](/) > [Vectors for Data Science](index.md) > Vector Equation of a Line

---

## A) What It Means

A line in vector form describes all points you can reach by starting somewhere and moving in a specific direction.

---

## B) How to Picture It

**Formula:** point = start + t × direction

Where t is any number. As t changes, you trace out the line.

```
t = -1      t = 0       t = 1       t = 2
  •-----------•-----------•-----------•→
            start       (one step)   (two steps)
```

Think of a hiking trail. The "start" is where you are. The "direction" is which way the trail goes.

> **📷 Image Idea (Realistic):** A hiking trail through a forest with distance markers, representing moving along a line direction
> 
> *Alt text:* Hiking trail with distance markers showing linear progression
> 
> *Caption:* Walking along a trail = moving along a line with parameter t

---

## C) Business Example

**Situation:** Predicting how Alice might change over time.

```
Start (now):        x_start = [28, 45, 5]  (age, income_k, satisfaction)
Change per year:    d = [1, 3, 0.5]  (age +1, income +$3k, satisfaction +0.5)

Where will Alice be in t years?
x_future = x_start + t × d

In 5 years (t = 5):
x_future = [28, 45, 5] + 5 × [1, 3, 0.5]
         = [28, 45, 5] + [5, 15, 2.5]
         = [33, 60, 7.5]
```

Alice at age 33, earning $60k, satisfaction 7.5!

---

## D) Where It Shows Up in ML

**Plain words:** Lines help us think about trends and gradual changes.

**In machine learning, "gradient descent" follows this exact pattern:**

`new_weights = old_weights - learning_rate × gradient`

This is the line equation! Start at old weights, move in the gradient direction. Each step improves your model's predictions.

> **📊 Image Idea (Infographic):** Animation-style diagram showing a ball rolling downhill in steps, labeled with gradient descent formula
> 
> *Alt text:* Gradient descent visualization with steps down a slope
> 
> *Caption:* Gradient descent: step by step toward better predictions

---

## E) Worked Numeric Example

```
Start (now):     x₀ = [25, 40]   (age, income_k)
Direction:       d  = [1, 2]     (each year: age +1, income +$2k)
Time:            t  = 3 years

Future position:
x = x₀ + t × d
x = [25, 40] + 3 × [1, 2]
x = [25, 40] + [3, 6]
x = [28, 46]
```

In 3 years: age 28, income $46k.

---

## F) Python (NumPy) Snippet

```python
import numpy as np

# Starting point
x0 = np.array([25, 40])

# Direction of change
d = np.array([1, 2])

# Calculate position at t = 0, 1, 2, 3
for t in [0, 1, 2, 3]:
    x = x0 + t * d
    print(f"t = {t}: age = {x[0]}, income = $" + str(x[1]) + "k")

# Output:
# t = 0: age = 25, income = $40k
# t = 1: age = 26, income = $42k
# t = 2: age = 27, income = $44k
# t = 3: age = 28, income = $46k
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
> - Line = start point + t × direction
> - Changing t moves you along the line
> - Gradient descent (how models learn) follows this exact pattern

---

## H) Common Mistakes

> ❌ **Avoid These Errors**
> 
> - Forgetting that t can be negative (going backward on the line)
> - Confusing the direction vector with the destination point
> - Forgetting that in high dimensions, a 'line' is still just start + t × direction

---

## 📝 Practice Questions

**Question 1:** Given start = [10, 20] and direction = [2, 5], find the point at t = 4

<details>
<summary>Show Answer</summary>

[10, 20] + 4×[2, 5] = [10+8, 20+20] = [18, 40]

</details>

**Question 2:** In gradient descent, what does the 'direction' represent?

<details>
<summary>Show Answer</summary>

The gradient - the direction of steepest improvement for the model

</details>

---

## 📚 Learning Resources

| Type | Resource | Link |
|------|----------|------|
| 🎬 Video | Khan Academy: Parametric equations of lines | [Link](https://khanacademy.org/math/multivariable-calculus) |
| ✏️ Practice | MIT OCW: Linear Algebra Problem Sets | [Link](https://ocw.mit.edu/courses/18-06-linear-algebra-spring-2010/) |
| 🤖 Applied ML | Google ML Crash Course: Gradient Descent | [Link](https://developers.google.com/machine-learning/crash-course/reducing-loss/gradient-descent) |

---

## Navigation

[← Cross Product](cross-product.md) | [Course Home](index.md) | [Plane Equation →](plane-equation.md)

---

*© 2026 Your Website Name*
