# Data-Science-Salary-Comparison-Dashboard

**To view the dashboard, please <a href="https://app.powerbi.com/view?r=eyJrIjoiZTdlNzExNDktM2RkMi00MzBhLTljYmUtNmQ0Mjc2MzlhNzZlIiwidCI6ImE5ZGQ1OTEwLTZmMTktNDk5My04OGUyLWI0ZGMyZmQyZjhmYSJ9">click here</a>.**


## Overview

This Power BI dashboard provides valuable insights into the salaries of different fields in Data Science from 2020 to 2023. It not only helps you understand trends in the industry but also allows you to customize your search based on the desired country, year, job type (entry-level, mid-level, or senior-level) and employment type (full-time, part-time).

### Dataset Source

The dataset was obtained from Kaggle:
<a href ="https://www.kaggle.com/datasets/arnabchaki/data-science-salaries-2023">Data Science Salaries Dataset</a>

### Data Transformation and Enhancements

Using SQL in MySQL, the dataset was enriched with three additional columns: employee_residence_full, salary_currency_full, and remote_ratio_full. These columns were added to improve data visualization, understandability, and analysis quality.

### SQL Analysis

All analysis and changes in the dataset were done using SQL in MySQL. The SQL code snippets provided in the README file give a clear understanding of the transformations carried out to create the dashboard.

### Power BI Dashboard

The dashboard highlights different aspects of the Data Science industry, such as:

- Salaries of different positions in Data Science, ranked from highest to lowest.
- The ranking of countries based on salaries offered in the field of Data Science.
- A rising trend in salaries between 2020 to 2023.
- A graph comparing the size of companies and the type of jobs (remote, hybrid, and office job) offered by them.
- The percentage of people working in remote, hybrid, and office jobs.

### SQL Code Examples In this section, you can find sample SQL code snippets used for data transformation and analysis: sql

The following SQL code snippets are used to update the `employee_residence_full` and `salary_currency_full` columns in the `ds_salaries` table.

#### Update Employee_Residence_Full

This code updates the `employee_residence_full` column in the `ds_salaries` table based on the `employee_residence` column values:
```
UPDATE ds_salaries
SET employee_residence_full = 
    CASE employee_residence 
        WHEN 'ES' THEN 'Spain'
        WHEN 'CA' THEN 'Canada'
        WHEN 'US' THEN 'United States'
        WHEN 'DE' THEN 'Germany'
        WHEN 'GB' THEN 'United Kingdom'
        WHEN 'NG' THEN 'Nigeria'
        WHEN 'IN' THEN 'India'
        WHEN 'HK' THEN 'Hong Kong'
        WHEN 'PT' THEN 'Portugal'
        WHEN 'NL' THEN 'Netherlands'
        WHEN 'CH' THEN 'Switzerland'
        WHEN 'CF' THEN 'Central African Republic'
        WHEN 'FR' THEN 'France'
        WHEN 'AU' THEN 'Australia'
        WHEN 'FI' THEN 'Finland'
        WHEN 'IE' THEN 'Ireland'
        WHEN 'UA' THEN 'Ukraine'
        WHEN 'IL' THEN 'Israel'
        WHEN 'GH' THEN 'Ghana'
        WHEN 'AT' THEN 'Austria'
        WHEN 'CO' THEN 'Colombia'
        WHEN 'SG' THEN 'Singapore'
        WHEN 'SE' THEN 'Sweden'
        WHEN 'SI' THEN 'Slovenia'
        WHEN 'MX' THEN 'Mexico'
        WHEN 'UZ' THEN 'Uzbekistan'
        WHEN 'BR' THEN 'Brazil'
        WHEN 'TH' THEN 'Thailand'
        WHEN 'HR' THEN 'Croatia'
        WHEN 'PL' THEN 'Poland'
        WHEN 'KW' THEN 'Kuwait'
        WHEN 'VN' THEN 'Vietnam'
        WHEN 'CY' THEN 'Cyprus'
        WHEN 'AR' THEN 'Argentina'
        WHEN 'AM' THEN 'Armenia'
        WHEN 'BA' THEN 'Bosnia and Herzegovina'
        WHEN 'KE' THEN 'Kenya'
        WHEN 'GR' THEN 'Greece'
        WHEN 'MK' THEN 'North Macedonia'
        WHEN 'LV' THEN 'Latvia'
        WHEN 'RO' THEN 'Romania'
        WHEN 'PK' THEN 'Pakistan'
        WHEN 'IT' THEN 'Italy'
        WHEN 'MA' THEN 'Morocco'
        WHEN 'LT' THEN 'Lithuania'
        WHEN 'AS' THEN 'American Samoa'
        WHEN 'HU' THEN 'Hungary'
        WHEN 'SK' THEN 'Slovakia'
        WHEN 'CN' THEN 'China'
        WHEN 'CZ' THEN 'Czech Republic'
        WHEN 'CR' THEN 'Costa Rica'
        WHEN 'TR' THEN 'Turkey'
        WHEN 'CL' THEN 'Chile'
        WHEN 'PR' THEN 'Puerto Rico'
        WHEN 'DK' THEN 'Denmark'
        WHEN 'BO' THEN 'Bolivia'
        WHEN 'PH' THEN 'Philippines'
        WHEN 'DO' THEN 'Dominican Republic'
        WHEN 'BE' THEN 'Belgium'
        WHEN 'EG' THEN 'Egypt'
        WHEN 'ID' THEN 'Indonesia'
        WHEN 'AE' THEN 'United Arab Emirates'
        WHEN 'MY' THEN 'Malaysia'
        WHEN 'JP' THEN 'Japan'
        WHEN 'EE' THEN 'Estonia'
        WHEN 'HN' THEN 'Honduras'
        WHEN 'RU' THEN 'Russia'
        WHEN 'DZ' THEN 'Algeria'
        WHEN 'IQ' THEN 'Iraq'
	    	WHEN 'BG' THEN 'Bulgaria'
	    	WHEN 'JE' THEN 'Jersey'
	    	WHEN 'RS' THEN 'Serbia'
	    	WHEN 'NZ' THEN 'New Zealand'
	    	WHEN 'MD' THEN 'Moldova'
	    	WHEN 'LU' THEN 'Luxembourg'
	    	WHEN 'MT' THEN 'Malta'
	    	ELSE 'Unknown'
        end;
```

#### Update Salary_Currency_Full

This code updates the `salary_currency_full` column in the `ds_salaries` table based on the `salary_currency` column values:
```
UPDATE ds_salaries
SET salary_currency_full = 
    CASE salary_currency
        WHEN 'EUR' THEN 'Euro'
        WHEN 'USD' THEN 'United States Dollar'
        WHEN 'INR' THEN 'Indian Rupee'
        WHEN 'HKD' THEN 'Hong Kong Dollar'
        WHEN 'CHF' THEN 'Swiss Franc'
        WHEN 'GBP' THEN 'Great British Pound'
        WHEN 'AUD' THEN 'Australian Dollar'
        WHEN 'SGD' THEN 'Singapore Dollar'
        WHEN 'CAD' THEN 'Canadian Dollar'
        WHEN 'ILS' THEN 'Israeli New Shekel'
        WHEN 'BRL' THEN 'Brazilian Real'
        WHEN 'THB' THEN 'Thai Baht'
        WHEN 'PLN' THEN 'Polish Zloty'
        WHEN 'HUF' THEN 'Hungarian Forint'
        WHEN 'CZK' THEN 'Czech Koruna'
        WHEN 'DKK' THEN 'Danish Krone'
        WHEN 'JPY' THEN 'Japanese Yen'
        WHEN 'MXN' THEN 'Mexican Peso'
        WHEN 'TRY' THEN 'Turkish Lira'
        WHEN 'CLP' THEN 'Chilean Peso'
        ELSE 'Unknown'
    END;
```

#### Update remote_ratio_full

This code updates the `remote_ratio_full` column in the `ds_salaries` table based on the `remote_ratio` column values:
```
update ds_salaries
set remote_ration_full = case remote_ratio
when 100 then 'remote job'
when 50 then 'hybrid job'
when 0 then 'office job'
else 'office job'
end;
```

### Conclusion

The Data Science Salaries Power BI Dashboard is a useful tool for anyone interested in the field of Data Science, providing important insights on job titles, geographies, and compensation trends across experience levels and employment types. By using this dashboard, users can make well-informed decisions for their career growth and development in the Data Science industry.
