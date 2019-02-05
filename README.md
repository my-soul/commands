# commands


## 查看端口占用

``` bash
lsof -i:8080

netstat -tunlp | grep 8080
```
## 查看进程占用的PID号
```bash
ps aux | grep 进程名 
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

## ln 连接
```bash
ln -s 原文件 目标文件 # 软连接
ln 原文件 目标文件 # 硬连接
```
## node安装 [nvm](https://github.com/creationix/nvm#install-script)

## svn install

```bash
yum install subversion

mkdir -p /server/svn/chunk

svnadmin create /server/svn/chunk

cd /server/svn/repo/chunk/

vim passwd 

vim authz

vim svnserve.conf

vim /etc/sysconfig/svnserve

systemctl start svnserve.service
```
