# 账号密码

下面分别就数据库和操作系统的账号密码进行说明：

## 数据库

### 用户名、密码和管理地址

不同的数据库有一定的差异，参考下表：

| 名称                    | 用户名     | 密码           | 可视化管理地址           |
| ----------------------- | ---------- | -------------- | ------------------------ |
| MySQL/Mariadb PHP环境中 | root       | 123456 | http://公网IP/phpmyadmin |
| MySQL/Mariadb 其他      | root       | 123456  | http://公网IP:9090       |
| PostgreSQL              | postgres   | 123456  | http://公网IP:9090       |
| Mongodb                 | adminmongo | 123456  | http://公网IP:9091       |
| Oracle                  | system     | 123456 | 暂无                     |
| SQLServer               | sa         | websoft9!  | 使用客户端管理           |

如果以上密码不可用，那么请通过下面的方案获取密码

### 获取数据库密码

#### Linux系统

对于Linux系统来说，数据库密码存储在您的服务器指定文件中：*`/credentials/password.txt`*。建议通过云控制台直接连接服务器，进入命令终端，运行cat命令获取数据库密码：

![运行cat命令](https://libs.websoft9.com/Websoft9/DocsPicture/zh/common/catdbpassword-websoft9.png)

#### Windows系统

对于Windows系统来说，数据库密码存储在您的服务器指定文件中：*`c:/credentials/password.txt`*

服务器的桌面上会有打开数据库密码文件的快捷方式



## 操作系统

阿里云Linux系统默认的账号名称为：`root`  
阿里云Windows系统默认的账号名称为：`administrator`