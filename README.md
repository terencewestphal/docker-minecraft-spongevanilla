[![Docker Build Statu](https://img.shields.io/docker/build/terencewestphal/minecraft-spongevanilla.svg)](https://hub.docker.com/r/terencewestphal/minecraft-spongevanilla/builds/) ![Docker Stars](https://img.shields.io/docker/stars/terencewestphal/minecraft-spongevanilla.svg) [![Docker Pulls](https://img.shields.io/docker/pulls/terencewestphal/minecraft-spongevanilla.svg)](https://hub.docker.com/r/terencewestphal/minecraft-spongevanilla/) 

[![SpongeVanilla](https://github.com/terencewestphal/docker-minecraft-spongevanilla/blob/master/logo.png?raw=true)](https://www.spongepowered.org) 

# Docker - Minecraft SpongeVanilla

- Minimalistic and simple to configure.
- Works out-of-the-box. Defaults are provided if no volume is mounted.
- Based on the [Docker Minecraft](https://hub.docker.com/r/terencewestphal/minecraft/) image.

## Supported tags and Dockerfile

- `1.12-7.0.0-BETA-277`, `1.12-7.0.0-BETA-288`, `develop` ([Dockerfile](https://raw.githubusercontent.com/terencewestphal/docker-minecraft-spongevanilla/develop/Dockerfile))
- `1.11.2-6.1.0-BETA-6`, `latest` ([Dockerfile](https://raw.githubusercontent.com/terencewestphal/docker-minecraft-spongevanilla/1.11.2-6.1.0-BETA-6/Dockerfile))


## Pull  

Get the latest version:
```
docker pull terencewestphal/minecraft-spongevanilla:latest
```

## Build  

Build the latest Minecraft version and tag the image:   
```
docker build -t minecraft-spongevanilla .
```

Optional: Build with a specific Minecraft version:   
```
docker build --build-arg VERSION=1.12-7.0.0-BETA-288 -t minecraft-spongevanilla .
```

## Run
  
Run with default settings:
```
docker run -d -p 25565:25565 --name spongevanilla terencewestphal/minecraft-spongevanilla
```

Run with volume mounted: 
```
docker run -d -p 25565:25565 -v $PWD:/srv/minecraft --name spongevanilla terencewestphal/minecraft-spongevanilla
```

## Interactive Mode 

Attach an interactive console in order to use the SpongeVanilla server commands:
```
docker attach spongevanilla
```