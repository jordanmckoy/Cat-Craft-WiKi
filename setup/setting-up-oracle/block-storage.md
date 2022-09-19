# Block Storage

Block storage is an optional (but useful!) addition to your Minecraft server. At launch, oracle provides \~45 gigs of storage to your instance. It does not take long to fill up that space with a larger Minecraft world. However, we can add an additional 145 gigs of storage in a Block Volume, for larger worlds, or additional databases and backups. It's a few extra steps, but well worth your time.&#x20;

Navigate to the Storage tab, and click on Block Volume.&#x20;

![](<../../.gitbook/assets/image (12).png>)

From there, you'll want to Select Create Block Volumes.\
![](<../../.gitbook/assets/image (1) (1).png>)

From there, you'll want to Create a Block Volume. Remember when I said remembering the instance was going to be important later? This is the later. Whatever domain the instance is running on, the block volume MUST be on that same domain. Failure to do so will mean you won't be able to properly mount your boot volume to the server. I have set my block volume to 100 gigs, because I have additional things running on this instance. IF you're only running one instance on a free Oracle account, you should be able to set your block volume to 145 GB, and still stay within the free confines of your account. \
![](<../../.gitbook/assets/image (10) (1) (1).png>)

With that, your Block Volume should be allocated. Now we just need to link it to the instance.\
![](<../../.gitbook/assets/image (6) (1).png>)

Scrolling down on the Block Volume Page, you'll find an Attached Instances option. Opening that, and it will give you the option to add a new instance to your Block Volume. \
![](<../../.gitbook/assets/image (1).png>)

Scroll down to the Instances section, and select your instance from the pre-generated list. \
![](<../../.gitbook/assets/image (9) (1).png>)

After you hit the attach button, it should look like this.\
![](<../../.gitbook/assets/image (2) (2).png>)\
