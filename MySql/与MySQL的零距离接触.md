## 初涉MySQL

### 操作MySQL软件
### MySQL配置
MySQLInstanceConfig.exe(my.ini)  
是否安装为服务  
加入PATH  
设置root用户的密码  

``` sql
-- 单行注释，前面有空格
#单行注释
/*多行注释*/
```

ASCII图学习下
mock的作用就是隔离
接口的作用也是隔离

### 登录与退出
mysql -uroot -proot -h127.0.0.1 -P3306


### 操作数据库
+ 创建
create database/schema if not exists name;
- 删除
* 修改
* 查看
show databases/schemas; -- 查看所有
select database/schema(); -- 查看当前
* 打开
use name;

## 数据类型与操作表
概念-安装-配置-操作使用
3306 root create/alter/drop database


### 操作表
+ 创建
create table if not exist tablename (
    field type null key default extra
    columnname1 type pk nn uq,
    columnname2 tinyint unsigned,
    columnname3 float(8,2) unsigned,
);
- 删除
- 修改
- 查看
show tables [from dbname] [like 'pattern' | where expr]; -- 查看所有
show columus from tablename; -- 查看当前field type null key default extra




#### 类型与约束
field type null key default extra

- 整型
- 1B tinyint signed/unsigned
- 2B smallint signed/unsigned
- 3B mediumint signed/unsigned
- 4B int signed/unsigned
- 8B bigint signed/unsigned

- 浮点型
- float[(m,d)] 默认d最大就是精确到小数点后7位 数字最大为10的38次方
- double[(m,d)] 数字最大为10的308次方

- 日期时间型
- 1 year
- 3 date 1000-9999
- 3 time
- 8 datetime
- 4 timestamp 1970-2037

- 字符型
- char(m) 0-255
- varchar(m) 0-65535
- tinytext 2的8
- text 2的16
- mediumtext 2的24
- longtext 2的32
- enum('a','b',...) 最多65535
- set('a','b',...) 最多64 任意的成员的排列组合

- null
可取值：not null  

- key
可取值：primary key | unique key
只能存在一个主键
主键自动为not null
唯一约束也是保证记录唯一性的
可以存在多个唯一键
唯一键可以为null

- default
可取值：default 'foobar'

- extra
可取值：auto_increment  
type必须为整数或浮点数，如果为浮点数则小数位数必须为0   
key必须为primary key，不能单独出现来约束列


### 操作记录
+ 插入
insert [into] name[(col1,col2,col3)] values(val1,val2,val3);  
- 删除
* 修改
* 查看
select expr,... from name;     *表示字段的过滤，而不是记录的过滤  



## 函数

## 存储过程


## 存储引擎


## 图形化管理工具