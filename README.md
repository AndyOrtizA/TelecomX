# TelecomX Customer Churn Analysis

## Project Overview
This project analyzes customer churn for TelecomX to identify factors influencing customer attrition and provide insights for retention strategies. The analysis involves data extraction, transformation, exploratory data analysis (EDA), and the generation of insights and recommendations.

## Data Source
The data is sourced from a JSON file hosted on GitHub: `https://raw.githubusercontent.com/ingridcristh/challenge2-data-science-LATAM/main/TelecomX_Data.json`.

## Analysis Steps

1.  **Data Extraction:** The JSON data is loaded into a pandas DataFrame.
2.  **Data Transformation:**
    *   Nested JSON columns ('customer', 'phone', 'internet', 'account') are normalized into a flat DataFrame.
    *   Data types of relevant columns are converted (e.g., to integer, float, boolean).
    *   A new feature 'Cuentas_Diarias' (Daily Charges) is engineered from 'Charges.Monthly'.
    *   Missing values in 'Charges.Total' are handled (e.g., by dropping rows or imputation).
3.  **Exploratory Data Analysis (EDA):**
    *   Descriptive statistics are computed for numerical columns.
    *   The distribution of the target variable 'Churn' is visualized.
    *   The relationship between 'Churn' and categorical variables (e.g., gender, contract type, payment method, internet service) is explored using countplots.
    *   The relationship between 'Churn' and numerical variables (e.g., tenure, monthly charges, total charges, daily charges) is explored using box plots.
4.  **Conclusion and Insights:** Key findings from the EDA are summarized to understand which factors are associated with customer churn.
5.  **Recommendations:** Strategic suggestions are provided based on the insights to help reduce churn.

## Key Findings
*   Customers with month-to-month contracts have a higher churn rate.
*   Electronic check payment method is associated with higher churn.
*   Fiber optic internet service has a higher churn rate.
*   Churned customers tend to have shorter tenures.
*   Churned customers tend to have higher monthly charges but lower total charges.

## How to Reproduce the Analysis
1.  Open the provided Google Colab notebook.
2.  Run the code cells sequentially to perform data extraction, transformation, and EDA.
3.  Review the generated visualizations and the final report within the notebook for detailed findings and recommendations.

## Technologies Used
*   Python
*   pandas
*   numpy
*   matplotlib
*   seaborn
*   requests
