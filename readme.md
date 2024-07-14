<div align="center">

# Docker image for Fooocus

[![python](https://img.shields.io/badge/python-3.10-green)](https://www.python.org/downloads/)
[![cuda](https://img.shields.io/badge/cuda-12.4-green)](https://developer.nvidia.com/cuda-downloads)
[![by-nc-sa/4.0](https://img.shields.io/badge/license-CC--BY--NC--SA--4.0-lightgrey)](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.en)
</div>

## Tags
| Tag    | Description                      | Size      |
| ------ | -------------------------------- | --------- |
| latest | python 3.10, Fooocus 2.4.3 | ~ 14.5 GB |


## Models
- juggernautXL_v8Rundiffusion	

## Ports

| Connect Port | Internal Port | Description   |
| ------------ | ------------- | ------------- |
| 22           | 22            | SSH Server    |
| 7860         | 7860          | Automatic1111 |
| 8888         | 8888          | Jupyter Lab   |

## Environment Variables

Each of the following environment variable is optional, set either `SSH_PASSWORD` or `PUBLIC_KEY` for ssh access

| Variable     | Description                             |
| ------------ | --------------------------------------- |
| SSH_PASSWORD | Password for ssh access                 |
| PUBLIC_KEY   | Public Key for ssh access               |
| SSH_USER     | Username for ssh access (default: root) |


## Running locally
```bash
docker run -d \
  --gpus all \
  -p 22:22 \
  -p 7860:7860 \
  -p 8888:8888 \
  yuvraj108c/a1111:latest
```

## Building the docker image
```bash
git clone https://github.com/yuvraj108c/Fooocus-Docker.git
cd Fooocus-Docker
docker-compose build latest
```

## License
CC BY-NC-SA 4.0