# Setting Up Instance (Portainer Agent)

The Portainer Agent is a docker container that will be responsible for connecting your Virtual Machine instance to the [Portainer Server](setting-up-instance-portainer-server.md) we set up in the last section.

The Portainer agent also runs in a Docker container, so ensure that you have [Docker installed](setting-up-instance-portainer-server.md#docker) and the port 9001 open on your firewall.&#x20;

In the last section after installing docker we also started a container for the Portainer Server. This is the only change from the last section. This can  run on the same instance as the Portainer Server or on a remote server.

```
// Portainer Agent Docker Container

sudo docker run -d -p 9001:9001 --name portainer_agent --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v /var/lib/docker/volumes:/var/lib/docker/volumes portainer/agent:latest
```

To connect the Portainer Agent to the Portainer Server, follow this guide below =)

[https://docs.portainer.io/admin/environments/add/docker](https://docs.portainer.io/admin/environments/add/docker)
