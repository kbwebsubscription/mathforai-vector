# Web Content Pack: Site Structure & URL Guide

## Folder Structure

```
web_content_pack/
├── html/                          # Clean HTML files (copy-paste ready)
│   ├── index.html                 # Landing page with course overview & FAQ
│   ├── what-is-a-vector.html      # Topic 0
│   ├── vector-addition.html       # Topic 1
│   ├── vector-subtraction.html    # Topic 2
│   ├── scalar-multiplication.html # Topic 3
│   ├── dot-product.html           # Topic 4 ⭐ Most important!
│   ├── cross-product.html         # Topic 5
│   ├── line-equation.html         # Topic 6
│   ├── plane-equation.html        # Topic 7
│   ├── line-intersections.html    # Topic 8
│   └── plane-intersections.html   # Topic 9
│
├── markdown/                      # Markdown versions (for any CMS)
│   ├── index.md
│   ├── what-is-a-vector.md
│   ├── vector-addition.md
│   ├── vector-subtraction.md
│   ├── scalar-multiplication.md
│   ├── dot-product.md
│   ├── cross-product.md
│   ├── line-equation.md
│   ├── plane-equation.md
│   ├── line-intersections.md
│   └── plane-intersections.md
│
└── SITE_STRUCTURE.md              # This file
```

## Suggested URL Slugs

| Lesson | URL Slug |
|--------|----------|
| Landing Page | `/vectors/` |
| Topic 0 | `/vectors/what-is-a-vector/` |
| Topic 1 | `/vectors/vector-addition/` |
| Topic 2 | `/vectors/vector-subtraction/` |
| Topic 3 | `/vectors/scalar-multiplication/` |
| Topic 4 | `/vectors/dot-product/` |
| Topic 5 | `/vectors/cross-product/` |
| Topic 6 | `/vectors/line-equation/` |
| Topic 7 | `/vectors/plane-equation/` |
| Topic 8 | `/vectors/line-intersections/` |
| Topic 9 | `/vectors/plane-intersections/` |

## SEO Summary (All Pages)

| Page | SEO Title | Meta Description |
|------|-----------|------------------|
| Landing | Vectors for Data Science: A Beginner's Guide | Learn vector operations for machine learning with beginner-friendly marketing examples. Master dot products, vector addition, and more with hands-on Python code. |
| Topic 0 | What Is a Vector? - Lesson 0 | Learn what vectors are and how they represent customer data in machine learning. |
| Topic 1 | Vector Addition Explained - Lesson 1 | Learn how to add vectors to combine customer profiles and calculate averages. |
| Topic 2 | Vector Subtraction Explained - Lesson 2 | Learn how to subtract vectors to measure differences and track changes over time. |
| Topic 3 | Scalar Multiplication - Lesson 3 | Learn how to multiply vectors by scalars to scale features and adjust importance. |
| Topic 4 | Dot Product - Lesson 4 | Master the dot product - the foundation of machine learning predictions. |
| Topic 5 | Cross Product Explained - Lesson 5 | Learn the cross product for 3D geometry applications. |
| Topic 6 | Vector Equation of a Line - Lesson 6 | Learn line equations and how they connect to gradient descent. |
| Topic 7 | Equation of a Plane - Lesson 7 | Learn how plane equations create decision boundaries in ML. |
| Topic 8 | Line Intersections - Lesson 8 | Learn how to find where two lines cross - solving systems of equations. |
| Topic 9 | Plane Intersections - Lesson 9 | Learn how plane intersections relate to constrained optimization in ML. |

## Page Template Features

Every lesson page includes:

### Header
- Breadcrumbs: `Home > Vectors for Data Science > [Topic Name]`
- Lesson number badge
- H1 title

### Content Sections (A-H)
- **A) What It Means** - 1-2 sentence definition
- **B) How to Picture It** - Visual intuition with ASCII diagram
- **C) Business Example** - Marketing/survey context
- **D) Where It Shows Up in ML** - Plain explanation → ML terminology
- **E) Worked Numeric Example** - Step-by-step calculation
- **F) Python (NumPy) Snippet** - Code with "Try It Yourself" instructions
- **G) Key Takeaways** - Green callout box with checkmarks
- **H) Common Mistakes** - Red callout box with warnings

### Practice Section
- 2 practice questions with expandable answers

### Resources Section
- 🎬 Video resource (free)
- ✏️ Practice resource (free)
- 🤖 Applied ML resource

### Navigation
- Previous/Next lesson links
- Back to course home link

## Image Prompt Ideas

Each page includes 2 image prompt suggestions with alt text:

1. **Realistic image** - Photo-style representation of the concept
2. **Infographic** - Diagram/visualization for learning

Example from Topic 4 (Dot Product):
- Realistic: "A calculator display showing multiplication sequence with customer data on sticky notes"
- Infographic: "Visual equation showing features × weights = score with colored boxes"

## Accessibility Features

- Semantic HTML5 structure
- ARIA labels on navigation
- Descriptive alt text for all images
- Short paragraphs (2-3 sentences max)
- Descriptive link text (no "click here")
- High contrast color scheme
- Expandable answer sections for cognitive load management

## CMS Integration Notes

### For WordPress/Ghost/etc:
1. Use the Markdown files in `/markdown/`
2. The frontmatter includes: title, description, keywords, slug
3. Images are placeholders - generate using the prompts provided

### For Static Site Generators (Hugo, Jekyll, etc):
1. Use Markdown files with frontmatter
2. Update internal links to match your site structure

### For Direct HTML Publishing:
1. Use the HTML files in `/html/`
2. Update relative links if needed
3. Add your own CSS for custom styling (base styles included)

## Dataset Used Throughout

**"Cozy Corner Shop"** - Online store selling candles and home goods

Customer feature vector:
```
x = [age, income_k, visits, emails_opened, prior_purchases, satisfaction]
```

Example customers:
| Customer | Age | Income | Visits | Emails | Purchases | Satisfaction |
|----------|-----|--------|--------|--------|-----------|--------------|
| Alice | 28 | $45k | 5 | 3 | 2 | 8 |
| Bob | 52 | $80k | 1 | 0 | 0 | 5 |
| Carol | 35 | $60k | 8 | 6 | 5 | 9 |

Outcomes predicted:
1. **Conversion** - Did they buy after receiving an email?
2. **Churn** - Did they stop buying from us?

---

*Generated January 2026*
