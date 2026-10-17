# 📐 Key DAX Measures & Formulas

This document outlines the core DAX (Data Analysis Expressions) calculations utilized across the Marketing Campaign Performance & ROI Dashboard.

---

### 1. Total Marketing Spend
```dax
Total Spend = SUM('marketing campaign performance'[Spend])
```

---

### 2. Total Attributed Revenue
```dax
Total Revenue = SUM('marketing campaign performance'[Revenue])
```

---

### 3. Average Return on Investment (ROI)
```dax
Average of ROI = AVERAGE('marketing campaign performance'[ROI])
```

---

### 4. Click-Through Rate (CTR %)
```dax
CTR % = 
DIVIDE(
    SUM('marketing campaign performance'[Clicks]),
    SUM('marketing campaign performance'[Impressions]),
    0
)
```

---

### 5. Conversion Rate %
```dax
Conversion Rate % = 
DIVIDE(
    SUM('marketing campaign performance'[Conversions]),
    SUM('marketing campaign performance'[Clicks]),
    0
)
```

---

### 6. Cost Per Conversion (CAC Proxy)
```dax
Cost Per Conversion = 
DIVIDE(
    [Total Spend],
    SUM('marketing campaign performance'[Conversions]),
    0
)
```
