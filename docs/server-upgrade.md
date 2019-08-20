# 系统更新

登录ECS，通过输入更新命令或操作更新功能而实现更新。

### Linux更新

Linux服务器的更新，只需要运行一条更新命令，即可安装大部分更新

```shell
#CentOS or Redhat
sudo yum update -y

#Ubuntu
apt update && apt upgrade -y
```

实际上，Websoft9提供的镜像已经将以上更新命令通过计划任务定期执行。

### Windows更新

Windows服务器的更新与本地电脑类似，手动找到更新管理程序，设置自动下载自动更新即可。