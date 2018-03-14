日志在目录/usr/local/mysql/data下：可见图


insert log如下:
================&gt; binlog[mysql-bin.000009:7185] , name[lemall,ky_user] , eventType : INSERT
id : 11    update=false
name : test    update=false
job : 哈哈    update=false
area_no : 777    update=false


update log如下:
================&gt; binlog[mysql-bin.000009:7389] , name[lemall,ky_user] , eventType : UPDATE
-------&gt; before
id : 11    update=false
name : test    update=false
job : 哈哈    update=false
area_no : 777    update=false
-------&gt; after
id : 11    update=false
name : 王宇    update=true
job : 家里蹲    update=true
area_no : 777    update=false

delete log如下：
================&gt; binlog[mysql-bin.000009:7620] , name[lemall,ky_user] , eventType : DELETE
id : 11    update=false
name : 王宇    update=false
job : 家里蹲    update=false
area_no : 777    update=false



ddl 为表增加一个字段 log如下：
================&gt; binlog[mysql-bin.000009:7702] , name[lemall,ky_user] , eventType : ALTER
ddl 建表 log如下：
================&gt; binlog[mysql-bin.000009:7832] , name[lemall,ky_user999] , eventType : CREATE
