---
title: "[MySQL] How to Drop foreign key"
categories:
- MySQL
last_modified_at: 2021-07-28T14:00:00+09:00
toc: true
---
## How to Drop a Foreign Key in MySQL


~~~sql
ALTER  TABLE  'table_name'  DROP  FOREIGN  KEY  'foreign_key'
~~~
and I got an error as below:
~~~sql
#1091  - Can't DROP 'foreign_key'; check that column/key exists
~~~

1. Find the foreign key contraint using 
	~~~sql
	SHOW  CREATE  TABLE  'table_name';
	~~~
	Normally it's 'table_name_ibfk_1'. <br>
2. Drop Foreign key
	~~~sql
	ALTER  TABLE  'table_name'  DROP  FOREIGN  KEY 'table_name_ibfk_1﻿';  
	ALTER  TABLE  'table_name'  DROP  INDEX  'column';
	~~~

<br>
Reference:

[https://stackoverflow.com/questions/25079645/cant-drop-foreign-key-in-mysql](https://stackoverflow.com/questions/25079645/cant-drop-foreign-key-in-mysql)

Any advice and suggestions are welcome and appreciated!
	