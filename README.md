# Application server
Docker compose file for a basic application server consisting of Nginx Proxy Manager (NPM) and Portainer. All other stacks connect to this instance of Portainer over port 10000.

Set the following variables in the .env file, examples are given in square brackets:
- PUID [the PUID of your user account ] 
- PGID [the PGID of your user account] 
- TZ ["Europe/London"]
- DOCKERDIR ["/home/user/docker"]

View the PUID and PGID for the current user using the ```id``` command.

Bring up the stack:
```
sudo docker-compose -p up -d
```

Applications included with this stack:
- [9000] NGINX proxy manager
- [9001] Portainer

## Post installation
There are no post installation tasks for this stack.

### Updating containers
A simple bash script for updating your docker containers: https://gist.github.com/kris-smarthome/f759238723c1fff33f24ece580359a46
