# Chest X-ray Report Generation

A deep-learning project exploring automatic generation of radiology reports from paired chest X-ray images.

> **Research and educational use only.** This project is not a medical device. Generated reports may be inaccurate or incomplete and must not be used for diagnosis or clinical decisions.

## Model implementations

### 1. CNN + Transformer
- Extracts visual features from frontal and lateral chest X-ray views.
- Uses a Transformer-based encoder-decoder to generate report text.
- Includes training, BLEU/ROUGE evaluation, and a Gradio inference notebook.

### 2. ResNet + GPT-2
- Uses a pretrained ResNet backbone for image feature extraction.
- Projects visual features into a prefix consumed by GPT-2.
- Includes training, report-generation evaluation, and a Gradio inference notebook.

## Repository contents

The notebooks and supporting configuration files are being added to this folder. Large trained checkpoints are intentionally excluded for now, including `best.pt`, `.h5`, and `.keras` files. They can be hosted separately (for example, on Hugging Face Hub) and linked here later.

## Data and privacy

The dataset is not included. Obtain it from its original provider and comply with its access terms and data-use agreement. Do not upload patient images, radiology reports, identifiers, or restricted dataset files to a public repository.

## Running the project

The two implementations have separate dependency lists and should be run in separate Kaggle or Google Colab environments. Open the corresponding notebook, configure the dataset paths, and execute cells in order. Checkpoint paths in inference notebooks must match the files produced by your own training run.

## Evaluation

The notebooks contain BLEU and ROUGE evaluation workflows. Final metric values will be documented only after verifying the held-out test results.

## Limitations

- Generated text can hallucinate findings or omit clinically relevant details.
- Results depend on dataset access, preprocessing, model checkpoints, and environment versions.
- This project is intended for experimentation, not clinical use.
