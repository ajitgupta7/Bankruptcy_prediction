# Bankruptcy_prediction
Bankruptcy prediction machine learning model - Binary Classification


# Predicting Firms Bankruptcy from Financial Indicators

Contributors: 
 - Ajit Gupta
 - Tejas Choudekar
 - Cristian Castro
 - Karthik Ananthakrishnan


This Project consists of:
 - Data Exploration, Cleaning and Imputation.
 - Feature Selection
 - Model Selection
 - Model Assesment
 - Proposal of a classification model for predicting firm's bankruptcy.


# Findings:
- In terms of data pre-processing, the dataset resulting from replacing missing data with the median (because of highly skewed data), deleting duplicates and replacing outliers by the maximum/minimum IQR values prove to provide more information for building different type of classifiers.
- It was found that only 10 features (out of the intial 64) are sufficient to confidently predict the response variable. These features are: **'Attr6', 'Attr15', 'Attr20', 'Attr23', 'Attr27','Attr39','Attr41','Attr59','Attr61' and 'Attr64'.**
- Assessing the different kinds of classifiers, **the best performance was obtained by training a Random Forest Classifier**.
- This can be observed when comparing SVCs, Logits, KNNs and the Random Forests Classifiers in the ROC/AUC analysis.
- The trained Random Forest Classifier, is characterized by the following hyperparameters:
    - Class_weight: {0: 1, 1: 20},
    - Criterion: gini,
    - max_depth: 10,
    - n_estimators: 100
- The maximum perfomance is at:
    - Recall Score of 99.6 % on training set,
    - Recall Score of 97% on test set.
    - F1 Score 98%
- According to the results, the classifier don't exhibit overfitting, and the variance-bias is well traded.
- **This Random-Forest-Based classifier is recommended to be deployed, and be used into predicting bankruptcy for different companies**.
- It is of knowledge, that the Random-Forests-Classifiers cannot extrapolate beyond the limits of the database base on which it was trained. Nonetheless, based on the proposed outlier approach, this is expected to be handled by the models methodology.
