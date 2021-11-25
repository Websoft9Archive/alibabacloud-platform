# Image Deployment

Websoft9 have published hundred of images on AlibabaCloud Marketplace, customers (IT professionals and developers) can discover, try to buy these open source solution built for AlibabaCloud

>  Do you want to deploy images of Websoft9, click [Here](https://marketplace.alibabacloud.com/store/2116499.html) to list all images of Websoft9 on AlibabaCloud Marketplace

How to deploy image on AlibabaCloud? There are three methods:


## Deployment By Marketplace

1. Login to [AlibabaCloud Marketplace](https://marketplace.alibabacloud.com) or [Websoft9 on AliababaCloud](https://marketplace.alibabacloud.com/store/2116499.html)

2. Search the keyword `websoft9`, list all the image of Websoft9
   ![Search websoft9 image](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-searchwebs9-websoft9.png) 

3. Access to product detail page and click the 【Choose Your Plan】 button
   ![Buy websoft9 image](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-buyproduct-websoft9.png) 

4. Then you should start the process to get a suitable ECS for product
   ![Buy websoft9 image](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-buyproductecs-websoft9.png) 

5. When you complete the buy process, you have obtain an usable product and matched ECS 


## Deployment By Console

When you create a new ECS by Console, you can deploy Websoft9's image very easy

1. Login to console, open【Elastic Compute Service】>【Instances】, click button 【Create Instance】
   ![create instance](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-createcs001-websoft9.png)

2. At the 【Image】configuration, select the 【Marketplace Image】
   ![Marketplace Image](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-images-1-websoft9.png)

3. Search the keyword `websoft9`, list all the image of Websoft9
   ![Search websoft9 image](http://libs.websoft9.com/Websoft9/DocsPicture/en/alicloud/aliyun-images-2-websoft9.png)

4. Complete the next steps for running ECS

5. When you complete the create process, you have obtain an usable product and matched ECS 

## Deployment By Replacing Disk

If you have a running ECS, you can also deploy our image buy **replacing System Disk**

> Replace System Disk will clear all data of system disk of ECS, make sure this is suitable for you

1. Login to Console, Stop your ECS

2. Then open:【More】>【Disk and Image】>【Replace System Disk】
   ![Replace System Disk](https://libs.websoft9.com/Websoft9/DocsPicture/en/alicloud/aliyun-changesysdisk-websoft9.png)

2. Start to list the images by searching 【websoft9】, then select one product you want to use
   ![Replace System Disk](http://libs.websoft9.com/Websoft9/DocsPicture/en/alicloud/aliyun-images-2-websoft9.png)

3. Set your new password and waiting for the ECS restarting

In addition to the image deployment, you can git our [Ansible Scripts on Github](https://github.com/websoft9) for Ansible automation.