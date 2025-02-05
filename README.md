import pandas as pd
from sklearn.preprocessing import StandardScaler
import os

# Step 1: Load the dataset
# (Assuming the dataset file "argodatathon2019.csv" has been downloaded from Kaggle
#  and placed in a folder named "Dataset" in the project directory.)
data_path = os.path.join("Dataset", "argodatathon2019.csv")
df = pd.read_csv(data_path)

# Confirming the structure: printing number of rows, columns, and data types
print("Dataset Shape (rows, columns):", df.shape)
print("\nColumns and Data Types:")
print(df.dtypes)

# Step 2: Feature Engineering

# Identify continuous (numeric) and categorical variables
# We assume numeric types (int64, float64) are continuous and 'object' types are categorical.
cont_cols = df.select_dtypes(include=['int64', 'float64']).columns.tolist()
cat_cols = df.select_dtypes(include=['object']).columns.tolist()

# 2a. Normalize/Scale continuous variables
# Scaling helps in bringing all numerical features to a similar range,
# which is crucial for many machine learning algorithms that are sensitive to feature scales.
scaler = StandardScaler()
df[cont_cols] = scaler.fit_transform(df[cont_cols])

# 2b. Encode categorical variables
# Encoding transforms categorical features into numerical format, which is required by most ML models.
# Here we use one-hot encoding (with drop_first to avoid dummy variable trap).
df = pd.get_dummies(df, columns=cat_cols, drop_first=True)

# Step 3: Document the Feature Transformations (via comments)
# - Normalization (StandardScaler): This standardizes continuous variables by removing the mean and scaling to unit variance.
#   It ensures that features contribute equally to the distance computations and helps many models converge faster.
# - One-hot Encoding: Converts categorical variables into binary columns,
#   providing a numerical representation that preserves the categorical distinctions without implying any order.

print("\nProcessed Dataset Shape (after encoding):", df.shape)
df.head()  # Display the first few rows of the transformed dataset

