# Reimbursement report using DAX

## Objective
Use Power BI to analyze box office data for a set of movies, create engaging visuals, and extract meaningful insights.

## Dataset
- **Dataset File:** [Employee_reimbursement_dataset.xlsx](https://github.com/Vivek-S1n9h/Reimbursement_report_with_PowerBI/blob/main/Employee_reimbursement_dataset.xlsx)

## Task

1. **Import Data and Open Power Query**
   - Import the data and open the Power Query.

2. **Data Cleaning**
   - Correct spelling and punctuation errors in the expense type column.
   - Make project names uniform.

3. **Handling Missing Values**
   - The Currency column has some missing values. Create a new custom column based on the amount.
   
     ```PowerQuery
     if [Currency] = null and [Amount] >= 1000 then "INR" 
     else if [Currency] = null and [Amount] < 1000 then "USD" 
     else [Currency]
     ```

4. **Normalize Amount Column**
   - Normalize the amount column into INR based on the currency column.

5. **Create Measures**
   - Create a measure to calculate the sum of reimbursed amount in INR.
   - Use the calculate function and check the total reimbursed amount for Project_B.
   - Create a measure to check the count of declined requests.

6. **Create Visuals**
   - Create a slicer visual for the Project and employee.
   - Create a bar chart for employees and reimbursement amount.
   - Create a pie chart for Project vs reimbursement amount.

# PowerBI Report:

![Report](https://github.com/Vivek-S1n9h/Reimbursement_report_with_PowerBI/assets/121023465/3fa4bbc3-1095-4075-89bd-b4d5a34c6b4e)

Feel free to explore and customize further as needed. Happy analyzing!
