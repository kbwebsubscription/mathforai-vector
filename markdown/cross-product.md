---
title: "Cross Product Explained | Vectors for Data Science - Lesson 5"
description: "Learn the cross product for 3D geometry. While less common in tabular ML, it's essential for computer vision and robotics applications."
keywords:
  - cross product
  - vector product
  - 3D vectors
  - perpendicular vector
  - surface normal
slug: /vectors/cross-product/
---

# Lesson 5: Cross Product

**Breadcrumbs:** [Home](/) > [Vectors for Data Science](index.md) > Cross Product

---

## A) What It Means

The cross product takes two vectors (in 3D) and produces a new vector that is perpendicular (at a 90° angle) to both original vectors.

---

## B) How to Picture It

Imagine two arrows lying on a table. The cross product gives you an arrow pointing straight UP, perpendicular to the table.

```
        ↑ (a × b) points UP
        |
        |
    ----+----→ b
       /
      /
     ↙ a
```

The length of a × b tells you the area of the parallelogram formed by a and b.

> **📷 Image Idea (Realistic):** A smartphone showing orientation sensors with 3D arrows indicating x, y, z axes and rotation
> 
> *Alt text:* Smartphone displaying 3D orientation axes from sensors
> 
> *Caption:* Your phone uses cross products to know which way is 'up'

---

## C) Business Example

**Note: Cross products are mostly used in 3D geometry, not typical customer spreadsheets.**

**Where you might see it:**

- **Phone orientation:** Your phone knows which way is "up" using cross products of sensor readings
- **3D product visualization:** If your online store shows 3D models customers can rotate
- **Geospatial analysis:** Delivery routes on Earth's surface (a 3D sphere)

---

## D) Where It Shows Up in ML

**Plain words:** For typical tabular/spreadsheet data (customers with features like age, income), you almost never use cross products. The dot product is your workhorse.

**However,** cross products show up in:
- Computer vision (3D object detection)
- Robotics (arm movements, drone navigation)  
- Physics simulations (games, VR)

**In machine learning for 3D data, this might be called "surface normal calculation."**

> **📊 Image Idea (Infographic):** Two flat arrows on a plane with a third arrow pointing perpendicular, labeled with the cross product formula
> 
> *Alt text:* Cross product creating perpendicular vector diagram
> 
> *Caption:* Cross product: find the direction perpendicular to two vectors

---

## E) Worked Numeric Example

```
a = [1, 0, 0]  (pointing "right")
b = [0, 1, 0]  (pointing "forward")

Cross product formula:
a × b = [a₂b₃ - a₃b₂, a₃b₁ - a₁b₃, a₁b₂ - a₂b₁]
      = [(0×0 - 0×1), (0×0 - 1×0), (1×1 - 0×0)]
      = [0, 0, 1]
```

Result: [0, 0, 1] points "up" — perpendicular to both!

---

## F) Python (NumPy) Snippet

```python
import numpy as np

a = np.array([1, 0, 0])  # right
b = np.array([0, 1, 0])  # forward

# Cross product
c = np.cross(a, b)
print("a × b =", c)

# Verify it's perpendicular (dot products should be 0)
print("c · a =", np.dot(c, a))
print("c · b =", np.dot(c, b))

# Output:
# a × b = [0 0 1]
# c · a = 0
# c · b = 0
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
> - Cross product is for 3D vectors only
> - Result is a new vector, perpendicular to both inputs
> - Rare in spreadsheet ML, common in graphics/physics/robotics

---

## H) Common Mistakes

> ❌ **Avoid These Errors**
> 
> - Trying to use cross product on non-3D data (it doesn't work!)
> - Confusing cross product (gives vector) with dot product (gives number)
> - Order matters! a × b = -(b × a) — they point opposite directions

---

## 📝 Practice Questions

**Question 1:** What type of result does a cross product give: a number or a vector?

<details>
<summary>Show Answer</summary>

A vector (perpendicular to both inputs)

</details>

**Question 2:** Can you compute the cross product of [1, 2] and [3, 4]?

<details>
<summary>Show Answer</summary>

No! Cross product only works for 3D vectors.

</details>

---

## 📚 Learning Resources

| Type | Resource | Link |
|------|----------|------|
| 🎬 Video | 3Blue1Brown: Cross products | [Link](https://youtube.com/watch?v=eu6i7WJeinw) |
| ✏️ Practice | Khan Academy: Cross product exercises | [Link](https://khanacademy.org/math/linear-algebra/vectors-and-spaces/dot-cross-products) |
| 🤖 Applied ML | PyTorch3D Documentation | [Link](https://pytorch3d.org/docs/cameras) |

---

## Navigation

[← Dot Product](dot-product.md) | [Course Home](index.md) | [Line Equation →](line-equation.md)

---

*© 2026 Your Website Name*
