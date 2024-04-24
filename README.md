
# Assignment: Parameter Optimization SVM

## Overview
This document presents an in-depth examination of the Dry Bean Dataset, accessible through the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Dry+Bean+Dataset) (Dataset ID: 602).

## Methodology
1. **Data Acquisition**: Utilizing the UCI ML Repository API, the Dry Bean Dataset is retrieved.
2. **Data Preprocessing**: The dataset undergoes segmentation into features (X) and target (y). A partition into training and testing subsets is executed for model evaluation.
3. **Model Selection**: Leveraging Nu-Support Vector Classifier (NuSVC) with Bayesian Optimization, hyperparameters are optimized.
4. **Model Assessment**: Cross-validation and convergence plots are employed to assess the model's accuracy.
5. **Result Interpretation**: Analysis is conducted on the optimal hyperparameters and achieved accuracy.

## Dataset Overview
The Dry Bean Dataset encompasses a diverse array of attributes pertaining to dry beans, comprising geometric, shape, and texture characteristics utilized for bean categorization.

### Features
- Area
- Perimeter
- MajorAxisLength
- MinorAxisLength
- AspectRatio
- Eccentricity
- ConvexArea
- EquivDiameter
- Extent
- Solidity
- Roundness
- Compactness
- ShapeFactor1
- ShapeFactor2
- ShapeFactor3
- ShapeFactor4

### Target
The target variable denotes the class of the dry bean.

## Exploratory Data Analysis

### Summary Statistics
```python
# Summary statistics of the dataset
summary_statistics = X.describe()
print(summary_statistics)
```

```python
# Class distribution
class_distribution = y['Class'].value_counts()
print(class_distribution)
```

```python
import seaborn as sns
# Calculate correlation matrix
correlation_matrix = X.corr()
# Plot heatmap
plt.figure(figsize=(12, 8))
sns.heatmap(correlation_matrix, annot=True, cmap='coolwarm', fmt=".2f")
plt.title('Correlation Heatmap')
plt.show()
```

## Result Table

![Result Table](Result_Table.png)

## Result Graph

![Result Graph](Result_Graph.png)
