As the developer makes changes to the Dockerfile, they test locally, then push the changes to a private Docker Hub repo. After this, the changes can be used by a deployment process to a Cloud or by another developer.

https://github.com/udacity/DevOps_Microservices/tree/master/Lesson-2-Docker-format-containers/class-demos

You can find Noah's code here, within the demos subdirectory. Note that he has begun filling out the Dockerfile and run_docker.sh files in the video.

Docker Cheat Sheet
Use docker image ls to see all of your created Docker images
docker run -it {image name} bash ran Noah's Docker image

Dockerfile
FROM python:3.7.3-stretch

# Working Directory
WORKDIR /app

# Copy source code to working directory
COPY . app.py /app/

# Install packages from requirements.txt
# hadolint ignore=DL3013
RUN pip install --upgrade pip &&\
    pip install --trusted-host pypi.python.org -r requirements.txt

run_docker.sh
#!/usr/bin/env bash

## Complete the following steps to get Docker running locally

# Step 1:
# Build image
docker build --tag=demolocal

# Step 2: 
# List docker images
docker image ls

# Step 3: 
# Run flask app
docker run -it demolocal bash


to run:
<!-- Desktop/local_env/demos-docker/demos/flask-sklearn-student-starter$ docker build --tag=demolocal . -->
docker build --tag=demolocal .
docker image ls
docker run -it demolocal bash

after d last one:
uname -a

python

import pandas as pd






