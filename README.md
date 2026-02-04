# Sampling Techniques on Imbalanced Credit Card Dataset

## Objective
The objective of this assignment is to study the impact of different sampling techniques on a highly imbalanced credit card fraud dataset and analyze how these techniques affect the accuracy of multiple machine learning models.

---

## Dataset
- Dataset Name: Creditcard_data.csv
- Target Variable: Class
- Problem Type: Binary Classification
- Issue: Highly imbalanced classes

Dataset Link:
https://github.com/AnjulaMehto/Sampling_Assignment/blob/main/Creditcard_data.csv

---

## Class Balancing Strategy
The given dataset was highly imbalanced. To handle class imbalance, the dataset was converted into a balanced dataset using Random Over Sampling (ROS).  
This ensures equal representation of both classes and reduces bias during model training.

---

## Sampling Techniques Used
After balancing the dataset, the following sampling techniques were applied:

1. Simple Random Sampling  
2. Stratified Sampling  
3. Systematic Sampling  
4. Cluster Sampling  
5. Bootstrap Sampling  

Each technique generated a separate dataset sample.

---

## Machine Learning Models Used

| Model Code | Algorithm |
|------------|-----------|
| M1 | Logistic Regression |
| M2 | Decision Tree |
| M3 | Naive Bayes |
| M4 | Random Forest |
| M5 | Support Vector Machine (SVM) |

All models were trained using standard preprocessing and evaluated using accuracy score.

---

## Accuracy Results Table

Rows represent ML Models and columns represent sampling techniques.

| Model / Sampling | Sampling1 (Simple Random) | Sampling2 (Stratified) | Sampling3 (Systematic) | Sampling4 (Cluster) | Sampling5 (Bootstrap) |
|------------------|--------------------------:|------------------------:|------------------------:|--------------------:|----------------------:|
| M1_LogisticRegression | 90.22 | 86.96 | 89.22 | 94.57 | 95.65 |
| M2_DecisionTree       | 94.57 | 97.83 | 95.10 | 100.00 | 98.91 |
| M3_NaiveBayes         | 76.09 | 61.96 | 80.39 | 64.13 | 71.74 |
| M4_RandomForest       | 100.00 | 98.91 | 100.00 | 100.00 | 100.00 |
| M5_SVM                | 95.65 | 94.57 | 96.08 | 97.83 | 97.83 |

Highest Accuracy: 100.00%  
Lowest Accuracy: 61.96%

---

## Best Sampling Technique for Each Model

| Model | Best Sampling Method | Best Accuracy |
|------|-----------------------|-------------:|
| M1_LogisticRegression | Sampling5 (Bootstrap) | 95.65% |
| M2_DecisionTree | Sampling4 (Cluster) | 100.00% |
| M3_NaiveBayes | Sampling3 (Systematic) | 80.39% |
| M4_RandomForest | Sampling1 / Sampling3 / Sampling4 / Sampling5 (Tied) | 100.00% |
| M5_SVM | Sampling4 / Sampling5 (Tied) | 97.83% |

---

## Overall Best Combination
Model: M2_DecisionTree  
Sampling Technique: Sampling4 (Cluster Sampling)  
Accuracy: 100.00%

---

## Discussion

### Model Performance Analysis
- Random Forest (M4) produced the most stable results and achieved 100% accuracy in most sampling techniques.
- Decision Tree (M2) performed extremely well and achieved 100% accuracy with Cluster Sampling.
- SVM (M5) performed consistently strong with accuracy between 94.57% and 97.83%.
- Logistic Regression (M1) showed higher variation and performed best with Bootstrap Sampling.
- Naive Bayes (M3) produced comparatively lower accuracy, indicating weaker suitability for this dataset.

### Sampling Technique Analysis
- Cluster Sampling (Sampling4) gave the best overall results and achieved the highest performance in multiple models.
- Bootstrap Sampling (Sampling5) improved Logistic Regression and gave the best or tied-best accuracy for SVM.
- Systematic Sampling (Sampling3) worked best for Naive Bayes and also achieved perfect accuracy for Random Forest.
- Stratified Sampling (Sampling2) did not outperform other methods significantly because the dataset was already balanced.

---

## Conclusion
This experiment shows that balancing the dataset using Random Over Sampling (ROS) significantly improves model performance.  
Sampling methods affect each model differently, and Cluster Sampling provided the best overall results.

Best Overall Combination: Decision Tree with Cluster Sampling (100% accuracy)  
Most Stable Model: Random Forest (100% accuracy in most sampling techniques)

---

