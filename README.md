# Data-Science-Salary-Comparison-Dashboard

 This Power BI dashboard on Data Science salaries is immensely useful as it empowers users to make data-driven decisions regarding their careers. By synthesizing complex salary data into a visually appealing and comprehensible format, users can easily identify trends, high-paying positions, and desirable work setups. As an aspiring data professional, leveraging Power BI to create this dashboard highlights your skills in data visualization, business intelligence, and analysis. This project not only showcases your technical proficiency in Power BI but also demonstrates your ability to effectively communicate complex insights, making you a valuable candidate for potential employers in the data-driven job market.

**To view the dashboard, please <a href="https://app.powerbi.com/view?r=eyJrIjoiZTdlNzExNDktM2RkMi00MzBhLTljYmUtNmQ0Mjc2MzlhNzZlIiwidCI6ImE5ZGQ1OTEwLTZmMTktNDk5My04OGUyLWI0ZGMyZmQyZjhmYSJ9">click here</a>.**


## Overview

This Power BI dashboard provides valuable insights into the salaries of different fields in Data Science from 2020 to 2023. It not only helps you understand trends in the industry but also allows you to customize your search based on the desired country, year, job type (entry-level, mid-level, or senior-level) and employment type (full-time, part-time).

### Getting the Dataset

The dataset has been downloaded from Kaggle via the following link:
https://www.kaggle.com/datasets/arnabchaki/data-science-salaries-2023

### Dataset Details

The Data Science Job Salaries Dataset contains 11 columns:

1. work_year: The year the salary was paid.
2. experience_level: The experience level in the job during the year
3. employment_type: The type of employment for the role
4. job_title: The role worked in during the year.
5. salary: The total gross salary amount paid.
6. salary_currency: The currency of the salary paid as an ISO 4217 currency code.
7. salaryinusd: The salary in USD
8. employee_residence: Employee’s primary country of residence in during the work year as an ISO 3166 country code.
9. remote_ratio: The overall amount of work done remotely
10. company_location: The country of the employer’s main office or contracting branch
11. company_size: The median number of people that worked for the company during the year

### Changes made in the Dataset

Three additional columns have been added to the dataset for better visualization:

1. employee_residence_full: This column contains the full form of the country name used in the ‘employee_residence’ column.
2. salary_currency_full: This column contains the full form of the currency name used in the ‘salary_currency’ column.
3. remote_ratio_full: This column contains more readable values for the ‘remote_ratio’ column, replacing 100 with ‘remote’, 50 with ‘hybrid’, and 0 with ‘office job’.

### SQL Analysis

All analysis and changes in the dataset were done using SQL in MySQL. The SQL code snippets provided in the README file give a clear understanding of the transformations carried out to create the dashboard.

### Power BI Dashboard

The dashboard highlights different aspects of the Data Science industry, such as:

- Salaries of different positions in Data Science, ranked from highest to lowest.
- The ranking of countries based on salaries offered in the field of Data Science.
- A rising trend in salaries between 2020 to 2023.
- A graph comparing the size of companies and the type of jobs (remote, hybrid, and office job) offered by them.
- The percentage of people working in remote, hybrid, and office jobs.

### Making Your Life Easier

This Power BI dashboard simplifies complex data and presents it in a visually appealing manner, allowing users to understand trends easily and make informed decisions about their career choices in the Data Science industry.

### Conclusion

The Data Science Salaries Power BI Dashboard is a useful tool for anyone interested in the field of Data Science, providing important insights on job titles, geographies, and compensation trends across experience levels and employment types. By using this dashboard, users can make well-informed decisions for their career growth and development in the Data Science industry.
