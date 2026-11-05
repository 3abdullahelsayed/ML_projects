# Gas Turbine NOx Emission Prediction

A regression project that predicts nitrogen-oxide (NOx) emissions from gas-turbine sensor measurements.

## Project details

- **Task:** Regression
- **Dataset:** UCI dataset 551 — 36,733 records and 11 input features
- **Model:** Random Forest Regressor; RandomizedSearchCV explored as a tuning step
- **Reported baseline result:** R² = 0.883 and MSE = 15.24 on the test split (RMSE ≈ 3.9)

## Method

- Used an 80/20 random train/test split.
- Trained a Random Forest regression baseline.
- Explored hyperparameters with cross-validation.

## Limitations

- Some cross-validation fits failed because `max_features='auto'` is not accepted by recent scikit-learn versions; replace it with a supported value and rerun the search.
- The reported test metrics refer to the baseline model, not a refit using the best search parameters.
- Because records span multiple years, a time-based evaluation should be compared with the random split.
- Check whether the CO measurement would be available at the point when a real prediction is needed.

## Next improvements

Fix the search parameter grid, refit the selected estimator on the training data, evaluate the test set once, and compare random versus year-based splits.
