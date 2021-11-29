# Snapshot and Image

The reason we put snapshots and image together is because there is a certain relationship between the two, and even there is an alternate relationship.

## Relationship

A snapshot is a "photographing" of a disk. As the name suggests, it is to back up the data of a disk at a certain point in time. It is a backup method.  

Following key information points are listed:

* A snapshot can be created based on the disk.
* A image can be created by snapshot, and the image cannot be directly converted into a snapshot.
* You can create a ECS directly based on Image, and you can create a image directly based on the ECS.

> Summary: (disk --> snapshot) --> (image - VM)


## Create Snapshot

1. Login to AlibabaCloud console, lis all disk by 【Elastic Compute Service】>【Disk】

2. Click the【Create Snapshot】 button to start it
   ![disk to snapshot](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-disktosnapshot-websoft9.png)
   
3. Go to the next steps to complete it

## Create Image

Image can be created based on snapshots, and image can be created based on ECS.

### By ECS

1. Login to AlibabaCloud console, lis all ECS by 【Elastic Compute Service】>【Instances】

2. Click the menu 【Disk and Image】>【Create Custom Image】
   ![create image](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-createimage-websoft9.png)

3. Go to the next steps to complete it

### By Snapshot

1. Login to AlibabaCloud console, lis all disk by 【Elastic Compute Service】>【Storage & Snapshots】>【Snapshots】

2. Select your Snapshot and create an Image for it
   ![create image](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-snapshottoimage-websoft9.png)

3. Go to the next steps to complete it

### By local image

You can also create Image by OSS file which is your uploaded your local image

1. Login to AlibabaCloud console, lis all ECS by 【Elastic Compute Service】>【Instances and Images】>【Images】

2. Then click the **Import Image** link to create image by OSS file
   ![create image by OSS file](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/alibabacloud-importimage001-websoft9.png)

3. Set the parameters and you must select the correct **Operating System/Platform** for you image

   > What the difference between 【Others Linux】 and 【Customized Linux】? refer to [here](https://help.aliyun.com/document_detail/48226.html)

   ![](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/alibabacloud-importimage002-websoft9.png)


> If you upload OracleLinux to create image, you should select the CentOS