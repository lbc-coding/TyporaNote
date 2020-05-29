# Ubuntu18.04如何安装mysql8.0.20

## 一、彻底删除mysql5.7

### 	1、查看mysql依赖项

​		dpkg --list|grep mysql

### 	2、卸载

​		sudo apt-get remove mysql-common

​		sudo apt-get autoremove --purge mysql-server-5.7

​		dpkg -l|grep ^rc|awk '{print$2}'|sudo xargs dpkg -P

### 	3、再次查看依赖项

​		dpkg --list|grep mysql

​		dpkg --list|grep mysql

​		若依然有依赖项，执行

​		sudo apt-get autoremove --purge mysql-apt-config

​	4、没有依赖项后，接着安装mysql8.0.20

## 二、下载bundle.tar完整安装包，解压后，按以下顺序安装mysql8.0.20

​		1.sudo dpkg -i mysql-common_8.0.20-1ubuntu18.04_amd64.deb

​		sudo apt-get update

​		2.sudo dpkg -i libmysqlclient21_8.0.20-1ubuntu18.04_amd64.deb

​		sudo apt-get update

​		3.sudo dpkg -i libmysqlclient-dev_8.0.20-1ubuntu18.04_amd64.deb

​		sudo apt-get update

​		4.sudo dpkg -i mysql-community-client-core_8.0.20-1ubuntu18.04_amd64.deb

​		sudo apt-get update

​		5.sudo apt-get install libaio1 libmecab2 openssh-client

​		sudo apt-get update

​		6.sudo dpkg -i mysql-community-server-core_8.0.20-1ubuntu18.04_amd64.deb

​		sudo apt-get update

​		7.sudo dpkg -i mysql-community-client_8.0.20-1ubuntu18.04_amd64.deb

​		sudo apt-get update

​		8.sudo dpkg -i mysql-client_8.0.20-1ubuntu18.04_amd64.deb

​		sudo apt-get update

​		9.sudo dpkg -i mysql-community-server_8.0.20-1ubuntu18.04_amd64.deb

​		sudo apt-get update

​		10.sudo dpkg -i mysql-community-server-core_8.0.20-1ubuntu18.04_amd64.deb

​		sudo apt-get update

​		11.sudo dpkg -i mysql-community-server-debug_8.0.20-1ubuntu18.04_amd64.deb

​		sudo apt-get update

​		12.sudo dpkg -i mysql-community-test_8.0.20-1ubuntu18.04_amd64.deb

​		sudo apt-get update



