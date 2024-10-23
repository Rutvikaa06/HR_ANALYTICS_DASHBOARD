
# HR Analytics Dashboard

Dashboard Link : https://github.com/Rutvikaa06/HR_ANALYTICS_DASHBOARD/blob/main/README.md

Problem Statement
This dashboard helps organizations understand their employee attrition trends and factors contributing to turnover. It provides insights into the demographics, job roles, and salary ranges most affected by attrition. By analyzing these factors, the organization can develop strategies to reduce turnover and improve employee retention.

The dashboard highlights key metrics such as the attrition rate, average salary, and tenure of employees leaving the organization. Insights into the employees' education, age group, salary range, and department are also provided. This helps HR departments address the root causes of attrition and improve retention strategies, particularly in departments with higher turnover.

### Steps followed
Step 1: Load data into Power BI Desktop from the HR Analytics dataset (CSV file).

Step 2: Open Power Query Editor. In the view tab, under the Data Preview section, enable "Column distribution," "Column quality," and "Column profile."

Step 3: Ensure that column profiling is based on the entire dataset to get an accurate overview of data quality.

Step 4: Analyze the dataset for errors and empty values. No significant issues were found, but some departments had higher attrition than others.

Step 5: Clean the data, ensuring null values in non-critical columns (like age or years of experience) are handled appropriately.

Step 6: In the Report View, apply the selected theme to enhance the visual appeal of the dashboard.

Step 7: Create key metrics, including attrition rate, average age, salary, and tenure using card visuals. These metrics provide an overview of employee demographics and job roles affected by attrition.

Step 8: Add visual filters (slicers) to the report to allow filtering by department, education level, and job role.

Step 9: A pie chart was created to represent attrition by education level, showing the proportion of employees leaving across different education categories.

Step 10: A bar chart was added to represent attrition by age group, allowing HR departments to assess which age brackets are more susceptible to turnover.

Step 11: Add a table visual showing a breakdown of job roles and total employees affected by attrition across departments.

Step 12: Create a line chart visual to depict attrition trends over time. The data reflects attrition rates in each year, showing a decrease over the years.

Step 13: Use calculated fields to analyze salary data, splitting it into various brackets to identify which income ranges are most affected by attrition.
Calculated Column Example:

less
Copy code
Salary Bracket = 
   IF(HRAnalytics[Salary] <= 5000, "Upto 5k", 
   IF(HRAnalytics[Salary] <= 10000, "5k-10k", 
   IF(HRAnalytics[Salary] <= 15000, "10k-15k", "15k+")))
Step 14: A new measure was created to calculate the overall attrition rate for the organization using the following DAX expression:
css
Copy code
Attrition Rate = 
DIVIDE(HRAnalytics[Count of Attrition], HRAnalytics[Count of Employee]) * 100
This percentage is displayed using a card visual on the dashboard.

Step 15: The report was published to Power BI Service, where HR teams can interact with the data, apply filters, and download relevant insights.
Insights
A single-page report was created in Power BI Desktop and then published to Power BI Service.

### Key insights from the dashboard include:

[1] Total Employees = 62
Attrition Count = 12

Attrition Rate = 19.4%

This shows that the overall attrition rate is significant, especially in specific job roles and education categories.

[2] Attrition by Age Group
Employees aged 26-35 have the highest attrition rate, with 8 employees leaving.
Employees aged 18-25 and 36-45 show lower attrition, with 2 employees each.

[3] Attrition by Education
58% of the employees leaving the organization are from the Human Resources department.
17% of the attrition is from employees with a Medical and Technical background.

[4] Attrition by Salary
Most attrition occurs in the lower salary bracket (upto 5k), where 10 employees left.
Employees in the 10k-15k and 5k-10k salary ranges show very low attrition.

[5] Job Role and Department Analysis
Human Resources has the highest attrition rate with 12 employees leaving.
Managerial roles show no attrition, indicating stability in senior roles.

[6] Trend Over Time
Attrition has reduced over the years, with a peak of 1 employee leaving in Year 5 and a gradual decline since.

### 
Conclusion:
The HR department should focus on addressing the concerns of employees in the 26-35 age group, particularly in Human Resources and those earning up to 5k. Retention strategies can be built around providing better benefits, career growth, and improving working conditions for employees in these categories.

Snapshots of the report :
![Screenshot (20)](https://github.com/user-attachments/assets/eaf69756-c182-422e-9c8c-1e4d46573f61)

