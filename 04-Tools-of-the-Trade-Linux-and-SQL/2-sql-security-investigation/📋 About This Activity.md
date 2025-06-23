This project presents a **Portfolio Activity** conducted as part of the **Google Cybersecurity Professional Certificate**. The objective was to demonstrate hands-on experience using SQL filters to investigate potential security issues involving login attempts and employee machines. This activity showcases practical database querying skills essential for cybersecurity analysts conducting security investigations.

## 🎯 Scenario

You are a security professional at a large organization investigating security issues to help keep the system secure. Recent discoveries revealed potential security issues involving login attempts and employee machines. Your task is to examine the organization's data in the `employees` and `log_in_attempts` tables, using SQL filters to retrieve records from different datasets and investigate these potential security issues.

## 🔍 Applied Methodology

- **Tool**: SQL database queries with filtering operators
- **Database Tables**: `log_in_attempts` and `employees` tables
- **Operators Used**: AND, OR, NOT, LIKE with wildcards (%)
- **Focus**: Security incident investigation through data analysis

## 📊 Key Findings

### **SQL Investigations Completed:**

**After Hours Security Analysis:**

- Filtered failed login attempts occurring after 18:00 using time-based conditions
- Used `WHERE login_time > '18:00' AND success = 0` to identify suspicious activity

**Specific Date Investigation:**

- Investigated suspicious events on 2022-05-09 and preceding day
- Applied `OR` operator to capture login attempts across multiple dates

**Geographic Filtering:**

- Identified login attempts outside Mexico using `NOT LIKE` with wildcards
- Handled multiple country representations (MEX and MEXICO) in database

**Employee Machine Updates:**

- **Marketing Department (East Building)**: Filtered employees using department and office location
- **Sales and Finance Departments**: Used `OR` operator to target multiple departments
- **Non-IT Employees**: Applied `NOT` operator to exclude Information Technology department

**Advanced Filtering Techniques:**

- `LIKE` with `%` wildcards for pattern matching
- Date and time filtering for temporal analysis
- Multiple condition combinations using logical operators

## 🎯 Analysis Results

Successfully conducted comprehensive security investigations using SQL queries to identify potential threats and target specific employee groups for security updates. The systematic approach demonstrated how database filtering can effectively support cybersecurity investigations and incident response activities.

## 📁 Documentation

- **Portfolio Project**: Complete SQL filtering demonstration for security analysis
- **Query Documentation**: Six different SQL queries with detailed explanations
- **Investigation Results**: Analysis of login patterns and employee data
- **Security Recommendations**: Data-driven insights for security improvements

## 💼 Skills Demonstrated

- SQL query writing and database filtering proficiency
- Security incident investigation through data analysis
- Advanced filtering techniques (AND, OR, NOT, LIKE operators)
- Pattern matching and wildcard usage in SQL
- Date/time filtering for temporal security analysis
- Multi-table database navigation and analysis