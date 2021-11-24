# 磁盘与存储

对于阿里云平台来说，常用的是对云盘和对象存储进行操作：  

* 云盘（磁盘）可以是单独的一种计算资源（单独创建、单独计费、单独管理等），同时也可以被集成到服务器实例，作为其中的一个组件。
* 对象存储（OSS）是一种无需绑定服务器就能使用的云储存方案，它非常类似企业网盘。

下面我们介绍常见的操作场景：  

## 增加云盘

1. 登录到阿里云控制台->ECS，点击**存储与快照**下的**云盘**

2. 点击“创建云盘”按钮
   ![创建云盘](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-createdisk-websoft9.png)

3. 设置磁盘类型，大小等，确认无误后开始创建
   ![设置磁盘](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-createdisk2-websoft9.png)

4. 将创建好的磁盘，挂载到ECS实例
   ![挂载磁盘](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-attachdisk-websoft9.png)

5. “磁盘挂载”执行成功后，需登录本实例对挂载的磁盘进行“分区格式化和挂载新分区”的操作：
    - Windows, 请参考阿里云官方文档 [Windows格式化数据盘](https://help.aliyun.com/document_detail/25418.html)
    - Linux，请参考阿里云官方文档 [Linux格式化数据盘](https://help.aliyun.com/document_detail/25426.html) 

5. 以上所有设置后方可使用磁盘

## 卸载云盘

将磁盘从ECS中解除绑定关系(卸载)，操作如下

1. 登录到阿里云控制台->ECS，点击**存储与快照**下的**云盘**

2. 找到所需卸载的磁盘，依次打开：更多->卸载
   ![卸载磁盘](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-ditachdisk-websoft9.png)

3. 根据提示完成后续操作

> 磁盘卸载后，会保留，不会被删除，可以被其他ECS挂载

## 磁盘扩容

阿里云支持在线扩容**系统盘**和**数据盘**，即无需重启ECS实例便可以完成扩容。

> 大多数情况下，磁盘只能增加大小，而不能降低大小

1. 登录到阿里云控制台->ECS，点击**存储与快照**下的**云盘**

2. 找到所需卸载的磁盘，依次打开：更多->磁盘扩容
   ![修改卷](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-changedisks-websoft9.png)

3. 选择【[在线扩容](https://help.aliyun.com/document_detail/111738.html)】方式

4. 等待扩容后的反馈


## 磁盘挂载

某些磁盘扩容后，文件系统的容量并没有增加。这个时候，就需要进行手工的磁盘挂载操作。  

1. 连接服务器，安装 `growpart` 磁盘挂载软件
   ```
   yum install -y cloud-utils-growpart
   growpart /dev/vda 1
   ```
2. 将磁盘挂载到指定磁盘的第一个分区
   ```
   # 挂载到系统盘的第一个分区
   growpart /dev/vda 1

   # 挂载到数据盘的第一个分区
   growpart /dev/vdb 1
   ```
3. 处理扩容后文件系统，以符合 Linux 要求
   ```
   # 适用于 ext 文件系统
   resize2fs /dev/vda1 

   # 适用于 xfs 文件系统
   xfs_growfs /dev/vda1 
   ```

## OSS 挂载

方案繁琐，参考[官方文档](https://help.aliyun.com/document_detail/134092.html)。  

#### OSS 设置 HTTPS

主要步骤：

1. 完成 CNMAE 域名解析以及绑定至目标 Bucket
2. 进入阿里云控制台的[云盾](https://yundun.console.aliyun.com/)下，申请一个免费赠书（有效期为一年）
3. 证书申请成功后，下载它
4. 到 Bucket 的 HTTPS 配置项中绑定证书
5. 等待几分钟，HTTPS 生效

## 场景问题

#### 推荐将 OSS 挂载到 ECS 吗？

不推荐，理由有三：

* OSS 不同于磁盘，它不是 ECS 的组成部分，挂载后后期维护难以察觉
* OSS 挂载到 ECS 涉及多层计费，财务成本和管理成本大大增加
* OSS 主要是独立的向外部提供图片和视频的载体，与ECS并没有强相关性


#### 需要 OSS 这种上传和管理的便捷性怎么办？

可以将磁盘改造成 OSS，参考：[Minio](https://github.com/Websoft9/docker-minio)
