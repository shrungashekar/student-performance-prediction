# Student Performance Prediction

A machine learning project that predicts student examination scores using academic, behavioural, and socio-economic factors.

## Overview

This project explores how different student-related factors are associated with academic performance and develops a regression model to estimate examination scores.

It covers the complete machine learning workflow, including data cleaning, exploratory data analysis, preprocessing, model training, evaluation, and prediction through a Streamlit application.

## Objectives

- Explore factors associated with student examination performance.
- Perform data cleaning and exploratory data analysis.
- Apply appropriate preprocessing techniques to numerical and categorical data.
- Train and evaluate regression models.
- Build an interactive application for predicting student scores.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Streamlit
- Joblib
- Google Colab

## Dataset

The project uses the Student Performance Factors dataset.

- Initial dataset: 6,607 records and 20 columns.
- Input features: 19.
- Target variable: `Exam_Score`.

The features include study hours, attendance, previous scores, sleep hours, parental involvement, access to resources, motivation, and other student-related factors.

Dataset source:

[Student Performance Factors Dataset](https://github.com/omaarrx/Student-Score-Prediction)

## Machine Learning Workflow

1. Data loading and inspection
2. Data cleaning and handling missing values
3. Exploratory Data Analysis (EDA)
4. Feature and target separation
5. Train-test splitting (80:20)
6. Numerical and categorical preprocessing
7. Linear Regression model training
8. Model evaluation
9. Model serialization using Joblib
10. Interactive prediction application using Streamlit

## Models Evaluated

Two regression models were evaluated:

- Linear Regression
- Random Forest Regressor

Linear Regression achieved better overall performance on the selected test split.

## Model Performance

| Metric | Linear Regression |
|---|---:|
| MAE | 0.416 |
| MSE | 2.314 |
| R² Score | 0.825 |

**Important limitation:** The model performs poorly on exceptionally high scores (above 80), significantly underpredicting these cases. Its overall metrics should not be interpreted as equal accuracy across all score ranges.

## Interactive Application

A Streamlit application was developed to collect student details and generate predicted examination scores using the saved machine learning pipeline.

To run locally:

```bash
pip install -r requirements.txt
streamlit run app.py
```

Ensure `student_performance_model.pkl` is present in the same directory as `app.py`.

## Project Structure

```text
student-performance-prediction/
│
├── Student_Performance_Prediction.ipynb
├── student_performance_model.pkl
├── app.py
├── requirements.txt
├── Student_Performance_Prediction_Report.pdf
└── README.md
```

## Future Improvements

- Improve predictions for exceptionally high-scoring students.
- Perform cross-validation for more robust evaluation.
- Experiment with additional regression algorithms.
- Improve the interactive application.
- Deploy the application for public access.

## Conclusion

This project demonstrates an end-to-end machine learning workflow for student examination score prediction, combining exploratory analysis, data preprocessing, regression modelling, model evaluation, and application development.

---

**Project:** Student Performance Prediction  
**Category:** Machine Learning | Regression
