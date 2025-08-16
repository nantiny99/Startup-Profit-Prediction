# Startup Profit Prediction
This project predicts **startup profits** using regression models and presents the findings through **Python analysis** and an interactive **Power BI dashboard**.

## Dataset
- **Source:** `1000_Companies.csv` from Kaggle
- **Features:**  
  - R&D Spend  
  - Administration  
  - Marketing Spend  
  - State (categorical)  
  - Profit (target variable)  

## Workflow
1. **Data Cleaning**
   - Removed duplicates
   - Filled missing values (numeric: median, categorical: mode)
   - Removed negative/invalid entries
2. **Exploratory Data Analysis (EDA)**
   - Correlation heatmap
   - Scatter plots for predictors vs. Profit
   - Boxplots and distribution analysis
3. **Preprocessing**
   - One-hot encoding for categorical features
   - Feature scaling with StandardScaler
   - Train-test split (80/20)
4. **Modeling**
   - Linear Regression
   - Ridge Regression
   - Lasso Regression
   - Random Forest Regression
5. **Evaluation**
   - Metrics: RMSE, R²
   - Feature importance analysis

## Results
| Model              | R²    | RMSE    |
|--------------------|-------|---------|
| Linear Regression  | 0.98  | 5,059.59 |
| Ridge Regression   | 0.98  | 5,059.59 |
| Lasso Regression   | 0.98  | 5,059.59 |
| Random Forest      | 1.00  | 1,032.91 |

- **Random Forest** performed best (lowest RMSE, highest R²).
- **R&D Spend** was the most important feature (~85% importance).
- State had negligible impact on profit prediction.

## Power BI Dashboard
The Power BI dashboard provides:
- **Overview Page**: KPIs, profit distribution, profit by state
- **Relationships Page**: Scatter plots for each predictor vs. profit
- **Model Performance Page**: RMSE & R² comparison table, feature importance chart

## Tech Stack
- **Python**: pandas, numpy, matplotlib, seaborn, scikit-learn
- **Power BI**: Interactive visualizations and dashboard design
