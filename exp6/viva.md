📘 Viva Questions & Answers
1. What is Naive Bayes?
A probabilistic classifier based on Bayes' Theorem with the naive assumption that all features are independent.

2. Why use Gaussian Naive Bayes?
Because it handles continuous, normally distributed features — perfect for datasets like Iris.

3. Bayes' Theorem formula?
𝑃
(
𝑌
∣
𝑋
)
=
𝑃
(
𝑋
∣
𝑌
)
⋅
𝑃
(
𝑌
)
𝑃
(
𝑋
)
P(Y∣X)= 
P(X)
P(X∣Y)⋅P(Y)
​
 
4. Why encode the target variable?
Because ML models can only work with numerical values, not strings.

5. Why do we scale the features?
To make all features contribute equally — especially important in distance-based or probabilistic models.

6. What does the confusion matrix show?
Class	TP	FP	FN
Setosa (0)	10	0	0
Versicolor (1)	9	0	0
Virginica (2)	11	0	0

7. What are:
TP (True Positive): Correctly classified as its own class

FP (False Positive): Incorrectly classified as this class

FN (False Negative): Belongs to the class but classified wrongly

TN (True Negative): Not of this class and correctly not predicted as it

8. Metric Formulas:
Accuracy:

Accuracy
=
𝑇
𝑃
+
𝑇
𝑁
𝑇
𝑃
+
𝐹
𝑃
+
𝑇
𝑁
+
𝐹
𝑁
Accuracy= 
TP+FP+TN+FN
TP+TN
​
 
Precision (Macro):

Precision
=
1
𝐶
∑
𝑇
𝑃
𝑖
𝑇
𝑃
𝑖
+
𝐹
𝑃
𝑖
Precision= 
C
1
​
 ∑ 
TP 
i
​
 +FP 
i
​
 
TP 
i
​
 
​
 
Recall (Macro):

Recall
=
1
𝐶
∑
𝑇
𝑃
𝑖
𝑇
𝑃
𝑖
+
𝐹
𝑁
𝑖
Recall= 
C
1
​
 ∑ 
TP 
i
​
 +FN 
i
​
 
TP 
i
​
 
​
 
Error Rate:

1
−
Accuracy
1−Accuracy
9. Is 100% accuracy realistic?
Not always. In real-world noisy data, it's rare. In clean, small datasets like Iris, it can happen. But it's always worth questioning.

✅ Conclusion
The Naive Bayes classifier achieved perfect performance on the Iris dataset. It shows how powerful simple probabilistic models can be when data is clean, structured, and balanced.
