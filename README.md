# Student Performance Analysis

This project looks at data from 1,000 students to figure out what actually affects how well they score in math, reading, and writing. I wanted to see if things like parental education, lunch type, or test preparation made any real difference, and also find out which students might need extra help.

## Dataset

- File: `StudentsPerformance.csv`
- 1,000 rows, 9 columns
- Columns: gender, race/ethnicity, parental level of education, lunch type, test preparation course, math score, reading score, writing score, total score
- No missing values, no duplicates

## Tools Used

- Python (Pandas, NumPy)
- Matplotlib and Seaborn for charts
- Jupyter Notebook

## What I Did

1. Cleaned up the column names, lowercase, underscores instead of spaces.
2. Checked for missing or duplicate data but there wasn't any.
3. Added two new columns like average score, and a performance category(High, Medium, Low).
4. Looked at how parental education, test prep, and gender connect to scores with relations.
5. Checked how closely math, reading, and writing scores relate to each other.
6. Marked students as "at-risk" if they scored below 50 in any subject, then checked what makes a student more likely to fall into that group

## Key Findings

1. Kids whose parents have a master's degree score the highest on average. The lower the parent's education level, the lower the student's average score tends to be.

2. Students who took a test prep course scored about 7-8 points higher on average than those who didn't. So test prep genuinely helps.

3. Reading and writing scores go hand-in-hand almost every time (correlation of 0.95). Math is a bit more independent, so being good at math doesn't automatically mean being good at reading or writing.

4. Girls scored higher overall, especially in reading and writing. Boys scored higher in math. So gender does seem to affect which subjects students are stronger in.

5. About 1 in 5 students (18.8%) are at-risk, meaning they scored below 50 in at least one subject. Two things stood out as reasons why:
   - Students on free/reduced lunch are at-risk almost 3 times more often than students on standard lunch (31% vs 12%).
   - Students who skipped test prep are at-risk more than twice as often as those who took it (24% vs 10%).

## Recommendations

- Make test prep more accessible, maybe free or built into the school day, since it clearly helps.
- Give extra support to students on free/reduced lunch, since they're struggling the most.
- Treat math help separately from reading/writing help, since they don't seem to improve together automatically.

## Most Surprising Finding

The thing that surprised me the most was how big a role lunch type plays. Almost 1 in 3 students on free/reduced lunch are struggling, compared to about 1 in 8 on standard lunch. I expected test prep to be the bigger factor, but it looks like a student's home situation might matter even more than the school resources they use.

## Repository Structure

```
├── StudentsPerformance.csv              # Raw dataset
├── Student_performance_cleaned.csv      # Cleaned dataset with new columns
├── stuperfomance_analysis.ipynb         # Main analysis notebook
└── README.md                            # This file
```

## How to Run

1. Install the required libraries:
   ```
   pip install pandas numpy matplotlib seaborn
   ```
2. Put `StudentsPerformance.csv` in the same folder as the notebook
3. Open and run `studentperfomance_analysis.ipynb` in Jupyter Notebook
