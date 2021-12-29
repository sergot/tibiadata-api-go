# TibiaData API in Golang

[![GitHub CI](https://github.com/TibiaData/tibiadata-api-go/workflows/build/badge.svg?branch=main)](https://github.com/TibiaData/tibiadata-api-go/actions?query=workflow%3Abuild)
[![GitHub go.mod version](https://img.shields.io/github/go-mod/go-version/tibiadata/tibiadata-api-go)](https://github.com/tibiadata/tibiadata-api-go/blob/main/go.mod)
[![Docker version](https://img.shields.io/docker/v/tibiadata/tibiadata-api-go/latest)](https://hub.docker.com/r/tibiadata/tibiadata-api-go)
[![Docker size](https://img.shields.io/docker/image-size/tibiadata/tibiadata-api-go/latest)](https://hub.docker.com/r/tibiadata/tibiadata-api-go)
[![GitHub license](https://img.shields.io/github/license/tibiadata/tibiadata-api-go)](https://github.com/tibiadata/tibiadata-api-go/blob/main/LICENSE)

TibiaData API written in Golang and deployed in container (which contains v3)

Current status of v3 is in beta and information like documentation can be found on [tibiadata.com](https://tibiadata.com/doc-api-v3/v3-beta/).

### Table of Contents

- [How to use](#how-to-use)
  - [Docker](#docker)
  - [Docker-compose](#docker-compose)
  - [Local development](#local-development)
  - [Environment variables](#environment-variables)
- [API documentation](#api-documentation)
  - [Available endpoints](#available-endpoints)
- [General information](#general-information)
- [Credits](#credits)

## How to use

You can either use it in a Docker container or go download the code and deploy it yourself on any server.

Keep in mind that there are restrictions on tibia.com that might impact the usage of the application being hosted yourself.

### Docker

Our images are available on both [GitHub Container Registry](https://github.com/TibiaData/tibiadata-api-go/pkgs/container/tibiadata-api-go) and [Docker Hub](https://hub.docker.com/r/tibiadata/tibiadata-api-go).

This is how to pull and run the _latest_ release of TibiaData from [GHCR](https://github.com/TibiaData/tibiadata-api-go/pkgs/container/tibiadata-api-go):

```console
docker pull ghcr.io/tibiadata/tibiadata-api-go:latest
docker run -p 127.0.0.1:80:8080/tcp --rm -it ghcr.io/tibiadata/tibiadata-api-go:latest
```
You can also use [Docker Hub](https://hub.docker.com/r/tibiadata/tibiadata-api-go) to pull your images from.

If you want to run the latest code you can switch from _latest_ to _main_.

### Docker-compose

_Information will be added at a later stage._

### Local development

Build the code on your computer

```console
docker build -t tibiadata .
```

Run your build locally

```console
docker run -p 127.0.0.1:80:8080/tcp --rm -it tibiadata
```

### Environment variables

_Information will be added at a later stage._

## API documentation

Current status of v3 is in beta and information like documentation can be found on [tibiadata.com](https://tibiadata.com/doc-api-v3/v3-beta/).

There will be autogenerated code-documentation available later on.

### Available endpoints

Those are the current existing endpoints.

- GET `/ping`
- GET `/health`
- GET `/v3/characters/character/:character`
- GET `/v3/creatures`
- GET `/v3/creatures/creature/:creature`
- GET `/v3/fansites`
- GET `/v3/highscores/world/:world`
- GET `/v3/highscores/world/:world/:category`
- GET `/v3/highscores/world/:world/:category/:vocation`
- GET `/v3/killstatistics/world/:world`
- GET `/v3/spells`
- GET `/v3/spells/spell/:spell`
- GET `/v3/spells/vocation/:vocation`
- GET `/v3/worlds`
- GET `/v3/worlds/world/:world`
- GET `/versions`

## General information

Tibia is a registered trademark of CipSoft GmbH. Tibia and all products related to Tibia are copyright by CipSoft GmbH.

## Credits

- Authors: Tobias Lindberg – [List of contributors](https://github.com/tibiadata/tibiadata-api-go/graphs/contributors)
- Distributed under MIT License
