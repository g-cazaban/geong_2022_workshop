---
title: Step 1 - Count fire in grid
parent: Enrich our model - part 2
nav_order: 1
---

## Step 1: Count fire in grid

### A - Add Create a Grid algorithm
  - Grid type: *rectangle (polygon)*
  - Grid extent: *“administrative polygon layer”*
  - Horizontal *spacing: 1*
  - Vertical *spacing: 1*
  - Horizontal *overlay: 0*
  - Vertical *overlay: 0*
  - Grid CRS: *use project CRS*

### B - Add 3 Count points in polygon algorithm (One for each confidence level, rename it), ex: “Count point in grid high fire”

  - Polygon input: Grid from algorithm “Create grid”
  - Point input: Matching features from algorytm “Extract by expression high fire”
  - Field name: nb_high_fire
  - Same for nominal and low fire

>**💡You can copy, paste the algorithm selected in the Graphical modeller.**

### C - Manage dependencies

- Define dependencies depending on algorithm execution order set (Count points in grid high, …nominal, …low).

### D - Run the model to test results consistency.

![image](/assets/images/5_1_a_schema.png)

### E - Save as you model, in case further developments break its execution. It will help you to get back on a solid base, if you mess up the processing.

> Model output: Model_on_fire_v3.1.model3

