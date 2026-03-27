# Batch Job Failure Prediction using Machine Learning

## Problem Statement
Batch jobs in enterprise systems are critical for processing large volumes of data. Failures are typically detected only after execution, leading to delays, increased operational effort, and impact on downstream systems.

---

## Objective
To build a machine learning model that predicts whether a batch job will fail or succeed based on historical execution data and system metrics.

---

## Dataset Description
- Synthetic dataset with 2000 records
- Features include:
  - run_time
  - cpu_time
  - memory_usage
  - records_processed
  - dependency_count
  - previous_failure_count
  - day_of_run
- Target:
  - job_status (success / fail)

---

## Exploratory Data Analysis (EDA)
Key insights:
- Higher runtime, CPU usage, and memory increase failure probability
- Mondays show higher failure rates
- Jobs with more dependencies are more failure-prone
- Historical failures strongly influence future failures

---

## Approach
1. Data preprocessing (encoding, cleaning)
2. Handling class imbalance:
   - Undersampling
   - Class weighting
3. Model training and evaluation
4. Model comparison
5. Hyperparameter tuning

---

## Models Used
- Logistic Regression (Imbalanced)
- Logistic Regression (Undersampling)
- Logistic Regression (Class Weight)
- Random Forest (Tuned)

---

## Final Model: Random Forest (Tuned)

### Performance
- Accuracy: **96%**
- Precision: **95.7%**
- Recall: **99.7%**
- F1 Score: **0.976**

---

## Feature Importance
Top factors influencing job failure:
- previous_failure_count
- run_time
- cpu_time
- memory_usage
- dependency_count

---

## Conclusion
The model effectively predicts batch job failures with high accuracy and recall. It can be used in real-world systems to proactively identify high-risk jobs and reduce operational effort.

---

## Tech Stack
- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib / Seaborn

---

## Project Structure
batch-job-failure-prediction/
│
├── data/
├── notebooks/
├── model/
└── README.md

---

## Author
Elizabeth Nancy J
