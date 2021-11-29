# Backups

We know that no one (organization) can guarantee that the ECS will always be up and running. If the ECS fails to start or fails to connect, what would happen without backups? Is this worthwhile to try?

If there is a backup, it can be restored to the state at the time of backup, greatly reducing the loss.

The best backup method is automatic backup, you can use the Snapshot function of AlibabaCloud to backup your Disk automatically.  

You can backup your disk by the below methods:  


### Set automatic Snapshot

1. 登录到阿里云控制台->存储和快照->快照

2. 打开“自动快照策略”标签 或 自己创建策略
    ![创建快照生命周期策略](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-snapshotstart-websoft9.png)

3. 在已有的快照策略下，设置磁盘（即将磁盘加入到所属的快照策略中）
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-snapshotconf-websoft9.png)

4. 下面是一个已经被设置的磁盘示例
    ![设置磁盘](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-snapshotsetdisk-websoft9.png)

### Create Custom Image

如果不做自动备份，而是手动根据需要备份，创建自定义镜像即可：

1. 登录到阿里云控制台->ECS，找到需要操作的目标实例

2. 依次打开：更多->磁盘和镜像->创建自定义镜像
   ![创建自定义镜像](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-createimage-websoft9.png)

3. 根据提示完成后续操作