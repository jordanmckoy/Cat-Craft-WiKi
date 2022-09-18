# Setting up Instance (Portainer Server)

To set up Portainer on an instance, we need to ensure that we have the subnet ad the proper dependencies installed. \
\
Dependencies :&#x20;

* Docker
* Firewalld(Recommended) or UFW

#### Docker&#x20;

{% code overflow="wrap" %}
```
// Installing Docker on Ubuntu

// Removing Old Versions Of Docker

sudo apt-get remove docker docker-engine docker.io containerd runc
 
// Updating Packages

sudo apt-get update

// Installing Packages to Allow apt to user a repository over HTTPS
 
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release

// Adding Docker GPG key

sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

// Setting Up Repositoy 

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

// Installing Docker Engine 

// Update Packeges
sudo apt-get update

// Install Docker Engine
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin


// If you get a GPG error after sudo apt-get update run

sudo chmod a+r /etc/apt/keyrings/docker.gpg

// Then Try Installing the Docker Engine Again

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```
{% endcode %}

#### Portainer Install

To adapt to your specific setup, you can read the setup documentation [here](https://docs.portainer.io/start/install).\
\
In our case, we are setting up Portainer in a standalone docker container on a Linux VM\


Ensure that you have the ports open for Portainer on both [Oracle ](../setting-up-oracle/setting-up-oracle-subnet.md)and your [VM](firewall-setup.md). Check the previous [section](../setting-up-oracle/what-ports-to-open.md) on what ports to open for the ports to your specific installation.

<pre data-overflow="wrap"><code>//  Making Portainer Data Volume For Data Storage
sudo docker volume create portainer_data

// Making Portainer Docker Container

<strong>sudo docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest
</strong></code></pre>

You can now login to portainer via `https://localhost:9443`\
\
Replace `localhost` with the relevant IP address or FQDN if needed\


You can find out more on how to connect and finish setup of Portainer on their [web docs](https://docs.portainer.io/start/install/server/setup).



