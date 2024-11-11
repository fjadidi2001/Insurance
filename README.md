Here's a table summarizing the 12 IPYNB files and a brief explanation of each:

| File Name                                       | Description                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Analyze_Telematics_syn.ipynb**                | Analyzes synthetic telematics data with a high number of zero values in `AMT_Claim`, a typical scenario in insurance where claims are rare. Discusses potential techniques like zero-inflated models (e.g., ZIP, ZINB, and Zero-Inflated Beta) and two-stage modeling to handle zero-inflated data. Outlier handling methods like Winsorization and robust regression are also considered.                  |
| **ClaimYN_Prediction_TabNet_80result.ipynb**    | Implements a simple TabNet model to predict `ClaimYN`. After 50 epochs, achieves a best accuracy of 78.4% at epoch 46. The preprocessing steps include creating the `ClaimYN` label based on `NB_Claim` and `AMT_Claim` and three levels of preprocessing before training.                                                                                                                            |
| **ClaimYN_Prediction_TabNet_Bad_Result.ipynb**  | Reattempts the `ClaimYN` prediction with more extensive preprocessing and feature engineering, including encoding categorical features and applying scaling. The model achieves an accuracy of 85%. The model evaluation shows the importance of using appropriate scaling and preprocessing for better results.                                              |
| **ClaimYN_Prediction_With_DL&ML.ipynb**         | Predicts `ClaimYN` with both deep learning and machine learning models. Includes steps like handling missing values, encoding, standardizing, balancing the dataset with SMOTE, and dropping irrelevant columns. The data is split into training, testing, and validation sets (70%-15%-15%) to ensure reliable evaluation.                                                                        |
| **Insurance_TabNet_AMT_Claim_Prediction.ipynb** | Attempts a regression task to predict `AMT_Claim` using TabNet but notes unsatisfactory results, leading to abandoning the approach for this specific task.                                                                                                                                                                                                                     |
| **NB_Claim_Prediction_FirstV_without_balance.ipynb** | Predicts `NB_Claim` without addressing data imbalance, leading to overly optimistic results (100% accuracy) across all algorithms. This highlights the importance of handling imbalance to avoid misleading performance metrics.                                                                                                                         |
| **NB_Claim_Prediction_Insurance.ipynb**         | Compares various models for `NB_Claim` prediction, with results showing high accuracy for Logistic Regression, XGBoost, TabNet, Random Forest, and LightGBM. After using SMOTE and hyperparameter tuning, the models achieve excellent performance, effectively handling class imbalance.                                                                  |
| **NB_Claim_Prediction_TabNet_Tuning.ipynb**     | Step-by-step guide for model training, including TabNet hyperparameter tuning with RandomizedSearchCV. Data preprocessing includes standardization, normalization, and feature engineering. The TabNet model is then trained and tuned to maximize accuracy and interpretability for insurance risk pricing.                                                    |
| **Risk_Category_TabNet.ipynb**                  | Predicts `Risk_Category` using TabNet. Sets up the `Risk_Category` label as a binary indicator based on claims and claim amount, achieving a test accuracy of 75.44% and F1 score of 75.25%.                                                                                                                                                                    |
| **Risk_Category_TabNet_best_version.ipynb**     | A refined version of `Risk_Category` prediction with PCA applied for dimensionality reduction before training the TabNet model. Achieves high accuracy (99.53%), showing improved performance due to feature reduction and optimal data processing.                                                                                                          |
| **insurance_classification_ensemble_model_claim_YN.ipynb** | Utilizes both TabNet and DNN in an ensemble model for `ClaimYN` classification. Metrics for the ensemble model include 97.47% accuracy, with other metrics calculated for deeper insights into model performance (precision, recall, F1 score, AUC).                                                                                                          |
| **predict_ClaimYN_with_combined_models.ipynb**  | Uses SMOTE, feature engineering, and visualization for `ClaimYN` prediction. Evaluates TabNet, XGBoost, and ensemble models, with detailed performance metrics, showing the impact of ensemble approaches for robustness.                                                                                                                                                      |
| **telematics_syn_Risk_Category.ipynb**          | Implements TabNet for predicting `Risk_Category` using synthetic telematics data, achieving near-perfect validation accuracy (99.98%) and F1 score (99.98%). The model is saved for future use, indicating it has performed well on this synthetic dataset.                                                                                                                                                      |


