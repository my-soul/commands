# commands


## 查看端口占用

``` bash
lsof -i:8080

netstat -tunlp | grep 8080
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
