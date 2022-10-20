---
title: Step 3 - Calculate density of  high fire
parent: Enrich our model - part 2
nav_order: 3
---

## Step 3: Calculate density of  high fire

### A - Add Reproject layer algorithm, rename it: “Reproject layer grid”

- Input layer: Count from algorithm “Count point in grid low fire”
- Target CRS: *EPSG: 3857 - WGS 84 / Pseudo-Mercator*

### B - Add Field Calculator algorithm, rename it: “Field Calculator_grid”

- Input layer: Reprojected from algorithm “Reproject layer grid”
- Field name: *h_fire_density*
- Type: *Decimal*
- Length: *30*
- Precision: *10*
- Expression: *"nb_high_fire" / $area*
- Output: *fire_grid_density*

### C - Manage dependencies

- “Reproject layer admin” depend of “Count point in grid low fire”
- “Field Calculator h_fire_density grid” depend of “Reproject layer grid”

### D - Understand density value

**Depending on the Project properties** you have, the function $area will calculate area in **m²** or **km²**, or other units. 
As all grid squares have the same area, these steps are not really useful, but let keep it mind: we should represent the polygon with graduated colour value from a ratio and not an integer according to semiological rules.

### E - Run the model to test results consistency.

![image](/assets/images/5_3_a_schema.png)

### F - Save as you model, in case further developments break its execution. It will help you to get back on a solid base, if you mess up the processing.

> Model output: Model_on_fire_v3.3.model3
