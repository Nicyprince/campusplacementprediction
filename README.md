College Placement Models

1. Dataset Description and Preprocessing
The dataset used for this study consists of students' academic and demographic features, aiming to predict their placement status. The dataset was preprocessed as follows:
•	Feature Selection: Dropped sl_no (serial number) and salary columns, as they are either irrelevant or introduce data leakage.
•	Exploratory Data Analysis (EDA): A pair plot was generated to understand feature distributions and relationships.
•	Encoding Categorical Variables: Label encoding was applied to ssc_b, hsc_b, workex, and status, while one-hot encoding was used for hsc_s, degree_t, and specialisation.
•	Feature Scaling: Standardization was performed on numerical features to ensure uniformity in training models.
•	Train-Test Split: The dataset was divided into 70% training and 30% testing data.

2. Model Selection and Justification
Three machine learning models were selected:
•	XGBoost: A powerful gradient boosting model known for handling imbalanced datasets and capturing complex patterns.
•	Naïve Bayes: A probabilistic model well-suited for categorical data and simple decision-making.
•	K-Nearest Neighbors (KNN): A distance-based model useful for non-linear relationships.
Additionally, a Voting Classifier was implemented to aggregate predictions from these models and improve overall performance.

3. Model Evaluation
Each model was evaluated using accuracy, precision, recall, and F1-score metrics.
XGBoost Model
•	Accuracy: 81.5%
•	Precision: 82%
•	Recall: 93.2%
•	F1-Score: 87.2%
•	Confusion Matrix:
o	True Positives: 41, False Positives: 9
o	True Negatives: 12, False Negatives: 3

Naïve Bayes Model
•	Accuracy: 72.3%
•	Precision: 75%
•	Recall: 88.6%
•	F1-Score: 81.3%
•	Confusion Matrix:
o	True Positives: 40, False Positives: 15
o	True Negatives: 6, False Negatives: 4

Voting Classifier
•	Accuracy: 75.4%
•	Precision: 76.9%
•	Recall: 90.9%
•	F1-Score: 83.3%
•	Confusion Matrix:
o	True Positives: 40, False Positives: 12
o	True Negatives: 9, False Negatives: 4

4. Conclusion
•	Best Performing Model: XGBoost demonstrated the highest accuracy (81.5%) and recall (93.2%), making it the most reliable model for predicting college placement.
•	Trade-offs: While Naïve Bayes performed well in recall, it had lower accuracy due to misclassification. KNN did not significantly improve the results.
•	Ensemble Learning: The Voting Classifier provided a balanced performance, aggregating strengths from multiple models but did not surpass XGBoost.
•	Future Improvements: Hyperparameter tuning, feature engineering, and increasing training data could further improve model performance.
