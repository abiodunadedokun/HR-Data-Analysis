

# Human Resources (HR) Exploratory Data Analysis.

[HR.Data.csv](https://github.com/user-attachments/files/17042874/HR.Data.csv)
[hr_report.pdf](https://github.com/user-attachments/files/17042873/hr_report.pdf)
[HR Data.csv](https://github.com/user-attachments/files/17042872/HR.Data.csv)
[Percentage_Hire_Change.csv](https://github.com/user-attachments/files/17042871/Percentage_Hire_Change.csv)
[State distribution.csv](https://github.com/user-attachments/files/17042869/State.distribution.csv)
[age group distribution by gender.csv](https://github.com/user-attachments/files/17042868/age.group.distribution.by.gender.csv)
[employee_hire_count.csv](https://github.com/user-attachments/files/17042867/employee_hire_count.csv)
[employee_state_distribution.csv](https://github.com/user-attachments/files/17042866/employee_state_distribution.csv)
[hr_query.pdf](https://github.com/user-attachments/files/17042865/hr_query.pdf)
[job_title_distribution.csv](https://github.com/user-attachments/files/17042864/job_title_distribution.csv)
[remote_employees.csv](https://github.com/user-attachments/files/17042863/remote_employees.csv)
[tenure_department.csv](https://github.com/user-attachments/files/17042862/tenure_department.csv)
[turnover rate.csv](https://github.com/user-attachments/files/17042861/turnover.rate.csv)


### 1. **Introduction**

This project provides an in-depth exploration of human resources data using SQL for analysis and Power BI for dynamic visualizations. It uncovers critical insights into key HR metrics such as employee turnover, diversity, recruitment efficiency, and performance evaluations. By creating interactive dashboards, the analysis equips HR professionals with the tools to make data-driven decisions and formulate strategic workforce planning initiatives. These insights are crucial for enhancing organizational effectiveness, optimizing talent management, and driving informed business strategies. This report covers the entire process, from **dataset cleaning** to **visualization, reporting, and deriving key indicators**.

#### Tool
      MS SQL SERVER 2022 and MS POWER BI

### 2. **Dataset Overview** [HR Data.csv](https://github.com/user-attachments/files/17043154/HR.Data.csv)

The dataset includes the following key attributes:

- **Employee Information**: Employee ID, Name, Age, Gender, Department, and Position.
- **Employment Dates**: Hire date, End date (if applicable), and Tenure.
- **Performance Metrics**: Performance rating, Promotions, and Salary changes over time.
- **HR Metrics**: Employee turnover status, Diversity metrics, and Recruitment effectiveness.
- **Compensation and Benefits**: Salary, Bonus, and Benefits packages.
- **Other Information**: Training completion, Employee satisfaction score, and Office location (remote or on-site).

### 3. **Data Cleaning Process**

Before conducting the analysis, it was crucial to clean and prepare the dataset. Here are the key steps involved in the data-cleaning process:

#### a. **Handling Missing Values**
   - Missing values were identified in fields such as employee tenure, performance ratings, and salary.
   - For numeric fields (like tenure and salary), missing values were imputed using the median to maintain the integrity of the data distribution.
   - Categorical fields (such as department or job title) were assigned a default category, such as "Unknown," to prevent information loss.

#### b. **Removing Duplicates**
   - Identified and removed duplicate employee records to ensure unique entries for each employee.
   - Ensured no repeated entries for the same employee over time unless they represented valid data (e.g., rehire after a break).

#### c. **Correcting Data Types**
   - Ensured that date fields (hire date, end date) were formatted correctly as `DateTime`.
   - Converted numerical fields like salary, bonuses, and performance scores to their appropriate data types for accurate calculations.

#### d. **Dealing with Outliers**
   - Outliers in salary and performance scores were examined using interquartile range (IQR) methods.
   - Extreme values, such as abnormally high bonuses or unusually low-performance scores, were reviewed and handled to avoid skewing the analysis.

#### e. **Standardizing Formats**
   - Standardized department names, job titles, and other categorical fields to maintain consistency in grouping and reporting.
   - Ensured consistent formatting of text fields like employee names and job titles to avoid issues during aggregation and analysis.
---

### 4. **Data Visualization and Reporting** [hr_report.pdf](https://github.com/user-attachments/files/17043831/hr_report.pdf)

![hr_report_page-0001 1](https://github.com/user-attachments/assets/a8f2aeb1-1aab-46a3-bcbd-5e96891562b6)
![hr_report_page-0002 1](https://github.com/user-attachments/assets/a30ae77f-f0db-4df1-a515-7625f5ed9be7)



Questions:
1.  What is the age distribution in the company?
2.  What is the gender breakdown in the company?
3.  How does gender vary across departments and job titles?
4.  What is the race distribution in the company?
5.  What is the average length of employment in the company?
6.  Which department has the highest turnover rate?
7.  What is the tenure distribution for each department?
8.  How many employees work remotely for each department?
9.  What is the distribution of employees across different states?
10. How are job titles distributed in the company?
11. How have employee hire counts varied over time?
    
Results:
Demographic and Employment Insights:

1.  The company has a higher number of male employees compared to female or non-conforming individuals.
2.  Gender distribution is relatively even across departments, although there is a slight overall prevalence of male employees.
3.  The 21-30 age group has the fewest employees, with the majority falling within the 31-50 age range. Surprisingly, the 50-and-over 
    age group constitutes the largest segment of the workforce.
4.  Most employees are of Caucasian ethnicity, followed by mixed race, black, Asian, Hispanic, and Native American backgrounds.
5.  On average, employees have a tenure of 7 years with the company.
6.  Auditing experiences the highest turnover rate, followed by Legal, Research & Development, and Training. Business Development & 
    Marketing exhibits the lowest turnover rates.
7.  Employee tenure is typically 6-8 years, with a fairly even distribution across departments.
8.  Approximately 25% of employees work remotely.
9.  Ohio has the highest employee concentration (14,788), followed by Pennsylvania (930), Illinois (730), Indiana (572), Michigan 
   (569), Kentucky (375), and Wisconsin (321).
10. The company boasts 182 job titles, with Research Assistant II having the highest count (634). In contrast, positions l 
    like Assistant Professor, Marketing Manager, Office Assistant IV, Associate Professor, and VP of Training and Development each 
    have only one employee.
11. Over the years, there has been an increase in employee hiring counts.
