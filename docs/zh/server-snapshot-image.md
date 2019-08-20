# 快照与镜像

之所以我们把快照和镜像放在一起描述，是因为这两者有一定的关联，甚至说有互生关系。

## 关系

此处不对快照和镜像进行抽象概念描述，只列出如下几个关键信息点：

* 基于磁盘可以创建一个快照。

  快照是对磁盘进行“拍照”，顾名思义就是备份某个时间点卷（磁盘）的数据，是一种备份手段

* 基于快照可以创建一个镜像，而镜像无法直接转换成快照。

* 基于镜像可以直接创建一个实例，基于实例也可以直接创建一个镜像

总结：（卷-->快照） --> （镜像--实例）

## 创建快照

对于AWS来说，基于卷来创建快照

1. 登录到AWS控制台，打开EC2 Dashboard
2. 打开ELASTIC BLOCK STORE下的卷功能，选择一个卷后，实现“创建”快照操作
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aws/aws-createsnapshot-websoft9.png)
3. 给快照命名后，开始创建

## 创建镜像

前面讲过，基于快照可以创建镜像，基于实例也可以创建镜像

### 实例创建镜像

1. 登录到AWS控制台
2. 打开需要创建镜像的实例，打开：操作->映像->创建镜像
![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aws/aws-ec2toimage-websoft9.png)
3. 根据提示完成后续步骤

### 快照创建镜像

1. 登录到AWS控制台，进入EC2 Dashboard
2. 找到ELASTIC BLOCK STORE下的快照功能，列出所有快照
3. 选择所需的快照，对它进行创建镜像操作
   ![打开快照](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aws/aws-snapshot-websoft9.png)