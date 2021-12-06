# docker_pyroute
Building Docker images for testing Pyroute


## Directory Structure

     ├── app       # The non-.git repo stuff of traveller_pyroute repo
     ├── files     # The docker files, like Dockerfile.fedora

## Building (using Fedora as an example):

 Get the fedora stuff into your docker setup.
     docker pull fedora

 Build the image. 
     docker build . -t pyroute_fedora -f files/Dockerfile.fedora

 The output will contain, near the end, something like:
     Successfully tagged pyroute_fedora:latest

 You can then run it, and "log in", with:
     docker run -it  pyroute_fedora:latest /bin/bash


