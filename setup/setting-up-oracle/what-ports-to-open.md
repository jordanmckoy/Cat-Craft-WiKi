# What Ports To Open?

The services that are going to be running on the server will dictate what firewall ports are being open.\
\
If you are using Portainer you will need to add the ports:

* 9443 For the Web GUI&#x20;
* 9001 For the Client (This is on the servers you intend on managing)

Pterodactyl Panel (Web GUI) Requires :&#x20;

* 80 TCP HTTP Connection
* 443 TCP HTTPS Connection
* 3306 TCP if you want to access the database

Pterodactyl Wings (Client) Requires:&#x20;

* 8080 TCP Wings Port For Communication
* 25565 TCP Minecraft Default Port

Optional Ports&#x20;

* 8100 TCP Bluemap
* 8804 TCP Plan Player Analytics
* 3306 TCP For MariaDB/MySQL Databases
* 19132 UDP Geyser

