# MNIST Digit Classifier — Computer Vision Project

A shallow neural network (dense layers, no convolutions) that classifies handwritten digits from the MNIST dataset. Trains on the built-in MNIST training set, then lets you upload your own CSV of digit images and predicts on it.

## Model Architecture

| Layer | Type | Nodes | Activation |
|---|---|---|---|
| Input | Dense | 512 | ReLU |
| Dropout | - | 0.2 | - |
| Hidden | Dense | 512 | ReLU |
| Dropout | - | 0.2 | - |
| Output | Dense | 10 | Softmax |

- **Loss:** Categorical Crossentropy
- **Optimizer:** Adam
- **Batch size:** 128
- **Epochs:** 10

## Files

| File | Description |
|---|---|
| `MNIST_CV_Project_Colab.ipynb` | Colab notebook, split into 10 steps (train, upload data, predict, visualize) |
| `sample_mnist_test.csv` | 200 real MNIST test digits — `label` column + `pixel0`–`pixel783` |
| `HOW_TO_RUN.md` | Step-by-step execution guide and troubleshooting |
| `mnist-classifier-first-deep-learning-project.ipynb` | Original Kaggle notebook |

## Quick Start (Google Colab)

1. Open [colab.research.google.com](https://colab.research.google.com) → File → Upload notebook → `MNIST_CV_Project_Colab.ipynb`.
2. Run cells 1–6 to load MNIST, build, and train the model.
3. Run cell 7 → click **Choose Files** → select `sample_mnist_test.csv`.
4. Run cells 8–10 to preprocess, predict, and visualize results.

## Input Data Format

CSV with 784 pixel columns (`pixel0` … `pixel783`, values 0–255). An optional `label` column enables accuracy reporting.

> Most pixel values are `0` — that's the black background around each digit, not missing data.

## Requirements

```bash
pip install tensorflow numpy pandas matplotlib ipywidgets
```

(Preinstalled on Google Colab.)

## Reference

https://medium.com/analytics-vidhya/get-started-with-your-first-deep-learning-project-7d989cb13ae5
