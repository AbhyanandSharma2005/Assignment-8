# Handwritten Digit Recognition using Artificial Neural Networks (ANN)

## Objective
A postal service organization wants to automate the recognition of handwritten digits on postal codes. This project builds and evaluates an Artificial Neural Network (ANN) that classifies handwritten digits (0–9) using the MNIST dataset.

## Dataset Link
MNIST Handwritten Digits Dataset (CSV format) — Kaggle:
https://www.kaggle.com/datasets/oddrationale/mnist-in-csv

> No dataset file is included in or needs to be manually added to this repository. The notebook fetches the MNIST data automatically at runtime using `sklearn.datasets.fetch_openml("mnist_784")`, which mirrors the same data as the Kaggle CSV above. Just run the notebook — an internet connection is required the first time (the dataset is cached locally afterward).

## Libraries Used
- `pandas` — data loading and exploration
- `numpy` — numerical operations
- `matplotlib` — visualizing sample digits and training curves
- `scikit-learn` — train/test split, confusion matrix, classification report
- `tensorflow` / `keras` — building, training, and evaluating the ANN

## Methodology
1. **Data Understanding** — Loaded the dataset, inspected its structure, identified the input features (784 pixel columns) and target variable (`label`), and visualized a sample digit.
2. **Data Preprocessing** — Checked for missing values, separated features/target, normalized pixel values to the 0–1 range, split the data into 80% training and 20% testing, and one-hot encoded the target labels.
3. **Model Development** — Built a Sequential ANN in Keras with two hidden layers (128 and 64 neurons, ReLU activation) and a 10-neuron Softmax output layer. Compiled with the Adam optimizer and categorical crossentropy loss, then trained for 10 epochs.
4. **Model Evaluation** — Assessed performance using test accuracy, a confusion matrix, and a classification report, and plotted accuracy/loss curves across epochs.
5. **Conclusion** — Summarized key findings, the role of hidden layers, an advantage of Deep Learning over traditional ML, and a limitation of ANN.

## Model Architecture
| Layer | Type | Units | Activation |
|---|---|---|---|
| Input | — | 784 | — |
| Hidden Layer 1 | Dense | 128 | ReLU |
| Hidden Layer 2 | Dense | 64 | ReLU |
| Output Layer | Dense | 10 | Softmax |

- **Optimizer:** Adam
- **Loss Function:** Categorical Crossentropy
- **Metric:** Accuracy
- **Epochs:** 10

## Results
After running `Assignment-8.ipynb`, record the following here:
- Final test accuracy and loss
- Confusion matrix screenshot/summary
- Key numbers from the classification report
- Accuracy vs Epoch and Loss vs Epoch graphs

*(Fill in with actual values obtained after running the notebook.)*

## Conclusion
This project demonstrated that a simple ANN with two hidden layers can classify handwritten digits from the MNIST dataset with high accuracy, making it a viable approach for automating postal code digit recognition. The hidden layers allow the network to learn increasingly abstract, non-linear combinations of pixel intensities, transforming raw pixel data into representations that are linearly separable at the output layer. A key advantage of Deep Learning over traditional Machine Learning is its ability to automatically learn relevant features directly from raw data, without manual feature engineering. A limitation of a plain ANN is that it treats each pixel independently and ignores the 2D spatial structure of the image — unlike Convolutional Neural Networks (CNNs), which better exploit spatial patterns and typically achieve higher accuracy on image data.

## Repository Contents
- `Assignment-8.ipynb` — Full notebook covering Tasks 1–5
- `README.md` — This file
