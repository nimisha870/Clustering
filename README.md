# 🌸 Iris Dataset Clustering: An Unsupervised Learning Exploration
This project investigates unsupervised clustering on the classic Iris dataset using various preprocessing pipelines and clustering algorithms. Performance is benchmarked with standard clustering evaluation metrics.

--- 

## 📂 Dataset Overview
Source: sklearn.datasets.load_iris()

Features: 4 numerical features describing iris flower morphology

Labels: 3 iris species (used only for evaluation)

---

## 🤖 Clustering Techniques
The following clustering algorithms were applied:

🔹 K-Means Clustering

🔹 Agglomerative (Hierarchical) Clustering

🔹 Mean Shift Clustering

---

## 🧪 Preprocessing Strategies
Six different preprocessing workflows were explored:


Label	Description
Raw	No transformation
Normalized	StandardScaler
Transformed	PowerTransformer
PCA	PCA (2 components)
Norm + Trans	StandardScaler + PowerTransformer
Norm + Trans + PCA	Combined scaling, transformation, and PCA (2D)

---

## 📊 Evaluation Metrics
Clustering quality was measured using:

Silhouette Score → Higher is better

Calinski-Harabasz Index → Higher is better

Davies-Bouldin Score → Lower is better

---

## 📌 Experiment Summary
Cluster counts of 2, 3, 4, and 5 were evaluated for KMeans and Hierarchical Clustering.

Mean Shift automatically estimated cluster counts based on bandwidth.

PCA was used to reduce dimensionality in select pipelines.

---

## 🏅 Top Performing Configuration

Algorithm	Preprocessing	Optimal Clusters	Silhouette Score
Hierarchical	PCA	2	0.7112
✔️ This setup achieved the best clustering performance across all tested combinations.

---

## 💡 Key Insights
Hierarchical Clustering + PCA achieved the highest silhouette score.

KMeans was reliable, though marginally behind in performance.

Mean Shift was sensitive to preprocessing and bandwidth.

Combining Normalization + Transformation improved results in several cases.

Dimensionality reduction with PCA often enhanced clustering separation.

---

## 📈 Visual Results
The following chart compares the silhouette scores across preprocessing and clustering combinations:

---

## 🧾 Conclusion
Clustering effectiveness depends heavily on preprocessing choices. In this study, the Hierarchical Clustering with PCA pipeline provided the most meaningful cluster separation. This reinforces the need to experiment with preprocessing and algorithm combinations when applying clustering to real-world datasets.