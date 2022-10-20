---
title: Step 2 - Export as centroid for proportional symbols
parent: Enrich our model - part 2
nav_order: 2
---

## Step 2: Export as centroid for proportional symbols

### A - Add Centroids algorithm, rename it: “Centroids grid”

- Input layer: “Count point in grid low fire”
- Output:
  - Name it: *count_fire_grid_centroid*
  - Remove output from “Count point in grid low fire”

### B - Manage dependencies

- “Centroids grid” depend of “Count point in grid  low fire”

### C - Run the model to test results consistency.

![image](/assets/images/5_2_a_schema.png)

### D - Save as you model, in case further developments break its execution. It will help you to get back on a solid base, if you mess up the processing.

> Model output: Model_on_fire_v3.2.model3
