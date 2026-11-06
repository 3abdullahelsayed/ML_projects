# Machine Learning Projects

**Abdullah Elsayed Masoud** · Cairo University, Faculty of Computers and Artificial Intelligence

A collection of practical projects in machine learning, deep learning, natural language processing, clustering, computer vision, and regression. Each project folder documents its problem, dataset, methodology, reported results, and limitations.

## Project index

| # | Project | Area | Main techniques | Reported result* |
|---|---|---|---|---|
| 01 | [Anemia Types Classification](01-anemia-classification/) | Classification | Random Forest, class weighting, Gradio | 97.8% accuracy · macro F1 0.94 |
| 02 | [Animal Image Classification](02-cnn-image-classification/) | Deep learning / Computer vision | CNN, TensorFlow/Keras, augmentation | 83.5% validation accuracy |
| 03 | [Facebook Live Sellers Clustering](03-facebook-live-clustering/) | Unsupervised learning | K-Means, PCA, silhouette analysis | Silhouette ≈ 0.58 at K=2 |
| 04 | [TV Genre Text Classification](04-tv-genre-text-classification/) | NLP | TF-IDF, lemmatization, Naive Bayes | 81.9% reported test accuracy* |
| 05 | [Bankruptcy Prediction](05-bankruptcy-prediction/) | Imbalanced classification | Decision Tree, class weights | 69% recall on bankrupt class |
| 06 | [Gas Turbine NOx Regression](06-gas-turbine-nox-regression/) | Regression | Random Forest, RandomizedSearchCV | R² = 0.883 (baseline test result) |

*Reported values are taken from the project notebooks/notes and have not been independently reproduced as part of this repository preparation. Some projects have evaluation caveats documented in their READMEs; use the limitations before interpreting the scores.*

## Tech stack

Python · pandas · NumPy · scikit-learn · TensorFlow/Keras · NLTK · Matplotlib · Seaborn · Gradio

## Repository structure

Each numbered folder contains a project README and its Jupyter notebook. Some projects require downloading their dataset separately; datasets and trained model artifacts are intentionally excluded.

## Getting started

1. Clone the repository.
2. Install the dependencies: `pip install -r requirements.txt`
3. Open a project notebook in Jupyter or Google Colab.
4. Follow the dataset and path instructions in that project's README.

## Notes on reproducibility

- Results may vary with package versions, random seeds, and dataset revisions.
- The animal image dataset is not included because of its size; see its project README for the expected folder structure.
- For a fair final evaluation, keep the test set untouched during model selection. The CNN and text-classification notebooks have this limitation documented and should be revised before quoting their reported test scores.
- The anemia project is educational only and is not a medical diagnostic tool.
