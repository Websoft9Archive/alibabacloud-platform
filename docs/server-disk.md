# Disk and Storage

You need to grasp the below storage solution of AlibabaCloud:  

* [Cloud disks](https://www.alibabacloud.com/help/en/doc-detail/25381.html) for ECS
* Object Storage Service - OSS

## Create Cloud disks

1. Login to Console to list all disk by 【Elastic Compute Service】>【Storage & Snapshot】>【Disk】

2. Click the 【Create Disk】 button 
   ![Create Disk](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-createdisk-websoft9.png)

3. Set the **Storage** and **Disk Name**
   ![Set the disk](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-createdisk2-websoft9.png)

4. Attach your disk to target ECS
   ![Mout Disk](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-attachdisk-websoft9.png)

5. Then create partitions and file systems after the disk is attached to the instance

   * [Linux partitions](https://www.alibabacloud.com/help/doc-detail/25426.htm)
   * [Windows partitions](https://www.alibabacloud.com/help/en/doc-detail/25418.htm)

## Detach Cloud disks

1. Login to Console to list all disk by 【Elastic Compute Service】>【Storage & Snapshot】>【Disk】

2. Click the 【More】>【Detach】
   ![Detach Disk](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-ditachdisk-websoft9.png)

3. Go to the next steps

## Resize Disks

You can resize your **System Disk** and **Data Disk** online by console

> Resize most of time mean increase disk storage

1. Login to Console to list all disk by 【Elastic Compute Service】>【Storage & Snapshot】>【Disk】

2. Click the 【More】>【Resize Disk】
   ![Resize Disk](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-changedisks-websoft9.png)

3. Check option【[Online Resizing](https://help.aliyun.com/document_detail/35095.html)】

4. Waiting for the result


## 磁盘挂载

If you run `df -m` to list all file system and found that there not increase disk storage, how to resolve it?  

1. Connect ECS and install `growpart` for it
   ```
   yum install -y cloud-utils-growpart
   growpart /dev/vda 1
   ```

2. Add the new added disk to the first partition
   ```
   # Attach to the first partition of first disk (System Disk)
   growpart /dev/vda 1

   # Attach to the first partition of second disk (Data Disk)
   growpart /dev/vdb 1
   ```

3. Run the file system command
   ```
   # ext
   resize2fs /dev/vda1 

   # xfs
   xfs_growfs /dev/vda1 
   ```