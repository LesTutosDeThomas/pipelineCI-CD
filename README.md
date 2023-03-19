# pipelineCI-CD

## setup

### install vm
- on Windows: virtualbox + iso alpine 
- setup-alpine
- select disk sda
- set rootpermitpassword yes
- install, reboot, unmount iso on virtualbox
- change password root: `passwd root`
- on virtualbox set redirection host port:22 dest port:22
- on windows: ssh root@localhost

### instal docker, docker-compose on alpine
```
apk add docker docker-compose docker-cli docker-cli-compose --repository http://dl-cdn.alpinelinux.org/alpine/latest-stable/community
apk add python3
python3 -m ensurepip
pip install docker-compose
apk add vim
rc-update add docker
mkdir /training-pipeline-gitlab
cd /training-pipeline-gitlab
```
create docker-compose file:  vim docker-compose.yaml   
more info on: https://docs.gitlab.com/ee/install/docker.html
#docker-compose.yaml
```

```
mkdir gitlab_data
