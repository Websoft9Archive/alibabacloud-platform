# 操作

下面是一些常见的ECS操作

## 启动、停止和终止

在ECS控制台可以对实例状态进行修改，包括：

- 启动
- 停止
- 重启
- 释放
- 升降配

释放=删除ECS，使用于按量购买的服务器

## 重置密码

忘记密码，可以通过阿里云控制台重置：

1. 登录到阿里云控制台，找到所需操作的ECS

2. 点击下面的“重置实例密码”，输入新密码
   ![调整配置](https://libs.websoft9.com/Websoft9/DocsPicture/en/alicloud/aliyun-resetpw-1-websoft9.png)
   
   ![调整配置](https://libs.websoft9.com/Websoft9/DocsPicture/en/alicloud/aliyun-resetpw-2-websoft9.png)
   
3. 重启ECS实例，方可生效

## 升降配

ECS的配置可以调整，具体操作如下：

1. 登录到阿里云控制台，找到所需操作的ECS
2. 点击右侧的“升降配”，选择一种变更方案
   ![调整配置](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-changeecsconfigure-websoft9.png)
3. 依据相关的操作向导完成变更

## 重新初始化磁盘

如果你想将服务器恢复到刚安装之时的状态，就需要用到**重新初始化镜像**操作。

1. 登录到阿里云控制台，找到所需操作的ECS
2. 停止ECS示例
2. 依次打开：更多->磁盘和镜像->重新初始化镜像
   ![获取系统日志](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-iniecs-websoft9.png)
3. 根据系统提示完成后续步骤

> 建议仔细理解**更换系统盘**和**重新初始化镜像**的差异