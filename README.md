# Credit Card Fraud Detection - ML

The goal of this project is to develop a machine learning model that can accurately detect fraudulent credit card transactions using historical data. By analyzing transaction patterns, the model should be able to distinguish between normal and fraudulent activity, helping financial institutions flag suspicious behavior early and reduce potential risks.

Data link: https://media.geeksforgeeks.org/wp-content/uploads/20240904104950/creditcard.csv

Challenges include:

- Handling imbalanced datasets where fraud cases are a small fraction of total transactions.
- Ensuring high precision to minimize false positives (flagging a valid transaction as fraud).
- Ensuring high recall to detect as many fraud cases as possible.

### Building and Training the Model:

Train a Random Forest Classifier to predict fraudulent transactions.

### Model Evaluation Metrics:
The model accuracy is high due to class imbalance so we will have computed precision, recall and f1 score to get a more meaningful understanding. We observe:

- Accuracy: 0.9995: Out of all predictions, 99.95% were correct. However, in imbalanced datasets (like fraud detection), accuracy can be misleading i.e. a model that predicts everything as "not fraud" will still have high accuracy.
- Precision: 0.9615 (TP/(TP + FP)): When the model predicted "fraud", it was correct 96.15% of the time. High precision means very few false alarms (false positives).
- Recall: 0.7653 (TP/(TP + FN)): Out of all actual fraud cases, the model detected 76.53%. This shows how well it catches real frauds. A lower recall means some frauds were missed (false negatives).
- F1-Score: 0.8523: A balance between precision and recall. 85.23% is strong and shows the model handles both catching fraud and avoiding false alarms well.
- Matthews Correlation Coefficient (MCC): 0.8576: A more balanced score (from -1 to +1) even when classes are imbalanced. A value of 0.8576 is very good, it means the model is making strong, balanced predictions overall.

We can balance dataset by oversampling the minority class or by undersampling the majority class we can increase accuracy of our model.
