---
title: "[MySQL] Change Date Format"
categories:
- MySQL
last_modified_at: 2021-07-28T14:00:00+09:00
toc: true
---

## MySQL Date Formats (YY MM DD)
<br>
Frequently used date formats:
<br>

| Format | Output |
|--|--|
| %Y | Year (4-digit value) |
| %y | Year (2-digit value) |
| %M | Month (January ~ December) |
| %m | Month (01 ~ 12) |
| %D | Day with suffix (1st ~ 31st) |
| %d | Day (01 ~ 31) |
| %e | Day (1 ~ 31) |
| %H | Hour (00 ~ 23) |
| %h | Hour (0 ~ 12) |
| %p | AM/PM |

<br>

### 1. [**August 11 2021**] 
<br>

~~~sql
SELECT DATE_FORMAT(NOW(), '%M %d %Y');
-- Result: August 11 2021
~~~
<br>

### 2. [**2021/08/11**] 
<br>

~~~sql
SELECT DATE_FORMAT(NOW(),'%Y-%m-%d');
-- Result: 2021-08-11
~~~
<br>

### 3. [**2021-08-11 12:00 AM**]    
<br>

~~~sql
SELECT DATE_FORMAT(NOW(), '%Y-%m-%d %h:%i %p');
-- Result: 2021-08-11 12:00 AM
~~~
<br>

### 4. [**2021.08.11**] 
<br>

~~~sql
SELECT DATE_FORMAT(NOW(),'%Y.%m.%d');
-- Result: 2021.08.11
~~~
<br>

### 5. [**2021.08.11**] 
<br>

~~~sql
SELECT DATE_FORMAT(NOW(),'%Y.%m.%d');
-- Result: 2021.08.11
~~~
<br>

### 6. [**Wednesday August 2021**] 
<br>

~~~sql
SELECT DATE_FORMAT(NOW(), '%W %M %Y');
-- Result: Wednesday August 2021
~~~
<br>



Reference:
[https://www.w3schools.com/mysql/func_mysql_date_format.asp](https://www.w3schools.com/mysql/func_mysql_date_format.asp)

Any advice and suggestions are welcome and appreciated!