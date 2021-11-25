# Username and Password

You can get the credentials of Database and OS from this chapter.

## Database

### Database Password

Getting password from Linux and Windows have some difference

#### Linux

For Linux, all passwords are stored in the file of your ECS: *`/credentials/password.txt`*. You can use the online SSH terminal from **AlibabaCloud Console** to run the the `cat` command to get the password：

![run cat Command](https://libs.websoft9.com/Websoft9/DocsPicture/zh/common/catdbpassword-websoft9.png)

#### Windows

For Window, the database password is stored in the file of your ECS:*`c:/credentials/password.txt`*

You can also find the shortcut for password file from the Windows Desktop.

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

阿里云Linux系统默认的账号名称为：root
阿里云Windows系统默认的账号名称为：administrator