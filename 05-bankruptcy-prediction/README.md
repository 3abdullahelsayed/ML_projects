# Taiwanese Company Bankruptcy Prediction

A binary classification project focused on identifying bankrupt companies in a highly imbalanced dataset.

## Project details

- **Task:** Imbalanced binary classification
- **Dataset:** UCI dataset 572 — 6,819 companies and 95 financial features
- **Model:** Pruned Decision Tree with class weights
- **Reported result:** 69% recall and 29% precision for the bankrupt class on the test split

## Method

- Used a stratified 75/25 train/test split.
- Trained a shallow Decision Tree with class weighting to give greater importance to the minority bankrupt class.
- Evaluated the confusion matrix and minority-class precision/recall rather than relying on accuracy alone.

## Limitations

- The dataset is highly imbalanced, so accuracy alone is misleading.
- Hyperparameters were selected manually; a cross-validated search on the training data would provide a more systematic comparison.
- The decision threshold should reflect the relative cost of missed bankruptcies and false alarms.
- Reported metrics have not been independently reproduced during repository preparation.

## Next improvements

Compare PR-AUC and ROC-AUC, tune the threshold using validation data, and compare the tree with ensemble models and resampling approaches.
