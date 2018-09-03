# Lychee + Freedy

[![Docker Stars](https://img.shields.io/docker/stars/kolex/freedy.svg?style=flat-square)](https://hub.docker.com/r/kolex/freedy/)
[![Docker Pulls](https://img.shields.io/docker/pulls/kolex/freedy.svg?style=flat-square)](https://hub.docker.com/r/kolex/freedy/)
[![MicroBadger Layers](https://img.shields.io/microbadger/layers/kolex/freedy.svg?style=flat-square)](https://hub.docker.com/r/kolex/freedy)


![Freedy](https://i.imgur.com/hjSzeZs.jpg)

## What is Freedy?

Freedy is a free and simple RSS/ Atom reader for the browser, written in Python with Flask.

Feel free to check out our image on the [Docker Hub](https://hub.docker.com/r/kolex/freedy) as well!

## Features

- Amount of the recent posts shown of each feed can be configured
- Add as many feeds as you like

## Description

xxxxxxx

## Usage

```docker
docker run -p 5000:5000 -v /home/konstantin/Development/Docker/freedy-docker/urls.txt:/home/freedy/config/urls.tx t kolex/freedy:latest
```
