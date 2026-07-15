# Project Description

In this project, I used SQL queries to investigate potential security incidents involving employee login attempts and workstation management. By applying filtering techniques with operators such as `AND`, `OR`, `NOT`, and `LIKE`, I retrieved relevant records from the `log_in_attempts` and `employees` tables. These queries helped identify suspicious login activity and locate employee systems that required security updates.

---
# Apply Filters to SQL Queries

## Project Description

This project demonstrates how SQL filtering techniques can be used to investigate potential security incidents. Using the `log_in_attempts` and `employees` tables, I created SQL queries to identify suspicious login activity, analyze failed login attempts, and retrieve records based on specific dates and locations.

The project highlights the use of SQL operators such as `AND`, `OR`, `NOT`, and `LIKE` to efficiently filter security-related data.

---

## Objectives

- Investigate failed login attempts after business hours.
- Retrieve login attempts from specific dates.
- Identify login attempts originating outside Mexico.
- Practice SQL filtering techniques used in cybersecurity investigations.

---

## Scenario

As a cybersecurity professional, I investigated potential security incidents involving employee login attempts. By applying SQL filters, I retrieved only the records relevant to each investigation, helping identify suspicious activities while reducing unnecessary data.

---

# Part 1 – Retrieve After-Hours Failed Login Attempts

To identify failed login attempts that occurred after 6:00 PM, I filtered the login records by combining two conditions:

- Login time after 18:00
- Failed login attempts (`success = 0`)

### SQL Query

```sql
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00'
AND success = 0;
```

### Explanation

This query returns only login attempts that:

- occurred after 18:00;
- were unsuccessful.

Using the `AND` operator ensures both conditions are true before returning a record.

---

# Part 2 – Retrieve Login Attempts on Specific Dates

To investigate a suspicious event, I searched for login attempts that occurred on May 8 and May 9, 2022.

### SQL Query

```sql
SELECT *
FROM log_in_attempts
WHERE login_date = '2022-05-08'
OR login_date = '2022-05-09';
```

### Explanation

The `OR` operator returns records matching either date, allowing both days to be investigated in a single query.

---

# Part 3 – Retrieve Login Attempts Outside Mexico

The security team confirmed that the suspicious activity did not originate from Mexico.

To retrieve login attempts from every other country, I excluded records where the country starts with "MEX".

### SQL Query

```sql
SELECT *
FROM log_in_attempts
WHERE NOT country LIKE 'MEX%';
```

### Explanation

The `LIKE` operator matches any value beginning with `MEX`, including:

- MEX
- MEXICO

Using `NOT` excludes those records and returns only login attempts originating outside Mexico.

---
# Part 4 – Retrieve Employees in Marketing

The security team needed to deploy updates to employee machines located in the East building. I filtered the employee records to identify only employees from the Marketing department whose office is located in the East building.

### SQL Query

```sql
SELECT *
FROM employees
WHERE department = 'Marketing'
AND office LIKE 'East%';
```

### Explanation

This query returns employees who meet both conditions:

- They belong to the **Marketing** department.
- Their office location begins with **East** (such as `East-170` or `East-320`).

The `LIKE 'East%'` operator matches every office located in the East building.

---

# Part 5 – Retrieve Employees in Finance or Sales

The security team also needed to deploy updates to employees working in the Finance and Sales departments.

### SQL Query

```sql
SELECT *
FROM employees
WHERE department = 'Finance'
OR department = 'Sales';
```

### Explanation

The `OR` operator returns employees who belong to either the **Finance** or **Sales** departments, making it possible to update both groups with a single query.

---

# Part 6 – Retrieve All Employees Not in IT

Employees in the Information Technology department had already received the required update. Therefore, I retrieved all employees from every other department.

### SQL Query

```sql
SELECT *
FROM employees
WHERE NOT department = 'Information Technology';
```

### Explanation

The `NOT` operator excludes employees from the **Information Technology** department, returning only employees who still require the security update.

---
# Skills Demonstrated

Throughout this project, I developed and demonstrated the following cybersecurity and SQL skills:

- SQL query development
- Data filtering using `WHERE`
- Logical operators (`AND`, `OR`, `NOT`)
- Pattern matching with `LIKE`
- Database querying and analysis
- Authentication log analysis
- Security event investigation
- Employee asset identification
- Access and login monitoring
- Incident investigation techniques
- Cybersecurity data analysis
- Security administration support
- Problem-solving using SQL
- Relational database fundamentals

---
