# 创建

下面介绍阿里云上创建服务器实例的说明。

创建实例最基本的条件是需要给服务器准备一个系统盘的启动模板文件，这个模板最常见的表现形式就是镜像文件

下面介绍基于镜像创建云服务器的操作步骤：

## 创建ECS

1. 登录到阿里云管理控制台，以此打开：【云服务器 ECS】>【实例】>【创建实例】，
   ![进入ecs控制台](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-createecs-websoft9.png)

2. 选择计费方式、实例类型等
   ![选择ECS规格](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-guige-websoft9.png)

   - 包年包月：一口价包干付费制
   - 按量付费：按小时付费，用一小时给一小时的钱
   - 抢占式实例：按小时付费，但每个小时价格会发生变化，例如：0.07--0.8之间波动，最高价0.8是自行设置，当阿里云价格超过0.8这个最高值之时，ECS将自动释放

3. 在镜像一栏，有多种选择。
   - 公共镜像：阿里云官方提供的操作系统镜像
   - 自定义镜像：用户自己的镜像
   - 共享镜像：其他人共享给用户的镜像
   - 镜像市场：由阿里云云市场伙伴提供的镜像（Websoft9 是这种镜像市场的主要供应商之一）

4. 如果选择镜像市场，可以通过搜索关键件词“websoft9”，列出我们相关镜像
   ![选择Websoft9镜像](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-searchw9image-websoft9.png)

4. 选择一个你所需的镜像，开始创建ECS实例

5. 后续动作基本都会要求用户完成：网络和安全组、密码、公网带宽等设置

6. 等待几分钟，ECS创建完成后，镜像会作为ECS实例的系统盘启动，即镜像自动部署到实例中

## 秘钥对

在创建ECS时，如下采用秘钥对作为登录凭证，需要提前创建秘钥对

1. 登录控制台，打开：【云服务器 ECS】>【实例】>【创建实例】>【秘钥对】，点击“**创建秘钥对**”按钮
   ![创建秘钥对](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-createkeys-websoft9.png)

2. 为秘钥对命名，例如“myKey”

3. 点击确认后系统会自动将秘钥对文件 myKey.pem 保存到本地电脑