# Upgrade

You can upgrade system by commands when you connect to it.    

### Linux Upgrade

Linux OS update, you only need to run an update command to install most updates

```shell
#CentOS or Redhat
sudo yum update -y

#Ubuntu
apt update && apt upgrade -y
```

In fact, the image provided by Websoft9 has periodically executed the above update commands through cron of Linux.

### Windows Upgrade

The update of the Windows server is similar to that of the local computer. Manually find the update management program and set the automatic download automatic update.