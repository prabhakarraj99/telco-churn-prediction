# Telco Customer Churn Analysis

**by Prabhakar**

## Project Overview

This project explores and analyzes the Telco Customer Churn dataset to understand customer churn behavior and build a predictive model for customer retention. The analysis involves data preprocessing, exploratory data analysis (EDA), machine learning classification using Random Forest, and answering key business questions through visualizations.

## Dataset

- **Source**: [Kaggle - Telco Customer Churn Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Size**: 7,043 customers with 21 features
- **Target Variable**: Churn (Yes/No)

The dataset includes customer demographics, account information, service subscriptions, and billing details.

## Key Features

- **Customer Demographics**: Gender, Senior Citizen status, Partner, Dependents
- **Account Information**: Tenure, Contract type, Payment method, Billing preferences
- **Services**: Phone service, Internet service type, Online security, Tech support, Streaming services
- **Charges**: Monthly charges, Total charges

## Research Questions Answered

1. **What is the average tenure of customers who have churned vs. those who haven't?**
   - Non-churned customers: ~37.6 months
   - Churned customers: ~18 months
   - Finding: Longer tenure correlates with lower churn probability

2. **What is the churn rate for each Internet Service type?**
   - Fiber optic: 40-45% (highest churn)
   - DSL: ~20%
   - No service: <10% (lowest churn)

3. **Do customers with shorter contract types churn more frequently?**
   - Month-to-Month: 40-45% churn rate
   - One-year: 10-15% churn rate
   - Two-year: <5% churn rate
   - Finding: Contract duration is a strong predictor of churn

4. **What is the average LTV (Lifetime Value) of churned vs. retained customers?**
   - Retained customers have significantly higher LTV
   - Visualization provided via pie chart comparison

5. **Which variable affects LTV the most?**
   - InternetService has the highest impact on LTV
   - Contract type is the second most influential factor
   - Gender and Dependents show minimal impact

## Methodology

### 1. Data Preprocessing
- Removed unnecessary columns (customerID, index column)
- Label encoded categorical features
- Binary encoded target variable (Churn: No=0, Yes=1)
- Split data: 80% training, 20% testing

### 2. Machine Learning Model
- **Algorithm**: Random Forest Classifier
- **Parameters**: 100 estimators, random_state=42
- **Evaluation Metrics**: 
  - Confusion Matrix
  - Classification Report (Precision, Recall, F1-Score)
  - Feature Importance Analysis

### 3. Feature Importance
Identified the most influential features for predicting churn through feature importance visualization.

## Technologies Used

- **Python 3.x**
- **Libraries**:
  - pandas - Data manipulation
  - numpy - Numerical operations
  - matplotlib - Data visualization
  - seaborn - Statistical visualizations
  - scikit-learn - Machine learning (Random Forest, preprocessing, metrics)
  - joblib - Model persistence

## Project Structure

```
Customer-Churn-Analysis/
├── Customer_Churn-prediction-analysis.ipynb   # Main analysis notebook
├── Customer-Churn_Telco_Clean.csv            # Clean dataset
├── README.md                                   # Project documentation
├── LICENSE                                     # MIT License
└── .gitignore                                  # Git ignore rules
```

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/Customer-Churn-Analysis.git
   cd Customer-Churn-Analysis
   ```

2. Install required dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn joblib
   ```

3. Open and run the Jupyter notebook:
   ```bash
   jupyter notebook Customer_Churn-prediction-analysis.ipynb
   ```

## Key Insights

- **Early Retention is Critical**: Customers with tenure less than 18 months are at high risk of churning
- **Contract Type Matters**: Month-to-month contracts have 8-9x higher churn rates than two-year contracts
- **Fiber Optic Challenge**: Fiber optic internet customers churn at 2x the rate of DSL customers
- **InternetService & Contract**: These two factors have the strongest influence on customer lifetime value
- **Actionable Strategy**: Focus retention efforts on month-to-month customers, especially those with fiber optic service in their first 18 months

## Future Enhancements

- Implement additional ML models (XGBoost, Neural Networks) for comparison
- Perform hyperparameter tuning to optimize model performance
- Create an interactive dashboard using Power BI or Tableau
- Develop a real-time churn prediction API
- Integrate customer segmentation analysis

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

**Prabhakar**

Feel free to reach out for any questions or collaboration opportunities!

## Acknowledgments

- Dataset provided by [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- Inspiration from various data science community projects
