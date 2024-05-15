# Hepatic Cirrhosis Survival Prediction

This project aims to predict the survival status of patients with liver cirrhosis using Machine Learning. I implemented three models: K-Nearest Neighbors (KNN), Decision Tree, and Support Vector Machine (SVM), evaluating them based on precision, recall, accuracy, F1-score, and ROC curve analysis.

#### Performance Metrics
- **Precision**: Proportion of correct positive predictions.
- **Recall**: Proportion of actual positives correctly identified.
- **Accuracy**: Overall correctness of predictions.
- **F1-score**: Harmonic mean of precision and recall.
- **AUC-ROC**: Ability to distinguish between classes.

#### Techniques Used
- **Data Preprocessing**: 
  - Imputed missing values from the training data to handle incomplete datasets.
- **Grid Search**:
  - Employed `GridSearchCV` to find the best hyperparameters for each model:
    - **KNN**: Optimized for the number of neighbors (`n_neighbors`), weights (`weights`), and distance metric (`metric`).
    - **Decision Tree**: Tuned `max_depth`, `criterion`, and `min_samples_split` to balance bias and variance.
    - **SVM**: Selected the best values for `C`, `kernel`, `degree`, and `gamma`.
- **Cross-Validation**:
  - Utilized 10-fold cross-validation to ensure robust performance estimates, improving the generalization of the models.
- **Model Evaluation**:
  - Developed custom evaluation functions to calculate detailed performance metrics for each model.
- **Pruning**:
  - Implemented a pruning technique for the Decision Tree model to prevent overfitting and ensure a more generalizable model.

#### Selected Model: SVM
The SVM model outperformed the other models, showing the highest accuracy (0.65), precision (0.73), recall (0.65), and F1-score (0.69). It also had the highest AUC-ROC values (0.84 micro-average, 0.80 macro-average), indicating strong performance in distinguishing between survival statuses.

#### Summary
The SVM model was chosen for its superior performance and balanced precision and recall, making it the best option for predicting the survival status of patients with liver cirrhosis in this study.
