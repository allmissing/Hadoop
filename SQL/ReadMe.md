# SQL
DDL(Data Definition Language): Create,Insert,Update,Alter,Drop,etc  
DML(Data Manipulation Language): select,insert,update,delete,merge,call,Explain,etc  
DCL(Data Control Language):Control flow statement,GRANT,Store Procedures,functions,etc  

## SQL语句快速学习
主看3,1辅助练习  

1. SQL练习网站：https://sqlbolt.com  
   对应中文网站：http://xuesql.cn/ （翻译的不全）  
2. 在线数据库：http://www.sqlfiddle.com/#!9/99010e  
3. 菜鸟查询手册：https://www.runoob.com/sql/sql-tutorial.html  

## SQL8.0新增窗口函数语法（面试题会涉及）
1.Over的用法: select 度量 Over 维度/窗口 as 度量名 From 表名  
参考：https://www.bilibili.com/video/av30579111?from=search&seid=7719848635273543563

窗口可以用两种方式来书写：  
（1）Over(窗口内容)  
（2）...Over 窗口名 ....  
     window 窗口名 as(窗口内容)  

eg:

    select col1,col2,sum(col2) over w as NEW_COL_NAME from TABLE_NAME
    window w as
    (Order by col1
    range between interval 1 week preceding and current row)
    Order by col1


## MySql8.0安装
参考https://www.cnblogs.com/luoli-/p/9249769.html

## Mysql注意事项
1. 表名、列名等表示字符串的不是用引号括起来的，是用ESC键下面的那个键。  
2. Workbunch中运行脚本后刷新才能看到结果。  
