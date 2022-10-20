---
title: Step 2 - Manage date of data as input
parent: Enrich our model - part 1
nav_order: 2
---

## Step 2: Manage date of data as input

### A - Add two date input
- Date from
- Date To

![image](/assets/images/4_2_a_date_from.png)

### B - Add Extract by expression algorithm (rename it, “Extract by expression dates”)

- Input layer: Fire point layer
Expression: 
```
"ACQ_DATE" > @date_from AND "ACQ_DATE" < @date_to
```

### C - Manage dependencies and link “Extract by expression date” algorithm in the right place of the processing

- Change input layer of  “Field calculator conf_l” algorithm and put Matching features from algorithm “Extract by expression date”
“Field calculator conf_l” depend “Extract by expression date”

### D - Run the model to test results consistency

![image](/assets/images/4_2_b_schema.png)

### E - Save as you model, in case further developments break its execution. It will help you to get back on a solid base, if you mess up the processing

> Model output: Model_on_fire_v2.2.model3
