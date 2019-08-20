# Backups

We know that no one (organization) can guarantee that the VM will always be up and running. If the VM fails to start or fails to connect, what would happen if there was no backup? Is this less worthwhile to try?

If there is a backup, it can be restored to the state at the time of backup, greatly reducing the loss.

AWS Portal-> All service ->Storage, the "Recovery Services vaults" service is for backup of VM:

![Recovery Services vault](https://libs.websoft9.com/Websoft9/DocsPicture/en/AWS/AWS-backuprs-websoft9.png)



Below we explain how to set up backups for existing VMs and create VMs.

## Existing VM settings

For the VM that has been created, set the automatic backup strategy, please refer to the following figure.

![set backcup](https://libs.websoft9.com/Websoft9/DocsPicture/en/AWS/AWS-backupstart-websoft9.png)

## Create VM settings

When creating a VM, we can set up automatic backup mode.

1. Create a VM, backup items under the Management tab, Enable backup
   ![enable backup](https://libs.websoft9.com/Websoft9/DocsPicture/en/AWS/AWS-backupmanage-websoft9.png)

2. Select an already created vault name or create a new vault name and set a backup policy
   ![backup policy](https://libs.websoft9.com/Websoft9/DocsPicture/en/AWS/AWS-backuppolicy-websoft9.png)

3. Increasing the frequency of backups is a good choice when budget allows.