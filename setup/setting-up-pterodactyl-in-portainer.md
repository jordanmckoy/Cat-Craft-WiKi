# Setting Up Pterodactyl in Portainer

{% hint style="danger" %}
N.B. If you haven't read [setting-up-instance-portainer-agent.md](setting-up-instance/setting-up-instance-portainer-agent.md "mention") go and read it as it is a requirement to continue.
{% endhint %}

#### Panel

Log into Portainer and select the environment that you set up had set up on Portainer agent.

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

Select any of the highlighted areas in the picture below

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

Select Add Stack

<figure><img src="../.gitbook/assets/image (4) (2).png" alt=""><figcaption></figcaption></figure>

After reading [panel-docker-compose-file.md](../resources/panel-docker-compose-file.md "mention") you can edit the values as you need, I'm going to leave it as default. Paste the config file here in the web editor

<figure><img src="../.gitbook/assets/image (16) (1).png" alt=""><figcaption></figcaption></figure>

You can now deploy the stack and you will be golden.

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

You can now see all the stack you deployed

<figure><img src="../.gitbook/assets/image (17) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

To access your webpage, navigate to the [FQDN ](https://www.google.com/search?q=fqdn\&rlz=1C1GCEA\_enJM1022JM1022\&oq=FQDN\&aqs=chrome.0.0i67j0i512l9.1960j0j7\&sourceid=chrome\&ie=UTF-8)you set or the ipaddress in your browser.

Wings

To deploy wings it is the same as above but with a different config file. The wings config file can be found at [wings-docker-compose-file.md](../resources/wings-docker-compose-file.md "mention"). \


{% hint style="info" %}
If you use Lets Encrypt while installing the panel you will need to generate a certificate for your wings install and remove the # from infront of the option

`#- "/etc/letsencrypt/:/etc/letsencrypt/"`

Read this [article](https://pterodactyl.io/tutorials/creating\_ssl\_certificates.html) to learn on how to generate this certificate
{% endhint %}

To link your wings to the panel you can follow this [guide](https://pterodactyl.io/community/config/nodes/add\_node.html#configuring-the-node).
