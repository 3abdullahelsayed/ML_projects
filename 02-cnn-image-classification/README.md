# CNN Image Classification — 64 Classes

A convolutional neural network built with TensorFlow/Keras to classify images across 64 animal categories.

## Project details

- **Task:** Multi-class image classification
- **Data:** 9,200 training, 2,301 validation, and 2,876 test images (fold 1)
- **Model:** CNN with three convolutional blocks and dropout
- **Reported result:** 83.5% final validation accuracy; the notebook also reports 83.1% test accuracy

The image dataset is not included in this repository. Configure `DATA_DIR` to point to the directory containing the images and the CSV split files.

## Method

- Applied image augmentation to the training data.
- Trained a CNN using Adam and categorical cross-entropy.
- Used separate training, validation, and test CSV splits.

## Important evaluation note

The notebook evaluates the test set at multiple training stages and then continues training. This means the test set was not kept fully untouched during model development. **Treat the 83.1% test score as provisional; the validation score is the more appropriate development metric.** A revised experiment should use validation data for all model-selection decisions and evaluate the test set once at the end.

## Next improvements

Use transfer learning (for example, MobileNet or EfficientNet), add a confusion matrix and per-class metrics, and record the exact dataset source and class mapping.
