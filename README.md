# Customer Churn Analysis ( Power Bi Dashboard )

## Problem Statement

This dashboard helps businesses understand their customer churn better. It identifies the percentage of customers who have churned and the factors contributing to customer churn. Through various visualizations, it provides insights into customer retention and areas that require improvement to reduce churn rates.

### Steps Followed

- Step 1: Load Data
  - Load the dataset (Excel file) into Power BI Desktop.
-  Step 2: Open Power Query Editor
   - In the View tab, under Data Preview section, enable "Column distribution," "Column quality," and "Column profile" options.
   - Select "Column profiling based on the entire dataset."

- Step 3: Data Cleaning and Preparation
   - Handle missing values and errors appropriately. For example, filter out rows where essential data like 'Churn Label' is missing.

- Step 4:Create Calculated Columns and Measures
   ```dax    
    CustomerLost = CALCULATE(COUNTROWS(Telco_Churn), Telco_Churn[Churn Label] = "Yes") 

    TotalCustomers = COUNT(Telco_Churn[CustomerID])

    ChurnRate = DIVIDE([CustomerLost], [TotalCustomers]) * 100

- Step 5:Create Visuals

  - KPI Cards:
    - Card for Total Customers
    - Card for Customer Lost
    - Card for Churn Rate with percentage formatting applied
    - Total monthly charges
  - Bar Chart:
    - To show count of customers by payment method
    - Monthly charges in each cities
  - Coumn Chart:
    - To show Churn Reason vs Cistomers data
  - Pie Chart:
     - Churn rate by contact
  - Donut Chart:
     - Count of customers by churn
     - monthly charges by internet services  
  - Tree Map:
     - Customer churn y paper billing 
  - Map:
     - Churn rate in different cities around the world 
  - Slicers(Filters):
     - Add slicers for fields like 'Payment method', 'Contract Type', 'Gender'
  - Snap of the dashboard
   ![Dashboard_upload](https://github.com/abcdefhgikhushi/Customer-Churn-Power-Bi-Dashboard/issues/1#issue-2378577469)       
