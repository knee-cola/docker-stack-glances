# Docker Stack Glances

This repository contains the configuration to deploy Glances as a Docker Stack on NUC servers (nuc-server-susak and nuc-server-budakova).

## Purpose

Glances collects system info (CPU usage, free RAM, free Disk space, etc ...) which is then processed and displayed by Home Assistant instance.

## Files

- `docker-compose-deploy.yml` - Docker Compose configuration for deployment
- `deploy.sh` - Deployment script that creates the Docker stack

## Networking
The container is connected to `traefik-network` so that Home Assistant could reach it

Instead of creating a dedicated overlay network we re-use existing `traefik-network`, although it was primarily intended to be used for publishing.
