Improving Linear Regression Using Power Transformer

📖 Overview

This project focuses on improving Linear Regression performance by handling skewed data using PowerTransformer (Yeo-Johnson).
We analyze the data distribution, apply preprocessing, and compare model performance before and after transformation.

📊 Dataset

Name: California Housing Dataset

Source: Scikit-learn

Rows: 20,640

Columns: 9

Target Variable: MedHouseVal

🛠 Tools & Libraries

Python

Pandas, NumPy

Matplotlib, Seaborn

Scikit-learn

⚙️ Steps Followed

1️⃣ Load the dataset
2️⃣ Select numeric features
3️⃣ Replace zero values with 0.001
4️⃣ Check skewness of data
5️⃣ Split into train and test sets
6️⃣ Apply Linear Regression (Before Transformation)
7️⃣ Evaluate using R² and RMSE
8️⃣ Apply PowerTransformer (Yeo-Johnson)
9️⃣ Train model again
🔟 Re-evaluate and compare results

📈 Results
Model	R² Score	RMSE
Before PowerTransformer	0.57	0.74
After PowerTransformer	0.60	0.71

✔ Skewness was reduced
✔ Model performance improved
✔ Data became more normally distributed

🧠 Conclusion

The dataset was highly right-skewed before preprocessing.
After applying PowerTransformer, most features became approximately normally distributed.
This helped Linear Regression perform better, increasing R² and reducing error.

Power transformation is useful when data is highly skewed.
