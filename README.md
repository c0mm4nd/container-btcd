# container-btcd

![example workflow](https://github.com/c0mm4nd/container-btcd/actions/workflows/ghcr.yml/badge.svg)

This repo is just a temporary solution for [btcd issue#1833](https://github.com/btcsuite/btcd/issues/1833)

last manual updated at 2023-08-04

## Release

Container locates in https://github.com/C0MM4ND/container-btcd/pkgs/container/container-btcd

## Usage

Please refer https://github.com/btcsuite/btcd/blob/master/docs/using_docker.md, **replacing all `btcsuite/btcd:latest` to `ghcr.io/c0mm4nd/container-btcd:dev`**

e.g. 

```bash
docker run ghcr.io/c0mm4nd/container-btcd:dev
```

```yml
version: "3"

services:
  btcd:
    container_name: btcd
    hostname: btcd
    image: ghcr.io/c0mm4nd/container-btcd:dev
    restart: unless-stopped
    volumes:
      - /mnt/hdd14t:/root/.btcd
    ports:
      - 8333:8333

```
