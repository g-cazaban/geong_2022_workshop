---
title: Step 3 - Export as centroid for proportional symbols
parent: Enrich our model - part 1
nav_order: 3
---

## Step 3: Export as centroid for proportional symbols

### A - Add Centroids algorithm, rename it: “Centroids admin”
- Input layer: “Count point in polygon low fire”
- Output:
  - Name it: count_fire_admin_centroid
  - Remove output from “Count point in polygon low fire”

### B - Manage dependencies

- “Centroids admin” depend of “Count point in polygon low fire”

### C - Run the model to test results consistency.

![image](/assets/images/4_3_a_schema.png)

### D - Save as you model, in case further developments break its execution. It will help you to get back on a solid base, if you mess up the processing.

> Model output: Model_on_fire_v2.3.model3
