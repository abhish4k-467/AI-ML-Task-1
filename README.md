# AI-ML-Task-1

## By Abhishek Mitra

|----------------------Elevate Labs AI/ML Intern Task - 1-------------------------|




Task 1: Data Cleaning & Preprocessing

Objective: Learn how to clean and prepare raw data for ML.

Tools: Python, Pandas , Matplotlib/Seaborn , Sci-kit learn



# Titanic Survival Prediction – Data Preprocessing

This project focuses on **data preprocessing and exploratory analysis** of the Titanic dataset from Kaggle. It prepares the dataset for machine learning by cleaning, encoding, scaling, and removing outliers using Python (Pandas, Seaborn, Scikit-learn).

---

## 🧩 Dataset
The dataset contains passenger information used to predict survival on the Titanic. Key features include:
- `Age`, `Fare`, `Pclass`, `Sex`, `SibSp`, `Parch`, and `Embarked`.
- The target variable is `Survived` (0 = No, 1 = Yes).

---

## ✅ Steps Completed

### 1. Data Import & Exploration
- Loaded the dataset and examined null values, data types.

  ![image](https://github.com/user-attachments/assets/4a0c4557-2c74-4f54-ae4c-de65243646a7)
  
- Identified missing values in `Age` and `Embarked`.

  ![image](https://github.com/user-attachments/assets/cd090ce0-f333-421b-a3a9-e58c1b6ac5a9)

  


### 2. Handling Null/Missing Values
- Dropped the `Cabin` column due to excessive missing data.
- Filled `Age` using **median** (recommended for skewed data).
  ![image](https://github.com/user-attachments/assets/1afae2d5-aedd-433a-9f7c-24e8841e428c)

- Filled `Embarked` with **mode** (most common port).
  ![image](https://github.com/user-attachments/assets/d3cb448b-6044-479d-a11c-6d20ebc0f42f)



### 3. Feature Encoding
- Converted `Sex` to binary (0 = male, 1 = female).
- One-hot encoded `Embarked` into `Embarked_Q`, `Embarked_S`.
- Ensured all boolean columns were converted to integers (`0`, `1`).
![image](https://github.com/user-attachments/assets/2dcf70bf-53d9-4a8a-bb3f-d59102028486)


### 4. Feature Scaling
- Standardized `Age` and `Fare` using **StandardScaler**.
- Other columns like `Pclass`, `SibSp`, `Parch` were left unscaled as they are categorical or small integers.
  ![image](https://github.com/user-attachments/assets/4d59b66c-4ac9-498a-a363-993ee9297002)


### 5. Outlier Detection & Removal
- Used **boxplots** to visualize outliers in `Age` and `Fare`.
- Removed extreme outliers based on **z-score filtering** (kept values within ±2.5).
  ![image](https://github.com/user-attachments/assets/2b61234d-d634-430f-8619-20e0dc12cbdf)


---

## 📊 Visualizations
- Histogram to confirm `Age` is right-skewed.
- Boxplots to identify and remove outliers from standardized `Age` and `Fare`.

---

## 📁 Project Structure
dataset_preprocessing/
│
├── data/
│ ├── titanic_unprocessed.csv # Raw dataset
│ └── titanic_processed.csv # Cleaned dataset 
│
├── notebook/
│ └── titanic_preprocessing.ipynb 
│
└── README.md # This file



