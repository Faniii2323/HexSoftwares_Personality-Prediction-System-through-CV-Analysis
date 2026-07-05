# HexSoftwares_Personality-Prediction-System-through-CV-Analysis
Task 3, project 2 Personality Prediction System through CV Analysis

# Personality Prediction System Through CV Analysis

This project was completed as part of the **@HexSoftwares Internship**.  
The goal of this project is to build a machine learning system that analyzes CV/resume-style text and predicts a candidate's personality category.

The system uses Natural Language Processing (NLP) and machine learning algorithms to extract useful patterns from candidate profiles such as education, skills, experience, projects, achievements, certifications, and work style.

---

## Project Objective

The objective of this project is to predict personality traits from CV-style text using supervised machine learning and transformer-based NLP models.

The model predicts one of the following personality classes:

- Dependable
- Extraverted
- Lively
- Responsible
- Serious

---

## Dataset Overview

The dataset used in this project is an augmented CV-style personality dataset.

### Dataset Shape

```text
Rows: 709
Columns: 18
```

After preparing the combined CV text column, the final dataset shape became:

```text
Rows: 709
Columns: 20
```

### Main Columns Used

The following CV-related columns were combined to create the final text input:

- Education
- Skills
- Experience
- Projects
- Achievements
- Certifications
- Work_Style
- CV_Text

The target column used for prediction was:

```text
Personality (Class label)
```

---

## Personality Class Distribution

```text
serious        161
extraverted    150
dependable     138
lively         134
responsible    126
```

---

## Algorithms Applied

Five algorithms were implemented and compared:

| No. | Algorithm |
|---:|---|
| 1 | TF-IDF + Logistic Regression |
| 2 | TF-IDF + Linear SVM |
| 3 | Random Forest |
| 4 | Gradient Boosting |
| 5 | DistilBERT / BERT |

---

## Train-Test Split

The dataset was split into training and testing sets using stratified sampling.

```text
Training samples: 567
Testing samples: 142
```

---

## Model Performance

All five models achieved perfect results on the test set.

| Model | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|
| TF-IDF + Logistic Regression | 1.00 | 1.00 | 1.00 | 1.00 |
| TF-IDF + Linear SVM | 1.00 | 1.00 | 1.00 | 1.00 |
| Random Forest | 1.00 | 1.00 | 1.00 | 1.00 |
| Gradient Boosting | 1.00 | 1.00 | 1.00 | 1.00 |
| DistilBERT / BERT | 1.00 | 1.00 | 1.00 | 1.00 |

### Best Model

Based on F1-score, the selected best classical model was:

```text
TF-IDF + Logistic Regression
```

---

## Classification Report of Best Model

```text
              precision    recall  f1-score   support

  dependable       1.00      1.00      1.00        28
 extraverted       1.00      1.00      1.00        30
      lively       1.00      1.00      1.00        27
 responsible       1.00      1.00      1.00        25
     serious       1.00      1.00      1.00        32

    accuracy                           1.00       142
   macro avg       1.00      1.00      1.00       142
weighted avg       1.00      1.00      1.00       142
```

---

## Sample Prediction

A sample CV profile was tested using the trained model.

### Sample Input

```text
Education: BS Computer Science.
Skills: Python, machine learning, data analysis, teamwork, communication, problem solving.
Experience: 1 year internship as a machine learning intern.
Projects: Resume screening system, sentiment analysis project, spam email classifier.
Achievements: Completed multiple AI projects and led a small student project team.
Certifications: Python for Data Science, Machine Learning Basics.
Work style: Responsible, organized, analytical, focused on completing tasks on time.
```

### Output

```text
Predicted Personality using selected classical model: serious
Predicted Personality using DistilBERT / BERT: serious
```

---
## Conclusion

This project successfully demonstrates how NLP and machine learning can be used to predict personality categories from CV-style candidate profiles.

Multiple classical ML models and a transformer model were trained and compared. The project also includes evaluation metrics, confusion matrices, classification reports, sample CV prediction, and model saving.

---

## Author
Fani2323
@HexSoftwares Internship 
Computer Science
