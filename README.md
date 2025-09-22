# Resume Classification using Machine Learning

This project demonstrates how to build a **resume classification system** that categorizes resumes into predefined job roles using **Natural Language Processing (NLP)** and **Machine Learning models**.  
It involves **data preprocessing, visualization, feature engineering, class balancing, and training multiple ML models** to evaluate performance.

---

## Project Overview

- Dataset: **UpdatedResumeDataSet.csv**  
  - 962 resumes labeled across 25 categories.
  - Each resume has two columns:
    - `Category`: Target job role (e.g., Data Science, Java Developer, HR, etc.)
    - `Resume`: Raw text data of candidate resumes.

- Tasks performed:
  1. **Data Cleaning** – Removing URLs, mentions, punctuation, stopwords, etc.
  2. **Exploratory Data Analysis (EDA)** – Category distribution, bar plots, pie charts, and word cloud generation.
  3. **Feature Engineering** – TF-IDF vectorization of text data.
  4. **Class Imbalance Handling** – Using **SMOTE** for oversampling minority classes.
  5. **Model Training & Evaluation** – Logistic Regression, SVM, Random Forest, Naive Bayes, Gradient Boosting, etc.
  6. **Performance Metrics** – Accuracy, Precision, Recall, F1 Score, Confusion Matrix.

---

## 📊 Data Exploration

- **Categories Distribution (Top 5)**:
  - Java Developer: 84 resumes
  - Testing: 70 resumes
  - DevOps Engineer: 55 resumes
  - Python Developer: 48 resumes
  - Web Designing: 45 resumes

---

## 🛠️ Data Preprocessing

1. **Text Cleaning**  
   - Removed URLs, hashtags, mentions, non-ASCII characters, punctuation.
   - Converted text to lowercase and stripped extra spaces.

2. **Stopwords Removal**  
   - Used **NLTK English stopwords** to remove irrelevant words.

3. **Feature Extraction**  
   - Applied **TF-IDF Vectorization** for text representation.

4. **Label Encoding**  
   - Encoded 25 job categories into integers.

5. **Handling Imbalanced Classes**  
   - Applied **SMOTE (Synthetic Minority Oversampling Technique)**.

---

## Models Used

The following classifiers were trained and evaluated:

- Logistic Regression (OvR)
- SVM (OvR & OvO)
- Random Forest
- Decision Tree
- Naive Bayes
- K-Nearest Neighbors (KNN)
- Gradient Boosting
- Linear Discriminant Analysis (LDA)

---

## 📈 Results

| Model                        | Train Accuracy | Test Accuracy | Precision | Recall | F1 Score |
| ---------------------------- | -------------- | ------------- | --------- | ------ | -------- |
| Logistic Regression (OvR)    | 0.9988         | **0.9948**    | 0.9955    | 0.9948 | 0.9949   |
| Logistic Regression (OvO)    | 0.9988         | 0.9928        | 0.9937    | 0.9928 | 0.9930   |
| SVM (OvR)                    | 1.0000         | **0.9948**    | 0.9955    | 0.9948 | 0.9949   |
| SVM (OvO)                    | 1.0000         | 0.9938        | 0.9945    | 0.9938 | 0.9939   |
| Random Forest                | 1.0000         | 0.9897        | 0.9911    | 0.9897 | 0.9899   |
| Decision Tree                | 1.0000         | 0.9826        | 0.9851    | 0.9826 | 0.9830   |
| Naive Bayes                  | 0.9554         | 0.9275        | 0.9377    | 0.9275 | 0.9293   |
| K-Nearest Neighbors (KNN)    | 0.9875         | 0.9796        | 0.9819    | 0.9796 | 0.9799   |
| Gradient Boosting            | 0.9916         | 0.9856        | 0.9871    | 0.9856 | 0.9858   |
| Linear Discriminant Analysis | 0.9979         | 0.9918        | 0.9929    | 0.9918 | 0.9920   |


✅ Logistic Regression and SVM achieved the **best performance (99.48% accuracy)**.  

