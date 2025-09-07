# Machine Learning Project Documentation

## Project Overview
This project involves analyzing purchase order items data using machine learning techniques.

## Dataset Information
- **File**: `purchase-order-items.xlsx`
- **Total Records**: 3,150 entries
- **Columns**: 11 total columns

### Dataset Structure
| Column | Non-Null Count | Data Type |
|--------|----------------|-----------|
| Item ID | 3,150 | int64 |
| Item Name | 2,910 | object |
| Quantity | 3,150 | float64 |
| Total Bcy | 3,150 | float64 |
| Sub Total Bcy | 3,150 | float64 |
| Purchase Order ID | 3,150 | int64 |
| Product ID | 2,910 | float64 |
| Currency Code | 3,150 | object |
| Account ID | 3,150 | int64 |
| Tax ID | 3,085 | float64 |
| Project ID | 0 | float64 |

## Libraries Used
```python
import warnings
import numpy as np
import matplotlib.pyplot as plt
import pandas as pd
import seaborn as sns
from sklearn.impute import KNNImputer
from sklearn.metrics import confusion_matrix, precision_score, recall_score, accuracy_score, f1_score
```

## Data Analysis Steps

### 1. Data Import
- ✅ Successfully loaded dataset from Excel file
- ✅ Initial data exploration completed

### 2. Data Quality Assessment
- **Missing Values Identified**:
  - Item Name: 240 missing values (7.6%)
  - Product ID: 240 missing values (7.6%)
  - Tax ID: 65 missing values (2.1%)
  - Project ID: 3,150 missing values (100% - completely empty column)

### 3. Key Observations
- All transactions are in SAR currency
- Project ID column is completely empty and may need to be dropped
- Item Name and Product ID have the same missing pattern (240 records)

### 4. Correlation Analysis
- ✅ **Correlation Matrix Computed and Visualized**

```python
# Step 2: Compute correlation matrix
corr_matrix = df.corr()

# Step 3: Optional - Visualize the correlation matrix
plt.figure(figsize=(10, 8))
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm', vmin=-1, vmax=1)
plt.title('Correlation Matrix')
plt.show()
```

**Key Findings:**
- **Tax ID**: Shows empty/weak correlation with other variables
- **Project ID**: Completely empty column with no correlations
- Empty relationships identified between certain columns
- These columns may not contribute to predictive modeling

## Next Steps
- [ ] Handle missing values in Item Name and Product ID
- [x] Correlation analysis completed
- [ ] Drop columns with empty relationships (Tax ID, Project ID)
- [ ] Exploratory data analysis (EDA)
- [ ] Feature engineering
- [ ] Model selection and training
- [ ] Model evaluation

## Notes
- Dataset appears to be financial/procurement data
- Need to investigate the relationship between missing Item Name and Product ID values
- **Correlation findings**: Tax ID and Project ID show empty relationships with other variables
- Consider dropping columns with no predictive value before modeling

---
*Last Updated: [Current Date]*