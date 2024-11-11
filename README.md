!pip install down

!gdown 1CkUp_wtuauTNL9aOW-K52jDlTXqD4KWS

import pandas as pd
df = pd.read_csv('/Users/bodantodorovski19/PycharmProjects/aaa/diabetes.csv') 

df.columns

import pandas as pd
df = pd.read_csv('/Users/bodantodorovski19/PycharmProjects/aaa/diabetes.csv')

missing_values = df.isnull().sum()

missing_percentage = (missing_values / len(df)) * 100
print(missing_percentage)

--------------------

import missing as mono

mono.matrix(df) prikazuvanje so matrica
plt.show()

import seaborn as sns
import matplotlib.pyplot as plt

# Create a DataFrame with boolean values indicating missing data (True for missing, False for not missing)
missing_data = df.isnull()

# Create a heatmap showing the correlation between missing values in different columns
plt.figure(figsize=(10, 8))
sns.heatmap(missing_data.corr(), annot=True, cmap='coolwarm', fmt='.2f', linewidths=0.5)
plt.title("Correlation Heatmap of Missing Data")
plt.show()

sozdavanje na heatmap


plt.figure(figsize=(10, 8))
sns.heatmap(df.corr(), annot=True, cmap='coolwarm', fmt='.2f', linewidths=0.5)
plt.title("Correlation Heatmap of the Data")
plt.show()

prikazuvanje korelacija so heatmap

msno.dendrogram(df)
plt.show()

-----------------------

df.to_csv('diabetes_cleaned.csv', index=False)  # 'diabetes_cleaned.csv' is the new file name


df_cleaned = pd.read_csv('diabetes_cleaned.csv')

print(df_cleaned.head())

----------------------------------------

import pandas as pd
from sklearn.model_selection import train_test_split

# Load the cleaned dataset
df = pd.read_csv('diabetes_cleaned.csv')  # Replace with your actual cleaned file path

# Verify the columns and the first few rows of the dataset to confirm it's correct
print(df.head())

# Define features (X) and target variable (y)
X = df.drop('Outcome', axis=1)  # All columns except 'Outcome'
y = df['Outcome']  # 'Outcome' is the target variable

# Split the dataset into training (80%) and testing (20%) sets
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Verify the shape of the resulting splits
print(f"X_train shape: {X_train.shape}")
print(f"X_test shape: {X_test.shape}")
print(f"y_train shape: {y_train.shape}")
print(f"y_test shape: {y_test.shape}")


----------------------------------------


