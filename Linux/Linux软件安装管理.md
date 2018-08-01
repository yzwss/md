## rpm安装

下载mysql-8.0.12-1.el7.x86_64.rpm-bundle.tar  
rpm -ivh mysql-community-common-8.0.12-1.el7.x86_64.rpm  
rpm -ivh mysql-community-libs-8.0.12-1.el7.x86_64.rpm  
rpm -ivh mysql-community-libs-compat-8.0.12-1.el7.x86_64.rpm  
rpm -ivh mysql-community-client-8.0.12-1.el7.x86_64.rpm  
rpm -ivh mysql-community-server-8.0.12-1.el7.x86_64.rpm  

grep 'temporary password' /var/log/mysqld.log  
alter user 'root'@'localhost' identified by 'xxxxxxxx';  
INSTALL PLUGIN validate_password SONAME 'validate_password.so';
SHOW VARIABLES LIKE 'validate_password%';  
set global var=0;
alter user 'root'@'localhost' identified by 'aaaaaaaa';  

## yum安装


## 源码安装
/usr/local/src  
/usr/local  