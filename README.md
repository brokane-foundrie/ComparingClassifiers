# ComparingClassifiers
Practical Application 7.1

Objective
The goal is to evaluate the performance of classifiers—K-nearest neighbors (KNN), logistic regression (LR), decision trees (DT), and support vector machines (SVM)—on a dataset from a Portuguese bank's telemarketing campaigns. This dataset includes 17 campaigns and over 79,354 contacts, with the objective of predicting customer acceptance of a long-term deposit product.

Scoring Metrics
To assess model performance:

Primary metric: AUC-ROC, to balance true positives (buyers) against false positives (non-buyers).
Additional metrics: Accuracy, F1, Precision, and Recall to understand overall model performance.
Runtime: To evaluate tradeoffs between accuracy and computational efficiency.
Findings
The dataset is highly imbalanced (89% "no" and 11% "yes"). After parameter optimization via GridSearch, the results are:

Logistic Regression: Best performer with an AUC-ROC of 65% and an F1 score of 25%. Efficient runtime makes it practical for use.
Decision Trees: Runner-up with an AUC-ROC of 64.7%, but a significantly lower F1 score (.44%) and longer runtime.
SVM: Tested on a subset of 5,000 observations due to high computational demands. Results were inconclusive for larger datasets.
KNN: Struggled with class imbalance, leading to suboptimal performance.
Recommendations
Logistic regression is the preferred model, balancing performance and efficiency. Decision trees may be considered in scenarios where interpretability is prioritized.

Next Steps
Model Refinement: Further parameter optimization for LR and DT.
Class Imbalance: Address imbalance using oversampling, undersampling, or class weighting.
Feature Engineering: Incorporate macroeconomic data, temporal features (months, days), and refine existing variables.
Data Cleaning: Handle "unknown" values and remove inconclusive contacts to improve dataset quality.
Conclusion
Logistic regression provides the best balance of performance and practicality for predicting telemarketing campaign success. Further exploration of the dataset and techniques can unlock additional improvements.
