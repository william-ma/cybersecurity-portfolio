# Apply filters to SQL queries

## Project description

Recently a few potential security issues have been discovered that involve login attempts and employee machines. 
I will conduct an investigation using SQL to query the `log_in_attempts` and `employees` table.  

## Retrieve after hours failed login attempts

There were failed login attempts made after usual business hours. Usual office hours end at '18:00'. 

So, the following query is ran, which selects all the columns in the `log_in_attempts` table, where the log in attempt occurred after 6PM and were unsuccessful. 

![image](https://github.com/user-attachments/assets/9f501b17-8fd6-45bf-8b94-aa18426e0556)

## Retrieve login attempts on specific dates

A suspicious event occurred on 2022-05-09. To investigate this issue, I will retrieve all login attempts that occurred on 2022-05-09 or 2022-05-08. 

![image](https://github.com/user-attachments/assets/d46d6328-2f53-4773-9ee3-0ac82d7cd12f)

The above query returns all the columns and rows in the log_in_attempts table where the login_date column is '2022-05-08' or login_date is '2022-05-09'. 

## Retrieve login attempts outside of Mexico

There's been suspicious activity with login attempts, but the team has determined that this activity didn't originate in Mexico. 
Now, I'll investigate the login attempts that occurred outside of Mexico.

![image](https://github.com/user-attachments/assets/86d38769-608c-487a-94ba-20b413630675)

The query works because in the `country` column Mexico is stored as either 'Mex' or 'Mexico' and has possibly other variations. 
So, we'll considered all log in attempts are from Mexico if the `country` column begins with 'Mex'. We use `LIKE 'Mex%'`, because `%` is a wildcard that matches anything afterwards. 
We then negate this condition with a `NOT` in front, so we retrieve all login attempts outside of Mexico. 

## Retrieve employees in Marketing

My team wants to perform security updates on specific employee machines in the Marketing department and for offices in the East building.

![image](https://github.com/user-attachments/assets/43be8e89-ec4e-4252-bf4a-dab5eacba41d)

The `office` column contains values such as 'East-170' or 'East-320'.
And, because we want to retrieve all offices in the East building, we use a wildcard as described in the previous step. 

## Retrieve employees in Finance or Sales

My team now needs to perform a different security update on machines for employees in the Sales and Finance departments. 

![image](https://github.com/user-attachments/assets/f9711b30-704c-47ae-b81e-ef299cb1cd18)

## Retrieve all employees not in IT

My team needs to make one more update to employee machines. 
The employees who are in the Information Technology department already had this update, but employees in all other departments need it. 

![image](https://github.com/user-attachments/assets/8e7a1bf3-6e57-4707-b2c4-4d42c8b2cb35)

## Summary

SQL was used to query the `log_in_attempts` and `employees` table. 
This helped narrow down the suspicious activity related to login attempts that failed after normal business hours and login attempts outside of Mexico. 
This also helped find the employees who's machines needed security updates, this helps keep software up to date, reducing the attack surface of the organization. 
