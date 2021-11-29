# Manage

These steps for you to manage ECS

## Start, Stop and Release

You can manage the ECS on Console, includes:

- Start
- Stop
- Restart
- Release
- Upgrade/Downgrade

释放=删除ECS，使用于按量购买的服务器

## Reset password

忘记密码，在阿里云控制台有两种方式可以重置密码：

### Reset by Console

1. 登录到阿里云控制台，找到所需操作的ECS

2. 点击下面的“重置实例密码”，输入新密码
   ![reset password](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-resetpw-1-websoft9.png)
   ![reset password](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-resetpw-2-websoft9.png)

3. 重启ECS实例，方可生效

### Reset by Command

1. 登录到阿里云控制台，找到所需操作的ECS

2. 点击右侧【远程连接】>【发送命令】，打开相关窗口

3. 输入的命令如下，点击【执行】按钮
   ```
   echo "yourpassword" | passwd --stdin root  
   ```
4. 提示如下的信息即表示执行成功
   ```
   Changing password for user root.
   passwd: all authentication tokens updated successfully.
   ```

## Upgrade/Downgrade

ECS 的配置可以调整，具体操作如下：

1. 登录到阿里云控制台，找到所需操作的ECS

2. 点击右侧的“升降配”，选择一种变更方案
   ![调整配置](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-changeecsconfigure-websoft9.png)

3. 依据相关的操作向导完成变更

## Replace System Disk

如果你想将服务器恢复到刚安装之时的状态，就需要用到**重新初始化镜像**操作。

1. 登录到阿里云控制台，找到所需操作的ECS

2. 停止ECS示例

2. 依次打开：更多->磁盘和镜像->重新初始化镜像
   ![Reset System disk](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-changesysdisk-websoft9.png)

3. 根据系统提示完成后续步骤

> 建议仔细理解**更换系统盘**和**重新初始化镜像**的差异

## API/CLI

阿里云为服务器提供一套功能强大、完整的 [API](https://next.api.aliyun.com/) 以及 CLI 操作方式，为自动化提供了坚实的基础。  