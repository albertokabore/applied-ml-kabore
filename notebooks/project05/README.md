# Wine Quality Prediction with Ensemble Machine Learning

 ## Project Overview

This project implements and evaluates ensemble machine learning models to predict red wine quality based on physicochemical properties. Using the UCI Wine Quality Dataset, we compare various ensemble techniques to classify wines into three quality categories: Low, Medium, and High.

### Key Features:

•	Comprehensive comparison of ensemble methods (Random Forest, Voting Classifiers)

•	Detailed performance analysis with multiple metrics

•	Feature importance analysis for model interpretability

•	Handling of class imbalance in wine quality data

•	Cross-validation for robust model evaluation

### Business Problem

Wine quality assessment traditionally relies on human expert tasting, which can be subjective and time-consuming. This project explores whether machine learning can provide:

•	Objective quality predictions based on measurable chemical properties

•	Insights into key factors driving wine quality

•	Scalable quality control for wine production

•	Data-driven decision support for winemakers

## Dataset

#### Source: UCI Machine Learning Repository - Wine Quality Dataset

Size: 1,599 red wine samples

#### Features (11 physicochemical properties):

•	Fixed acidity

•	Volatile acidity

•	Citric acid

•	Residual sugar

•	Chlorides

•	Free sulfur dioxide

•	Total sulfur dioxide

•	Density

•	pH

•	Sulphates

•	Alcohol

Target Variable:

•	Original: Quality score (3-8)

•	Transformed: Three categories (Low: 0-4, Medium: 5-6, High: 7-8)

#### Project Structure

text

project05/
│
├── ensemble-yourname.ipynb          # Main Jupyter notebook
├── winequality-red.csv              # Dataset
├── requirements.txt                 # Python dependencies
├── README.md                       # Project documentation
└── images/                         # Generated plots and visualizations

#### Installation & Setup

Prerequisites

•	Python 3.8+

•	Jupyter Notebook

•	Required Python packages

Installation Steps

1.	Clone the repository

```Powershell
git clone https://github.com/albertokabore/applied-ml-kabore
```

2.	Create virtual environment (recommended)

```Powershell
python -m venv venv
```
source venv/bin/activate  # On Windows: venv\Scripts\activate

3.	Install dependencies

```Powershell
pip install -r requirements.txt
```
4.	Launch Jupyter Notebook

```Powershell
jupyter notebook
Dependencies
txt
pandas>=1.5.0
numpy>=1.21.0
scikit-learn>=1.2.0
matplotlib>=3.5.0
seaborn>=0.11.0
jupyter>=1.0.0
```
#### Usage

Running the Analysis

1.	Open ensemble-yourname.ipynb in Jupyter Notebook

2.	Execute cells sequentially:

o	Data Loading & Exploration: Understand dataset structure

o	Data Preprocessing: Quality categorization and feature engineering

o	Model Training: Implement ensemble methods

o	Evaluation: Compare model performance

o	Analysis: Interpret results and feature importance

#### Key Sections

1.	Data Preparation

o	Load and inspect wine quality data

o	Transform quality scores into categorical labels

o	Handle class imbalance

2.	Feature Analysis

o	Correlation matrix visualization

o	Feature distribution analysis

o	Target variable exploration

3.	Model Implementation

o	Random Forest Classifier

o	Voting Classifier (DT + SVM + Neural Network)

o	Performance metrics calculation

4.	Results Comparison

o	Accuracy and F1-score analysis

o	Overfitting assessment (train-test gaps)

o	Cross-validation results

#### Results

Model Performance Summary

Model	Test Accuracy	Test F1-Score	Accuracy Gap	Best For
Random Forest (100)	0.7594	0.7548	0.0412	Overall Performance
Voting (DT+SVM+NN)	0.7344	0.7233	0.0521	Ensemble Diversity

#### Key Findings

•	Random Forest achieved the best balance of performance and generalization

•	Alcohol content was the most important feature for quality prediction

•	Volatile acidity and sulphates were also significant contributors

•	All models handled class imbalance reasonably well

•	Small train-test gaps indicated good generalization across models

#### Feature Importance (Top 5)

1.	Alcohol (22.1%)

2.	Volatile acidity (15.8%)

3.	Sulphates (12.3%)

4.	Total sulfur dioxide (9.7%)

5.	Density (8.9%)

Algorithms Implemented

#### Ensemble Methods

•	Random Forest: Homogeneous ensemble with 100 decision trees

•	Voting Classifier: Heterogeneous ensemble combining:

o	Decision Tree

o	Support Vector Machine

o	Neural Network (MLP)

Evaluation Metrics

•	Accuracy: Overall prediction correctness

•	Precision: Quality of positive predictions

•	Recall: Coverage of actual positive cases

•	F1-Score: Balance between precision and recall

•	Confusion Matrix: Detailed class-wise performance

### Insights & Business Value

Technical Insights

•	Ensemble methods significantly outperform individual base models

•	Random Forest provides excellent interpretability through feature importance

•	Chemical properties are strong predictors of perceived quality

•	Model performance is constrained by inherent class imbalance

#### Business Applications

1.	Quality Control: Predict quality from measurable chemical properties

2.	Production Optimization: Focus on key factors (alcohol, acidity)

3.	Blending Guidance: Data-driven decisions for wine blending

4.	Cost Reduction: Reduce reliance on extensive human tasting panels

