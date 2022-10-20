---
title: Step 4 - Calculate density of high fire
parent: Enrich our model - part 1
nav_order: 4
---

## Step 4: Calculate density of high fire

### A - Add Reproject layer algorithm, rename it: “Reproject layer admin”

- Input layer: Count from algorithm “Count point in polygon low fire”
- Target CRS: *EPSG: 3857 - WGS 84 / Pseudo-Mercator*

### B - Add Field Calculator algorithm, rename it: “Field Calculator admin”

- Input layer: Reprojected from algorithm “Reproject layer admin”
- Field name: *h_fire_density*
- Type: *Decimal*
- Length: *30*
- Precision: *10*
- Expression: *"nb_high_fire" / $area*
- Output: *fire_admin_density*

### C - Manage dependencies

- “Reproject layer admin” depend of “Count point in polygon low fire”
- “Field Calculator h_fire_density admin” depend of “Reproject layer admin”

### D - Understand density value

- Depending on the Project properties you have, the function $area will calculate area in m² or km², or other units.

### E - Run the model to test results consistency.

![image](/assets/images/4_4_a_schema.png)


### F - Save as you model, in case further developments break its execution. It will help you to get back on a solid base, if you mess up the processing.

> Model output: Model_on_fire_v2.4.model3
