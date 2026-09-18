# Iris Flower Classification Report

## 1. Project Overview

This project aimed to build a machine learning model capable of classifying iris flowers into their three species:

- Iris-setosa
- Iris-versicolor
- Iris-virginica

The workflow used a well-known iris dataset with four numeric features: sepal length, sepal width, petal length, and petal width. The goal was to compare several classification algorithms and identify the model that best generalizes to unseen flower samples.

## 2. Dataset Description

The dataset contains 150 observations, evenly distributed across the three species:

- 50 Iris-setosa
- 50 Iris-versicolor
- 50 Iris-virginica

This balanced structure helps make model comparison more reliable and reduces the risk that a model performs well simply because one class dominates the dataset.

## 3. Exploratory Data Analysis

Before model construction, the dataset was explored using descriptive statistics and visualizations. The analysis showed that:

- Iris-setosa has noticeably smaller petal dimensions than the other two classes.
- The feature distributions for versicolor and virginica overlap more than setosa does.
- Pairwise relationships between features reveal strong separation for setosa and some overlap between versicolor and virginica.

These observations suggest that the classification problem is approachable with standard supervised learning techniques, while also indicating that distinguishing versicolor from virginica may be more difficult than separating setosa from the other two species.

## 4. Methodology

The modelling process followed a standard supervised learning workflow:

1. Loaded the iris dataset.
2. Split the data into training and testing sets using an 80/20 ratio.
3. Evaluated multiple classification algorithms, including Logistic Regression, Linear Discriminant Analysis, K-Nearest Neighbors, Decision Tree, Naive Bayes, and Support Vector Classifier.
4. Selected the best-performing model based on accuracy and classification quality.
5. Trained the final model on the training set and evaluated it on the test set.

## 5. Model Results

Among the candidate models, the Support Vector Classifier (SVC) produced the strongest performance and was therefore selected as the final model.

### Test Accuracy

The final SVC model achieved a test accuracy of 96.67%.

### Classification Report

| Class | Precision | Recall | F1-Score | Support |
| --- | ---: | ---: | ---: | ---: |
| Iris-setosa | 1.00 | 1.00 | 1.00 | 11 |
| Iris-versicolor | 1.00 | 0.92 | 0.96 | 13 |
| Iris-virginica | 0.86 | 1.00 | 0.92 | 6 |
| Accuracy |  |  | 0.97 | 30 |
| Macro Avg | 0.95 | 0.97 | 0.96 | 30 |
| Weighted Avg | 0.97 | 0.97 | 0.97 | 30 |

## 6. Interpretation of Results

The results demonstrate that the classifier performs extremely well overall. The most important findings are:

- Iris-setosa is classified perfectly, which is consistent with the exploratory analysis showing that it is clearly separated from the other species.
- Iris-versicolor and Iris-virginica are slightly harder to distinguish because their feature distributions overlap more.
- The model still achieves strong results for both classes, indicating that the decision boundary is effective even in the more difficult cases.
- A 96.7% accuracy rate suggests the model generalizes well to unseen iris samples and can be considered robust for this dataset.

## 7. Conclusions

This project shows that classical machine learning methods can classify iris species with very high accuracy using only flower measurements. The model was not only accurate overall, but also reliable across all three classes, with particularly strong performance for Iris-setosa.

The main takeaway is that the iris dataset is a good example of a clean, well-structured classification problem where simple features and standard algorithms are enough to achieve strong predictive performance. The success of the SVC model also highlights the importance of testing multiple algorithms before finalizing a solution, since different models can perform differently depending on how the classes are separated in feature space.

## 8. Final Summary

The Iris flower classification project successfully demonstrates the pipeline of data exploration, model selection, evaluation, and interpretation. The final SVC model achieved 96.7% accuracy on the test set and produced highly competitive precision, recall, and F1-scores across all three species.

This indicates that the selected model is effective and suitable for this dataset, and it reinforces the broader lesson that even relatively simple machine learning approaches can yield strong results when the data is well-structured and the class patterns are clear.
