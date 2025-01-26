# Titanic Analysis

This project analyzes the Titanic dataset using Python and provides insights through data exploration and modeling. Below is an overview of the notebook steps:

**Code Example:** `print("Running")`

## DATA LOADING

**Code Example:** `import pandas as pd`

**Code Example:** `df=pd.read_csv("titanic.csv")`

#### SHAPE

**Code Example:** `df.shape`

**Code Example:** `df.head(2)`

**Code Example:** `df.tail(2)`

**Code Example:** `df.sample(2)`

**Code Example:** `df.columns`

**Code Example:** `df.rename(columns={'Survived': 'Alive'}, inplace=True)`

**Code Example:** `df.describe()`

**Code Example:** `df.describe(include="all")`

**Code Example:** `df.info()`

## DATA CLEANING:

### 1. Handling Missing Data

#### Check for missing values

**Code Example:** `df.isnull().sum()`

#### Drop rows with missing values

**Code Example:** `df.dropna(inplace=True)`

#### Drop columns with missing values:

**Code Example:** `df.dropna(axis=1, inplace=True)`

#### Fill missing values with a specific value:

**Code Example:** `df.fillna(value=99, inplace=True)`

#### Replace specific missing values:

**Code Example:** `df["Fare"].fillna(900)`

#### Remove duplicate rows:

**Code Example:** `df.drop_duplicates(inplace=True)`

#### Replacing value

**Code Example:** `df.loc[1, "Fare"]=999`

#### Data Correlation

**Code Example:** `df[['Age','SibSp','Fare']].corr()`

#### ADDING new column

**Code Example:** `df['col'] = 12`

#### DELETING COLUMNS

**Code Example:** `df.drop(['col','Fare'], axis=1,inplace=True)`

#### Deleting Row

**Code Example:** `df.drop(1,inplace=True)`

#### Slicing

**Code Example:** `df[3:5]`

**Code Example:** `df[2:5:9]`

## DATA PREPROCESSING

#### Load the dataset

**Code Example:** `def load_data(file_path):`

#### Handle missing values

**Code Example:** `def handle_missing_values(df, strategy="mean"):`

#### Encode categorical variables

**Code Example:** `def encode_categorical(df):`

#### Feature scaling

**Code Example:** `def scale_features(df):`

#### Preprocessing function

**Code Example:** `def preprocess_data(df, target_column, missing_value_strategy="mean"):`

#### Split data into training and test sets

**Code Example:** `def split_data(X, y, test_size=0.2, random_state=42):`

#### Shuffle the DataFrame

**Code Example:** `df.sample(frac=1).reset_index(drop=True)`

#### DATA ENCODING

**Code Example:** `pd.get_dummies(df, columns=['Age'])`

#### Random Sampling with Replacement

**Code Example:** `bootstrap_sample = df.sample(n=len(df), replace=True)`

## DATA PLOTING:

**Code Example:** `import pandas as pd`

**Code Example:** `df["Fare"].value_counts().plot(kind='bar')`

**Code Example:** `df["Fare"].value_counts().plot(kind='barh')`

**Code Example:** `df["Fare"].value_counts().plot(kind='box')`

**Code Example:** `df["Fare"].value_counts().plot(kind='area')`

**Code Example:** `df["Fare"].value_counts().plot(kind='density')`

**Code Example:** `df["Fare"].value_counts().plot(kind='line')`

**Code Example:** `df["Fare"].value_counts().plot(kind='pie')`

**Code Example:** `df['Fare'].plot(kind='hist', bins=6, title='Sales Distribution', color='c', edgecolor='black')`

## Data Save

**Code Example:** `df.to_excel('data.xlsx', index=False)`

