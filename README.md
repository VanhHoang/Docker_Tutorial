# Docker_Tutorial for Windows

# Download Docker Desktop
* https://www.docker.com/get-started/

# Download WSL 
* wsl --install

# If error Ubuntu 
* Check "Task Manager" -> "Peformance" -> "CPU"
* If "Virtualization: 'Disable' "
=> Go BIOS and Enable Visualization

# CMD Docker
* List : ls
* Read file: cat .\Dockerfile
* Build image: docker build -t welcome-to-docker .
* Run Docker: docker run file.py
* Run in Docker: docker run -it file.py bash

# HUB DOCKER
* FROM ubuntu

# Dockerfile

FROM ubuntu

WORKDIR /src

RUN apt-get update
RUN apt-get -y install python3

COPY file.py ./file.py

CMD ["python3", "file.py"]
