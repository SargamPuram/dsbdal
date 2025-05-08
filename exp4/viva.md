# Viva Questions – Linear Regression on California Housing Dataset

## 🔍 Dataset and Preprocessing

### Q1. What dataset did you use and why?
**A:** I used the California Housing dataset as the Boston Housing dataset is deprecated. It provides data about housing in California and is suitable for regression problems.

### Q2. What does the target variable represent?
**A:** The target variable `PRICE` represents the median house value (in $100,000s) for California districts.

### Q3. How many features and samples are there?
**A:** There are 8 feature variables and 20,640 samples in total.

### Q4. What preprocessing steps did you apply?
**A:** 
- Loaded the dataset using `fetch_california_housing()`
- Converted it into a pandas DataFrame
- Checked for and confirmed that there were no missing values
- Split the data into features (X) and target (y)

## 🤖 Model and Training

### Q5. Which model did you use?
**A:** I used Linear Regression from `sklearn.linear_model`.

### Q6. How did you split the dataset?
**A:** I used an 80-20 train-test split using `train_test_split()`.

### Q7. What metrics did you use to evaluate your model?
**A:** I used **Mean Squared Error (MSE)** to evaluate model performance on both training and testing data.

### Q8. What were the results of your model?
**A:**
- **Training MSE**: 0.5234
- **Testing MSE**: 0.5290

### Q9. Is your model underfitting or overfitting?
**A:** The model is performing similarly on both training and testing data, so it is not overfitting. However, linear regression may not capture complex nonlinear relationships.

## 📊 Visualization and Interpretation

### Q10. What does the scatter plot represent?
**A:** The scatter plot shows the relationship between true and predicted house prices for both training and testing sets. Ideally, the points should lie close to the diagonal.

### Q11. What would you do to improve the model?
**A:**
- Try polynomial or nonlinear models like Random Forest or XGBoost
- Perform feature scaling or transformation
- Analyze residuals and outliers

### Q12. Why did you not use Boston Housing?
**A:** The Boston Housing dataset has been deprecated due to ethical concerns, so we used the California Housing dataset instead.

---

## ✅ Conclusion

The linear regression model shows low and consistent error, indicating a reasonable fit. With further tuning or advanced models, performance could be improved for real-world prediction tasks.

