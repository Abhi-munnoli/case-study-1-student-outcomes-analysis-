# 📊 EduPulse Analytics — Student Outcomes Analysis

### Junior Data Analyst Case Study

A data analytics project focused on student academic performance, attendance patterns, and pass/fail outcomes using Python and data visualization libraries.

## 📌 Project Overview

This project analyzes student performance data to identify academic trends, examine the relationship between attendance and marks, calculate pass/fail statistics, and visualize student outcomes.

The analysis uses Python libraries to transform the dataset into meaningful statistical insights and actionable recommendations.

## 🎯 Project Objectives

- Calculate the average and median student marks.
- Analyze the correlation between attendance percentage and marks.
- Classify students as Pass or Fail using a threshold of 50 marks.
- Calculate the number and percentage of passing and failing students.
- Visualize the distribution of student marks.
- Identify high-performing students.
- Highlight students who may require additional academic support.

## 🗂️ Project Structure

```text
student-outcomes-analysis/
│
├── README.md
├── Student_Outcomes_Analysis.ipynb
├── student_performance_dataset.csv
└── student_outcomes_analysis_report.pdf
```

## 📁 Dataset Description

The dataset contains 20 student records with the following original columns:

| Column | Description |
|---|---|
| `Student_ID` | Unique student identifier |
| `Name` | Student name or label |
| `Age` | Student age in years |
| `Marks` | Academic marks out of 100 |
| `Attendance_Percentage` | Student attendance percentage |

A derived `Pass` column is created during the analysis.

## 🛠️ Technologies Used

- **Python** — Programming language
- **Pandas** — Data manipulation and analysis
- **Matplotlib** — Data visualization
- **Seaborn** — Statistical visualization
- **SciPy** — Statistical analysis
- **Jupyter Notebook / Google Colab** — Interactive development environment

## ⚙️ Analysis Performed

### 1. Data Loading and Exploration

Loaded the CSV dataset into a Pandas DataFrame and examined the student records.

### 2. Average Marks Calculation

Calculated the mean and median to understand overall academic performance.

### 3. Attendance and Marks Correlation

Used Pearson correlation analysis to investigate the linear association between attendance percentage and academic marks.

### 4. Pass/Fail Classification

Applied the following passing rule:

```python
df["Pass"] = df["Marks"] >= 50
```

Students scoring 50 or above are classified as Pass, while those scoring below 50 are classified as Fail.

### 5. Data Visualization

Created visualizations to explore:

- Distribution of student marks.
- Attendance percentage versus marks.
- Pass/fail outcome counts.
- Comparative student performance.

## 📈 Key Findings

The following results are reported in the accompanying PDF analysis report.

| Metric | Result |
|---|---:|
| Total students analyzed | 20 |
| Average marks | 74.55 |
| Median marks | 75.50 |
| Standard deviation | 18.17 |
| Lowest marks | 45 |
| Highest marks | 99 |
| Average attendance | 81.60% |
| Attendance range | 61%–99% |
| Students passed | 18 |
| Students failed | 2 |
| Pass percentage | 90% |
| Fail percentage | 10% |
| Pearson correlation coefficient | -0.524 |
| Two-sided p-value | 0.018 |

### Key Observations

- The average student mark was 74.55 out of 100.
- Eighteen students passed under the defined threshold.
- Two students scored below 50 marks and may benefit from additional academic support.
- The observed attendance–marks correlation was moderately negative in this sample.
- The marks distribution indicates differences in academic performance across the students.

**Note:** Correlation does not establish causation. These findings apply only to the supplied 20-student dataset and should not be generalized without further analysis.

## 💡 Recommendations

1. Provide targeted academic support to students scoring below the passing threshold.
2. Investigate subject difficulty, assessment methods, and prior academic performance.
3. Analyze additional student records to improve the reliability of findings.
4. Repeat the analysis across multiple assessment periods to identify trends.
5. Maintain a consistent passing threshold to ensure reproducible reporting.

## 🚀 How to Run the Project

### Option 1: Google Colab

1. Download or open `Student_Outcomes_Analysis.ipynb`.
2. Visit [Google Colab](https://colab.research.google.com/).
3. Upload the notebook.
4. Upload `student_performance_dataset.csv` when requested by the notebook.
5. Execute the cells sequentially.
6. Review the analysis results and visualizations.

### Option 2: Run Locally

**Step 1: Clone the repository**

```bash
git clone https://github.com/YOUR_USERNAME/student-outcomes-analysis.git
```

**Step 2: Navigate to the project directory**

```bash
cd student-outcomes-analysis
```

**Step 3: Install the required libraries**

```bash
pip install pandas matplotlib seaborn scipy jupyter
```

**Step 4: Start Jupyter Notebook**

```bash
jupyter notebook
```

Open `Student_Outcomes_Analysis.ipynb` and execute the notebook cells.

Ensure the notebook reads `student_performance_dataset.csv` from the project directory when running locally.

## 📄 Project Report

The `student_outcomes_analysis_report.pdf` file contains the detailed report, including:

- Introduction and objectives.
- Dataset description.
- Python analysis code.
- Summary statistics.
- Pass/fail analysis.
- Data visualizations.
- Key findings and recommendations.
- Limitations and conclusion.

## ⚠️ Limitations

- The analysis includes only 20 student records.
- The dataset represents a single snapshot of student outcomes.
- Correlation does not establish a causal relationship.
- Other factors influencing academic performance are not included.
- Additional data is needed to validate whether the observed patterns persist.

## 🏁 Conclusion

The analysis shows an average mark of 74.55 and a pass rate of 90% among the 20 students studied. Although the overall results are encouraging, variation in marks and two below-threshold outcomes indicate opportunities for targeted academic support.

The observed negative attendance–marks correlation requires further investigation before drawing broader conclusions.

## 👨‍💻 Author

**Abhinandan Babu Munnoli**

Aspiring AI & Machine Learning Engineer | Python Developer | Final-Year Computer Science Engineering Student

- **GitHub:** [Abhi-munnoli](https://github.com/Abhi-munnoli)
- **LinkedIn:** [Connect with me](https://www.linkedin.com/in/abhinandan-munnoli-361a932bb/)

---

⭐ If you find this project useful, consider giving the repository a star.

*Developed for educational purposes as a student outcomes data analysis case study.*
