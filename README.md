# Handwritten Digit Classification Using Logistic Regression

A machine learning project using **scikit-learn Logistic Regression** to classify handwritten digits from the built-in handwritten digits dataset.

The project demonstrates a complete supervised machine learning workflow, including dataset loading, data exploration, visualization, train/test splitting, model training, prediction, and performance evaluation.

## Project Overview

This project uses the scikit-learn handwritten digits dataset to build a Logistic Regression classification model.

Each handwritten digit is represented numerically as a set of features. The project explores the dataset, separates the data into training and testing subsets, trains a Logistic Regression model, and evaluates its classification accuracy.

The final model achieved an accuracy of:

**97.5%**

on the testing dataset.

## Machine Learning Workflow

```text
Handwritten Digit Dataset
          │
          ▼
   Dataset Exploration
          │
          ▼
   Feature / Label Setup
          │
          ▼
     Train/Test Split
       80% / 20%
          │
          ▼
   Logistic Regression
        Training
          │
          ▼
     Test Prediction
          │
          ▼
    Accuracy Evaluation
          │
          ▼
       97.5% Accuracy
```

## Dataset

The project uses the built-in handwritten digits dataset provided by scikit-learn.

The dataset contains images of handwritten digits represented as numerical data. Each image is represented using **64 numerical features**, corresponding to the pixels of the low-resolution digit image.

The project separates the dataset into:

* **Features (`X`)** — numerical representation of the digit images
* **Labels (`y`)** — the corresponding digit classifications

## Data Exploration

The notebook examines the dataset and its structure before model development.

The feature representation is checked using:

```python
digits['data'][0].shape
```

which produces:

```text
(64,)
```

The project also visualizes a handwritten digit using Matplotlib to provide a visual representation of the data being classified.

## Train/Test Split

The dataset is divided into training and testing data using scikit-learn's `train_test_split()`.

```python
X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42
)
```

The configuration uses:

* **80%** of the data for training
* **20%** of the data for testing
* `random_state=42` for reproducibility

## Model Development

The project uses Logistic Regression as the classification algorithm.

```python
from sklearn.linear_model import LogisticRegression

LR = LogisticRegression(max_iter=2000)

LR.fit(X_train, y_train)
```

The model is trained using the training features and their corresponding digit labels.

## Prediction

After training, the model generates predictions using the test dataset:

```python
y_pred = LR.predict(X_test)
```

These predictions are then compared with the known test labels.

## Model Performance Evaluation

Model performance is evaluated using classification accuracy:

```python
from sklearn.metrics import accuracy_score

accuracy = accuracy_score(y_test, y_pred)

accuracy
```

### Result

The Logistic Regression model achieved:

**97.5% test accuracy**

This result indicates that the model correctly classified the vast majority of handwritten digit samples in the testing dataset.

## Technologies Used

* Python
* Jupyter Notebook
* scikit-learn
* Matplotlib
* Logistic Regression
* Supervised Machine Learning
* Train/Test Split
* Accuracy Evaluation

## Project Structure

```text
Project-4-Handwritten-Digit-Classification/
│
├── .gitignore
├── README.md
├── requirements.txt
├── handwritten_digit_classification.ipynb
│
└── screenshots/
```

### File Descriptions

**`handwritten_digit_classification.ipynb`**

The primary Jupyter Notebook containing the complete machine learning workflow, code, visualizations, and evaluation results.

**`requirements.txt`**

Contains the Python packages required to run the project.

**`.gitignore`**

Prevents Python cache files, Jupyter checkpoints, virtual environments, logs, and local development files from being committed.

**`screenshots/`**

Contains selected screenshots documenting the major stages of the project.

## Installation

### 1. Clone the repository

```bash
git clone <repository-url>
cd Project-4-Handwritten-Digit-Classification
```

### 2. Create a virtual environment

```bash
python3 -m venv .venv
```

Activate the environment on macOS/Linux:

```bash
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch the notebook

Start Jupyter:

```bash
jupyter notebook
```

Then open:

```text
handwritten_digit_classification.ipynb
```

Run the notebook cells sequentially to reproduce the analysis.

## Results

The completed model achieved **97.5% accuracy** on the test dataset.

The project demonstrates that Logistic Regression can effectively classify the low-resolution handwritten digit dataset while providing a straightforward example of a complete supervised machine learning pipeline.

## Skills Demonstrated

This project demonstrates practical experience with:

* Python programming
* Jupyter Notebook development
* scikit-learn
* Supervised machine learning
* Classification
* Logistic Regression
* Dataset exploration
* Feature and label preparation
* Train/test data splitting
* Model training
* Model prediction
* Performance evaluation
* Accuracy measurement
* Data visualization
* Reproducible experimentation

## Future Development

Potential extensions to this project could include:

* Comparing Logistic Regression with other classifiers
* Testing different regularization settings
* Evaluating precision, recall, and F1-score
* Generating a confusion matrix
* Comparing multiple machine learning algorithms
* Performing cross-validation
* Exploring dimensionality reduction
* Evaluating model performance across individual digit classes

## Author

**Bradley Lueking**

Cybersecurity | AI | Machine Learning | Security Operations | GRC
