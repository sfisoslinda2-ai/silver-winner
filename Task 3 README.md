# Task 3: SQL Injection on DVWA (Low Security)
## Objective: Demonstrate an SQL Injection vulnerability on a web application (DVWA with low security).
DVWA was configured with the Low Security setting to demonstrate how SQL Injection vulnerabilities occur in poorly secured web applications.

The application failed to properly validate and sanitize user input before including it in an SQL query. Because user input was not filtered, an attacker could inject SQL code into the application.

A SQL Injection payload was entered into the input field. This payload modified the logic of the backend SQL query, causing the database to return unintended results. Instead of processing the query as intended, the application interpreted the injected SQL code as part of the database command.

The successful execution of the payload demonstrated that the application was vulnerable to SQL Injection attacks. In a real-world environment, such vulnerabilities could allow attackers to bypass authentication, access sensitive information, modify records, or compromise the database.

This vulnerability highlights the importance of implementing secure coding practices. Developers should use parameterized queries (prepared statements), proper input validation, and input sanitization to ensure that user-supplied data is treated as data rather than executable SQL code. These security measures help prevent SQL Injection attacks and protect sensitive information.
