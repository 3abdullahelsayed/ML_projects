# Anemia Types Classification (CBC Blood Tests)

A multi-class classification project that predicts one of nine labels (healthy plus eight conditions) from 14 complete blood count (CBC) measurements. A small Gradio interface is also included in the notebook.

## Project details

- **Task:** Imbalanced multi-class classification
- **Dataset:** Kaggle `ehababoelnaga/anemia-types-classification` — 1,281 records and 14 CBC features
- **Model:** Random Forest with balanced class weights
- **Reported result:** 97.8% test accuracy and 0.94 macro F1 on a 321-record test split

## Method

- Encoded the nine target labels.
- Used a stratified 75/25 train/test split.
- Trained a Random Forest with class weighting to address class imbalance.
- Added a Gradio demo that accepts CBC values and returns a predicted label.

## Limitations

- **Educational project only — not a diagnostic tool.** It must not be used for medical decisions.
- The rarest classes have very few test examples, so their per-class metrics are unstable.
- The source dataset contains suspicious measurements and may contain pre-imputed values.
- The relationship between CBC features and the diagnostic labels should be investigated. If labels were derived from CBC thresholds, high accuracy may partly reflect that construction.
- The reported metrics have not been independently reproduced during repository preparation.

## Next improvements

Validate the data quality, inspect label-generation rules, add cross-validation and feature-importance analysis, and document the demo's input validation.
