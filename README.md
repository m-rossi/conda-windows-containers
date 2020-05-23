# Conda for Windows containers

This repository contains the Dockerfiles to build Windows containers with [conda](https://docs.conda.io/en/latest/) inside.

## Supported tags

* `servercore-1909`, `latest`
* `servercore-1903`
* `servercore-ltsc2019`
* `servercore-1809`
* `servercore-1803`

## Build

```powershell
docker build --build-arg SERVERCORE_VERSION=1909 -t miniconda3:latest -t miniconda3:1909 miniconda3
docker build --build-arg SERVERCORE_VERSION=1903 -t miniconda3:1903 miniconda3
docker build --build-arg SERVERCORE_VERSION=ltsc2019 -t miniconda3:ltsc2019 miniconda3
docker build --build-arg SERVERCORE_VERSION=1809 -t miniconda3:1809 miniconda3
docker build --build-arg SERVERCORE_VERSION=1803 -t miniconda3:1803 miniconda3
```
