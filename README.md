# 🎓 Student Performance & Education Analytics

A pure Python Data Analytics project that explores student academic performance, study behavior, attendance, demographics, family background, support systems, and lifestyle factors.

The project focuses on **data cleaning, exploratory data analysis, statistical analysis, KPI development, advanced group analysis, and interactive visualization**.

> **Project scope:** Data Analytics only — no Machine Learning, Power BI, or Tableau.

---

## 📌 Project Overview

The goal of this project is to answer practical education-analytics questions such as:

- What is the overall student performance?
- What percentage of students pass?
- How does study time relate to final grades?
- How are absences associated with academic performance?
- How do previous failures relate to final grades?
- Are there differences across schools or demographic groups?
- How is parental education associated with student outcomes?
- How do school/family support factors compare across groups?
- Which numerical variables have the strongest correlation with final grade?
- What patterns appear when multiple student factors are analyzed together?

---

## 🛠️ Technologies & Libraries

| Technology | Purpose |
|---|---|
| Python | Core programming and analysis |
| Pandas | Data cleaning and data manipulation |
| NumPy | Numerical calculations |
| Matplotlib | Static visualization |
| Seaborn | Statistical visualization |
| Plotly | Interactive visualization |
| SciPy | Statistical testing |
| Jupyter Notebook | Analysis environment |

---

## 📂 Project Structure

```text
student-performance-analytics/
│
├── data/
│   ├── student-mat.csv
│   └── student_performance_cleaned.csv
│
├── notebooks/
│   ├── 01_data_loading.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_eda.ipynb
│   ├── 04_statistical_analysis.ipynb
│   ├── 05_kpi_advanced_analysis.ipynb
│   └── 06_interactive_visualization.ipynb
│
├── analysis_results/
│   ├── kpis.csv
│   ├── performance_summary.csv
│   ├── study_summary.csv
│   ├── absence_summary.csv
│   ├── failure_summary.csv
│   ├── gender_summary.csv
│   ├── school_summary.csv
│   ├── parent_education_summary.csv
│   ├── support_summary.csv
│   └── correlation_with_g3.csv
│
├── visualizations/
│   ├── performance_distribution.html
│   ├── study_time_analysis.html
│   ├── absences_vs_grade.html
│   └── correlation_heatmap.html
│
├── README.md
└── requirements.txt
```

---

# 📊 Analysis Pipeline

```text
Raw Student Data
       ↓
Data Cleaning
       ↓
Exploratory Data Analysis
       ↓
Statistical Analysis
       ↓
KPI & Advanced Analysis
       ↓
Interactive Plotly Visualization
       ↓
Analytical Insights
```

---

# 1️⃣ Data Loading & Understanding

The first notebook establishes the dataset structure and examines:

- Number of records
- Number of variables
- Data types
- Numerical variables
- Categorical variables
- Basic statistical summaries
- Target variable distribution

---

# 2️⃣ Data Cleaning

The cleaning stage includes:

- Missing-value checks
- Duplicate detection
- Data-type inspection
- Unique-value analysis
- Numerical range validation
- Performance-category creation
- Pass/fail classification

### Performance categories

```text
G3 < 10       → Fail
10–13         → Average
14–16         → Good
17–20         → Excellent
```

A cleaned dataset is exported as:

```text
data/student_performance_cleaned.csv
```

---

# 3️⃣ Exploratory Data Analysis

EDA investigates relationships between student characteristics and final grade (`G3`).

### Academic factors

- Study time
- Absences
- Previous failures
- Previous-period grades

### Demographic factors

- Gender
- Age
- School
- Urban/rural address
- Family size

### Family factors

- Mother's education
- Father's education
- Family support

### Other factors

- Internet access
- School support
- Paid classes
- Extracurricular activities
- Free time
- Going out
- Alcohol consumption
- Romantic relationship

---

# 4️⃣ Statistical Analysis

SciPy is used to move beyond visual observations and formally test selected relationships.

### Tests included

#### Pearson Correlation

Used for numerical relationships such as:

```text
Study Time ↔ Final Grade
Absences ↔ Final Grade
Previous Failures ↔ Final Grade
G1 ↔ G3
G2 ↔ G3
```

#### Welch's Independent t-test

Used to compare group means such as:

```text
Gender
Internet Access
School
```

#### One-way ANOVA

Used to compare final-grade means across multiple study-time groups.

### Significance level

```text
α = 0.05
```

Statistical significance is interpreted carefully. A statistically significant association or difference does **not** by itself establish causation.

---

# 5️⃣ KPI & Advanced Analytics

The project calculates key education-performance metrics.

### Core KPIs

- Total students
- Average final grade
- Median final grade
- Highest grade
- Lowest grade
- Grade standard deviation
- Pass rate
- Fail rate
- Average absences
- Excellent-performance rate

### Advanced analysis

- Study-time group performance
- Absence-group performance
- Previous-failure analysis
- School comparison
- Gender comparison
- Family-size comparison
- Parental education analysis
- Support-system analysis
- Lifestyle analysis
- Performance-group profiling

### Cross-analysis

Multiple variables are analyzed together, including:

```text
Study Time × Previous Failures
Absence Group × Study Time
Parent Education × Study Time
```

---

# 6️⃣ Interactive Visualization

Plotly is used to create browser-based interactive visualizations.

### Interactive charts

- Student performance distribution
- Study time vs final grade
- Absences vs final grade
- Previous failures vs performance
- Parent education vs final grade
- School and gender comparison
- Correlation heatmap
- Study time × previous failures
- Performance profile

The exported HTML files can be opened directly in any modern browser.

---

# 📈 Example Analytical Questions

The project is designed to answer questions such as:

### Academic Performance

> What does the overall grade distribution look like?

### Study Behavior

> How do final-grade averages differ across study-time groups?

### Attendance

> How do performance metrics vary across absence groups?

### Previous Performance

> How are previous academic failures associated with current final grades?

### Family Background

> How do outcomes vary across combined parental education levels?

### Support

> How do students receiving school or family support compare with other students?

### Relationships

> Which numerical variables have the strongest correlation with final grade?

---

# 📁 Generated Outputs

The notebooks export reusable CSV summaries into:

```text
analysis_results/
```

and interactive Plotly visualizations into:

```text
visualizations/
```

This keeps the project organized and makes the analysis results easy to reuse in reports or presentations.

---

# ⚠️ Analytical Considerations

This project focuses on **association and description**, not causal inference.

For example:

> If one group has a higher average grade than another, this does not prove that the group characteristic caused the difference.

Similarly:

> A statistically significant correlation does not necessarily mean that one variable causes the other.

The analysis therefore reports observed patterns, group differences, correlations, and statistical evidence without making unsupported causal claims.

---

# 📚 Dataset

This project uses the **Student Performance** dataset from the UCI Machine Learning Repository.

The dataset contains student performance and demographic/social information, including school information, family background, study behavior, absences, and grades.

Dataset:

**UCI Student Performance Dataset**

https://archive.ics.uci.edu/dataset/320/student+performance

---

# 🚀 How to Run the Project

## 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/student-performance-analytics.git
cd student-performance-analytics
```

## 2. Create a virtual environment

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### macOS/Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

## 3. Install dependencies

```bash
pip install -r requirements.txt
```

## 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

## 5. Run the notebooks in order

```text
01_data_loading.ipynb
        ↓
02_data_cleaning.ipynb
        ↓
03_eda.ipynb
        ↓
04_statistical_analysis.ipynb
        ↓
05_kpi_advanced_analysis.ipynb
        ↓
06_interactive_visualization.ipynb
```

Use **Run All** for each notebook.

---

# 🎯 Skills Demonstrated

This project demonstrates practical skills in:

- Python
- Pandas
- NumPy
- Data Cleaning
- Exploratory Data Analysis
- Statistical Analysis
- Hypothesis Testing
- Pearson Correlation
- t-tests
- ANOVA
- KPI Development
- Grouped Analysis
- Cross-tabulation
- Data Aggregation
- Data Visualization
- Seaborn
- Matplotlib
- Plotly
- Interactive HTML Visualization
- Analytical Storytelling

---

# 💼 Resume Description

**Student Performance & Education Analytics**

> Performed end-to-end student performance analysis using Python, Pandas, NumPy, SciPy, Matplotlib, Seaborn, and Plotly; conducted data cleaning, exploratory analysis, hypothesis testing, KPI analysis, correlation analysis, demographic comparisons, and multi-factor analysis, producing interactive visualizations and reusable analytical datasets.

---

# 👨‍💻 Author

**Dev Solanki**

Data Analytics | Python | SQL | Power BI | Machine Learning

GitHub: https://github.com/devsolanki0

---

## ⭐ Project Focus

**Pure Data Analytics**

```text
Python
+
Statistics
+
EDA
+
Visualization
+
Analytical Insights
```

No Machine Learning.  
No Power BI.  
No Tableau.
