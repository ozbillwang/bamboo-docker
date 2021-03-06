# Bamboo Agent
[matisq/bamboo-agent](https://hub.docker.com/r/matisq/bamboo-agent/) is a docker image to use with an [Atlassian Bamboo Agent](https://www.atlassian.com/software/bamboo) based on [phusion/baseimage-docker](https://github.com/phusion/baseimage-docker)

## Documentation
[Here](https://github.com/matisku/bamboo-docker/blob/master/doc/README.md) you can find info how to setup [Bamboo on Rancher](https://github.com/matisku/bamboo-docker/blob/master/doc/README.md).

## Info
This is a part of a [Bamboo Stack](https://github.com/matisku/bamboo-docker). You can download [docker-compose.yml](https://github.com/matisku/bamboo-docker/blob/master/docker-compose.yml) and check out how it works!

**Bamboo Stack** is also available in my custom [rancher-stack](https://github.com/matisku/rancher-catalog), so with just a few clicks you can use, scale and upgrade it!

## Usage
Agent can connect to already running Bamboo Server:
```
docker run \
  -e AGENT_VERSION=5.15.3 \
  -e BAMBOO_SERVER=192.168.0.12 \
  -e BAMBOO_SERVER_PORT=8085 \
  -e PACKAGES="mc firefox" \
  matisq/bamboo-agent
```

## Variables
* `AGENT_VERSION` - This should match the version of Bamboo Server
* `BAMBOO_SERVER` - URL or IP of Bamboo Server where agent should be attached
* `BAMBOO_SERVER_PORT` - External port of Bamboo Server UI. In case of using docker-compose stack, this can be linked name.
* `PACKAGES` - space separated list of additional packages which should be installed on Bamboo Agent

## Metadata
[![](https://images.microbadger.com/badges/image/matisq/bamboo-agent.svg)](http://microbadger.com/images/matisq/bamboo-agent "Get your own image badge on microbadger.com")

## Contributors
Any forks are welcome!
