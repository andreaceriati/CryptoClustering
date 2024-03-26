# CryptoClustering

In this repository you will find a "Resources" folder, which contains the data used for the analysis, an "Images" folder, which contains the results of the analysis, and a Jupyter notebook titled "Crypto_Clustering".

In the Jupyter notebook you will find the code with the analysis that led to the following answers:

**Question 1:** What is the best value for `k`?

<p align='center'> <img src='Images/elbow_curve.png'></p>

**Answer:** The best value for k based on the elbow curve is 4.

**Question 2:** What is the total explained variance of the three principal components?

**Answer:** The total explained variance of the three principal components is 89.5 meaning that between this three vectors we have 89.5% of the exploratory power out of the 100% that it was in the original matrix. We lost 11.5% of explained variance.

**Question 3:** What is the best value for `k` when using the PCA data?

<p align='center'> <img src='Images/elbow_curve_pca.png'></p>

**Answer:** The best value for `k` when using the PCA data is 4.

**Question 4:** Does it differ from the best k value found using the original data?

**Answer:** No, it does not.

**Question 5:** After visually analyzing the cluster analysis results, what is the impact of using fewer features to cluster the data using K-Means?

<p align='center'> <img src='Images/composite_elbow.png'></p>

<p align='center'> <img src='Images/composite_scatter.png'></p>

**Answer:** Upon examining the elbow curves, it's evident that they share similar shapes and indicate an optimal number of clusters at k=4. However, when utilizing PCA data, the curve manifests a lower inertia from the outset, implying a denser grouping of data points within the reduced dimensional space.

  Upon reviewing the scatter plots, it becomes apparent that the primary clusters (light-blue and yellow) remain consistent across both models. However, there's a noticeable difference in the positioning of the other two clusters (red and green).

  Using fewer features for K-Means clustering yielded consistent outcomes in terms of identifying the optimal number of clusters and effectively clustering the primary clusters. It also led to enhanced cluster separation and reduced computational demands. The sole drawback observed was the emergence of two outliers. This observation suggests that the model utilizing PCA data may exhibit reduced precision. Several factors should be considered:

  - The data might not have undergone adequate preprocessing prior to PCA, potentially resulting in outliers or noise affecting clustering outcomes.
  - The choice of the number of principal components could influence the representation of variance in the data, potentially leading to information loss or misrepresentation of the underlying structure.