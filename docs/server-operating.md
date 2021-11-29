# Manage

These steps for you to manage ECS

## Start, Stop and Release

You can manage the ECS on Console, includes:

- Start
- Stop
- Restart
- Release
- Upgrade/Downgrade

Release ECS mean delete it, suitable for a pay-as-you-go instance that is not locked

## Reset password

You can reset the ECS's password by the flowing method: 

### Reset by Console

1. Login to AlibabaCloud console, list the ECS

2. Open the menu:【Password/Key Pair】>【Reset Password】
   ![reset password](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-resetpw-1-websoft9.png)
   ![reset password](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-resetpw-2-websoft9.png)

3. Restart the ECS and it take effect

### Reset by Command

1. Login to AlibabaCloud console, list the ECS

2. Open the menu:【Connect】>【Send remote call】

3. Input your command like below click 【Run】 button
   ```
   echo "yourpassword" | passwd --stdin root  
   ```
4. You can receive below message when running successfully
   ```
   Changing password for user root.
   passwd: all authentication tokens updated successfully.
   ```

## Upgrade/Downgrade

If you want to change the ECS configuration for business, you should Upgrade or Downgrade it

1. Login to AlibabaCloud console, list the ECS

2. Open the 【Upgrade/Downgrade】menu of the target ECS
   ![upgrade](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-changeecsconfigure-websoft9.png)

3. You can choose from the following upgrade or downgrade schemes

## Reinitialize Disk

If you want to recover to ECS to the state of first installation, you need 【Reinitialize Disk】operation: 

1. Login to AlibabaCloud console, list the ECS

2. Stop your the target ECS

2. Open the menu: 【More】>【Disk and Image】>【Reinitialize Disk】
   ![Reset System disk](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-changesysdisk-websoft9.png)

3. Go to the next steps

> Could you distinguish **Reinitialize Disk** and **Replace System Disk**?

## API/CLI

You can use [API/CLI](https://next.api.aliyun.com/) to manage ECS except console