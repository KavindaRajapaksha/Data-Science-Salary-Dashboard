### Excel Salary Dashboard Overview  

#### **Introduction**  
This salary dashboard was designed to help job seekers explore compensation trends in data-related roles, ensuring they make informed career decisions. It uses data from my Excel course, focusing on job titles, salaries, locations, and skills, showcasing how Excel can transform raw data into actionable insights.  

---

#### **Dashboard File**  
The final version of the dashboard is saved in **1_Salary_Dashboard.xlsx**.  

---

#### **Excel Skills Utilized**  
Key Excel features applied during the project include:  
- **Charts**: For clear and interactive data visualization.  
- **Formulas and Functions**: To process and analyze salary data.  
- **Data Validation**: To ensure accurate and consistent user inputs.  

---

#### **Data Overview**  
The dataset, derived from real-world 2023 job market data, contains:  
- **Job Titles**: Information on various data-related roles.  
- **Salaries**: Annual averages for different jobs.  
- **Locations**: Country-specific salary data.  
- **Skills**: Essential qualifications for each role.  

---

### Key Dashboard Features  

#### **1. Data Science Job Salaries (Bar Chart)**  
- **Excel Features**: Horizontal bar chart created to compare median salaries.  
- **Design**: Sorted data by descending salary values for readability.  
- **Insights**: Highlights that senior positions and engineering roles typically offer higher salaries compared to analyst roles.  

#### **2. Country Median Salaries (Map Chart)**  
- **Excel Features**: Map chart to display global salary distribution.  
- **Design**: Color-coded regions emphasize salary variations by country.  
- **Insights**: Visualizes salary disparities, spotlighting regions with high and low-paying opportunities.  

---

### Advanced Excel Techniques  

#### **1. Median Salary Calculation (Formula)**  
Formula:  
```excel
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))* 
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```  
- **Purpose**: Calculates the median salary based on job title, country, schedule type, and salary data availability.  
- **Functionality**: Uses **MEDIAN()** with **IF()** to filter data dynamically.  

#### **2. Unique Job Schedule Types (Formula)**  
Formula:  
```excel
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```  
- **Purpose**: Generates a unique, clean list of job schedule types.  
- **Functionality**: Excludes invalid or duplicated entries using **FILTER()**.  

---

### Data Validation  
- **Implementation**:  
  - A filtered list is applied as a validation rule for user inputs like Job Title, Country, and Schedule Type.  
  - This prevents incorrect data entry and enhances dashboard usability.  

---

### **Conclusion**  
The salary dashboard is a comprehensive tool that combines advanced Excel techniques to provide insights into salary trends across job titles and regions. It equips users with the knowledge to assess how location, role, and schedule type impact compensation.  

This project demonstrates how Excel can transform raw data into actionable insights, empowering users to make well-informed career decisions.
