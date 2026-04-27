<center><h2>Lesson 7</h2></center> 
<h4>Queries:</h4>

### 1. Find the list of all buildings that have employees
~~~sql
SELECT DISTINCT building FROM employees;
~~~

### 2. Find the list of all buildings and their capacity
~~~sql
SELECT * FROM buildings;
~~~

### 3. List all buildings and the distinct employee roles in each building (including empty buildings)
~~~sql
SELECT DISTINCT building_name, role 
FROM buildings 
  LEFT JOIN employees
    ON building_name = building;
~~~