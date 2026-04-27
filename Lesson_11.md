<center><h2>Lesson 11</h2></center> 
<h4>Queries:</h4>

### 1. Find the number of Artists in the studio (without a HAVING clause)
~~~sql
SELECT COUNT(*) as Number_of_artists
FROM employees
WHERE role = "Artist";
~~~

### 2. Find the number of Employees of each role in the studio
~~~sql
SELECT role, COUNT(*) as Number_of_employees
FROM employees
GROUP BY role;
~~~

### 3. Find the total number of years employed by all Engineers
~~~sql
SELECT SUM(years_employed) as Total_years_employed
FROM employees
WHERE role = "Engineer";
~~~