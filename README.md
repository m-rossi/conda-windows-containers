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
docker build --build-arg SERVERCORE_VERSION=1909 -t rossimarco/miniforge3:latest -t rossimarco/miniforge3:1909 miniforge3
docker build --build-arg SERVERCORE_VERSION=1903 -t rossimarco/miniforge3:1903 miniforge3
docker build --build-arg SERVERCORE_VERSION=ltsc2019 -t rossimarco/miniforge3:ltsc2019 miniforge3
docker build --build-arg SERVERCORE_VERSION=1809 -t rossimarco/miniforge3:1809 miniforge3
docker build --build-arg SERVERCORE_VERSION=1803 -t rossimarco/miniforge3:1803 miniforge3
```
