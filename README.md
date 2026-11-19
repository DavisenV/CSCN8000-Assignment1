# CSCN8000 – Assignment 1: Parkinson's Disease Classification

**Name:** Davisen Veerasamy
**Course:** CSCN8000 Artificial Intelligence Algorithms and Mathematics

## About the assignment

The goal of this assignment is to predict whether a patient is likely to have Parkinson's disease
using measurements taken from their voice recordings. A model like this could be used as a
decision support tool to help medical professionals.

Four machine learning models are trained and compared:

- K-Nearest Neighbors (KNN)
- Random Forest
- Support Vector Machine (SVM)
- Decision Tree

## Dataset

[Parkinson's Disease Classification – UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/470/parkinson+s+disease+classification)

- 756 voice recordings from 252 patients (3 recordings per patient)
- 753 speech features plus the `id` and `class` columns
- `class` is the target: 1 = Parkinson's disease, 0 = healthy

## What the notebook covers

1. **Data preprocessing** – data analysis, removing the duplicate row and the `id` column, and standardizing the features
2. **Train/test split** – 80% of the samples for training and 20% for testing
3. **Model training** – KNN, Random Forest, SVM and Decision Tree
4. **Predictions** – predicting the class on the test data with all four models
5. **Predictive system** – a function that predicts Parkinson's disease for a new sample
6. **Evaluation** – accuracy, confusion matrix and classification report for each model, plus a summary
7. **Saving results** – all test predictions saved in one CSV file

## Results

| Model | Accuracy |
|---|---|
| **Random Forest (best)** | **86.75%** |
| SVM | 84.11% |
| KNN | 83.44% |
| Decision Tree | 81.46% |

Random Forest gave the highest accuracy. All four models were very good at finding people with
Parkinson's, but they made more mistakes with healthy people because the dataset has about
3 times more Parkinson's samples than healthy ones.

## Project structure

```
CSCN8000-Assignment1/
├── data/
│   └── pd_speech_features.csv              # dataset
├── docs/
│   └── cscn8000 Assignment1.pdf            # assignment instructions
├── Davisen_Veerasamy_Assignment_1.ipynb    # Jupyter notebook with the code
├── Davisen_Veerasamy_Assignment_1.html     # HTML version of the notebook
├── test_predictions.csv                    # test predictions (created by the notebook)
└── README.md
```

## How to run

1. Install the required libraries:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```

2. Open `Davisen_Veerasamy_Assignment_1.ipynb` in Jupyter or VS Code from the project folder.
3. Run all the cells. The notebook reads `data/pd_speech_features.csv` and saves `test_predictions.csv`.
