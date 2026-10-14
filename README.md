# 📊 Student Outcomes Analysis

### EduPulse Analytics | Junior Data Analyst Case Study

## 📌 Project Overview

Student Outcomes Analysis is a Python-based data analytics project that examines student academic performance, attendance patterns, and pass/fail outcomes using data analysis and visualization techniques.

The project uses Pandas, Matplotlib, Seaborn, and SciPy to explore student marks, calculate statistical measures, analyze the relationship between attendance and marks, and identify students who may require academic support.

## 🎯 Project Objectives

- Calculate the average and median student marks.
- Analyze the correlation between attendance percentage and academic marks.
- Classify students as Pass or Fail using a defined passing threshold.
- Calculate the total number of passing and failing students.
- Visualize the distribution of student marks.
- Identify high-performing students.
- Present meaningful findings and recommendations based on the dataset.

## 🗂️ Project Structure

```text
student-outcomes-analysis/
│
├── README.md
├── Student_Outcomes_Analysis.ipynb
└── student_performance_dataset.csv
```

### File Description

| File | Description |
|---|---|
| `README.md` | Project documentation, objectives, methodology, findings, and setup instructions |
| `Student_Outcomes_Analysis.ipynb` | Jupyter Notebook containing Python code, calculations, and visualizations |
| `student_performance_dataset.csv` | Dataset containing student information, marks, and attendance percentages |

## 📁 Dataset Description

The dataset contains 20 student records with the following original columns:

| Column | Description |
|---|---|
| `Student_ID` | Unique student identifier |
| `Name` | Student name or label |
| `Age` | Student age in years |
| `Marks` | Academic marks out of 100 |
| `Attendance_Percentage` | Student attendance percentage |

A derived `Pass` column is created during analysis using the passing criterion of 50 marks or above.

## 🛠️ Technologies Used

- **Python** — Programming language
- **Pandas** — Data manipulation and analysis
- **Matplotlib** — Data visualization
- **Seaborn** — Statistical visualization
- **SciPy** — Statistical analysis
- **Jupyter Notebook** — Interactive coding and analysis

## ⚙️ Project Workflow

### 1. Data Loading and Exploration

Load the CSV dataset into a Pandas DataFrame and examine the records and column structure.

### 2. Statistical Analysis

Calculate the average marks, median marks, standard deviation, minimum marks, maximum marks, and average attendance.

### 3. Pass/Fail Classification

Classify students according to the following rule:

```python
df["Pass"] = df["Marks"] >= 50
```

Students scoring 50 or above pass, while students scoring below 50 fail.

### 4. Attendance and Marks Correlation

Use Pearson correlation to investigate the linear relationship between attendance percentage and marks.

```python
from scipy.stats import pearsonr

correlation, p_value = pearsonr(
    df["Attendance_Percentage"],
    df["Marks"]
)

print("Correlation:", correlation)
print("P-value:", p_value)
```

### 5. Data Visualization

Create visualizations to understand:

- Distribution of student marks.
- Relationship between attendance and marks.
- Pass/fail outcome counts.
- Comparisons of individual student performance.

## 📈 Key Findings

According to the accompanying analysis results:

| Metric | Result |
|---|---:|
| Total students analyzed | 20 |
| Average marks | 74.55 / 100 |
| Median marks | 75.50 / 100 |
| Standard deviation | 18.17 |
| Lowest marks | 45 / 100 |
| Highest marks | 99 / 100 |
| Average attendance | 81.60% |
| Attendance range | 61%–99% |
| Students passed | 18 |
| Students failed | 2 |
| Pass percentage | 90% |
| Fail percentage | 10% |
| Pearson correlation | -0.524 |
| Two-sided p-value | 0.018 |

### Key Observations

- The average student mark was 74.55 out of 100.
- Eighteen out of 20 students passed the assessment.
- Student marks ranged from 45 to 99, indicating variation in performance.
- Attendance and marks showed a moderate negative linear correlation in this sample.
- Two students scored below the defined passing threshold and may benefit from further academic assessment.

**Note:** The observed negative correlation does not establish that attendance causes lower marks. The analysis covers only 20 students, so its findings should not be generalized without further investigation.

## 💡 Recommendations

1. Provide targeted academic support to students scoring below 50.
2. Investigate subject difficulty and assessment performance before recommending interventions.
3. Consider additional factors, such as prior academic performance and learning support.
4. Analyze more student records to improve the reliability of findings.
5. Repeat the analysis across additional assessment periods to identify persistent patterns.

## 🚀 How to Run the Project

### Option 1: Google Colab

1. Open [Google Colab](https://colab.research.google.com/).
2. Upload `Student_Outcomes_Analysis.ipynb`.
3. Upload `student_performance_dataset.csv` when required by the notebook.
4. Execute the cells sequentially.
5. Review the statistical results and visualizations.

### Option 2: Run Locally

**Step 1: Clone the repository**

```bash
git clone https://github.com/YOUR_USERNAME/student-outcomes-analysis.git
```

Replace `YOUR_USERNAME` with your GitHub username.

**Step 2: Enter the project directory**

```bash
cd student-outcomes-analysis
```

**Step 3: Install the required libraries**

```bash
pip install pandas matplotlib seaborn scipy jupyter
```

**Step 4: Launch Jupyter Notebook**

```bash
jupyter notebook
```

Open `Student_Outcomes_Analysis.ipynb` and execute the notebook cells.

**Important:** Ensure the notebook reads `student_performance_dataset.csv` from the project directory when running locally. If the notebook uses Google Colab upload commands, adjust the data-loading cell accordingly.

## ⚠️ Limitations

- The dataset contains only 20 student records.
- The data represents a single snapshot of student outcomes.
- Correlation does not imply causation.
- Additional information about subjects, assessment difficulty, and previous performance is unavailable.
- Findings are limited to the supplied dataset.

## 🏁 Conclusion

The analysis provides an overview of student academic outcomes using statistical calculations and visualizations. Although 90% of the students met the defined passing criterion, the variation in marks and the two failing outcomes indicate opportunities for further academic investigation.

The project demonstrates practical skills in Python programming, exploratory data analysis, statistical interpretation, and data visualization.

## 👨‍💻 Author

**Abhinandan Babu Munnoli**

Aspiring AI & Machine Learning Engineer | Python Developer | Final-Year Computer Science Engineering Student

- **GitHub:** [Abhi-munnoli](https://github.com/Abhi-munnoli)
- **LinkedIn:** [Connect with me](https://www.linkedin.com/in/abhinandan-munnoli-361a932bb/)

---

⭐ If you find this project useful, consider starring the repository.

*Developed for educational and data analytics purposes.*
