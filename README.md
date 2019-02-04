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
