# Customer Segmentation using K-Means Clustering

This project applies **K-Means Clustering** to segment customers based on their **Annual Income** and **Spending Score** using a mall customer dataset.

---

## 📌 Objective

To group customers into distinct clusters using K-Means based on spending behavior and income, helping businesses target specific customer segments more effectively.

---

## 📂 Dataset

The dataset contains customer data with the following features:

- `CustomerID`
- `Gender`
- `Age`
- `Annual Income (k$)`
- `Spending Score (1–100)`

---

## 🔧 Preprocessing

- Converted the `Gender` column to numerical values using Label Encoding:
  - `Male` → `1`
  - `Female` → `0`
- Selected relevant features: **Annual Income** and **Spending Score**
- Scaled or visualized features as necessary

---

## 📈 K-Means Clustering

1. **Elbow Method**:
   - Calculated **WCSS** for cluster values `k = 1` to `10`
   - Plotted WCSS vs. k to identify the **optimal number of clusters**
   - Used `init='k-means++'` for smart centroid initialization
   - Used `random_state=42` to ensure reproducible results

2. **Clustering**:
   - Final model used `k = 5`
   - Applied `fit_predict()` to assign cluster labels

3. **Visualization**:
   - Visualized clusters using `matplotlib`
   - Optional: Used a heatmap (`seaborn`) to visualize feature correlation

---

## 🧠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## 📊 Output

- Correlation Heatmap of features
- Elbow Curve to determine `k`
- Scatter plot showing customer segments with cluster centers

---

## 🤖 Sample Code Snippet

```python
from sklearn.cluster import KMeans

kmeans = KMeans(n_clusters=5, init='k-means++', random_state=42)
Y = kmeans.fit_predict(X)
