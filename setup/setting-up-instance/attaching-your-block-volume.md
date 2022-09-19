# Attaching Your Block Volume

Now that you've connected to your instance, we need to get your Block Volume attached via PowerShell, so we can actually access that additional disk space.&#x20;

In the Termius window, type **sudo -s** and hit enter. This sets you as the root user. Every time you launch Termius, this should be the first command you run. \
![](<../../.gitbook/assets/image (14).png>)

Back on your Oracle Instance, scroll down to the bottom, and select Attached Block Volumes. \
![](<../../.gitbook/assets/image (26).png>)

Select ISCSI Commands and Information. A window will pop up, click on LInux. That should bring you to this page. \
![](<../../.gitbook/assets/image (13).png>)

Under the Connect field, hit the copy button. Back in Termius, paste those 3 lines as one, using Ctrl+Shift+V and hit enter.\
![](<../../.gitbook/assets/image (3).png>)

Next, enter **sudo mkfs -t ext4 /dev/sdb** \
****![](<../../.gitbook/assets/image (23).png>)****

Enter **lsblk -f**\
****![](<../../.gitbook/assets/image (21).png>)****

**sudo mkdir /mnt/minecraft**

**sudo blkid**\
****![](<../../.gitbook/assets/image (11).png>)****

You'll want to copy and paste the sdb UUID to a notepad, for later use. \
![](<../../.gitbook/assets/image (17) (1).png>)

**sudo nano /etc/fstab**\
****![](<../../.gitbook/assets/image (15).png>)****

At the bottom of this document, you'll want to paste in your UUID, followed by this information, and shown here. \
**UUID="UUID goes here" /mnt/minecraft ext4 defaults,noatime,\_netdev 0 2**\
****![](<../../.gitbook/assets/image (18).png>)****

Ctrl+X, and then Y after this window pops up. \
![](<../../.gitbook/assets/image (10).png>)

**sudo mount -a**

**df -aTh**\
****This is checking to make sure the Block Volume is properly mounted. At the very bottom of the list, you should see /dev/sdb, with a size of \~143G. This will indicate that your block volume is correctly attached to your instance.\
![](<../../.gitbook/assets/image (4) (2).png>)



