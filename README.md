**Disease Prediction** 

This repository provides a comprehensive solution for disease prediction based on symptoms using machine learning models. The dataset used for this project is sourced from Kaggle (https://www.kaggle.com/datasets/kaushil268/disease-prediction-using-machine-learning). The entire process, from data preprocessing to model selection, evaluation, and combination, is detailed below.

**Dataset Overview**

The dataset contains information about various diseases and their associated symptoms. Each entry consists of symptoms and the corresponding disease label. This dataset serves as the foundation for training and evaluating machine learning models.

**Data Preprocessing and Cleaning**

The dataset undergoes essential preprocessing steps to ensure its suitability for model training. The primary preprocessing steps include:

- Handling Missing Values: Columns with null values are dropped, ensuring the dataset's integrity.
- Balancing the Dataset: The distribution of diseases is visualized to assess the dataset's balance, which is crucial for model training.
- Encoding the Target Value: The target values (disease labels) are encoded into numerical form using `LabelEncoder`. This conversion is essential for training machine learning models, as they typically require numerical target values.
**
Model Selection**

In selecting models, we consider a scenario where interpretability, simplicity, and accuracy are crucial factors:

1. Support Vector Machine (SVM)
- **Scenario Fit:** Well-suited for scenarios where the decision boundary between diseases is complex and not easily interpretable.
- **Strengths:** Effective in high-dimensional spaces, handles non-linear relationships well.

2. Naive Bayes
- **Scenario Fit:** Appropriate when interpretability and simplicity are crucial, making it suitable for medical applications.
- **Strengths:** Computationally efficient, assumes independence between features.

3. Random Forest
- **Scenario Fit:** Balances interpretability with high accuracy, making it suitable for scenarios where a combination of both is desired.
- **Strengths:** Robust, handles non-linearity, and reduces overfitting.

**Model Evaluation using K-fold cross-validation**

The selected models are evaluated using k-fold cross-validation, providing insights into their performance and generalization capabilities. Individual classifiers are also tested on a separate test dataset to assess their accuracy. The accuracy of all 3 models are high and similar.

![image](https://github.com/sudikshaacharya1/DiseasePrediction/assets/138321124/b5db5502-2951-4277-8642-aa46f221c4d5)

 

**Combining Models for Enhanced Prediction**

A combined model is created by integrating predictions from SVM, Naive Bayes, and Random Forest classifiers. This approach leverages the diverse strengths of each model to enhance overall prediction accuracy.

![image](https://github.com/sudikshaacharya1/DiseasePrediction/assets/138321124/853b1122-8446-4fc3-82ac-e8ef57b5fffd)



**Usage Example**

```python
# Testing the function
print(predictDisease("Continuous Sneezing"))
```
![image](https://github.com/sudikshaacharya1/DiseasePrediction/assets/138321124/4d80822a-4fd3-457b-b4c2-f1172c3593f3)


```python
# Testing the function
print(predictDisease("Skin Rash,itching"))
```
![image](https://github.com/sudikshaacharya1/DiseasePrediction/assets/138321124/95083961-6794-47ef-a257-3deb38564feb)


```python
# Testing the function
print(predictDisease("Skin Rash,itching"))
```
![image](https://github.com/sudikshaacharya1/DiseasePrediction/assets/138321124/c3e620b6-67c4-4cfd-96c3-6f5fb6a7dbda)

