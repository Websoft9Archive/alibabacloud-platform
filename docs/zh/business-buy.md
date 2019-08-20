# 订阅

下面简单的对AWS云市场镜像类商品的订阅（购买）做一个说明：

## 方式

订阅=购买，具体的表现形式就是 [部署镜像](/zh/stack-deployment.md)

AWS平台中，由于实例采用的是按小时计费，故镜像采用的是也是按小时计费模式，除此之外没有其他模式。

* 镜像部署到实例后，实例用多长时间=镜像订阅了多长时间
* 需要取消镜像订阅，就需要删除对应的实例
* 实例停止运行，镜像停止计费？

## 费用

AWS云市场中，有免费的镜像，也有收费的镜像。

Websoft9公司在AWS平台中提供都是收费镜像，因为我们的盈利模式就是通过收费，为有意愿付费的客户提供企业级开源镜像以及技术支持服务。

> 如果您希望免费使用我们的产品，请部署我们的Ansible自动化脚本（[Github上的主页](https://github.com/websoft9)）

我们的镜像费用会根据实例CPU核数来灵活定价，一般来说核数越大，价格越高。

以我们发布的Odoo商品为例，通过商品页面的 Pricing，列出的Software镜像定价

![Websoft9价格](https://libs.websoft9.com/Websoft9/DocsPicture/en/aws/aws-mkpricing-websoft9.png)

计价方式有：Hourly和Annual两个部分，对应的就是按小时付费和包年付费。

条款如下：

``` text
Pay-per-Use: For pay-per-use images, you do not need to make payments when purchasing them. The system generates bills every hour based on the actual usage and deducts fees from your account balance.

Yearly: Yearly images are charged a one-time payment and take effect immediately upon purchase. You do not have the option to specify the start date of the images.

```

## 查看和取消

1. 登录AWS控制台
2. 点击右上角的用户名称，下拉菜单下有一个“Your Marketplace Software”项
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/aws/aws-yoursb-websoft9.png)
2. 可以查看和取消所有订阅

## EULA

最终用户许可协议（End User Licence Agreement，EULA），指的是一家公司的软件与软件的使用者所达成的协议，此协议一般出现在软件安装时。如果使用者拒绝接受这家公司的EULA，那么便不能安装此软件。

一旦您同意在AWS上使用Websoft9的镜像，即表示您已经接受了我们的[《用户许可协议》](https://support.websoft9.com/docs/legal/zh/eula)