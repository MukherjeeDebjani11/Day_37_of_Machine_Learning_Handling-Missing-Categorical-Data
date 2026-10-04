🤖 CampusX Machine Learning Journey

<p align="center"><img src="https://img.shields.io/badge/Machine%20Learning-CampusX-blue?style=for-the-badge&logo=python" alt="Machine Learning"><img src="https://img.shields.io/badge/Python-3.x-yellow?style=for-the-badge&logo=python" alt="Python"><img src="https://img.shields.io/badge/NumPy-Scientific%20Computing-orange?style=for-the-badge&logo=numpy" alt="NumPy"><img src="https://img.shields.io/badge/Pandas-Data%20Analysis-purple?style=for-the-badge&logo=pandas" alt="Pandas"><img src="https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-red?style=for-the-badge&logo=scikit-learn" alt="Scikit-Learn"></p><p align="center">
  <b>A structured, hands-on Machine Learning learning repository based on the CampusX 100 Days of Machine Learning series.</b>
</p>---

📌 About This Repository

This repository documents my Machine Learning learning journey while following the CampusX 100 Days of Machine Learning series by Nitish Singh.

The goal of this repository is not simply to collect code, but to build a strong understanding of Machine Learning concepts, intuition, mathematics, preprocessing techniques, algorithms, and practical implementation.

Every topic is accompanied by:

- 📚 Conceptual understanding
- 🧠 Intuition behind the technique
- 💻 Python implementation
- 📊 Practical examples
- 📝 Notes and important observations
- 🔍 Model-related insights
- 🧪 Experiments wherever applicable

The CampusX series follows a structured path from ML fundamentals toward practical machine-learning workflows.

---

🎯 Learning Objectives

Through this repository, I aim to:

- Understand the fundamentals of Machine Learning
- Learn how real-world datasets are processed
- Develop strong data preprocessing skills
- Understand the mathematics behind important ML algorithms
- Implement algorithms using Python and Scikit-Learn
- Learn how to evaluate Machine Learning models
- Understand overfitting and underfitting
- Learn feature engineering techniques
- Develop an end-to-end Machine Learning workflow
- Build a strong foundation for Data Science and AI/ML
- Prepare for Machine Learning and Data Science interviews

---

🗺️ Machine Learning Roadmap

                 MACHINE LEARNING
                       │
                       ▼
              ┌──────────────────┐
              │ ML Fundamentals  │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Python for ML    │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Data Exploration │
              │ & EDA            │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Data Cleaning    │
              │ & Preprocessing  │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Feature          │
              │ Engineering      │
              └────────┬─────────┘
                       │
                       ▼
          ┌────────────────────────────┐
          │ Machine Learning Algorithms│
          └─────────────┬──────────────┘
                        │
             ┌──────────┴──────────┐
             ▼                     ▼
       Supervised            Unsupervised
          Learning              Learning
             │                     │
             ▼                     ▼
      Regression &          Clustering &
      Classification        Dimensionality
             │                Reduction
             └──────────┬──────────┘
                        ▼
                Model Evaluation
                        │
                        ▼
                 Model Selection
                        │
                        ▼
                 Hyperparameter
                    Tuning
                        │
                        ▼
                End-to-End ML
                    Projects

---

📚 Topics Covered

1️⃣ Machine Learning Fundamentals

- What is Machine Learning?
- AI vs ML vs Deep Learning
- Types of Machine Learning
  - Supervised Learning
  - Unsupervised Learning
  - Reinforcement Learning
- Batch Learning
- Online Learning
- Instance-Based Learning
- Model-Based Learning
- Challenges in Machine Learning
- Real-world applications of ML
- Machine Learning Development Life Cycle
- Data Scientist vs Data Analyst vs ML Engineer

---

2️⃣ Python for Machine Learning

Libraries used throughout the repository:

Python
│
├── NumPy
├── Pandas
├── Matplotlib
├── Seaborn
└── Scikit-Learn

Key areas:

- NumPy arrays
- Vectorized operations
- Pandas Series & DataFrames
- Data manipulation
- Data visualization
- Statistical analysis
- Dataset handling

---

🧹 3️⃣ Data Preprocessing

Data preprocessing is one of the most important stages of a Machine Learning pipeline.

Topics include:

- Handling missing values
- Numerical data imputation
- Categorical data imputation
- Encoding categorical variables
- Feature scaling
- Feature transformation
- Outlier handling
- Data cleaning
- Feature selection
- Feature construction

---

🟣 Current Topic: Handling Missing Categorical Data

🎥 Reference Video

CampusX — Handling Missing Categorical Data

"Watch the CampusX video on YouTube" (https://reference-url-citation.invalid/3)

Concepts Covered

This notebook focuses on techniques for handling missing values in categorical features.

The main approaches explored are:

1. Most Frequent Imputation

Missing categorical values can be replaced with the mode, i.e. the category that occurs most frequently.

Example:

Before:

City
----
Delhi
Mumbai
Delhi
NaN
Delhi
Mumbai
NaN

After Most Frequent Imputation:

City
----
Delhi
Mumbai
Delhi
Delhi
Delhi
Mumbai
Delhi

In this case:

Most Frequent Category = Delhi

Every missing value is replaced with "Delhi".

---

2. Missing Category Imputation

Another approach is to treat missingness as a separate category.

Example:

Before:

City
----
Delhi
Mumbai
NaN
Delhi
NaN

After:

City
----
Delhi
Mumbai
Missing
Delhi
Missing

This approach can be useful when the fact that a value is missing may itself contain meaningful information.

---

🧪 Example Implementation

import pandas as pd

df = pd.DataFrame({
    "City": [
        "Delhi",
        "Mumbai",
        "Delhi",
        None,
        "Delhi",
        "Mumbai",
        None
    ]
})

print(df)

Using Most Frequent Imputation

from sklearn.impute import SimpleImputer

imputer = SimpleImputer(strategy="most_frequent")

df["City"] = imputer.fit_transform(df[["City"]])

print(df)

Using a Separate Missing Category

imputer = SimpleImputer(
    strategy="constant",
    fill_value="Missing"
)

df["City"] = imputer.fit_transform(df[["City"]])

print(df)

---

📂 Repository Structure

CampusX-Machine-Learning/
│
├── README.md
│
├── 01_ML_Fundamentals/
│   ├── introduction_to_ml.ipynb
│   ├── ai_vs_ml_vs_dl.ipynb
│   └── types_of_machine_learning.ipynb
│
├── 02_Python_For_ML/
│   ├── numpy/
│   ├── pandas/
│   ├── matplotlib/
│   └── seaborn/
│
├── 03_Data_Preprocessing/
│   ├── missing_values/
│   │   ├── numerical_imputation.ipynb
│   │   ├── categorical_imputation.ipynb
│   │   └── missing_category_imputation.ipynb
│   │
│   ├── encoding/
│   ├── feature_scaling/
│   ├── feature_transformation/
│   └── outlier_detection/
│
├── 04_EDA/
│   ├── univariate_analysis/
│   ├── bivariate_analysis/
│   └── multivariate_analysis/
│
├── 05_Statistics/
│   ├── probability/
│   ├── distributions/
│   └── hypothesis_testing/
│
├── 06_Regression/
│   ├── linear_regression/
│   ├── multiple_linear_regression/
│   ├── polynomial_regression/
│   ├── ridge_regression/
│   ├── lasso_regression/
│   └── elasticnet/
│
├── 07_Classification/
│   ├── logistic_regression/
│   ├── knn/
│   ├── decision_tree/
│   ├── random_forest/
│   └── svm/
│
├── 08_Clustering/
│   ├── kmeans/
│   ├── hierarchical_clustering/
│   └── dbscan/
│
├── 09_Ensemble_Learning/
│   ├── bagging/
│   ├── boosting/
│   ├── random_forest/
│   └── stacking/
│
├── 10_Model_Evaluation/
│   ├── regression_metrics/
│   ├── classification_metrics/
│   └── cross_validation/
│
├── 11_Feature_Engineering/
│   ├── feature_selection/
│   ├── feature_transformation/
│   └── feature_construction/
│
├── 12_Projects/
│   ├── project_01/
│   ├── project_02/
│   └── project_03/
│
└── requirements.txt

---

🛠️ Tech Stack

Technology| Purpose
🐍 Python| Programming Language
🔢 NumPy| Numerical Computing
🐼 Pandas| Data Manipulation
📊 Matplotlib| Data Visualization
🎨 Seaborn| Statistical Visualization
🤖 Scikit-Learn| Machine Learning
📓 Jupyter Notebook| Experimentation
💻 Google Colab| Cloud-Based Development
🔧 Git & GitHub| Version Control

---

📈 Machine Learning Algorithms

The repository will progressively cover algorithms such as:

Regression

- Linear Regression
- Multiple Linear Regression
- Polynomial Regression
- Ridge Regression
- Lasso Regression
- ElasticNet Regression

Classification

- Logistic Regression
- K-Nearest Neighbors
- Decision Trees
- Random Forest
- Support Vector Machines
- Naive Bayes

Ensemble Learning

- Bagging
- Boosting
- Voting
- Stacking
- Random Forest
- Gradient Boosting
- XGBoost

Unsupervised Learning

- K-Means Clustering
- Hierarchical Clustering
- DBSCAN
- PCA

---

📊 Model Evaluation

Understanding an algorithm is not enough — evaluating its performance is equally important.

Regression Metrics

MAE
MSE
RMSE
R² Score
Adjusted R²

Classification Metrics

Accuracy
Precision
Recall
F1 Score
Confusion Matrix
ROC-AUC

Model Validation

- Train/Test Split
- Cross Validation
- K-Fold Cross Validation
- Bias-Variance Tradeoff
- Overfitting
- Underfitting

---

🧠 Important Learning Philosophy

This repository follows a concept → intuition → mathematics → implementation → experimentation approach.

Instead of blindly memorizing algorithms, I am focusing on understanding:

«Why does the algorithm work?»

«When should it be used?»

«What assumptions does it make?»

«What happens when those assumptions are violated?»

«How does it behave on real-world data?»

This approach is intended to build a strong foundation rather than simply completing a playlist.

---

🔬 Learning Method

For each topic, I follow this workflow:

        Watch Lecture
              ↓
        Understand Concept
              ↓
       Study Mathematics
              ↓
       Implement from Scratch
              ↓
      Implement with sklearn
              ↓
       Experiment with Data
              ↓
       Write Personal Notes
              ↓
       Solve Problems/Tasks
              ↓
       Apply in a Project

---

📓 Notebook Convention

Each notebook follows a consistent structure:

1. Problem Statement
2. Dataset
3. Concept Introduction
4. Intuition
5. Mathematical Foundation
6. Implementation
7. Visualization
8. Experimentation
9. Results
10. Key Takeaways
11. Common Mistakes
12. Interview Questions

---

🎯 Progress Tracker

Module| Status
ML Fundamentals| ⬜
Python for ML| ⬜
NumPy| ⬜
Pandas| ⬜
EDA| ⬜
Data Preprocessing| 🟡
Missing Value Handling| 🟢
Feature Engineering| ⬜
Statistics| ⬜
Linear Regression| ⬜
Logistic Regression| ⬜
KNN| ⬜
Decision Trees| ⬜
Random Forest| ⬜
SVM| ⬜
Naive Bayes| ⬜
Ensemble Learning| ⬜
K-Means| ⬜
Hierarchical Clustering| ⬜
PCA| ⬜
Model Evaluation| ⬜
Hyperparameter Tuning| ⬜
End-to-End Projects| ⬜

Legend

⬜ Not Started
🟡 In Progress
🟢 Completed

---

💡 Key Takeaways from Current Topic

Missing Categorical Data

When categorical data contains missing values, common approaches include:

                 Missing Category
                       │
             ┌─────────┴─────────┐
             │                   │
       Most Frequent       New Category
        Imputation          "Missing"
             │                   │
        Simple & Fast       Preserves
                            Missingness

Most Frequent Imputation

Advantages

- Simple
- Fast
- Easy to implement
- Works well when missing values are relatively small

Disadvantages

- Can distort the distribution
- Can increase the frequency of the dominant category
- May hide the information that a value was originally missing

Missing Category

Advantages

- Preserves missingness information
- Useful when missingness itself may be meaningful

Disadvantages

- Adds an additional category
- May not always be appropriate depending on the dataset and model

---

🚀 Future Improvements

As this repository grows, I plan to add:

- [ ] More detailed mathematical derivations
- [ ] Algorithms implemented completely from scratch
- [ ] Interactive visualizations
- [ ] Real-world datasets
- [ ] End-to-end ML projects
- [ ] Model comparison experiments
- [ ] Hyperparameter optimization
- [ ] ML pipelines
- [ ] Deployment experiments
- [ ] Interview preparation notes
- [ ] Kaggle projects
- [ ] MLOps concepts

---

📌 Why This Repository?

Machine Learning is much more than knowing the syntax of:

model.fit(X_train, y_train)

The real goal is to understand the complete pipeline:

Raw Data
   ↓
Data Understanding
   ↓
Data Cleaning
   ↓
EDA
   ↓
Feature Engineering
   ↓
Feature Selection
   ↓
Model Selection
   ↓
Training
   ↓
Evaluation
   ↓
Hyperparameter Tuning
   ↓
Final Model
   ↓
Deployment

This repository is my attempt to understand that complete journey step by step.

---

📚 Learning Resource

Primary learning resource:

CampusX — 100 Days of Machine Learning

The series is created by Nitish Singh (CampusX) and provides a structured Machine Learning learning path. CampusX currently also provides dedicated notes for its YouTube ML series.

🎥 YouTube:
https://www.youtube.com/@campusx-official

📚 CampusX:
https://learnwith.campusx.in/

---

⚠️ Disclaimer

This repository is an independent learning repository created while studying the CampusX Machine Learning series.

The original educational content, lectures, explanations, and intellectual property belong to their respective creators.

This repository contains my own:

- Implementations
- Experiments
- Notes
- Explanations
- Learning observations

It is intended for educational and learning purposes.

---

👩‍💻 Author

Debjani Mukherjee

B.Tech Computer Science & Engineering Student

Interested in:

Machine Learning
Artificial Intelligence
Data Science
Full Stack Development
Backend Development
Cloud Computing

---

<p align="center">⭐ If you find this repository useful, consider giving it a star!

Learn → Implement → Experiment → Build → Repeat 🚀

</p>
