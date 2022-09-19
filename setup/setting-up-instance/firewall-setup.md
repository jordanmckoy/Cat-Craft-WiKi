# Firewall Setup

By default, Ubuntu instances come with UFW installed. We have found that UFW has some weird behaviour with Oracles Subnets, so we use the [Firewalld package](https://www.redhat.com/sysadmin/secure-linux-network-firewall-cmd) instead.

```
// Update Packages
sudo apt update

//Removes UFW and then install Firewalld
sudo apt -y purge ufw && sudo apt -y install firewalld 

//Enables Firewalld on startup

sudo systemctl enable firewalld

//Starts Firewalld

sudo systemctl start firewalld

//Restarts Firewalld

sudo systemctl restart firewalld

// Get Status of Firewalld

sudo systemctl status firewalld

// Open Port 

sudo firewall-cmd --permanent --add-port=<port>/<Protocol> TCP or UDP

// Remove Port 

sudo firewall-cmd --permanent --remove-port=<port>/<Protocol> TCP or UDP

// Reload Firewall <- Required after an update to firewall rules 

sudo firewall-cmd --reload
```
