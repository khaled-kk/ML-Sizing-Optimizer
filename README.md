# ML Sizing Optimizer: K-Means Clustering of Body Measurements

A notebook that implements K-Means clustering from scratch (pandas/NumPy) to group people by five body measurements, measures how running time grows with sample size, and visualises the clusters after a from-scratch PCA projection to 2D.

## What it does

- Loads `group3.csv` with five numeric columns: **height, weight, body mass, shoulders, length of arms**.
- Normalises each column with z-score standardisation (`(x - mean) / std`).
- **K-Means implemented by hand**: random initial centroids sampled from the data, Euclidean distance to each centroid, assignment to the nearest centroid, centroid recomputation, repeated until the centroids stop changing. The number of clusters is fixed at **K = 5** (K = 3 is left commented out); no Elbow or Silhouette method is used.
- **Running-time experiment**: runs the clustering on random samples of 1,000, 2,000, 3,000 and 4,000 rows, records the time for each and plots it.
- **PCA implemented by hand** (covariance matrix, `np.linalg.eigh`, top eigenvectors) to reduce the five features to two components, then clusters a random 1,000-row sample in 2D, prints the share of points in each cluster and draws a scatter plot with the centroids.

## Results (from the saved notebook outputs)

These come from a single run with random sampling and random initial centroids, so re-running will give different numbers.

Running time of the 5-feature clustering:

| Sample size | Time (s) |
| ---: | ---: |
| 1,000 | 24.47 |
| 2,000 | 30.23 |
| 3,000 | 64.53 |
| 4,000 | 61.97 |

Cluster sizes on the PCA-reduced 1,000-row sample (K = 5): 15.3%, 25.0%, 15.0%, 23.2%, 21.5%.

## Tech stack

- Python 3, Jupyter Notebook / Google Colab
- pandas, NumPy, Matplotlib
- (`sklearn.cluster.KMeans` is imported but not used; clustering and PCA are written manually.)

## Repository contents

```
analysis.ipynb   Data loading, normalisation, K-Means, timing experiment, PCA and plots
README.md
```

The dataset `group3.csv` is **not** included in this repository.

## How to run

1. Open `analysis.ipynb` in Google Colab (badge at the top of the notebook) or Jupyter.
2. Place `group3.csv` (header row followed by five numeric columns in the order above) in the working directory.
3. Install the dependencies if needed: `pip install pandas numpy matplotlib scikit-learn`.
4. Run the cells in order. The timing cell iterates row by row and can take several minutes.

---
*Developed by Khaled Walid*
