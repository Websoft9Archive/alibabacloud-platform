# Upgrade

There are two options for updating the OS. One is an update management solution that launches the AWS Portal, and the other is using the OS's upgrade solution.

## Upgrade by AWS Portal

AWS have provided a complete [Automatic upgrade solution](https://aka.ms/updatemanagement)

1. Login AWS Portal, Click the "Update management" on Operation section, then "Enable" it
  ![Enable update management](https://libs.websoft9.com/Websoft9/DocsPicture/en/AWS/AWS-enableupdate-websoft9.png)
2. Wait for minutes and the AWS will create an update solution. Click "Schedule update deployment" to start set update policy
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/AWS/AWS-updateset-websoft9.png)

## Upgrade by OS

Upgrade by OS is implemented by logging in to the VM and inputting an update command or an operation update function, which is different from the update management function of the AWS portal.

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