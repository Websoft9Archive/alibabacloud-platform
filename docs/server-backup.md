# Backups

We know that no one (organization) can guarantee that the ECS will always be up and running. If the ECS fails to start or fails to connect, what would happen without backups? Is this worthwhile to try?

If there is a backup, it can be restored to the state at the time of backup, greatly reducing the loss.

The best backup method is automatic backup, you can use the Snapshot function of AlibabaCloud to backup your Disk automatically.  

You can backup your disk by the below methods:  


### Set automatic Snapshot

1. Login to Console, open:【Elastic Compute Service】>【Storage & Snapshots】>【Snapshots】

2. Click the 【Automatic Snapshot Policies】to list and create a policy for you
    ![create Snapshot policy](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-snapshotstart-websoft9.png)

3. **Apply or Disable Automatic Snapshot Policy** for your disk
   ![Apply or Disable Automatic Snapshot](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-snapshotconf-websoft9.png)

4. Then you can see that you disk have set snapshot successfully
    ![Disk snapshot](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-snapshotsetdisk-websoft9.png)

### Create Custom Image

If you don't want to set Snapshot, you can create a custom image for your ECS

1. Login to Console and list all ECS

2. Open the menu 【Disk and Image】>【Create Custom Image】 for your target ECS
   ![Create custom image](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-createimage-websoft9.png)

3. Go to the next steps