## 初涉MySQL
### MySQL配置
MySQLInstanceConfig.exe(my.ini)  
是否安装为服务  
加入PATH  
设置root用户的密码  


ASCII图学习下

## 数据类型与操作表
### 整型
- 1B tinyint signed/unsigned
- 2B smallint signed/unsigned
- 3B mediumint signed/unsigned
- 4B int signed/unsigned
- 8B bigint signed/unsigned


### 浮点型
- float[(m,d)] 默认d最大就是精确到小数点后7位 数字最大为10的38次方
- double[(m,d)] 数字最大为10的308次方


### 日期时间型
- 1 year
- 3 date 1000-9999
- 3 time
- 8 datetime
- 4 timestamp 1970-2037


### 字符型
- char(m) 0-255
- varchar(m) 0-65535
- tinytext 2的8
- text 2的16
- mediumtext 2的24
- longtext 2的32
- enum('a','b',...) 最多65535
- set('a','b',...) 最多64 任意的成员的排列组合




## 约束与修改表
表级约束、列级约束







## 操作记录


## 子查询与连接


## 运算符和函数

## 自定义函数

## 存储过程


## 存储引擎

## 图形化管理工具