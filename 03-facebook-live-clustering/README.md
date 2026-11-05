# Facebook Live Sellers in Thailand — Clustering

An unsupervised-learning project that explores engagement patterns in Facebook posts published by Thai retail sellers.

## Project details

- **Task:** Clustering
- **Dataset:** UCI dataset 488 — 7,050 posts from 10 seller pages
- **Methods:** K-Means, feature scaling, PCA, elbow analysis, and silhouette score
- **Reported result:** Best silhouette score of approximately 0.58 at K=2; the notebook also explores a K=3 solution

## Method

- Prepared post-type and timestamp features.
- Standardized numerical features.
- Compared K-Means solutions over a range of cluster counts.
- Used PCA to visualize the resulting clusters.

## Limitations

- The silhouette score favors K=2, while the notebook's final model uses K=3; the reason should be explained.
- Label-encoding post type creates an artificial numeric order. One-hot encoding is more suitable.
- Timestamp components may add noise when treated as ordinary numeric features.
- Cluster profiles are needed before assigning business meaning to the segments.

## Next improvements

Compare K=2 and K=3, profile each cluster using engagement statistics and post types, and test robust scaling or log transforms for skewed engagement counts.
