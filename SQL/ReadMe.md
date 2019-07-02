# SQL
DDL(Data Definition Language): Create,Insert,Update,Alter,Drop,etc  
DML(Data Manipulation Language): select,insert,update,delete,merge,call,Explain,etc  
DCL(Data Control Language):Control flow statement,GRANT,Store Procedures,functions,etc  

### SQL语句快速学习
主看3,1辅助练习  

1. SQL练习网站：https://sqlbolt.com  
   对应中文网站：http://xuesql.cn/ （翻译的不全）  
2. 在线数据库：http://www.sqlfiddle.com/#!9/99010e  
3. 菜鸟查询手册：https://www.runoob.com/sql/sql-tutorial.html  

### SQL8.0新增窗口函数语法（面试题会涉及）
##### 1. Over的用法: select 度量 Over 维度/窗口 as 度量名 From 表名  
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

注意点：
   （1）Over后窗口函数内的partition by(分组)、order by(排序)的执行要晚于外部的where、group by、order by的执行

##### 2. Row_number() Over()
参考：https://blog.csdn.net/qq_25221835/article/details/82762416  

理解：row_number()是给数据行递增编号的函数，其常用搭配主要有以下几种  
     （1）row_number() over(order by 排序列 desc) 先按某列排序然后按行递增编号  
     （2）row_number() over(partition by 分组列 order by 排序列 desc) 先按某些列对数据进行分组，每组内排序递增编号  
     （3）select row_number() over(partion by 分组列 order by 排序列 desc) as 新列名字 from 表名 where 
     

# MySQL
### MySql8.0安装
1. 参考https://www.cnblogs.com/luoli-/p/9249769.html
2. Workbench安装：sudo apt-get install mysql-workbench

### Mysql注意事项
1. 表名、列名等表示字符串的不是用引号括起来的，是用ESC键下面的那个键。  
2. Workbunch中运行脚本后刷新才能看到结果。 
3. 取别名时 as 可以省略掉

### 一些使用方法
1. 三种注释方式

      -- 注释内容  
      #注释内容  
      /*注释内容*/  

## 面试题
https://www.jianshu.com/p/77597eadd3cc
