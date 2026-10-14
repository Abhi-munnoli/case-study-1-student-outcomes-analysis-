# 📊 EduPulse Analytics — Student Outcomes Analysis

### Junior Data Analyst Case Study

A Python-based exploratory data analysis project that examines student academic performance, attendance patterns, and pass/fail outcomes using Pandas, Matplotlib, Seaborn, and SciPy.

## 📌 Project Overview

This project analyzes student performance data to understand the distribution of academic marks, examine the relationship between attendance percentage and marks, identify high-performing students, and summarize pass/fail outcomes.

Prepared as a Junior Data Analyst case study for **EduPulse Analytics**, the project demonstrates data cleaning and exploration, statistical analysis, feature engineering, visualization, and insight generation.

## 🎯 Objectives

- Calculate the average and median student marks.
- Identify students scoring above 75 marks.
- Measure the correlation between attendance percentage and marks.
- Create a `Pass` column using the rule `Marks >= 50`.
- Calculate the number and percentage of students who passed and failed.
- Visualize the distribution of marks using a histogram.
- Highlight high-performing students and students who may need additional academic support.
- Present findings and recommendations in a PDF report.

## 🗂️ Project Structure

```text
student-outcomes-analysis/
│
├── README.md
├── Student_Outcomes_Analysis.ipynb
├── student_performance_dataset.csv
├── requirements.txt
│
├── reports/
│   └── student_outcomes_analysis_report.pdf
│
└── images/
    ├── marks_distribution.png
    ├── attendance_vs_marks.png
    └── pass_fail_distribution.png
```

*Note: The images directory is optional. Add these files only after exporting the corresponding charts from your notebook.*

## 📁 Dataset Description

The dataset contains **20 student records** and the following five original columns:

| Column | Description |
|---|---|
| `Student_ID` | Unique student identifier |
| `Name` | Student label or name |
| `Age` | Student age in years |
| `Marks` | Academic marks out of 100 |
| `Attendance_Percentage` | Attendance rate expressed as a percentage |

The `Pass` column is derived during analysis and is not one of the five original CSV columns.

## 🛠️ Technologies Used

- **Python** — Core programming language
- **Pandas** — Data loading, manipulation, and aggregation
- **Matplotlib** — Data visualization
- **Seaborn** — Statistical charts and distribution plots
- **SciPy** — Pearson correlation and statistical significance testing
- **Jupyter Notebook / Google Colab** — Interactive analysis environment

## ⚙️ Analysis Workflow

### 1. Data Loading and Exploration

Load the CSV dataset into a Pandas DataFrame and inspect its structure, columns, and records.

### 2. Average Marks

Calculate the mean of the `Marks` column to summarize overall academic performance.

### 3. High-Performer Analysis

Filter records where:

```python
high_performers = df[df["Marks"] > 75]
```

This identifies students scoring strictly above 75 marks.

### 4. Attendance and Marks Correlation

Calculate the Pearson correlation coefficient between attendance percentage and marks.

```python
correlation = df["Attendance_Percentage"].corr(df["Marks"])
print("Correlation:", correlation)
```

A correlation coefficient indicates the direction and strength of a linear association. Correlation alone does not establish causation.

### 5. Pass/Fail Classification

Apply the specified passing threshold:

```python
df["Pass"] = df["Marks"] >= 50
print(df["Pass"].value_counts())
```

Students with marks of 50 or above are classified as passing; students scoring below 50 are classified as failing.

### 6. Data Visualization

The analysis uses visualizations to examine:

- Distribution of student marks.
- Relationship between attendance percentage and marks.
- Pass/fail outcome counts.
- Student performance comparisons.

## 📈 Key Findings

The accompanying analysis report presents the following results:

| Metric | Result |
|---|---:|
| Students analyzed | 20 |
| Average marks | 74.55 / 100 |
| Median marks | 75.50 / 100 |
| Standard deviation of marks | 18.17 |
| Lowest marks | 45 / 100 |
| Highest marks | 99 / 100 |
| Average attendance | 81.60% |
| Attendance range | 61%–99% |
| Students passed | 18 (90%) |
| Students failed | 2 (10%) |
| Pearson correlation coefficient | -0.524 |
| Two-sided p-value | 0.018 |

### Interpretation

- The cohort achieved an average mark of 74.55.
- Eighteen of the 20 students met the specified passing threshold.
- Marks ranged from 45 to 99, indicating variation in academic performance.
- The observed attendance–marks correlation was moderately negative in this sample.
- The two students below the passing threshold were identified for potential academic follow-up.

**Important:** These findings describe the supplied 20-student sample. The negative correlation does not mean that attendance causes lower marks. A larger dataset and additional contextual variables would be required for stronger conclusions.

## 💡 Recommendations

1. Provide targeted academic support to students who scored below 50.
2. Examine subject-level performance and assessment difficulty before recommending interventions.
3. Investigate additional factors that may be associated with academic achievement.
4. Repeat the analysis over additional assessment cycles to evaluate whether the observed patterns persist.
5. Retain the explicit passing threshold so that outcome counts remain reproducible.

## 🚀 How to Run the Project

### Option 1: Google Colab

1. Open [Google Colab](https://colab.research.google.com/).
2. Upload `Student_Outcomes_Analysis.ipynb`.
3. Upload `student_performance_dataset.csv` when prompted by the notebook.
4. Run the notebook cells sequentially.
5. Review the calculated results and generated visualizations.

### Option 2: Run Locally

**Step 1 — Clone the repository**

```bash
git clone https://github.com/YOUR_USERNAME/student-outcomes-analysis.git
cd student-outcomes-analysis
```

Replace `YOUR_USERNAME` with your GitHub username.

**Step 2 — Create a virtual environment**

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

**Step 3 — Install dependencies**

```bash
pip install -r requirements.txt
```

**Step 4 — Launch Jupyter Notebook**

```bash
jupyter notebook
```

Open `Student_Outcomes_Analysis.ipynb` and run the cells.

**Dataset path:** Ensure the notebook loads `student_performance_dataset.csv` from the repository root when running locally. If the notebook uses Google Colab's `files.upload()`, adapt the dataset-loading cell for local execution.

## 📄 Project Report

The `reports/` directory contains the detailed PDF report with the methodology, statistical findings, charts, recommendations, limitations, and conclusion.

## ⚠️ Limitations

- The analysis contains only 20 student records.
- The data represents a snapshot rather than repeated observations over time.
- Correlation does not demonstrate causation.
- Other factors, including subject difficulty and prior academic performance, are not included.
- The results should not be generalized to a larger student population without further evidence.

## 👨‍💻 Author

**Abhinandan Babu Munnoli**

Aspiring AI & Machine Learning Engineer | Python Developer | Final-Year Computer Science Engineering Student

- GitHub: [Abhi-munnoli](https://github.com/Abhi-munnoli)
- LinkedIn: [Connect on LinkedIn](https://www.linkedin.com/in/abhinandan-munnoli-361a932bb/)

## ⭐ Acknowledgements

This project was developed as a student outcomes analysis case study using the supplied dataset and analysis requirements.

If you find this project useful, consider giving the repository a star.

---

*This project is intended for educational and analytical purposes. Findings should be interpreted within the limitations of the supplied dataset.*
