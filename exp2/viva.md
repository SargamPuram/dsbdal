✅ Does the Code Satisfy the Question?
✅ Question 1:
Scan for missing values and inconsistencies
✔ Done: You used df.isnull().sum() to identify missing values.

✔ Dealt with it: You used df.dropna() (or ideally fillna() if you correct the column name typo), which is a valid approach.

✅ Question 2:
Scan numeric variables for outliers and treat them
✔ Partially Done: You didn’t check for outliers visually/statistically (like using boxplots or IQR).

✅ You can satisfy this by adding:

python
Copy
Edit
# Boxplot to scan for outliers
sns.boxplot(df["math_score"])
plt.show()
Then, use IQR method if you want to remove them.

✅ Question 3:
Apply data transformation on at least one variable
✔ Done: You applied log transformation:

python
Copy
Edit
df["log_math_score"] = np.log(df["math_score"])
✅ This is a correct transformation to reduce skewness and make distribution closer to normal.

✅ In conclusion:
Your code mostly satisfies the assignment. You should:

Fix the column name typo (math score → math_score)

Mention you used log transformation

Add outlier detection (boxplot or IQR)

🗣️ How to Explain to the Examiner
You can say this:

I created an academic performance dataset using the StudentsPerformance.csv file.
First, I scanned all columns using isnull().sum() and found missing values in the math, reading, and writing scores.
I handled these by either removing them (dropna()) or filling them using the mean of that column.

Then, I checked for outliers using boxplots for numeric columns like math_score.

Finally, I applied a log transformation to the math score to reduce skewness and make it closer to a normal distribution.
This is important for further analysis or statistical modeling.

Optionally, I also added visualizations and performance labels to better understand the dataset.

🎤 Viva Questions and Answers
Q1. What is data wrangling?
A: Data wrangling is the process of cleaning, transforming, and preparing raw data into a usable format for analysis.

Q2. How did you handle missing values in your dataset?
A: I used df.isnull().sum() to identify missing values.
I handled them using dropna() to remove rows or fillna() to replace missing values with the column mean.

Q3. What method did you use to detect outliers?
A: I used boxplots to visually detect outliers.
Optionally, I can also use the IQR method to identify and treat them.

Q4. Why did you apply log transformation?
A: I applied a log transformation to math_score to reduce skewness and make the data distribution more normal, which is useful for statistical analysis and modeling.

Q5. What is skewness?
A: Skewness refers to the asymmetry in a data distribution. A skewed dataset is not symmetrical and can affect the accuracy of models.

Q6. Why is normal distribution important?
A: Many statistical tests assume that data follows a normal distribution.
Normalizing data improves the performance and validity of such tests and models.

Q7. What is the IQR method for detecting outliers?
A: IQR stands for Interquartile Range.
Outliers are values below Q1 - 1.5×IQR or above Q3 + 1.5×IQR.

Q8. How would you scale data if required?
A: I would use standardization (StandardScaler) or normalization (MinMaxScaler) to bring all variables to a similar scale.
