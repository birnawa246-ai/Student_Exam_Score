# 📊 Student Performance Data Analysis

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on student performance data using Python. The analysis focuses on understanding student demographics and examining how factors such as **parental education** and **ethnic group** relate to students' academic performance.

The project uses **Pandas** for data analysis and cleaning, and **Matplotlib** and **Seaborn** for data visualization.

---

## 🎯 Objectives

The main objectives of this project are:

* Analyze the student performance dataset.
* Understand the distribution of students by gender.
* Examine the relationship between parental education and student scores.
* Analyze the distribution of students across ethnic groups.
* Identify patterns and trends in Math, Reading, and Writing scores.
* Create visualizations to make the analysis easier to understand.

---

## 🛠️ Technologies Used

* **Python**
* **NumPy**
* **Pandas**
* **Matplotlib**
* **Seaborn**
* **Jupyter Notebook**

---

## 📂 Project Structure

```text
Student-Performance-Analysis/
│
├── Shubham.ipynb
├── Expanded_data_with_more_features.csv
└── README.md
```

---

## 📊 Dataset

The project uses:

`Expanded_data_with_more_features.csv`

The dataset contains student-related information including:

* Gender
* Ethnic Group
* Parental Education
* Math Score
* Reading Score
* Writing Score

---

## 🔍 Analysis Performed

### 1. Data Loading

The dataset is loaded using Pandas:

```python
df = pd.read_csv("Expanded_data_with_more_features.csv")
```

### 2. Data Exploration

Basic information about the dataset is examined using:

```python
df.describe()
df.info()
df.isnull().sum()
```

This helps understand the dataset structure, numerical statistics, data types, and missing values.

### 3. Data Cleaning

The unnecessary `Unnamed: 0` column is removed:

```python
df = df.drop("Unnamed: 0", axis=1)
```

### 4. Gender Distribution

A count plot is created to visualize the number of students in each gender category.

```python
sns.countplot(data=df, x="Gender")
```

### 5. Parental Education Analysis

The project groups students according to their parents' education level and calculates the average:

* Math Score
* Reading Score
* Writing Score

```python
gb = df.groupby("ParentEduc").agg({
    "MathScore": "mean",
    "ReadingScore": "mean",
    "WritingScore": "mean"
})
```

A heatmap is then used to visualize these average scores.

### 6. Ethnic Group Analysis

The project identifies the different ethnic groups present in the dataset and analyzes their distribution.

A pie chart and count plot are used to visualize the number of students in each group.

---

## 📈 Visualizations

The notebook includes visualizations such as:

* Gender Distribution
* Average Scores by Parental Education
* Parental Education Heatmap
* Ethnic Group Distribution
* Ethnic Group Count Plot

---

## 💡 Key Findings

Based on the analysis performed in the notebook:

* Student distribution can be examined across different gender categories.
* Parental education levels show differences in the average Math, Reading, and Writing scores.
* The dataset contains multiple ethnic groups with different numbers of students.
* Visualization makes it easier to identify patterns in student performance.

## 📌 Future Improvements

The project can be extended by adding:

*Correlation analysis between subjects.
* Gender vs academic performance analysis.
* Test preparation analysis.
* Lunch and parental education analysis.
* Interactive dashboards using **Power BI**.
* SQL-based data analysis.
* More advanced statistical analysis.
* Machine Learning models for predicting student performance.

---
### Skills Used

`Python` • `Pandas` • `NumPy` • `Matplotlib` • `Seaborn` • `Data Analysis` • `Data Visualization`

---

## ⭐ Project Purpose

This project was created as a **Data Analysis / Exploratory Data Analysis project** to practice Python-based data cleaning, analysis, grouping, and visualization.

## 👨‍💻 Author
**Shubham Maurya**
🎓 Computer Science Engineering Student
