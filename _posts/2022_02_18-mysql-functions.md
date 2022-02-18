## MySQL - Functions

For this session an overview of MySQL functions was reviewed.

```tsql
--Simple Join Query
SET @myVar1 = 5;

PREPARE myQuery
	FROM 'SELECT user_name, height FROM userTbl limit ?';
-- myQuery is saved to buffer. ? is the variable filled my myVar5;
EXECUTE myQuery USING @myVar5;
```

```tsql
SELECT CAST(avg(amount) AS signed integer) as 'average amount' FROM buyTbl;

SELECT IF(300 > 200, 'true', 'false');
SELECT IFNULL(null, 'isnull'), IFNULL(100, 'isnull');


SELECT
	CASE 10
    WHEN 1 THEN 'one'
    WHEN 5 THEN 'five'
    WHEN 10 THEN 'ten'
    ELSE 'idk'
    END as 'result';
```

Built-in functions

```tsql
  SELECT CONCAT('a','b','c','d');

  SELECT CONCAT_WS('---','1','2','3','4','5');

  SELECT FORMAT(1234.588475906205, 3);

  SELECT BIN(31), HEX(31), OCT(31);

  SELECT LEFT('abcdefgh', 3), RIGHT('abcdefgh', 4);

  SELECT LPAD('this', 6, '#');

  -- possible directions are BOTH, LEADING, TRAILING
SELECT TRIM(BOTH 'a' FROM 'aaaaaaaaaaaaaaaaaaaaaaaabaaaaaaaaaaaaa');

SELECT REPLACE('Coded with Java', 'Java', 'MySQL');

SELECT CONCAT('this', SPACE(50), 'that');

SELECT SUBSTRING('javaspringmysql', 6, 4);
```

Procedures in MySQL

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
