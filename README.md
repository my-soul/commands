# commands


## 查看端口占用

``` bash
lsof -i:8080

netstat -tlp | grep 8080
```
## 查看进程占用的PID号
```bash
ps -aux | grep 进程名 
```

## 软件安装目录
``` bash
whereis nginx
```

## systemctl
``` bash
systemctl status service
systemctl start service
systemctl stop service
systemctl restart service
systemctl enable service
```

## 查看系统资源
``` bash
# vmstat虚拟内存状态
vmstat

# df：查看硬盘使用情况
df -h

# free 内存
free -m

# cpu
lscpu
```

## rpm 
```bash
# 安装软件：执行rpm -ivh rpm包名，如：

rpm -ivh apache-1.3.6.i386.rpm

# 查询软件包的详细信息：执行
rpm -qpi rpm包名
```


## centOS 安装mysql

[Using the MySQL Yum Repository](https://dev.mysql.com/doc/mysql-yum-repo-quick-guide/en/)

## jenkins 安装
```bash
sudo wget -O /etc/yum.repos.d/jenkins.repo http://pkg.jenkins-ci.org/redhat/jenkins.repo
sudo rpm --import https://jenkins-ci.org/redhat/jenkins-ci.org.key
sudo yum install jenkins
systemctl start jenkins # /usr/bin/java 需存在

vim /etc/sysconfig/jenkins
# 修改$JENKINS_USER，并去掉当前行注释
$JENKINS_USER="root"
```

## jdk

```bash
yum -y list java*
yum -y install java-1.8.0-openjdk*

```

## ln 连接
```bash
ln -s 原文件 目标文件 # 软连接
ln 原文件 目标文件 # 硬连接
```
## node安装 [nvm](https://github.com/creationix/nvm#install-script)

## svn install

```bash
yum install subversion

mkdir -p /var/svn/repos

svnadmin create /var/svn/repos

cd /var/svn/repos/

vim passwd 

vim authz

vim svnserve.conf

vim /etc/sysconfig/svnserve

systemctl start svnserve.service # not sasl
```

## 内网穿透[frp](https://github.com/fatedier/frp)

cpu架构选择amd64

## redis

https://www.cnblogs.com/renzhicai/p/7773080.html

## mysql redis 端口转发
```bash
ssh -L 3306:localhost:3306 -L 6379:localhost:6379  root@tx.shartem.com
```
