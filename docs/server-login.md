# Linux Connect

There are two ways to connect to a Linux server: command line and SFTP:

## Connect by Command

The command is the basic operation of the Linux system. Blow are the methods for you:  

| Methods                                                   | Details                                                     |
| ------------------------------------------------------ | ------------------------------------------------------------ |
| Local SSH Connection                                   | Install [Putty](https://putty.org/) to your local computer and run it |
| [Workbench](https://ecs-workbench.aliyun.com/) Connection |An online web-based tool of AlibabaCloud  |
| VNC Connection                                           | VNC online web-based tool of AlibabaCloud, you can use it when you can not run Putty or Workbench|
| Send Remote Commands (Cloud Assistant)                   | To send remote commands, you must use the task execution feature provided by Cloud Assistant|


We use **Workbench Connection** to show you how to connect Linux:

1. Login to Console and list all you ECS, then click 【Connect】action for your target ECS
   ![Connect Action](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-remoteconnectweb-websoft9.png)

2. Then, click the 【Send Remote Call】button of 【Send Remote Commands (Cloud Assistant)】

3. Waiting for loading, and input username and password or Key Pairs to connect it

After connecting to the server through the command line, the following two most common examples of operations are required:

### Sample 1: Getting database password

For security reasons, each time a user deploys, a unique random database password is generated and stored in the service. Just one of the following commands to view

```shell
sudo cat /credentials/password.txt

//result
MySQL username:root
MySQL Password:@qDg1Vq1!V
```

### Sample 2: Disable the root username

For security and regulatory requirements, if you want to disable the `root` password you should set below:

```shell
sudo su
sudo sed -i 's/#PermitRootLogin yes/PermitRootLogin no/' /etc/ssh/sshd_config
sudo systemctl restart sshd
sudo passwd root
```

## Connect by SFTP

SFTP is an FTP mode that uses the SSH protocol, also known as security-enhanced FTP. The SFTP tool is a favorite operation mode for Linux users. The following is an example of WinSCP SFTP tool, which details the use of SFTP.

### Configure WinSCP

1. Download [WinSCP](https://winscp.net/) and install it, then start it to create a new connection
2. The following is based on the cloud server's **password verification** and **key-key pair** verification:
   - Password authentication(the most common way)
     ![Password authentication](http://libs.websoft9.com/Websoft9/DocsPicture/en/winscp/winscp-newsite.png)
   - Key-key pair authentication
     ![Key-key pair authentication](http://libs.websoft9.com/Websoft9/DocsPicture/en/winscp/winscp-secrets-websoft9.png)
3. You may want to save your session details to a site so you do not need to type them in every time you want to connect. Press Save button and type site name.
   ![Save session](http://libs.websoft9.com/Websoft9/DocsPicture/en/winscp/winscp-sessionsave-websoft9.png)
4. Successfully connected interface
   ![WinSCP GUI](http://libs.websoft9.com/Websoft9/DocsPicture/en/winscp/websoft9-winscp-success.png)

### Manage Files

WinSCP can easily upload and download files by dragging and dropping, and can perform various settings and operations on files (folders).

1. In general, the files on the website are placed in the */data/wwwroot* directory.
   ![upload files](http://libs.websoft9.com/Websoft9/DocsPicture/en/winscp/winscp-dragfile-websoft9.png)

2. You can perform multiple operations on the VM by right-clicking on a file or folder on the server.
   ![Setting file](http://libs.websoft9.com/Websoft9/DocsPicture/en/winscp/websoft9-winscp-youjian.png)

3. The relevant interface for modifying file permissions is as follows:

   ![Gourp and Owner settings](http://libs.websoft9.com/Websoft9/DocsPicture/en/winscp/websoft9-winscp-quanxian.png)

### Run Command

WinSCP is a built-in command run function, although the command function is limited to running non-interactive naming (that is, no feedback and process input are required during command execution), but it is simple and practical for beginners.

1. WinSCP logs in to the server, click on the command window icon from the menu (shortcut Ctrl+T is also available)
   ![Command of Winscp](http://libs.websoft9.com/Websoft9/DocsPicture/en/winscp/winscp-ucmd-websoft9.png)
2. In the pop-up command run window to execute the command (one command at a time), to query the memory usage as an example, run the command `free -m`
   ![Command of Winscp](http://libs.websoft9.com/Websoft9/DocsPicture/en/winscp/wincp-showmemory-websoft9.png)

### Putty Integration

Under certain specificities, you may need to use [Putty](https://putty.org/) to run commands. Since Putty is a command operation interface, you need to enter the root password every time you use it. If the password is complicated, it will make people feel more troublesome. In fact, WinSCP can be integrated with Putty. After integration, you can open Putty through WinSCP and log in to the server automatically.

1. Open the Preferences of WinSCP->Integration->Application, and input the local address of your Putty, click OK
   ![Putty Address](http://libs.websoft9.com/Websoft9/DocsPicture/en/winscp/websoft9-winscp-putty.png)
2. After the integration is successful, you only need to open the Putty through Winscp's window shortcut.
   ![Open Putty on WinSCP](http://libs.websoft9.com/Websoft9/DocsPicture/en/winscp/websoft9-winscp-puttyopen.png)

> Opening a Putty operation via Winscp is no different than opening a putty directly.