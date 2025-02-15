# MATH-CSCI485_Spring25_Snehitha_Gorantla

## PCA vs. t-SNE for Wine Quality Data Visualization

This report compares the use of Principal Component Analysis (PCA) and t-distributed Stochastic Neighbor Embedding (t-SNE) for visualizing the wine quality dataset.  Both methods aim to reduce the dimensionality of the data while preserving important information, but they approach this task differently and have distinct strengths and weaknesses.

**PCA:**

PCA is a linear dimensionality reduction technique that identifies the principal components of the data, which are orthogonal directions that capture the maximum variance.  It's computationally efficient and provides insights into the variance explained by each component.  However, PCA assumes linear relationships between features and may not capture complex non-linear structures in the data.

* **Strengths:** Computationally fast, explains variance, identifies important linear combinations of features.
* **Weaknesses:** Assumes linearity, may not be suitable for highly complex datasets.

**t-SNE:**

t-SNE is a non-linear dimensionality reduction technique that focuses on preserving the local structure of the data.  It models the probability distribution of pairwise similarities between data points and aims to embed them in a lower-dimensional space while minimizing the difference between the high-dimensional and low-dimensional distributions.  t-SNE is particularly effective at visualizing clusters and separating groups of data points. However, it's computationally intensive and the resulting visualizations can be sensitive to the choice of parameters (like perplexity).  Also, the axes in t-SNE plots don't have a direct interpretation like principal components in PCA.

* **Strengths:** Excellent for visualizing clusters and non-linear structures.
* **Weaknesses:** Computationally intensive, sensitive to parameters, axes are not directly interpretable.

**Key Observations from Visualizations:**

* **Correlation Heatmap:** The heatmap reveals correlations between different features.  For example, alcohol content appears positively correlated with quality, while volatile acidity seems negatively correlated. This information is useful for understanding the relationships between the original features.

* **PCA:** The 2D and 3D PCA plots show some separation between different quality levels, but the separation is not very distinct.  The explained variance by the first two components is relatively low, suggesting that much of the variance is still lost in the 2D projection.  The 3D plot provides a slightly better view, but still, the clusters overlap considerably.

* **t-SNE:** The t-SNE visualizations, both 2D and 3D, reveal more distinct clusters corresponding to different wine quality levels.  The separation between clusters is noticeably better than in the PCA plots, indicating t-SNE's ability to capture the non-linear structure of the data and preserve local neighborhoods.

**Trade-offs:**

The choice between PCA and t-SNE depends on the specific goals of the analysis.  If the primary goal is to understand the variance explained by different components and identify important linear combinations of features, PCA is a good choice.  If the goal is to visualize clusters and separate groups of data points, especially in the presence of non-linear relationships, t-SNE is generally more effective, although it is computationally more expensive and requires careful parameter tuning.  In this wine quality dataset, t-SNE proved to be more effective at revealing the underlying cluster structure related to wine quality.
