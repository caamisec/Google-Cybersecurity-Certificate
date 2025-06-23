
## Project Description

As part of my cybersecurity certification, I worked on a project to help make my organization's system more secure. My job was to investigate potential security issues and help update employee computers when needed.

In this project, I used SQL queries with different filters to analyze security data. The following examples show how I completed various security-related tasks using SQL to find important information in our database.

---

## Retrieve After Hours Failed Login Attempts

### The Problem

There was a potential security incident that happened after business hours (after 18:00). I needed to investigate all failed login attempts that occurred outside normal working hours to understand what happened.

### My SQL Query

I created this SQL query to find failed login attempts after 18:00:

```sql
SELECT *
FROM log_in_attempts  
WHERE login_time > '18:00' AND success = FALSE;
```

### How It Works

First, I selected all data from the log_in_attempts table using SELECT *. Then I used a WHERE clause with the AND operator to filter my results. I needed two conditions to be true:

- `login_time > '18:00'` - this finds login attempts after 6 PM
- `success = FALSE` - this finds only the failed attempts

The AND operator means both conditions must be true for a record to appear in my results.

### What I Found

This query helped me identify several suspicious login attempts that happened when nobody should have been working, which was important for our security investigation.

---

## Retrieve Login Attempts on Specific Dates

### The Problem

A suspicious event occurred on 2022-05-09. I needed to investigate any login activity that happened on that date or the day before (2022-05-08) to get a complete picture of what might have happened.

### My SQL Query

I wrote this query to find login attempts on both dates:

```sql
SELECT *
FROM log_in_attempts
WHERE login_date = '2022-05-09' OR login_date = '2022-05-08';
```

### How It Works

I started by selecting all data from the log_in_attempts table. Then I used a WHERE clause with the OR operator to filter for login attempts on either date:

- `login_date = '2022-05-09'` - finds logins on May 9th
- `login_date = '2022-05-08'` - finds logins on May 8th

The OR operator means records will show up if either condition is true, so I get results from both days.

### Results

This query returned all login attempts from both days, giving me a complete view of the login activity around the time of the suspicious event.

---

## Retrieve Login Attempts Outside of Mexico

### The Problem

After looking at our login data, I noticed there might be an issue with login attempts coming from outside Mexico. These attempts looked suspicious and needed investigation.

### My SQL Query

I created this query to find login attempts from countries other than Mexico:

```sql
SELECT *
FROM log_in_attempts
WHERE NOT country LIKE 'MEX%';
```

### How It Works

I selected all data from the log_in_attempts table, then used a WHERE clause with NOT to exclude Mexico. I used:

- `NOT` - excludes records that match the condition
- `LIKE 'MEX%'` - matches any country starting with "MEX"
- The `%` symbol means "any characters after MEX"

I used this pattern because our database stores Mexico as both "MEX" and "MEXICO", so the wildcard `%` catches both variations.

### Results

This query showed me all login attempts from countries outside Mexico, helping me identify potentially unauthorized access from unexpected locations.

---

## Retrieve Employees in Marketing Department

### The Problem

My team needed to update computers for employees in the Marketing department who work in the East building. I had to find which employee machines needed the security update.

### My SQL Query

I wrote this query to find Marketing employees in the East building:

```sql
SELECT *
FROM employees
WHERE department = 'Marketing' AND office LIKE 'East%';
```

### How It Works

I selected all employee data, then filtered using two conditions with AND:

- `department = 'Marketing'` - finds Marketing department employees
- `office LIKE 'East%'` - finds offices starting with "East"

I used LIKE with `East%` because the office column contains specific office numbers like "East-170", "East-195", etc. The `%` wildcard matches any characters after "East".

### Results

This query gave me a list of all Marketing employees in East building offices, so I knew exactly which computers needed updates.

---

## Retrieve Employees in Finance or Sales

### The Problem

Employees in both Finance and Sales departments needed a different type of security update. I had to get information about employees in these two departments only.

### My SQL Query

I created this query to find employees in either Finance or Sales:

```sql
SELECT *
FROM employees
WHERE department = 'Finance' OR department = 'Sales';
```

### How It Works

I selected all employee data and used WHERE with OR to find employees in either department:

- `department = 'Finance'` - finds Finance employees
- `department = 'Sales'` - finds Sales employees

I used OR instead of AND because I wanted employees from either department, not employees who somehow work in both departments (which wouldn't make sense).

### Results

This query returned all employees from both Finance and Sales departments, giving me the complete list for the security update.

---

## Retrieve All Employees Not in IT

### The Problem

My team needed to make one final security update for all employees except those in the Information Technology department. IT employees would handle their own updates, so I needed everyone else.

### My SQL Query

I wrote this query to find all non-IT employees:

```sql
SELECT *
FROM employees  
WHERE NOT department = 'Information Technology';
```

### How It Works

I selected all employee data and used WHERE with NOT to exclude the IT department:

- `NOT department = 'Information Technology'` - excludes IT employees
- This returns everyone who doesn't work in IT

The NOT operator is very useful when it's easier to exclude what you don't want rather than list everything you do want.

### Results

This query gave me all employees outside the IT department, so I could complete the security update for the rest of the organization.

---

## Summary

In this project, I successfully used SQL filters to get specific information about login attempts and employee data for security purposes. I worked with two main tables: `log_in_attempts` and `employees`.

**Key SQL operators I used:**

- **AND** - when I needed multiple conditions to be true
- **OR** - when I needed at least one of several conditions to be true
- **NOT** - when I needed to exclude certain results
- **LIKE with %** - when I needed to match patterns in text data

These SQL skills helped me efficiently analyze security data and support my organization's cybersecurity efforts. Being able to filter and query databases is an essential skill for cybersecurity professionals, and this project gave me practical experience with real-world security scenarios.