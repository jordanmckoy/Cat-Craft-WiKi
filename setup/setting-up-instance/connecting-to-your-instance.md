# Connecting To Your Instance

There are many ways to connect to your instance via PowerShell. Personally, I like using [Termius](https://termius.com), and that's what will be shown throughout this example.&#x20;

Open Termius, and in the upper left hand corner, you should see a small Gear Icon.&#x20;

![](<../../.gitbook/assets/image (2) (1).png>)

Within your Preferences section, you'll want to click on Keychain, to setup your new Instances Private Key. \
![](<../../.gitbook/assets/image (8).png>)

Click on New, and a side window should pop open. You'll want to fill out Set a Label, and then drag and drop your key file into the bottom box, and hit Export to Host.\
![](<../../.gitbook/assets/image (25).png>)

With your key file setup, we can now add the instance, and connect to it. In the Hosts panel, select Add. A window should pop in on the right. ![](<../../.gitbook/assets/image (24).png>)\


Label will be the name of the server you wish to connect to. The username, and address we'll get from Oracles Instance webpage, and the key file, should be found in your keychain. You just need to select the appropriate file.&#x20;

To find your username and Address, go back to Oracles Instance page, and under Instance Access, both are listed. Just copy and paste into your Termius Host setup. \
![](<../../.gitbook/assets/image (22).png>)

With that information saved, we can now connect to our instance for the first time. Simply double click on your instance name, select Add and Continue on the warning sign. and you're in. \
![](<../../.gitbook/assets/image (20).png>)

####
