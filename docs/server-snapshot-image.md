# Snapshot and Image

The reason we put snapshots and image together is because there is a certain relationship between the two, and even there is an alternate relationship.

## Relationship

A snapshot is a "photographing" of a disk. As the name suggests, it is to back up the data of a disk at a certain point in time. It is a backup method.

Following key information points are listed:

* A snapshot can be created based on the disk.
* A image can be created based on a snapshot, and the image cannot be directly converted into a snapshot.
* Based on the image, you can create a VM directly, and you can create a image directly based on the VM.

> Summary: (disk --> snapshot) --> (image - VM)

## Create Snapshot

1. Login to [AWS Portal](https://portal.AWS.com/)
2. Open the All Services->Compute->Snapshots
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/AWS/AWS-snapshot-websoft9.png)
3. Then, Click the "+Add" or "Create snapshot" in the Snapshots page
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/AWS/AWS-createsnapshot-websoft9.png)
4. Follow the prompts to complete the creation from **source disk** to snapshot

## Create Image

As mentioned earlier, image can be created based on snapshots, and image can be created based on VM.

### VM to Image

1. Login to [AWS Portal](https://portal.AWS.com/)
2. Open the VM, and click the "**Capture**" 
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/AWS/AWS-vmtoimage-websoft9.png)
3. Follow the prompts to complete the next steps
4. It's worth noting that the Capture operation also deletes the VM while creating the image.

### Snapshot to Image

1. Login to [AWS Portal](https://portal.AWS.com/)
2. Open the All Services->Compute->Snapshots
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/AWS/AWS-snapshot-websoft9.png)
3. You can see all image listed
4. Select the snapshot and create image for it