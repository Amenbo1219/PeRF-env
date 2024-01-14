# PeRF-env　version:1.0

This repository is used to run PERF on Docker.
# Requirement
* GPU server environment (assuming login via SSH connection)
* Docker system environment must have been built
* DockerCompose environment
# Installation

Get system from GitHub.
```bash
git clone https://github.com/Amenbo1219/PeRF-env.git
```
Go to the Lyon-Env directory.
```bash
cd PeRF-env
```
Build Docker-compose.
```bash
docker compose build
build 
```
Run the built image.
```bash
docker compose up -d
```
Manipulate the image.
```bash
docker compose exec -it py3 bash
```
# Note

* I want to change or modify an image.

     I want to add a module to [py3/Dockerfile](py3/Dockerfile)

* Want to change port number and GPU memory allocation data directory

     Modify [docker-compose.yml](docker-compose.yml).


# ReleaseNote
## 2024-01-14　Version1.0-release
* firstcommit
# Author

Enumerate creation information

* Created by: Amembo1219
* member：Faculty of Computer Science, Tokyo University of Technology 
* E-mail c0b20140d0@edu.teu.ac.jp

