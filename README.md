# Application server
Docker compose file for a basic application server consisting of Nginx Proxy Manager (NPM) and Portainer. All other stacks connect to this instance of Portainer over port 10000. NPM and Portainer are separated on external and internal networks. Remember to create the inside_network, outside_network and environment variables before bringing up the stack.

Create networks:
```
sudo docker network create inside_network
sudo docker network create outside_network
```

Set the following variables in the .env file, examples are given in square brackets:
- PUID= [the PUID of your user account ] 
- PGID= [the PGID of your user account] 
- TZ= ["Europe/London"]
- DOCKERDIR= ["/home/user/docker"]

View the PUID and PGID for the current user using the ```id``` command.

Bring up the stack:
```
sudo docker-compose -p application_server up -d
```

Applications included with this stack:
- [9000] NGINX proxy manager
- [9001] Portainer

## Post installation
There are no post installation tasks for this stack.