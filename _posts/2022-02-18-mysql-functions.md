## MySQL Introductory DML Functions

For this session an overview of MySQL functions was reviewed.

Similar to concepts and learning encountered in previous Java learning attempts:

Variables can be expressed in the following form in MySQL and queries can be assigned to a custom function:
```tsql
--Variables
SET @myVar1 = 5;

PREPARE myQuery
	FROM 'SELECT user_name, height FROM userTbl limit ?';
-- myQuery is saved to buffer. ? is the variable filled my myVar5;
EXECUTE myQuery USING @myVar5;
```

Similar to typecasting in Java, the data type of records in MySQL can be changed to
another using CAST() or CONVERT(), keeping in mind the (limited!) range of data types in
MySQL: DATE/TIME, CHAR, DECIMAL, SIGNED/UNSIGNED INT.
```tsql
SELECT CAST(avg(amount) AS signed integer) as 'average amount' FROM buyTbl;
```

If statements are fairly self explanatory. Their output can be defined as demonstrated below.
```tsql
SELECT IF(300 > 200, 'true', 'false');
SELECT IFNULL(null, 'isnull'), IFNULL(100, 'isnull');
```

SELECT-CASE is identical in function to switchcases in Java. END defines the end of the list of cases.
```tsql
SELECT
	CASE 10
    WHEN 1 THEN 'one'
    WHEN 5 THEN 'five'
    WHEN 10 THEN 'ten'
    ELSE 'idk'
    END as 'result';
```

MySQL has several built-in functions:
```tsql
#Concatenation
  SELECT CONCAT('a','b','c','d');

#Concatenation with string
  SELECT CONCAT_WS('---','1','2','3','4','5');

#Specific rounding, with specified decimal place
  SELECT FORMAT(1234.588475906205, 3);

#Converts input to decimal, hexadecimal, and octal
  SELECT BIN(31), HEX(31), OCT(31);

#Subselections in left and right directions
  SELECT LEFT('abcdefgh', 3), RIGHT('abcdefgh', 4);

#Padding, also possible from right with RPAD
  SELECT LPAD('this', 6, '#');

#Trimming. Self explanatory
  -- possible directions are BOTH, LEADING, TRAILING
SELECT TRIM(BOTH 'a' FROM 'aaaaaaaaaaaaaaaaaaaaaaaabaaaaaaaaaaaaa');

#Replacement. Self explanatory
SELECT REPLACE('Coded with Java', 'Java', 'MySQL');

#Space function. Adds specified amount of spaces
SELECT CONCAT('this', SPACE(50), 'that');

#Substring. Selects subset of string given parameters
SELECT SUBSTRING('javaspringmysql', 6, 4);
```

Stored Procedures in MySQL: Prepared code that can be executed later. Similar to methods
but these have to be fully independent blocks of code. As with methods, parameters can
be passed to the procedure when called. The syntax for a procedure that checks if an
employee has been employed for 5 years or not from the employees sample table is provided
below.

```tsql
DELIMITER $$
CREATE PROCEDURE checkFiveYear2(emp_num_input INTEGER)
BEGIN
	DECLARE hireDate DATE;
    DECLARE todayDATE DATE;
    DECLARE days INT;
    SELECT hire_date INTO hireDate
		FROM employees WHERE emp_no=emp_num_input;
	-- use INTO keyword to enter hire_date into hireDate
    SET todayDate = CURRENT_DATE();
    SET days = DATEDIFF(todayDATE, hireDATE);
    IF(days/365) >= 5 THEN
		SELECT CONCAT('입사한지', days, ' 일이 경과했습니다');
	ELSE
		SELECT CONCAT('5년 미만이고', days, ' 일째 근무중');
	END IF;
END $$
DELIMITER ;

CALL checkFiveYear2(10007);
```
