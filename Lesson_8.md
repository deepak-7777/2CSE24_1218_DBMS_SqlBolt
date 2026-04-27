<center><h2>Lesson 8</h2></center> 
<h4>Queries:</h4>

### 1. Find the name and role of all employees who have not been assigned to a building
~~~sql
SELECT name, role FROM employees
WHERE building IS NULL;
~~~

### 2. Find the names of the buildings that hold no employees
~~~sql
SELECT DISTINCT building_name
FROM buildings 
  LEFT JOIN employees
    ON building_name = building
WHERE role IS NULL;
~~~