Credit Risk and Financial Machine Learning Projects

This repository contains two projects focused on credit risk modelling and credit decision systems. The first project explores binary classification for credit card approvals using machine learning. The second project builds a simplified but complete IFRS 9-style Expected Credit Loss (ECL) framework using consumer loan data.

Note: I pursued the second project in order to better understand and learn more about credit risk modelling, as well as tackle the limitations I encountered from project 1.

Both projects focus on building models from the ground up, validating them properly, and understanding their practical limitations.

Project 1: Credit Card Approval Prediction

This project develops machine learning models to predict whether a credit card application should be approved or rejected.

The dataset includes numerical and categorical applicant features such as income, employment history, property ownership, and education level. After preprocessing (handling missing values, encoding categorical variables, normalization), two models were implemented:

Logistic Regression (implemented from scratch using gradient descent)

k-Nearest Neighbors (custom implementation with hyperparameter tuning)

Evaluation was carried out using accuracy, ROC curves, AUC, and confusion matrices.

Both models achieved high overall accuracy (around 90%), but ROC-AUC scores revealed weak class separation due to dataset imbalance. The project highlights the importance of looking beyond accuracy when evaluating classification models.

Main focus areas:

Manual implementation of logistic regression

Model validation and evaluation

Class imbalance analysis

Feature inspection and descriptive statistics

Project 2: Credit Risk Modelling and IFRS 9 Expected Credit Loss

This project builds an end-to-end credit risk workflow aligned with IFRS 9 principles using LendingClub loan data.

The objective was not to build a production banking model, but to construct a clean and transparent pipeline covering the core components of an expected credit loss framework:

Probability of Default (PD) modelling using logistic regression

Time-based validation split with maturity cutoff to reduce label censoring

SICR-based staging logic (Stage 1, Stage 2, Stage 3)

Contractual Exposure at Default (EAD) approximation

Assumption-based Loss Given Default (LGD)

Scenario-weighted Expected Credit Loss aggregation

The model achieved validation ROC-AUC around 0.70. Final portfolio-level aggregation produced a scenario-weighted ECL consistent with the assumed PD, LGD, and exposure structure.

The project demonstrates:

Practical PD modelling with proper temporal validation

Handling sampling bias with explicit weights

Building staging logic instead of treating it as a black box

Translating model outputs into portfolio-level loss estimates

Tools and Libraries

Python
NumPy
Pandas
scikit-learn
Matplotlib
