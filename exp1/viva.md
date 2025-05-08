🧠 How to Explain the Code in Viva
🔹 Q: What dataset did you choose and why?
Answer:

I used the Iris dataset which is available in the sklearn.datasets module. It is a classic dataset used for classification tasks and includes 150 flower samples across three species: Setosa, Versicolor, and Virginica. Each sample has four numerical features.

🔹 Q: What libraries did you use and why?
Answer:

I used:

pandas for data handling and analysis,

sklearn.preprocessing for normalization and encoding, and

sklearn.datasets to load the Iris dataset.

🔹 Q: How did you load and view the dataset?
Answer:

I loaded the Iris dataset using load_iris() and converted it into a pandas DataFrame with pd.DataFrame(). Then I added a Species column using category mapping of the target values.

🔹 Q: How did you check the basic structure of the dataset?
Answer:

I used:

df.info() to check data types and non-null counts,

df.describe() to get statistical summary,

df.isnull().sum() to check for missing values, and

df.dtypes to confirm variable types.

🔹 Q: What is Min-Max Normalization and why is it used?
Answer:

It scales all numeric features to a 0–1 range using:

arduino
Copy
Edit
(x - min) / (max - min)
I used MinMaxScaler to normalize the feature columns. It ensures that all features contribute equally to any ML model.

🔹 Q: What is Label Encoding?
Answer:

It converts categorical text values (like species names) into numeric codes using LabelEncoder. For example, setosa → 0, versicolor → 1, virginica → 2.

🔹 Q: What is One-Hot Encoding and how is it different?
Answer:

One-Hot Encoding creates a binary column for each category. It's used to avoid implying any order between categories (unlike label encoding). I used OneHotEncoder from sklearn.

🔹 Q: What is Dummy Encoding?
Answer:

It's like one-hot encoding but drops one of the columns to avoid multicollinearity. I used pd.get_dummies() with drop_first=True.

✅ Expected Viva Questions (With Answers)
Viva Question	Suggested Answer
What is data wrangling?	It's the process of cleaning, structuring, and enriching raw data into a desired format.
What is the Iris dataset?	A famous classification dataset with 150 flower records across 3 species and 4 features.
Why use pandas?	It provides powerful tools for data analysis, like DataFrames, missing value checks, and statistics.
What is the difference between Label Encoding and One-Hot Encoding?	Label encoding assigns a number to each category. One-hot encoding creates binary columns.
Why normalize data?	To ensure all features are on the same scale, improving the performance of ML models.
How did you check for missing values?	Using df.isnull().sum() which returns the count of nulls in each column.
What is .describe() used for?	To get summary statistics like mean, min, max, std, etc., for numeric columns.
How many rows and columns are there in Iris?	150 rows and 5 columns (4 features + 1 species label).
What is categorical data?	Data that represents categories or groups, like species names.
Can One-Hot Encoding be used for numeric data?	No, it's specifically for categorical variables.

