## Linux简介
1991年  
内核版本 www.kernel.org 2.6.18/3.16  
发型版本  
redhat/centos/fedora(redhat开发的个人版，但是不同于Windows的个人版)  
debian/ubuntu  

www.netcraft.com  
QuickSSHd  

## 系统安装
628M 图形安装界面   
桥接 
NAT 8  
Host Only 1  

分区 C D E编号或者取名字，至少一个分区  
主分区 最多4个  512-64/16*4  
扩展分区  最多1个，主分区加逻辑分区最多4个，只能包含逻辑分区
逻辑分区  D开始最多23个
1 2 3 4(5 6 7)
格式化 支持的分区、单个文件大小有限制  

硬件  对应的设备文件名  
IDE硬盘  /dev/hd[a-d][1-n]  
SCSI/SATA/USB硬盘  /dev/sd[a-p][1-n]  
光驱  /dev/cdrom或者/dev/hdc  
打印机（USB）  /dev/usb/lp[0-15]  
鼠标  /dev/mouse  

挂载点=盘符（也叫分区，注意跟上面的分区概念区别）   对硬盘对操作：分区-格式化-（Linux特有：取名）-挂载（分配盘符）
/
swap 4G以内两倍，以上则等同  
/boot  
/home  

最小安装  
安装时在图形安装界面上配置网络打开以太网连接  


不支持中文输入


## 文件命令
3000总共/200常用/60课程中学到  
多个选项可以写在一起  
简化选项 完整选项  
ls -aldhi  . centos6开始出现  
mkdir -p a/b/c/d  
cd  cd ~ cd -  命令补全、目录补全  
pwd  
rmdir  删除空目录  
rm -rf  删除文件或者目录，r的意思就是删除目录  
cp -rpd/-a  
mv  
ln -s 源文件 目标文件  


## 搜索命令
locate 文件名       /var/lib/mlocate updatedb  /etc/updatedb.conf
find  
whereis/which  
grep  




## 帮助命令


## 压缩命令


## 关机命令


## 其他命令


## Shell命令


## Vim


## 磁盘管理


## 用户管理

