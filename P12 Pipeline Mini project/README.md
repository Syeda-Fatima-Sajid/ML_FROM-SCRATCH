(Insurance Dataset Analysis & Modeling)
📌 Dataset Overview

In this project, we worked with an insurance dataset containing 1338 records and 7 columns.
The dataset includes information about individuals such as:

Age

Sex

BMI (Body Mass Index)

Number of Children

Smoking Status

Region

Medical Charges (Target Variable)

The main objective of this dataset is to analyze and predict medical insurance charges based on personal and lifestyle factors.

📊 Data Understanding & Exploration

To understand the dataset, we first performed Exploratory Data Analysis (EDA) using:

Pandas functions

YData Profiling

Statistical summaries

Correlation analysis

Skewness check

From the analysis, we observed:

There were no missing values, so no imputation was required.

No duplicate records were found.

The target variable charges was right-skewed (skewness ≈ 1.51), which means most people have lower charges, while a few have very high medical costs.

Correlation analysis showed that:

Age and BMI have a moderate positive correlation with charges.

Smoking status is one of the most important factors affecting insurance cost.

Other variables have weaker correlations.

These insights helped us understand which features influence medical expenses the most.

⚙️ Data Preprocessing & Feature Engineering

To prepare the data for machine learning, we used proper preprocessing techniques:

1️⃣ ColumnTransformer

We separated features into:

Numerical features → age, bmi, children

Categorical features → sex, smoker, region

Then:

Numerical features were scaled using StandardScaler.

Categorical features were encoded using OneHotEncoder.

This ensured that all features were in a suitable format for modeling.

2️⃣ Pipeline

We built a complete Machine Learning Pipeline that included:

Data preprocessing

Feature transformation

Model training

This allowed us to perform all steps automatically and avoided data leakage.

3️⃣ FunctionTransformer

We used FunctionTransformer to:

Analyze feature distributions

Apply log transformation to reduce skewness in the target variable

Log transformation was applied to make the data more normally distributed and to test its effect on model performance.

🤖 Model Building & Evaluation

We trained a regression model using the pipeline and evaluated it using:

R² Score

RMSE (Root Mean Squared Error)

Results (Without Log Transform):

R² Score: ~ 0.78

RMSE: ~ 5796

This shows that the model explains around 78% of the variance in medical charges, which is a good performance for a basic regression model.

Results (With Log Transform):

R² Score: ~ 0.60

RMSE: ~ 7814

After applying log transformation, the model performance decreased. This indicates that, for this dataset, log transformation did not improve predictions.

📈 Key Insights from the Project

From this project, we learned that:

Smoking status has a major impact on insurance charges.

Older people and individuals with higher BMI tend to have higher medical expenses.

The dataset is clean and well-structured, making it suitable for machine learning.

Proper preprocessing using pipelines improves reliability and reproducibility.

Log transformation is not always beneficial and should be tested before final use.

🎯 Final Conclusion

In this project, we successfully implemented a complete machine learning workflow, starting from data understanding to model evaluation. We applied modern preprocessing techniques using ColumnTransformer, Pipeline, and FunctionTransformer, ensuring a clean and efficient process.

The model achieved good performance without complex tuning, showing that even simple models can provide meaningful insights when proper preprocessing is applied.

Most importantly, this project helped in gaining practical experience with real-world machine learning pipelines and strengthened the understanding of core concepts such as feature scaling, encoding, distribution analysis, and model evaluation.
