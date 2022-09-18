# Setting Up Instance (Pterodactyl Panel - Standalone)

{% hint style="danger" %}
**N.B.** It is recommended that you read the docs. The method below is an installation script that automates the installation of Pterodactyl and is not supported by Pterodactyl Panel.
{% endhint %}

Pterodactyl Panel Docs - [https://pterodactyl.io/project/introduction.html](https://pterodactyl.io/project/introduction.html)

Pterodactyl has two main services that get installed to run, Pterodactyl Panel and Pterodactyl Wings.\
\
Panel is the web GUI for the service and is what the user will be interacting with to execute tasks.\
\
Wings is a way for the computer that you want the server to run on to communicate with the panel.\
\
Other services :&#x20;

* MariaDB/MySQL - This is a relational database that is responsible for data storage for use by the panel
* Redis - Redis is a caching solution to enable quick data queries
* Nginx - Used as a webserver
* CertBot - SSL certificate generation
* PHP - For the Panel

Installation Script Instructions\
\
`git clone https://github.com/TypicalTropic/pterodactyl-installer-script.git`&#x20;

`cd pterodactyl-installer-script`&#x20;

`bash install.sh`&#x20;

Follow the prompts =)
