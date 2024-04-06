# Exasens Analysis Toolbox 📊

Welcome to the Exasens Analysis Toolbox repository! This toolkit provides a set of functions and utilities to analyze the Exasens dataset available at UCI Machine Learning Repository.

## Features 🛠️
1. Data Preprocessing
Ignore specified columns: We handle extra columns at the end and multiple rows for column names.
Replace missing values: Replace missing values with the average between the median and mean column value.
2. Visualization
- Scatter Plots: Display scatter plots for distinct pairs of columns. Distinguish instances with missing values from those without.
2D Scatter Plot of Iris Dataset: Plot instances from the Iris dataset using PCA, color-coded by class.
3. Low Rank Reconstruction
- Custom Low Rank Reconstruction: Perform low rank reconstruction of a data matrix based on user-specified rank.
- Reconstruction Error Calculation: Compute reconstruction error for each instance.
4. Data Generation
- Generate Synthetic Data: Generate synthetic data with specified parameters like number of classes, instances, radius, and ratio.
- Generate Regular Grid: Generate regularly spaced instances in 2D with customizable density.
5. Linear Discriminant Analysis (LDA)
- Fit LDA Model: Fit an LDA classifier to the data.
- Test LDA Model: Make predictions using the trained LDA model.
