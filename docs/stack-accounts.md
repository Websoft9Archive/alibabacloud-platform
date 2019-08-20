# Username and Password

You can get the credentials of Database and OS from this chapter

## Database

### Database Password

Getting password from Linux and Windows have some difference

#### Linux

For Linux, the database password was storaged in the file of your VM: *`/credentials/password.txt`*. Suggest you log in AWS Portal and using the online SSH terminal to run the the `cat` command to get the password：

![run cat Command](https://libs.websoft9.com/Websoft9/DocsPicture/zh/common/catdbpassword-websoft9.png)

#### Windows

For Window, the database password was storaged in the file of your VM:*`c:/credentials/password.txt`*

You can also find the shortcut for password file from the Windows Desktop

### Database Username and GUI

Different databases have certain differences, refer to the following table:

| Database                    | Username     | GUI           |
| ----------------------- | ---------- | ------------------------ |
| MySQL/Mariadb with PHP | root       | http://Internet IP/phpmyadmin |
| MySQL/Mariadb     | root       | http://Internet IP:9090       |
| PostgreSQL              | postgres   | http://Internet IP:9090       |
| Mongodb                 | adminmongo | http://Internet IP:9091       |
| Oracle                  | system     | NO                     |
| SQLServer               | sa         | SQLServer Management Studio,one Desktop client     |



## OS

AWS在创建EC2的时候，只能选择采用秘钥对作为验证方式
![秘钥对设置](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aws/aws-ec2createpw-websoft9.png)

另外，针对于不同的操作系统（甚至发行版）其用户名是不一样的：

### Linux

- Get the default user name for the AMI that you used to launch your instance
- For an Ubuntu AMI, the user name is ubuntu.
- For Amazon Linux 2 or the Amazon Linux AMI, the user name is ec2-user.
- For a CentOS AMI, the user name is centos.
- For a Debian AMI, the user name is admin or root.
- For a Fedora AMI, the user name is ec2-user or fedora.
- For a RHEL AMI, the user name is ec2-user or root.
- For a SUSE AMI, the user name is ec2-user or root.

如果 ec2-user 和 root 无法使用，请与 AMI 供应商核实。

以上信息来源于 AWS官方说明，了解[详情](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/connection-prereqs.html)。

### Windows

The username is `Administrator`