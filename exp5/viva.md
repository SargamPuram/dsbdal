Logistic Regression Related Questions:
What is logistic regression, and how does it work?

Logistic regression is a statistical method used for binary classification. It predicts the probability of an event occurring based on input features. The model applies the sigmoid function to the linear combination of features to output a value between 0 and 1, which is then mapped to a class (0 or 1).

Why do we use logistic regression for classification problems instead of linear regression?

Linear regression is used for predicting continuous values, whereas logistic regression is used for binary classification problems. The output of linear regression is not bounded (i.e., it can go from -∞ to ∞), which doesn't suit classification tasks. Logistic regression outputs a probability between 0 and 1 by applying the sigmoid function.

What is the role of the sigmoid function in logistic regression?

The sigmoid function maps the linear output of the regression model (a real number) into a probability between 0 and 1. This probability is interpreted as the likelihood of the instance belonging to class 1.

Why is logistic regression a suitable model for binary classification problems?

Logistic regression is ideal for binary classification as it produces a probability score and uses a decision threshold (commonly 0.5) to classify inputs into two classes (0 or 1). It’s computationally efficient and works well when the relationship between the input variables and the output is approximately linear.

What is the difference between binary logistic regression and multinomial logistic regression?

Binary logistic regression is used for two-class problems (0 or 1), whereas multinomial logistic regression handles multiple classes (more than two categories).

What are the assumptions of logistic regression?

Logistic regression assumes:

A linear relationship between the independent variables and the log-odds of the dependent variable.

Independence of errors.

Little or no multicollinearity.

The dependent variable should be binary.

How does logistic regression handle non-linearity?

Logistic regression doesn't directly handle non-linearity but can model non-linear relationships using transformations of the features (e.g., polynomial features or interactions) or by using kernel methods.

What is the cost function used in logistic regression?

The cost function used in logistic regression is the log loss (also known as binary cross-entropy), which penalizes incorrect predictions by measuring the difference between the predicted probability and the actual label.

Explain the concept of regularization in logistic regression (L1 and L2 regularization).

L1 regularization (Lasso) adds the absolute value of the coefficients to the cost function, encouraging sparse models.

L2 regularization (Ridge) adds the squared value of the coefficients to the cost function, penalizing large coefficients and helping to prevent overfitting.

How would you evaluate a logistic regression model?

You can evaluate a logistic regression model using accuracy, precision, recall, F1-score, confusion matrix, and ROC curve. Cross-validation can also be used to assess the model's performance on different subsets of the data.

Classification Metrics:
What is the confusion matrix, and what do the terms TP, TN, FP, and FN represent?

A confusion matrix is a table that shows the performance of a classification algorithm. The terms are:

TP (True Positive): Correctly predicted positive cases.

TN (True Negative): Correctly predicted negative cases.

FP (False Positive): Incorrectly predicted as positive.

FN (False Negative): Incorrectly predicted as negative.

What is precision, and how does it differ from recall?

Precision is the proportion of true positive predictions out of all positive predictions.

Precision
=
𝑇
𝑃
𝑇
𝑃
+
𝐹
𝑃
Precision= 
TP+FP
TP
​
 
Recall (sensitivity) is the proportion of true positives out of all actual positives.

Recall
=
𝑇
𝑃
𝑇
𝑃
+
𝐹
𝑁
Recall= 
TP+FN
TP
​
 
Precision focuses on minimizing false positives, while recall focuses on minimizing false negatives.

How do you interpret the precision and recall scores in the context of your model?

A higher precision indicates that the model is good at predicting positive instances with fewer false positives. A higher recall indicates that the model is identifying most of the actual positives, though it may have more false positives.

What is the F1-score, and how is it calculated?

The F1-score is the harmonic mean of precision and recall, balancing both metrics. It is calculated as:

F1-score
=
2
×
Precision
×
Recall
Precision
+
Recall
F1-score=2× 
Precision+Recall
Precision×Recall
​
 
What is accuracy, and why might it be misleading in imbalanced datasets?

Accuracy is the proportion of correct predictions (both true positives and true negatives) out of all predictions. It can be misleading in imbalanced datasets because the model may predict the majority class correctly and still appear to have high accuracy, even if it fails to predict the minority class.

What is the relationship between precision, recall, and the F1-score?

The F1-score balances precision and recall. When precision and recall are high, the F1-score will also be high, indicating that the model is performing well in both minimizing false positives and false negatives.

What is the error rate, and how is it calculated?

The error rate is the proportion of incorrect predictions (false positives + false negatives) out of all predictions.

Error rate
=
𝐹
𝑃
+
𝐹
𝑁
𝑇
𝑃
+
𝑇
𝑁
+
𝐹
𝑃
+
𝐹
𝑁
Error rate= 
TP+TN+FP+FN
FP+FN
​
 
Explain why we scale data before training the model.

Scaling ensures that all features have the same scale, preventing models from being biased towards variables with larger numerical values. In logistic regression, scaling improves convergence speed and avoids issues with the gradient descent optimization.

What is the significance of using the random_state parameter during data splitting?

The random_state parameter ensures reproducibility by setting the random seed for data splitting. It allows the model to be trained and tested on the same subsets across different runs.

Data Preprocessing:
Why did you one-hot encode the 'Gender' column?

The 'Gender' column was one-hot encoded to convert categorical data into numerical format. Logistic regression requires numerical inputs, and one-hot encoding creates separate binary columns for each category.

Why did you drop the 'User ID' column from the dataset?

The 'User ID' column was dropped because it is an identifier and doesn’t have any predictive value. Including it could introduce noise into the model and affect its performance.

Why did you use drop_first=True during one-hot encoding?

Using drop_first=True prevents multicollinearity by dropping one of the categories (usually the first one) in the encoded columns, which helps to avoid redundancy in the features.

What are outliers, and how did you handle them in this dataset?

Outliers are extreme values that differ significantly from other data points. They can distort the model’s predictions. In this dataset, I handled outliers using the IQR (Interquartile Range) method, where data points outside the range of 1.5 * IQR from the 25th and 75th percentiles were removed.

Can removing outliers ever be harmful? Explain why or why not.

Removing outliers can be harmful if they represent important variance in the data. For example, in financial data, outliers might be critical for detecting fraud. Careful evaluation is necessary before removing them.

Why do we use the IQR method to detect and remove outliers?

The IQR method is robust to extreme values and helps identify data points that deviate significantly from the distribution, ensuring that they do not unduly influence the model’s performance.

What other techniques can be used to handle missing or null values in a dataset?

Missing values can be handled by:

Imputation (mean, median, mode).

Deleting rows or columns with missing values.

Using machine learning algorithms that can handle missing values.

Model Evaluation:
What is the purpose of evaluating the model using a confusion matrix?

A confusion matrix provides a clear breakdown of the true and false predictions made by the model, allowing you to calculate various metrics like accuracy, precision, recall, and F1-score.

Why is Mean Squared Error (MSE) typically used in regression problems rather than classification problems?

MSE is used in regression because it quantifies the difference between predicted and actual continuous values. In classification, metrics like accuracy, precision, and recall are used since the output is categorical.

What does it mean when your model has a high accuracy score but low precision and recall?

This indicates that the model is classifying most instances correctly (high accuracy) but is struggling to correctly identify positive cases (low precision and recall). This often happens in imbalanced datasets.

Explain why the evaluation metrics you selected (precision, recall, accuracy) are important for your model.

Precision, recall, and accuracy provide insights into how well the model is distinguishing between classes. Accuracy gives an overall measure, while precision and recall help assess performance with respect to positive class predictions, which is crucial in classification tasks.

What steps would you take if your model's accuracy is high but precision or recall is low?

I would focus on improving precision or recall by:

Tuning the decision threshold.

Trying different models or techniques (e.g., regularization, feature engineering).

Handling imbalanced classes (e.g., resampling techniques).

What is the significance of the learning curve, and how would you interpret one?

A learning curve shows the model’s performance over time (or with more data). A well-behaved curve shows consistent improvement. If the performance plateaus or worsens, it may indicate overfitting or underfitting.

