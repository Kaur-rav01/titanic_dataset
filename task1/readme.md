# Titanic Dataset - Data Preprocessing and Cleaning

This task involves preprocessing the Titanic dataset using Python and Pandas, performed step-by-step in a Jupyter Notebook. The goal is to prepare the data for machine learning by handling missing values, encoding categorical variables, scaling numerical features, and removing outliers.

---

##  Dataset

- **File Name**: `Titanic-Dataset.csv`
- **Source**: Local file path
- **Description**: A dataset containing information about Titanic passengers, used for survival prediction.

---

##  Steps Performed

### 1. Import Dataset and Explore

- Loaded the dataset using `pandas.read_csv()`.
- Explored the first few rows using `.head()`.
- Checked the data types and null values using `.info()` and `.isnull().sum()`.

### 2. Handle Missing Values

- **Age**: Filled missing values with **median** using `fillna()`.
- **Embarked**: Filled missing values with **mode** (most frequent value).
- **Cabin**: Dropped the column due to too many missing values.

### 3. Encode Categorical Features

- Converted the `Sex` column to numeric using `map()` (male: 0, female: 1).
- Used `pd.get_dummies()` for one-hot encoding the `Embarked` column.

### 4. Normalize/Standardize Numerical Features

- Applied **StandardScaler** from scikit-learn to scale `Age` and `Fare` columns to have mean = 0 and standard deviation = 1.

### 5. Visualize and Remove Outliers

- Used **Seaborn boxplots** to visualize outliers in `Age` and `Fare`.
- Created a custom function to remove outliers using the **IQR (Interquartile Range)** method:
  - Removed values outside the range `[Q1 - 1.5*IQR, Q3 + 1.5*IQR]`.

---

##  Tools and Libraries Used

- Python
- Pandas
- NumPy
- Seaborn
- Matplotlib
- Scikit-learn

---

##  Author

Ravjot Kaur  
Email: kaur.rav3001@gmail.com  
LinkedIn: [Ravjot Kaur](https://linkedin.com/in/ravjot-kaur2031)  
GitHub: [Kaur-rav01](https://github.com/Kaur-rav01)

---

