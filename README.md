# Lychee + Freedy

[![Docker Stars](https://img.shields.io/docker/stars/kolex/freedy.svg?style=flat-square)](https://hub.docker.com/r/kolex/freedy/)
[![Docker Pulls](https://img.shields.io/docker/pulls/kolex/freedy.svg?style=flat-square)](https://hub.docker.com/r/kolex/freedy/)
[![MicroBadger Layers](https://img.shields.io/microbadger/layers/kolex/freedy.svg?style=flat-square)](https://hub.docker.com/r/kolex/freedy)


![Freedy](https://i.imgur.com/hjSzeZs.jpg)

## What is Freedy?

Freedy is a free and simple RSS/ Atom reader for the browser, written in Python with Flask. Using Bootstrap as a mobile-first web framework, we were able to create a nice looking webapp for every kind of device.

Feel free to check out our image on the [Docker Hub](https://hub.docker.com/r/kolex/freedy) as well!

## Features


- Looks great on tablets, phones etc. thanks to Bootstrap.
- Compatible with RSS and Atom feeds.
- Add as many feeds as you like!
- Amount of the recent posts shown of each feed can be configured.
- Simple deployment via Docker and Docker Compose


## Description

The image contains the Python code and installs the dependencies automatically. When starting the container, it runs a gunicorn (web) server exposed on port 5000.

## Usage

```docker
docker run -d -it \
  --name freedy \
  --restart unless-stopped \
  -p 5000:5000 \
  -v ./urls.txt:/home/freedy/config/urls.txt
  kolex/freedy:1.0.0
```

You need to provide a urls.txt in your current working directory for this run command to work. In this file you need to enter one Atom/RSS feed URL per line. Again, this directly exposes the gunicorn service without any security measures, so it is heavily recommended
to put the app behind a reverse proxy such as nginx.

For production usage, we also provide a [docker-compose.yml file](https://github.com/konstantingoretzki/freedy-docker/blob/master/docker-compose.yml), which makes the deployment a little simpler. Please note that the urls.txt file needs to reside in the same directory as the compose file.
