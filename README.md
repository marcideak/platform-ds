
# Docker swarm based application platform - with traefik, portainer, prometheus, grafana

* Get a free linux (preferred: Ubuntu 20.04 LTS) from any of the cloud providers
(google, aws, azure, oracle)

## First steps till the portainer platform:
In linux terminal (refresh your linux repo, update your installation):
* sudo apt update
* sudo apt install
* sudo reboot

## Install portainer 
(based on: https://docs.portainer.io/v/ce-2.9/start/install/server/swarm/linux)
> curl -L https://downloads.portainer.io/portainer-agent-stack.yml \
    -o portainer-agent-stack.yml
    
### Deploy the portainer stack:
> sudo docker stack deploy -c portainer-agent-stack.yml portainer

After this stack deploy,  the portainer UI is ready on your public ip(url) at port 9000:

http://mypublicipurl:9000

github ci/cd pileline - github action is built in [check the docker-image.yml file] (.github/workflows/docker-image.yml) , 
so if you modify the .net core application source code, the action will be triggered, 
docker image will be built, and pushed to my repository


## if you clone this
** don't forget to change the docker image tagging from azitmentor (this is my docker hub account), to your docker hub account
