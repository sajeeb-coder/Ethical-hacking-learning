Lab Name: SQL injection vulnerability in WHERE clause allowing retrieval of hidden data
Date: 20 January 2026

Description:
In this lab, the application was vulnerable to SQL Injection in the WHERE clause of a SQL query.
The application filtered and displayed products based on a category parameter supplied by the
 user.
Some products were marked as hidden in the database and were not intended to be shown to
 normal users.

Vulnerability Analysis:
User-controlled input was directly concatenated into the SQL query.
This allowed manipulation of the WHERE clause logic using SQL injection techniques.

Exploitation:
By injecting a logical condition such as:
OR 1=1 --

I was able to bypass the original filtering condition.
This caused the SQL query to return all rows from the database, including hidden products.

Impact:
- Unauthorized access to hidden data
- Breakdown of application access control
- Potential data exposure

Learning Outcome:
- Understood how SQL injection affects WHERE clause logic
- Learned practical boolean-based SQL injection exploitation
- Gained hands-on experience with logic flaws due to improper input validation

Status: Lab successfully completed
