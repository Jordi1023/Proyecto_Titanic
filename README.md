# **Project Description**

This is my first Data Science and Machine Learning project, based on the famous Kaggle challenge: ["Titanic: Machine Learning from Disaster"](https://www.kaggle.com/c/titanic).

The goal is to predict which passengers were most likely to survive the tragic sinking of the Titanic in 1912, using features such as age, sex, ticket class, among others.

## **Objective**

Build a classification model that can accurately predict whether a passenger survived (1) or not (0), applying data cleaning techniques, exploratory analysis, and machine learning.

## **Results Obtained**

- **Model Accuracy:** 79% on the validation set
- **Model Used:** Random Forest Classifier (200 trees)
- **Best Predictors:** Sex, social class (Pclass), and age

## **Technologies and Libraries Used**

- **Python 3.x**
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computations
- **Matplotlib and Seaborn** - Data visualization
- **Scikit-learn** - Machine learning (Random Forest, train/test split, metrics)
- **SciPy** - Statistics (skewness calculation)

## **Analysis Structure**

### **1. Exploratory Data Analysis (EDA)**
- Initial exploration of variables
- Identification of missing values
- Outlier analysis in the Age column using the IQR method
- Distribution visualization (histograms and KDE)

### **2. Data Cleaning and Transformation**

**Age:**
- 11 outliers identified
- Skewness of 0.388 (approximately symmetric distribution)
- Missing values imputed with median (28 years)

**Embarked:**
- 2 missing values imputed with mode

**Cabin:**
- First letter extracted (deck)
- Missing values categorized as 'UNKNOWN' to avoid losing information

### **3. Feature Engineering**
- Conversion of categorical variables to numerical using one-hot encoding:
  - **Sex:** male/female
  - **Embarked:** Q, S, C
  - **Cabin:** A, B, C, D, E, F, G, T, UNKNOWN
- **Final features:** 16 characteristics for the model

### **4. Modeling**
- Data split: 80% training, 20% validation
- Algorithm: **Random Forest Classifier** with 200 trees
- Model training and validation

### **5. Evaluation**
- Metric used: Accuracy
- **Result:** 79% accuracy on validation set

## **Visualizations Included**
- Age box plot (outlier detection)
- Histogram with KDE curve of age distribution
- Visual comparison between mean and median

## **How to Run the Project**

### **Prerequisites**
Have Python 3.x installed along with the following libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn scipy
```
