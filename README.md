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

## Example Usage

```python
# Import necessary modules
import exasens_toolbox as etb

# Load the dataset
data = etb.load_dataset("https://archive.ics.uci.edu/ml/datasets/Exasens")

# Preprocess the data
cleaned_data = etb.preprocess_data(data)

# Visualize the data
etb.plot_scatter_pairs(cleaned_data)
etb.plot_iris_pca()

# Perform low rank reconstruction
reconstructed_data = etb.low_rank_reconstruction(cleaned_data, rank=3)

# Generate synthetic data
synthetic_data, targets = etb.make_data(k=5, num_instances=500, radius=10, ratio=2)

# Fit an LDA model
lda_params = etb.fit_LDA(synthetic_data, targets)

# Test the LDA model
predictions = etb.test_LDA(synthetic_data, lda_params)

# Generate a grid dataset
grid_data = etb.make_grid(density=10)

# Display scatter plot of grid dataset
etb.plot_grid_predictions(grid_data, lda_params)
```
