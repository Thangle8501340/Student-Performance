
# Student Performance Analysis

This project analyzes the relationship between various factors such as **Hours Studied** and **Attendance** with students' **Exam Scores**. The project uses both **linear regression** from the `scikit-learn` library and **OLS regression** from the `statsmodels` library to evaluate the strength of these relationships and make predictions.

## Project Structure

The analysis is performed in the following steps:
1. **Data Loading**: The dataset `student_performance.csv` is loaded and processed.
2. **Data Preprocessing**: The features and target variables are extracted, including:
   - `Hours_Studied`: Number of hours a student studied.
   - `Attendance`: Attendance percentage.
   - `Exam_Score`: The score obtained by students in their exams.
3. **Statistical Analysis**: 
   - Ordinary Least Squares (OLS) regression is used to evaluate the relationship between **Hours_Studied** and **Exam_Score**.
   - The OLS summary provides information about the coefficient, R-squared value, and other statistical metrics.
4. **Correlation Analysis**: 
   - A function checks the correlation between features (`Hours_Studied` and `Attendance`) and the target (`Exam_Score`).
5. **Linear Regression (scikit-learn)**:
   - Linear regression models are trained for both `Hours_Studied` and `Attendance` to predict `Exam_Score`.
   - Scatter plots with regression lines are generated to visualize the relationships.
6. **Plotting**: Visualizations include:
   - **Hours Studied vs Exam Scores** (with a regression line).
   - **Attendance vs Exam Scores** (with a regression line).

## Requirements

To run this project, you'll need the following Python libraries:
- `pandas`
- `matplotlib`
- `scikit-learn`
- `statsmodels`

You can install the dependencies by running:
```bash
pip install pandas matplotlib scikit-learn statsmodels
```

## Running the Project

1. Place the dataset `student_performance.csv` in the same directory as the notebook.
2. Run the notebook `student_performance.ipynb` to see the statistical analysis, correlation checks, and linear regression models.
3. Review the generated plots for visual insights on how `Hours_Studied` and `Attendance` correlate with `Exam_Score`.

## Insights

- The **OLS regression** results show that **Hours_Studied** has a statistically significant effect on **Exam_Score**.
- The correlation function reveals how strongly each feature correlates with the target variable.
- Linear regression models provide a straightforward way to predict exam scores based on hours studied and attendance.

## Example Output

```
                            OLS Regression Results                            
==============================================================================
Dep. Variable:             Exam_Score   R-squared:                       0.198
Model:                            OLS   Adj. R-squared:                  0.198
Method:                 Least Squares   F-statistic:                     1635.
Date:                Wed, 09 Oct 2024   Prob (F-statistic):          1.29e-319
No. Observations:                6607   AIC:                         3.524e+04
Df Residuals:                    6605   BIC:                         3.526e+04
Df Model:                           1                                         
Covariance Type:            nonrobust                                         
==============================================================================
                    coef    std err          t      P>|t|      [0.025      0.975]
------------------------------------------------------------------------------
const            61.4570      0.149    411.921      0.000      61.165      61.749
Hours_Studied     0.2893      0.007     40.436      0.000       0.275       0.303
==============================================================================
```

## License

This project is licensed under the MIT License.
