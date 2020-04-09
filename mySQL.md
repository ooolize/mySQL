### 数据库
> 用表的形式存储数据的相关信息。
大文件不会存储在数据库，而是存在磁盘上，数据库存储路径
### 库
+ 创建一个库：CREATE database testbase;
+ 显示所有库：show databases;
+ 删除一个库：drop testbase;
+ 进入一个库: show testbase;
### 表
表就像Excel的统计表一样，由一些字段(域)(列名)组成
+ 创建一个表:create table person(ID int audo_increment,name char(20),primary key(ID));
创建一个表，字段有ID,name。并且把主键设为ID,且是自增的。
+ 查看字段属性:show crete table person;
+ 增加表的字段:alter table person add english float DEAAULT 60;science float DEFAULT 50; 
向person表中增加英语和科学字段，默认为60和50；
+ 删除表的字段:ALTER TABEL person drop math
+ 修改表的字段:AKTER TAblE person CHANGE english default 0;
修改english默认值为0
### 数据
+ 增加数据：insert into person(ID,name,english) values(1,'lize',20) (2,'zyq',30);
+ 删除数据: delete from person where ID==1;
+ 修改数据: update person set ID=4 where english=20;
+ 查找数据：
  + 显示所有数据：select * from person 
  + 显示所有成绩的总和: select english+math+science as total from person;
### where操作符
+ 逻辑操作：等于= 不等于<> :select * from person where english>60;
+ BETWEEN AND区间:select * from person where english BETWEEN 60 AND 90
+ in():选择出现在集合区间的元素，select from person where english in(60,70);
+ like模糊查询:select * from person where name='%ze' 
%多位，_一位
+ 判空:select * from person where math is NULL;
### 排序order by
只看数学前三：select * from person order by math desc limit 3;

desc是升序，asc升序
### 数据完整性
### 多表设计
### 多表查询
+ 内连接
+ 外连接
### 函数
+ count
+ sum
+ avg select avg(english) from person where math>60;
+ max/min

