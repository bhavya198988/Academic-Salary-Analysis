# Academic Salary Analysis

## Getting Started
### Prerequisites
To run this project, you need:
- Python 3.8 or higher
- Required Python libraries: Pandas, NumPy, Matplotlib, Seaborn

### Installing
Clone this repository:
```bash
git clone https://github.com/bhavya198988/academic-salary-analysis.git
```
Navigate to the project directory:
```bash
cd academic-salary-analysis
```
Install the required dependencies:
```bash
pip install -r requirements.txt
```

## Running the Code
To execute the analysis:
1. Ensure the `Salaries.csv` dataset is in the project directory.
2. Run the Python script:
```bash
python lab55.py
```
The script will generate visualizations and display key insights in the console.

## Key Analyses
### 1. Salary Distribution by Rank
A box plot was created to visualize salary differences across ranks (e.g., Professor, Associate Professor, Assistant Professor).
```python
sns.boxplot(x='rank', y='salary', data=df)
plt.savefig('assets/rank_salary_dist.png')
```

### 2. Gender Representation Analysis
The distribution of salaries by gender was analyzed:
```python
gender_dist = df.sex.value_counts(normalize=True)
print(f"Gender distribution:\n{gender_dist}")
```

### 3. Years of Service vs Salary Correlation
A regression plot was used to analyze the correlation between years of service and salary:
```python
sns.regplot(x='service', y='salary', data=df)
```


## Visualizations
### Histogram of Salaries
```python
plt.hist(df['salary'], bins=10, density=True)
```

### Violin Plot of Salaries
```python
sns.violinplot(x="salary", data=df)
```

### Scatter Plot: Service vs Salary
```python
sns.jointplot(x='service', y='salary', data=df)
```

### Pair Plot for All Variables
```python
sns.pairplot(df)
```

## Tests and Validation
### Breakdown of Tests:
- **Data Cleaning**: Ensured no missing values or invalid entries.
- **Filtering**: Verified filtering logic for subsets (e.g., salaries > $120K).
- **Statistical Analysis**: Validated calculations for mean salaries by discipline.
- **Visualization**: Reviewed plots for accuracy and clarity.

## Deployment
This project is designed to run locally on a Python environment with Jupyter Notebook or as a standalone script (`salary_analysis.py`). No additional deployment steps are required.

## Author
**Bhavya**  
Data Science Student  
GitHub: [https://github.com/bhavya198988](https://github.com/bhavya198988)

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments
Special thanks to our instructor.

