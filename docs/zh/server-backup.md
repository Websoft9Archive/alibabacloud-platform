# 备份

我们知道任何人（组织）都无法保证ECS永远正常运行状态。假如ECS出现无法启动或无法连接的故障，若没有备份会是什么样的后果？这样的教训是否值得尝试？

如果有备份，就能够恢复到备份之时的状态，大大降低损失。

阿里云中对ECS实现备份的基本原理就是对ECS所属的磁盘做自动快照。

阿里云控制台提供了两种快照备份入口：


### 自动快照

1. 登录到阿里云控制台->存储和快照->快照
2. 打开“自动快照策略”标签 或 自己创建策略
    ![创建快照生命周期策略](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-snapshotstart-websoft9.png)
3. 在已有的快照策略下，设置磁盘（即将磁盘加入到所属的快照策略中）
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-snapshotconf-websoft9.png)
4. 下面是一个已经被设置的磁盘示例
    ![设置磁盘](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-snapshotsetdisk-websoft9.png)

### 创建自定义镜像

如果不做自动备份，而是手动根据需要备份，创建自定义镜像即可：

1. 登录到阿里云控制台->ECS，找到需要操作的目标实例
2. 依次打开：更多->磁盘和镜像->创建自定义镜像
   ![创建自定义镜像](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-createimage-websoft9.png)
3. 根据提示完成后续操作