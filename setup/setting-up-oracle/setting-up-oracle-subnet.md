# Setting Up Oracle Subnet

Now that your tea is brewed, it's time to get started setting up the ports you'll need to run a Minecraft server. Some of these will be optional, so only include the ones you'll actually need to make your server run. There are other ports that might need to be opened in the future, for other possible mods and add-ons. Follow these same steps, with the appropriate port numbers, to get everything setup.&#x20;

Under the Primary VNIC section of the Instance homepage, you should find a link to the subnet. Open that link.

![](<../../.gitbook/assets/image (8).png>)

Under Security Lists, click on Default Security List ![](<../../.gitbook/assets/image (3).png>)

Click on Add Ingress Rule

![](<../../.gitbook/assets/image (5).png>)

In the Add Ingress Rules panel, set your Source CIDR to 0.0.0.0/0, your destination port to whatever port number you need to open, and throw in a quick label, so you don't forget what each option is for. 99% of the time, you'll want to open ports on TCP. The only exception that I can think of at this point in time, is if you're setting up Geyser, in which case it is a UDP port. Additional information can be found on the Geyser setup wiki, if you so desire.

![](<../../.gitbook/assets/image (4).png>)
